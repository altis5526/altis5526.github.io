---
layout: post
title: "Understanding ECG Signs: How Are ST Elevation, T-wave Inversion, and Q waves Generated?"
tags: []
categories:
  - Medical Study
date: 2019-10-13 17:01:40
lang: en
---

In our school's electrocardiogram (ECG) course, the instructor thoroughly explained the meaning of different signs on an ECG. For example, S-T elevation might signal a myocardial infarction, T inversion indicates myocardial ischemia, and the appearance of a Q wave suggests necrosis after myocardial ischemia. However, the specific mechanisms that lead to these waveform patterns on an ECG were never elaborated or explained in class. In this article, I want to share the ECG logic I've pieced together. While the underlying principles of ECG might not be critically important in future clinical practice, a useful logical framework can undoubtedly help us remember and understand, rather than just rote memorization of facts.

![](https://i.imgur.com/JVCgPzL.jpg)

<!-- more -->

**Before delving into specific ECG phenomena such as T inversion and S-T elevation/inversion, I'd like to guide you through a more in-depth understanding of the ECG structure:**

I assume that most readers of this article already have a basic understanding of ECGs. Just in case, before I elaborate on the concepts I wish to share, I'll briefly review some fundamental ECG background knowledge. If you're already familiar, feel free to skip directly to the **QRS complex** section:

1.  The P wave represents atrial depolarization; the QRS complex represents ventricular depolarization, and the T wave represents ventricular repolarization.
2.  During myocardial cell depolarization, the intracellular potential becomes positive. Conversely, the extracellular environment becomes more negatively charged, essentially acting as the negative pole of a battery, while myocardial cells that have not yet depolarized act as the positive pole.
3.  When the extracellular cardiac vector caused by myocardial cell depolarization/repolarization is in the same direction as the ECG lead vector (here, the arrows of the vectors point towards higher potential), a positive signal will be observed on the ECG. Conversely, if they are in opposite directions, a negative signal will be seen on the ECG.
4.  The magnitude of the cardiac vector is related to the number of depolarized myocardial cells, and a larger component of the cardiac vector along the lead vector will result in a larger positive wave.

![](https://i.imgur.com/c9t19SG.png)

**QRS-complex**

**Now that we've reviewed the basic ECG concepts, let's dive into the main topic!**

We've all been taught that in a normal QRS complex, the Q wave dips slightly downwards, the R wave goes upwards, and the S wave immediately follows the R wave, also dipping downwards. However, why does the Q wave go down, and why does the S wave also go down?

**Why does the Q wave go down?**

Let's use Lead II as an example; recall that its vector direction is from the upper right of the heart towards the lower left.

Generally, the heart's electrical signal first travels from the SA node in the atria to the AV node, then down through the interventricular septum, and finally along the ventricular walls from the bottom (apex) upwards (base).

![](https://i.imgur.com/M3Ebgap.png)

During this transmission, sometimes the left side of the interventricular septum depolarizes earlier than the right side. Consequently, during this window when the right heart has not yet depolarized, the earlier depolarized left interventricular septum transmits a very weak signal to the right. When the direction of this vector is opposite to the direction of the Lead II vector, a weak negative Q wave will be observed on the ECG. (According to the example diagram I drew, Lead I would also produce a negative Q wave, but Lead III would not.)

![](https://i.imgur.com/MQn2ASd.png)

**Why does the S wave go down?**

Do you recall that after the heart's depolarization signal passes through the interventricular septum, it travels along the ventricular walls from the bottom upwards?

Because the left ventricle depolarizes slightly later, at the very end of cardiac depolarization, the electrical signal we expect to see primarily moves from the left ventricular apex to the left ventricular base. This direction is opposite to the original main cardiac vector (which travels from the upper right of the heart to the lower left), thus a negative S wave is observed on the lead.

![](https://i.imgur.com/nbSUwDU.png)

**Common ECG Phenomena**

**T-inversion**

We all know that T-inversion occurs when myocardial cells experience strain or ischemia, but what exactly is the underlying principle behind T-inversion?

This is an interesting question, but first, we should understand how the T wave is formed.

The T wave represents ventricular repolarization, which involves a charge flow in the exact opposite direction of depolarization. Therefore, if the directions of depolarization and repolarization signals were the same, one signal would form a positive wave, and the other a negative wave.

![](https://i.imgur.com/FQQNytc.png)

![](https://i.imgur.com/yNn3cug.png)

**When repolarization and depolarization directions are the same, the ECG shows opposite directions.**

However, generally on an ECG, we observe that both the QRS complex (representing depolarization) and the T wave (representing repolarization) are positive waves. Does this imply that the direction of the depolarization signal and the repolarization signal are opposite? Yes, precisely!

In addition to the cardiac signal transmission pathway mentioned earlier, within the myocardial layer, the depolarization signal also has a fixed direction: from the inner layer of the myocardium to the outer layer. However, contrary to intuition, in the ventricles, although the cells that depolarize earlier are those closer to the inner side of the myocardium, they do not repolarize earlier. Instead, the cells that depolarize later, i.e., those closer to the outer side of the myocardium, repolarize earlier. According to the 13th edition of Guyton's textbook, the reason for this phenomenon is currently thought to be related to the higher pressure on the inner ventricular wall during myocardial contraction, which reduces blood flow. Since the direction of depolarization is from inside to out, and the direction of repolarization is from outside to in, the "negative times negative equals positive" effect results in both depolarization and repolarization waveforms being positive.

![](https://i.imgur.com/APf5Smv.png)

When there are issues with the heart's blood vessels, the blood vessels on the inner side of the myocardium are more prone to ischemia due to compression from ventricular pressure, compared to the vessels on the outer side. Simply put, myocardial ischemia spreads from the inner side of the myocardium outwards.

During myocardial ischemia, the ATP-sensitive potassium channels on the affected inner myocardial cells open, accelerating the repolarization process, even earlier than in normal outer myocardial cells. This causes the direction of the repolarization signal to spread from the inner side of the myocardium outwards, thus turning the originally positive T wave into a negative one.

![](https://i.imgur.com/piL9xaO.png)

**S-T elevation**

I believe everyone is familiar with the appearance of S-T elevation and knows that it is a warning sign of myocardial infarction (MI). But why does S-T elevation occur?

When myocardial cells are damaged by ischemia, they cannot repolarize normally due to a lack of nutrients, causing them to remain in a depolarized state. As mentioned earlier, depolarization leads to an increase in extracellular negative charges. Therefore, compared to other normal, undamaged myocardial cells, the damaged cells will have a more negative potential. This creates a portion of the electrical vector (pointing from negative to positive) directed towards the normal, undamaged myocardial cells. For an electrode placed over the damaged area, it will sense an electrical vector moving away from it, causing the baseline signal of this electrode to be negatively shifted.

When all cardiac cells have completed depolarization, which is at the end of the S wave, all parts of the heart are negatively charged (including the damaged myocardial area that has remained depolarized), and there is no current flowing. At this point, we can observe a true zero potential point on the ECG (also known as the J point). Compared to the original baseline signal, this zero potential point is relatively positive, which is why the S-T segment after the S wave appears elevated on the ECG.

![](https://i.imgur.com/z2OKH37.png)

**S-T depression**

S-T depression is an ECG phenomenon observed during the early stages of myocardial infarction. How can we explain this phenomenon using the knowledge compiled in this article?

As mentioned earlier, ischemic damage to the myocardium begins from the inner side. Imagine if only the inner layer of the myocardium is damaged, while the outer layer remains intact. This would mean that the ECG baseline signal constantly shows a depolarization signal moving from the inner layer outwards. For an electrode placed over the damaged area, this inner-to-outer depolarization signal is positive, thus maintaining a positively shifted baseline signal.

Similarly, when the heart completes depolarization (at the end of the S wave), there is no current flowing in the heart, and we can observe a true zero potential point. This zero potential point will be more negative than the original baseline signal, making the S-T segment appear depressed.

![](https://i.imgur.com/t3jyhQ2.png)

These are my small insights into ECGs. While the explanations above may not fully answer all the questions I encounter when interpreting ECGs, they have at least given me a deeper conceptual understanding of ECGs, moving beyond just one-to-one correlations between ECG findings and diseases. The content in this article is based on my own research and findings, and I kindly ask for your understanding and guidance if there are any errors.

**References:**

Hall, J. E. (2016). _Guyton and Hall textbook of medical physiology 13rd Edition_. Elsevier Health Sciences.

Wu, De-Jin & Wu, Feng-Xu (Trans.) (2016). **Simplified Illustrated Electrocardiography** (Original author: Okude Jun). New Taipei City: Ho Chi Book Publishing.

He, Li-Ting (Trans.) (2014). **ECG Made Easy, Seventh Edition** (Original author: Malcolm S. Thaler). Taipei City: Watercool.