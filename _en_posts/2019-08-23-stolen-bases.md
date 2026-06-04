---
layout: post
title: "The Decline of the Stolen Base: Why Baseball Stopped Running"
tags: []
categories:
  - Baseball Analysis
date: 2019-08-23 09:50:13
lang: en
---

Stolen bases are an important tactic in baseball, representing a cat-and-mouse game between offense and defense. For the runner, observing the pitcher's motion, accurately judging the lead-off distance, timing the start, and knowing how to slide to minimize the chance of being out when the second baseman receives the throw a step early – every single step is crucial for a successful steal, and it's a gamble. For the pitcher and catcher, stolen bases are a nightmare; they cannot simply allow runners to advance, and they employ every trick to thwart the runner's attempts. Especially in close games, the stolen base tactic is truly heart-pounding.

![](https://i.imgur.com/co3kG5V.jpg)

<!-- more -->

When talking about a legendary stolen base master, one immediately thinks of **Rickey Henderson in the 1980s**. 1980 was his first full season, and that year he **stole an astonishing 100 bases**. In 1982, he stole an even more remarkable **130 bases, the second-highest in MLB history**. His career total of stolen bases is, without a doubt, the most in history, with 1406 steals, far surpassing the second-place record of 938. Let's revisit his highlights:

<style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://www.youtube.com/embed/LkvsGVQ7DKY' frameborder='0' allowfullscreen></iframe></div>

However, did you know that stolen bases, once prevalent for a long time, have been **gradually declining in recent years**?

According to data from an Athlon Sports article: [Why Baseball Players Rarely Steal Bases Anymore?](https://athlonsports.com/mlb/whats-stolen-base), it shows:

1.  The total number of stolen bases in 2018 was 2474, the lowest for a full season since 1973. Last year's league stolen base leader was Whit Merrifield, with only 45 steals, the lowest since 1963.
2.  Since 1900, there have been 23 seasons with players exceeding 80 stolen bases. However, there hasn't been such a player since 1988.
3.  In 2013, eight players had over 40 stolen bases, but in both 2017 and 2018, only three players reached that mark.

In fact, **no player has reached 40 stolen bases this year** yet. The closest to this number is Mallex Smith with 34 steals. The second-place player, Adalberto Mondesi, who was originally on the fastest pace, has had no game appearances since 7/16 due to injury, and his stolen base count remains at 31.

So, why exactly are players no longer stealing bases?

**The Fly Ball Revolution**

It probably goes without saying that the number of home runs in the league has been continuously rising in recent years. Many players even suspect that MLB has started using a "juiced ball" to make the ball fly farther and games more exciting. Setting aside the steroid era, let's directly look at the growth curve of the total number of home runs in the league over the past decade:

![](https://i.imgur.com/IShKI0r.png)

Total MLB Home Runs 2010-2019

We can see that the **total number of home runs has gradually increased over the past decade**. In 2017, the entire league hit 6105 home runs, setting a new historical record. So far this year, there have already been 5320 home runs. At this rate, the author predicts that this year's home run total is very likely to surpass the 2017 record, reaching over 6700.

Furthermore, although the league's fly ball rate hasn't significantly increased, this year's **HR/FB% (the rate at which fly balls become home runs) is the highest on record**, reaching 15.4%, which has also led to the surge in home run numbers this year.

Regardless of what caused the fly ball revolution, the result is an increase in home run numbers. So, what's the relationship between more home runs and stolen bases?

Remember that stolen bases are meant to advance runners and increase scoring opportunities? If **the batter at the plate hits a home run, then regardless of whether runners advanced, everyone on base can score, thus eliminating the need for the team to risk a stolen base attempt**.

**Increased Strikeout Rate, Decreased Batting Average**

Accompanying the home run revolution is the **continuous increase in the league's pitcher strikeout rate**. This is because batters' goal is **no longer just to make contact with the ball, but to hit it hard**, even if it means a larger swing path and a higher chance of striking out. We can look at the "Contact" statistic. Contact represents a batter's ability to make contact with the ball, so a lower Contact% means batters are making less contact, which leads to more strikeouts. **Over the past decade, batters' strikeout rates have continuously risen, while Contact% has steadily declined.** All of the above situations illustrate that for batters to score from base, **instead of waiting for a hit or hoping for an infield ground ball to advance, it's better to just blast the white ball out of the park**, which also makes stolen bases less important.

![](https://i.imgur.com/gqFWYyg.png)

<ins>MLB Batters' K% Over the Last Decade</ins>

![](https://i.imgur.com/36vVphF.png)

<ins>MLB Batters' Contact% Over the Last Decade</ins>

**The Impact of Stolen Bases on the Game**

While the effectiveness of stolen bases has decreased due to the increase in home runs, in fact, stolen bases offer more added value beyond just advancing runners.

An unnamed Braves legend once said:

> _I'd rather face Mark McGwire or José Canseco in a crucial moment than Rickey Henderson on base._

**The psychological pressure that stolen bases put on pitchers is difficult to quantify.** A speedy runner on base showing a desire to steal puts immense pressure on the pitcher. When they successfully steal, it makes the pitcher feel like they've given up a base for free, affecting their morale.

Furthermore, to **prevent stolen bases, pitchers' throwing strategies also change accordingly.** To shorten the time it takes for the ball to travel from the pitcher's mound to the catcher's mitt, thereby reducing the time for a pickoff, pitchers will **incorporate more fastballs** and reduce the use of off-speed pitches. For the batter at the plate, this makes it easier to anticipate pitch types and attack.

Therefore, stolen bases remain a very important tactic.

**Quantifying the Value of Stolen Bases?**

So, has the value of stolen bases truly decreased?

We can measure this using **runs generated after a stolen base**.

**The wSB statistic** simply put is: **runs added by a runner due to a stolen base - average runs added by league runners due to a stolen base**. Since wSB is a result of **comparison to the league average**, looking at the league average wSB cannot tell us the value of stolen bases (the league average wSB will be 0 every season).

However, we can use the **standard deviation of wSB for each season** to determine the value of stolen bases.

The concept of standard deviation is about dispersion. In this example, **the larger the standard deviation, the higher the wSB for the top 50% and the lower the wSB for the bottom 50%**. What does this phenomenon represent? **It means that players with wSB above average can generate more runs through stolen bases than average players, which indirectly indicates that the value of stolen bases is higher and can help score runs.**

_Small note: Of course, some readers might wonder if the value of stolen bases for the entire league simultaneously increased or decreased, the standard deviation would not change, making it impossible to observe changes in stolen base value. This statement is indeed correct. However, the trend of change in standard deviation in the data I collected is very clear, so the above concern can likely be dismissed._

If the preceding explanation confused you, I'll summarize my hypothesis again here:

**The larger the standard deviation of wSB for all players in a single season, the higher the value of stolen bases; the smaller the standard deviation of wSB for all players in a single season, the lower the value of stolen bases.** Therefore, let's look at the changes in wSB standard deviation over the past 10 years.

![](https://i.imgur.com/nZOtYCm.png)

It can be observed that the **standard deviation has shown a downward trend over the past 10 years**. In the chart, I also included data from 1980, when stolen bases were prevalent, for comparison. It can be seen that the wSB standard deviation in 1980 was indeed very high, indicating that **the impact of stolen bases on the game back then was much greater than it is now**!

**Has the Value of Stolen Bases Decreased, So We Shouldn't Steal Anymore?**

As mentioned earlier, "stolen base ability" can influence the game on the field in many ways, such as increasing pressure on the pitcher and creating good hitting opportunities. Furthermore, with the aid of modern technology, a lot of stolen base data and information can help teams determine in real-time whether it's a good time to steal, leading to a **gradual increase in stolen base success rates**. Therefore, rather than saying stolen bases are unimportant, it's more accurate to say that **stealing bases at the right moment with the appropriate player has become increasingly crucial.**

![](https://i.imgur.com/RfHbGep.png)

**Conclusion**

Due to the **fly ball revolution, the stolen base tactic is no longer prevalent in the league**. Instead, teams prefer to score by blasting the ball over the outfield wall. And according to our estimation using the standard deviation of wSB, **the run-scoring ability of stolen bases is indeed no longer as high as it once was**. However, the author believes that **stolen bases remain an indispensable tactic on the baseball field**, especially in do-or-die games like the postseason, where a single successful steal could very well be the key to the game!

Reference materials:

[https://athlonsports.com/mlb/whats-stolen-base](https://athlonsports.com/mlb/whats-stolen-base), [https://www.mlb.com/cut4/why-are-stolen-bases-so-rare/c-283918854](https://www.mlb.com/cut4/why-are-stolen-bases-so-rare/c-283918854)

Data Sources: Fangraphs, Baseball Reference

Video Source: Made the Cut: [https://www.youtube.com/watch?v=LkvsGVQ7DKY&t=50s](https://www.youtube.com/watch?v=LkvsGVQ7DKY&t=50s)

Cover Source: _Ed Zurga/Getty Images_