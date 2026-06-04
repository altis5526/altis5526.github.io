---
layout: post
title: Alphapose Principle - RMPE (Regional Multi-Person Pose Estimation)
tags: []
id: '1537'
categories:
  - - ML/DL Learning
date: 2021-12-05 16:41:55
---

<img src="https://i.imgur.com/Lq57wix.jpg?1" class="center">

**_This article is purely for academic sharing. All images within the text are from the original RMPE paper and another STN paper (Cover image: Photo by [Patricia Palma](https://unsplash.com/@laclem?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) on [Unsplash](https://unsplash.com/s/photos/pose?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText))_**

**_Fang, H. S., Xie, S., Tai, Y. W., & Lu, C. (2017). Rmpe: Regional multi-person pose estimation. In Proceedings of the IEEE international conference on computer vision (pp. 2334-2343)._** **_[https://arxiv.org/abs/1612.00137](https://arxiv.org/abs/1612.00137)_**

**_Jaderberg, M., Simonyan, K., & Zisserman, A. (2015). Spatial transformer networks. Advances in neural information processing systems, 28, 2017-2025._** _**[https://arxiv.org/abs/1506.02025](https://arxiv.org/abs/1506.02025 "https://arxiv.org/abs/1506.02025")**_

Currently, many models and techniques can implement pose estimation, and among them, Alphapose is certainly one that cannot be overlooked. Even though it was published back in 2016, Alphapose's comprehensive open-source API and decent accuracy still make it a valuable tool for many CV researchers today. The full name of the underlying principle behind this useful API is RMPE (Regional Multi-Person Pose Estimation). However, this name is perhaps just something to be aware of, as it appears in only a few lines in the introduction and conclusion throughout the entire paper, LOL. In any case, today we will be reviewing the paper RMPE: Regional Multi-Person Pose Estimation.

<!-- more -->

## Introduction

Generally, pose estimation is divided into two types: part-based frameworks and two-step frameworks. The former first identifies body keypoints and then reconstructs their relationships to predict human pose; the latter first detects human bounding boxes and then identifies human pose based on the bounding box locations. RMPE adopts this latter approach. However, this type of method has a drawback: if the bounding box localization is inaccurate, the performance of pose estimation will be significantly degraded. To address this issue, the authors proposed RMPE with three innovative architectures: (1) Symmetric STN and parallel SPPE (2) Parametric pose NMS (3) Pose-guided proposals generator. These three architectures will be discussed in detail next.

## Model Architecture

![](https://imgur.com/R6KblWC.png)

Figure 1

The overall architecture of RMPE is shown in the figure above: First, the input image passes through an existing Human detector to obtain human proposals. These human proposals then go through the aforementioned STN (spatial transformer network), SPPE (single person pose estimation), and SDTN (spatial de-transformer network) respectively. After these three steps, we predict the pose for each individual detected by the human detector. However, human proposals may be redundant rather than one-to-one, so we need to eliminate the extra pose estimations for the same person. This is done using pose NMS, and finally, pose estimation for a single image can be completed.

### Symmetric STN and parallel SPPE

First, let's look at the architecture of SSTN and parallel SPPE. Here, SSTN stands for symmetric spatial transformer network, but the 'transformer' referred to here is not the one commonly associated with self-attention, but rather a different architecture as shown in the figure below:

![](https://i.imgur.com/O76sbGh.png)

Figure 2

The purpose of STN is to use spatial mapping to bring people who are not necessarily in the center of the frame back to the center. The input here should be an image containing a human proposal. Then, through a Localisation network, an affine transformation matrix θ can be learned. Using this θ, we can apply an affine transformation to the coordinates on the original human proposal. This process is the grid generator, which then feeds into the sampler. The main purpose of the sampler is to solve the problem of non-differentiable integer coordinates (e.g., if Tθ(G) outputs a non-integer value, how do you map it to coordinates? Should it be rounded? But rounding makes it non-differentiable).

The mathematical proof of the sampler will not be explained in detail here, but we can still look at the formulas from the original STN paper:

![](https://i.imgur.com/bkHA4R2.png)

Figure 3

![](https://i.imgur.com/k0NjwT1.png)

Figure 4

The upper equation is the generalized form, and the lower equation assumes a function k. xi and yi can be thought of as the output coordinates of the grid generator. We use linear interpolation to find points (n,m) near xi, yi (using a max function, so points too far away are not used). We estimate the score at (xi, yi) using the score (U) of point (n,m), and such a function will be differentiable.

Alright, we've strayed a bit. Let's return to STN's θ. Recall that we use θ to spatially map points on our image. The paper dedicates a significant portion to explaining this:

![](https://i.imgur.com/AfzeB44.png)

Figure 5

\[θ1 θ2 θ3\] is a 2x3 matrix. θ1 and θ2 are mainly responsible for transformations like rotation and scaling, while θ3 is responsible for translation.

Since we mapped the coordinates to another space, we must map them back when outputting predictions. Thus, the entire SSTN architecture is actually like this:

![](https://i.imgur.com/ObGdWrC.png)

Figure 6

In addition to the forward STN, a SDTN (Spatial de-transformer network) is used to map the coordinates back to the original image. Thus, the de-transformer formula is as follows:

![](https://i.imgur.com/AE4CgEa.png)

And \[γ1, γ2\] are the inverse matrices of \[θ1, θ2\]. Since an inverse matrix must be a square matrix, γ3 needs to be handled separately:

![](https://i.imgur.com/fceGz47.png)

Here's a simple derivation I made:

![未提供說明。](https://scontent.ftpe7-3.fna.fbcdn.net/v/t1.15752-9/262915587_314501503677681_7771690257437202969_n.jpg?_nc_cat=102&ccb=1-5&_nc_sid=ae9488&_nc_ohc=Z8L5vdnVwAX9aHYCm&_nc_ht=scontent.ftpe7-3.fna&oh=7f5079e3a55a12652ab9b5b8d3cbfa12&oe=61D11731)

Figure 7

With these conditions, we can freely update the θ parameters using back-propagation:

![](https://i.imgur.com/gtbGP2H.png)

![](https://i.imgur.com/7Oox7nG.png)

Next, we discuss parallel SPPE. Theoretically, the output of STN would pass through SPPE for pose estimation, but this is not enough. In addition to the original SPPE, another SPPE is added, which is the parallel SPPE proposed by the authors. This additional SPPE (which we'll call SPPE-2) does not go into SDTN. The pose output by SPPE-2 is directly compared with the center-located ground truth; that is, all ground truths here are center-located. Do you remember the purpose of STN? It is to make the human pose center-located. Therefore, by using SPPE-2, we can fix the parameters of SPPE-2 during training, allowing the loss function to backpropagate and update the STN parameters, and simultaneously update the SDTN parameters (recall that SDTN parameters can be directly derived from θ). This makes STN easier to learn how to center the human pose in the image, thereby optimizing the prediction performance of the primary SPPE.

![](https://i.imgur.com/PSziJ6s.png)

Figure 8

One might wonder why such a parallel network is designed instead of simply adding a loss function with center-located ground truth directly after the original SPPE. The paper clarifies this: the reason is that the effect of STN transformation is limited and cannot perfectly center people in the frame. Therefore, if such a loss were added after SPPE while simultaneously updating SPPE's parameters, it would negatively impact the original SPPE's performance. Also, due to the imperfect nature of STN, parallel SPPE can continuously transmit a large amount of loss to optimize the STN architecture.

### Parametric Pose NMS

As mentioned earlier, human detectors often detect redundant human proposals. These extra proposals, when fed into SPPE, generate an equally redundant number of pose estimations. To solve this problem, we must be able to determine which redundant poses to eliminate. The authors designed an NMS (non-maximum suppression) criterion. Conceptually, it involves determining if the positions of two poses are sufficiently close. If they are, then one of the poses must be eliminated.

So, let's first look at the pose distance formula defined by the authors:

![](https://i.imgur.com/nw0B3ck.png)

![](https://i.imgur.com/hAHYbXn.png)

Ksim Definition

![](https://i.imgur.com/odUBrLB.png)

Hsim Definition

Pi and Pj represent two different pose estimations, while ci and cj are their respective confidence scores. The definitions of Ksim and Hsim are as above:

First, let's look at Ksim. We assume Bi is the bounding box of Pi, and B(kin) is a bounding box drawn around the n-th keypoint of the i-th pose, with its width and height being 1/10th of Bi's. Ksim represents the process where we use Pi as a reference and compare each keypoint in Pi with its corresponding keypoint in Pj. The first step is to check if keypoint kjn falls within the bounding box of kin. If it does, we proceed with the calculation; otherwise, the similarity score for these two points is directly set to 0. If kjn is within kin's bounding box, their respective confidence scores are passed through a tanh function and then multiplied. Finally, all pair scores are summed up to obtain the final Ksim value.

Next is Hsim, which is easier to understand. It calculates the distance between kin and kjn, but this distance is computed using an RBF function.

Finally, by adding Ksim and Hsim and applying a calibration weight λ, we obtain the pose distance formula defined by the authors.

Using this pose distance formula, the NMS criterion designed by the authors can be derived:

![](https://i.imgur.com/f88p0e3.png)

Here, ∧ and λ are merely parameters used in calculating the pose distance, and η is a defined threshold. If the pose distance is less than η, this indicator vector will be assigned a value of 1, meaning that this pose must be eliminated.

Additionally, the authors specifically emphasized that the four parameters in the elimination criterion: σ1, σ2, η, and λ, are all optimizable. The optimization method was not specifically described, but it could be traditional grid search or random search, for example.

### Pose-guided Proposals Generator

In fact, two-stage pose estimation is highly susceptible to slightly deviated human proposals. Therefore, the authors designed a data augmentation method and gave it a fancy name: Pose-guided Proposals Generator (PGPG). What PGPG does is to find the offset distribution between detected bounding boxes and ground truth bounding boxes for each pose. Simply put, every bounding box has four vertices: (xmin, xmax, ymin, ymax). We can compare the distance difference at these four points between each detected bounding box and its corresponding ground truth bounding box. By estimating these differences using a Gaussian model, we obtain four distribution maps. Using these distributions, we can perform random sampling to generate several times more human proposals on the original image and feed them into the model for training.

![](https://i.imgur.com/FYn1srn.png)

Figure 9

## Experiments and Results

Finally, we move on to the results. The authors primarily conducted evaluations on two datasets: MPII and MSCOCO. During testing, VGG was chosen as the human detector, and each human proposal's width and height were increased by 30% to avoid missing people. For the SPPE component, a stack hourglass model was used. While the stack hourglass model won't be detailed here, it is essentially a multi-layer residual CNN architecture. Because the feature map size first decreases and then is upsampled back to its original state, it resembles an hourglass shape. In fact, besides the aforementioned models, the authors also experimented with other models to demonstrate that the RMPE method is generalizable.

![](https://i.imgur.com/XuwhV8Z.png)

Figure 10

![](https://i.imgur.com/7bNJaOB.png)

Figure 11

The two figures above represent the test results for MPII and MSCOCO, respectively. Compared to models at the time, both achieved state-of-the-art performance.

### Ablation study

In the ablation study, the authors removed the three main architectures—Symmetric STN & Parallel SPPE, Parametric Pose NMS, and Pose-guided Proposals Generator—one by one, and found that each had a significant impact on the experimental results. Interestingly, in the Parametric Pose NMS experiment, the authors compared the effects of random jittering (which literally seems like random sampling) and PGPG, finding that PGPG still performed better. This suggests that data augmentation requires specific methods to improve performance. Furthermore, the authors believe their parametric Pose NMS outperforms others because its parameters can be optimized, whereas previous methods did not optimize NMS parameters.

Overall, this is a very interesting paper. The authors used many fancy methods to construct their model, and as a result, there might be many small details that couldn't be fully covered in this article. Those interested can refer to the original paper or related materials. Finally, thank you all for reading this far, and I hope those interested will enjoy it~~

## Reference

1.  **_Fang, H. S., Xie, S., Tai, Y. W., & Lu, C. (2017). Rmpe: Regional multi-person pose estimation. In Proceedings of the IEEE international conference on computer vision (pp. 2334-2343)._** **_[https://arxiv.org/abs/1612.00137](https://arxiv.org/abs/1612.00137)_**
2.  **_Jaderberg, M., Simonyan, K., & Zisserman, A. (2015). Spatial transformer networks. Advances in neural information processing systems, 28, 2017-2025._** _**[https://arxiv.org/abs/1506.02025](https://arxiv.org/abs/1506.02025)**_