---
layout: post
title: "Decoding Edwin Diaz's Meltdown: A Starter Savant Analysis"
tags: []
categories:
  - Baseball Analysis
date: 2019-08-16 11:01:42
lang: en
---

Last year, Edwin Diaz was dominant, striking out batters with his high-velocity fastball and nasty slider, and earning a remarkable 57 saves to become the closer king. This year, his performance has been abysmal. Out of 29 save opportunities, he blew 5 saves, and his **ERA is as high as 5.60, with a WHIP of 1.47**. This means that, on average, opponents reached base 1.47 times per inning against him this year.

![](https://i.imgur.com/xG4gXlX.jpg)

<!-- more -->

Although on August 5th (US time), Mets manager Mickey Callaway confidently stated that Edwin Diaz was still their closer, the truth is, **the Mets have quietly stopped deploying Diaz in critical situations**. On August 13th and 14th, Manager Callaway said the following in interviews:

> 8/13: I don't think anyone's position is fixed. We will do everything to win.
>
> 8/14: In critical moments, his performance makes it very difficult to put him out there.

The most likely candidate to replace Edwin Diaz as closer is **Seth Lugo, who just won National League Reliever of the Month in July**. However, on the day I'm writing this, he **pitched only 0.1 innings and gave up 5 runs QQ**...

Edwin Diaz's major meltdown this year roughly began on May 29th, in a game against the Dodgers where he gave up 4 runs in just 0.1 innings. Including that game, Edwin Diaz's ERA since then has been 9.39, meaning he has given up runs almost every time he's pitched, and his WHIP has skyrocketed to 1.87. Let's look at Diaz's performance before and after May 29th:

<figure class="wp-block-table is-style-regular"><table><tbody><tr><td>&nbsp;</td><td>ERA</td><td>WHIP</td><td>Batting Average Against</td></tr><tr><td>Before 5/28</td><td>1.64</td><td>1.05</td><td>0.205</td></tr><tr><td>After 5/29</td><td>9.39</td><td>1.87</td><td>0.327</td></tr></tbody></table></figure>

**What Happened After May 29th?**

Astute readers might be wondering, so what exactly happened to Edwin Diaz after May 29th?

The answer is: **nothing happened**.

The truth is, Diaz had been struggling since the start of the season; **his good performance early on was merely due to luck**. A closer look at advanced metrics reveals that, according to Fangraphs, Diaz's **Hard-hit rate from the start of the season until May 28th was 52.1%**, while **the league average this year is only 38.1%**. You might think that because Diaz throws hard, balls hit off him would naturally have higher exit velocities due to the physics of rebound. However, let's look at Diaz's **Hard-hit rate in his first three career seasons (2016-2018): they were only 28.8%, 32.5%, and 29.3% respectively**. **His Hard-hit rate at the beginning of this year was completely abnormal**, and it actually slightly decreased to 43.3% after May 29th.

 
<figure class="wp-block-table is-style-regular"><table><tbody><tr><td>&nbsp;</td><td>**Hard-hit Rate**</td></tr><tr><td>2016</td><td>28.8%</td></tr><tr><td>2017</td><td>32.5%</td></tr><tr><td>2018</td><td>29.3%</td></tr><tr><td>**2019 Season Start~5/28**</td><td>**52.1%**</td></tr><tr><td>**2019/After 5/29**</td><td>**43.3%**</td></tr><tr><td>**2019 League Average**</td><td>**38.1%**</td></tr></tbody></table></figure>

Let's look at another metric: **Line Drive Rate (calculated as: number of line drives / number of balls put in play)**. Line drives, due to their short airtime, are difficult to field and are usually hit solidly, making them **a type of batted ball that easily results in a hit**. According to MLB Savant data, **the league's Line Drive Rate this year is 25.5%**, but Edwin Diaz's **Line Drive Rate before May 28th was as high as 33.3%**. Before this year, his **career Line Drive Rate was only 21.6%**. The Line Drive Rate after May 29th was actually only 25%, which is lower than at the start of the season.

 
<figure class="wp-block-table is-style-regular"><table><tbody><tr><td>&nbsp;</td><td>**Line Drive Rate**</td></tr><tr><td>2016~2018</td><td>21.6%</td></tr><tr><td>**2019 Season Start~5/28**</td><td>**33.3%**</td></tr><tr><td>2019/After 5/29</td><td>25%</td></tr><tr><td>**2019 League Average**</td><td>**25.5%**</td></tr></tbody></table></figure>

So how did Edwin Diaz manage to pitch so well at the start of the season? The answer is simple: **Left-On-Base (LOB) percentage**.

From the start of the season until **May 28th, Edwin Diaz's LOB% was an astonishing 100%**. This means that **almost every runner who reached base could not be driven in by their teammates** (due to the calculation formula, a 100% LOB% doesn't literally mean no one scored from base). What **incredible luck**!

After **May 29th, Edwin Diaz's LOB% dropped to just 62.1%**. His luck index, **BABIP** ([I discussed BABIP in more detail in another article](https://www.sportsv.net/articles/65500)), also **soared from 0.311 to 0.462**. For pitchers, a **lower BABIP indicates more luck**, so Edwin Diaz's **poor performance after May 29th was simply because his luck ran out**.

_Small note: Some people familiar with advanced metrics might argue that a BABIP as high as 0.462 indicates Diaz is currently having extremely bad luck, as the league average BABIP is only around 0.29. However, do you recall the Hard-hit rate and Line Drive Rate mentioned earlier? The higher these two metrics are, the higher the BABIP tends to be. Therefore, Diaz's BABIP would naturally be higher than others, so the author believes his current struggles are not largely due to luck._

In conclusion, Edwin Diaz made some minor adjustments after May 29th and even pitched better than at the start of the season, but his early-season luck ran out, leading to his inevitable meltdown. In other words, **some of Edwin Diaz's problems have existed since the beginning of the season**.

So, what exactly are these problems?

**Struggling to Hit the Corners?**

The ability to throw pitches to the edges of the strike zone is crucial for a pitcher, because **pitches on the edges of the strike zone are difficult for batters to hit, yet they can still be called strikes**.

However, this year Edwin Diaz's **ability to locate pitches on the edges of the strike zone has deteriorated**.

 
<figure class="wp-block-table is-style-regular"><table><tbody><tr><td>&nbsp;</td><td>Pitches on the Edge of the Strike Zone / All Pitches</td></tr><tr><td>2016</td><td>41.4%</td></tr><tr><td>2017</td><td>41.8%</td></tr><tr><td>2018</td><td>39.3%</td></tr><tr><td>This Year</td><td>38.2%</td></tr></tbody></table></figure>

As we can see from the table above, this year Edwin Diaz's **percentage of pitches on the edge of the strike zone is a career low, at only 38.2%**. However, his overall strike rate is almost identical to last year. In other words, **while maintaining the same strike rate, Diaz is unable to locate pitches on the corners and is instead throwing them into more hittable areas**.

Furthermore, if we look at the **location of Edwin Diaz's slider**, a crucial weapon for inducing swings, we'll find that this year Edwin Diaz's **rate of throwing sliders down the middle** is also a career high.

![](https://i.imgur.com/owGZeqW.png)

Figure 1: Edwin Diaz's Rate of Throwing Sliders Down the Middle

Diaz's most recent outing was on August 11th (US time) against the Nationals, where he gave up a two-run homer to Victor Robles. The pitch hit out was precisely a slider that didn't break down. After the game, Diaz said:

> He hasn't been hitting sliders well this series, so I threw a slider. I just couldn't put the ball where I wanted it, and that's why he was able to hit it out. I wanted to throw a low-and-away slider that would induce a ground ball.

Therefore, Edwin Diaz's **command has indeed been an issue** this season, forcing him to throw pitches into the sweet spot of the strike zone, which could be a reason for his meltdown.

**Change in Release Point?**

Another point I'm concerned about is: **Edwin Diaz's release point for different pitches has varied more this year**.

For a pitcher, it's best if the **release points for different pitches do not vary**, so that batters cannot anticipate the pitch type from the release point.

Edwin Diaz primarily throws two pitches: a **four-seam fastball and a slider**. **Because he doesn't have many pitch types, release point consistency is even more crucial for Diaz**; if the release point varies too much, batters can easily guess the pitch beforehand. Let's look at the year-by-year differences in Diaz's four-seam/slider release points:

![](https://i.imgur.com/CbpG2EH.jpg)

Figure 2: Release Point Location for Each Pitch Type (Vertical)

![](https://i.imgur.com/NXFMFXq.jpg)

Figure 3: Release Point Location for Each Pitch Type (Horizontal)

From the vertical release points of each pitch type, it can be observed that this year, **the vertical release point difference between Edwin Diaz's four-seam fastball and slider is the largest in his career**, approximately **0.21 feet (6.4 cm)**. While I don't know if such a difference is significant enough for professional MLB hitters to directly identify the pitch type from the release point, **the increased variation is a warning sign regardless**.

Furthermore, a year-by-year analysis of his release point shows that Edwin Diaz's release point has **consistently moved closer to the ground and gradually extended towards the outside of the pitcher's plate**. This is a noteworthy trend, and I'll leave a small foreshadowing here, as we'll discuss this very soon.

**Change in Pitching Mechanics?**

We've discussed many potential issues with Edwin Diaz this year, but ultimately, what is the underlying reason for the changes in his command or release point?

I wonder if everyone has heard of a term: **Perceived velocity**.

Unlike the actual velocity we usually measure, **Perceived velocity is related not only to the actual ball speed but also to the pitcher's release point**. For a batter, **if the pitcher's release point is closer to home plate (the release point extends further forward), then the ball's flight distance in the air will be shortened, and the ball will reach home plate in less time. Consequently, batters will perceive the ball as faster than its actual velocity** – this is called Perceived velocity. Conversely, if the pitcher's **release point is further back, the ball will take more time to reach home plate, thus reducing the Perceived velocity**.

Therefore, I've noticed that Edwin Diaz seems to have been **trying to extend his release point forward** in recent years, possibly to increase his Perceived velocity. Let's look at Edwin Diaz's average actual velocity and Perceived velocity for each pitch type year by year. I've also used these two data points to calculate the **estimated release point location (zero point is the front edge of the pitcher's plate; '+' indicates the release point is forward; '-' indicates the release point is backward)**.

 
<figure class="wp-block-table is-style-regular"><table><tbody><tr><td>&nbsp;</td><td>**Four-Seam Fastball Actual Velocity**</td><td>**Four-Seam Fastball Perceived Velocity**</td><td>**Four-Seam Fastball Release Point**</td><td>**Slider Actual Velocity**</td><td>**Slider Perceived Velocity**</td><td>**Slider Release Point**</td></tr><tr><td>2016</td><td>97.0 mph</td><td>97.13 mph</td><td>+3.5cm</td><td>87.3 mph</td><td>86.99 mph</td><td>-6.6cm</td></tr><tr><td>2017</td><td>97.4 mph</td><td>97.92 mph</td><td>+9.8cm</td><td>88.0 mph</td><td>88.09 mph</td><td>+1.9cm</td></tr><tr><td>2018</td><td>97.3 mph</td><td>97.77 mph</td><td>+8.8cm</td><td>89.1 mph</td><td>89.50 mph</td><td>+8.2cm</td></tr><tr><td>**2019**</td><td>97.2 mph</td><td>97.92 mph</td><td>**+13.5cm**</td><td>89.1 mph</td><td>89.76 mph</td><td>**+13.5cm**</td></tr></tbody></table></figure>

As you can see, **this year Edwin Diaz has clearly extended his release point forward towards home plate, by a length of 13.5 cm**. While this increased his Perceived velocity (the speed perceived by batters), such a **change in pitching mechanics may have consequently affected his command, and also potentially altered the release points of his four-seam fastball and slider**.

Returning to the charts of release points for each pitch type (Figures 2, 3), I mentioned that Edwin Diaz has **extended his release point downwards** year by year. I believe this could also be a change in his release point made by Diaz **to extend his arm further forward** and increase Perceived velocity. And the purpose of **extending the release point outwards should be to increase the movement of his slider**, as Edwin Diaz's **slider movement is actually below the league average**. However, data shows no significant change in Diaz's slider movement in recent years.

**Conclusion**

Based on the discussion above, Edwin Diaz's major meltdown this year can likely be **attributed to a change in his pitching mechanics (release point location)**. Whether intentional or unintentional, this change has **worsened his command this year, making him unable to locate pitches on the edges of the strike zone**. However, constantly throwing pitches down the middle has led to him being consistently attacked. This year's **increase in Hard-hit rate and Line Drive Rate** both indicate that batters are hitting the ball more solidly. The good news is that, although I haven't presented the data, Diaz's pitch quality doesn't seem to be a major issue; **his velocity and spin rate this year are still at their usual levels, so it's likely not an injury affecting Diaz's pitching mechanics**. Hopefully, after the coaching staff changes his pitching role, he can properly adjust himself and regain his glory as a closer!

![](https://i.imgur.com/MbkXcTS.jpg)

Analysis Data Sources:

MLB Official Website, Fangraphs, MLB Savant, Brooks Baseball

In-article News Interview Sources:

1.  New York Post: [https://nypost.com/2019/08/13/mets-have-only-one-way-out-of-edwin-diaz-wreck/](https://nypost.com/2019/08/13/mets-have-only-one-way-out-of-edwin-diaz-wreck/)
2.  New York Post: [https://nypost.com/2019/08/14/seth-lugo-bumps-edwin-diaz-to-uncertain-place-in-mets-pen/](https://nypost.com/2019/08/14/seth-lugo-bumps-edwin-diaz-to-uncertain-place-in-mets-pen/)
3.  New York Post: [https://nypost.com/2019/08/13/mets-have-only-one-way-out-of-edwin-diaz-wreck/](https://nypost.com/2019/08/13/mets-have-only-one-way-out-of-edwin-diaz-wreck/)

Image Source:

MLB Mets Official Website PC: _Kathy Willens/AP_

Cover Image Source:

MLB Mets Official Website PC: _Al Bello/Getty Images_