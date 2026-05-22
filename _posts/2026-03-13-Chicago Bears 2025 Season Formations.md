---
layout: post
title: "Breaking Down the Chicago Bears Formations for the 2025/2026 Season"
date: 2026-03-13
categories: [research]
tags: [NFL, Chicago Bears]
---

In this article, I will examine the defensive formations and personnel groupings the Chicago Bears used during the 2025 NFL season. I will be breaking down the regular season and postseason data using play-by-play data from nflverse. The goal is to break down what formations the Bears used on both sides of the ball and get a better understanding of their identity. The full R code used to produce the tables below is available [here](https://github.com/MantovBiz/NFL-fast-R-Data-Visualizations-and-Breakdowns/tree/main/Chicago-Bears/2025)

---

## Terminology

Here are some football terms that will be mentioned throughout the article.

**EPA (Expected Points Added)** measures how much a play helped or hurt a team relative to what was expected given the down, distance, and field position. A positive EPA means the play outperformed expectations; a negative EPA means it didn't.

**Success Rate** is defined as a play that gains aleast 40% of the required yards on first down, 60% on second down, and 100% on third or fourth down. 

**Yards Per Play (YPP)** is the average yards gained per play. On defense, this is known as Yards Per Attempt (YPA) since it applies only to pass plays.

---

## Offense

### Playcaller and Roster

**Offensive Playcaller:** Ben Johnson

| Position | Players |
|---|---|
| QB | Caleb Williams, Tyson Bagent, Case Keenum |
| RB | D'Andre Swift, Kyle Monangai, Roschon Johnson |
| WR | DJ Moore, Rome Odunze, Luther Burden III, Olamide Zaccheaus, Devin Duvernay  |
| TE | Colston Loveland, Cole Kmet |

---

### Personnel Groups

NFL offensive personnel is described using a two-digit shorthand based on the number of running backs and tight ends on the field. The first digit represents the number of RBs (including fullbacks), and the second represents the number of TEs. The remaining skill players are wide receivers.

![Personnel Groupings Chart](https://github.com/user-attachments/assets/43a6524f-ff83-4a97-9637-3f01afb9d3c7)

For example, **11 personnel** means 1 RB, 1 TE, and 3 WRs. **12 personnel** means 1 RB, 2 TEs, and 2 WRs.

<img width="1466" height="980" alt="chi_offense_personnel" src="https://github.com/user-attachments/assets/635935e0-6520-4195-8fa5-dde789fe9ca6" />

The Chicago Bears were a heavy 11-personnel team with 663 of their plays being run in that group. Then 428 plays in 12 personnel and 120 in 13 personnel. After seeing those numbers I decided to look into the snap counts of the tight ends by using PFF. Kmet had 768, Loveland had 701, Smythe had 293 and Carlson had 14 which amounts to 1776. After adding up the plays from R it came out to be (1*685) + (2*439) + (3*122) = 1929 total TE snaps on R. Which I think is a significant differnce and it is important to note that PFF says snap counts are unofficial. After looking further into this I learned that offesnive linemen can come in as one of hte tight ends. This is typically done in short yard situations to help bring a bigger body. It doesnt happen very often hence why there is a 153 snap count difference between tight ends and the overall personeel groups. Context matters a lot if we want to understand the bigger picture. 

The Chicago Bears 12 man personeel had the highest success rate with 46.96% (min of 10 plays) and the most yards per play at 6.04. The two most promiment tight ends being played were Cole Kmet and Colsten Loveland and there was draft captial behind Loveland because he was the 10th overall pick. So Ben Johnson drafted him with the intention of using him, which they did throughout the course of the season. 

### Regular Season vs Playoffs
<img width="1548" height="1598" alt="chi_offense_reg_vs_playoffs" src="https://github.com/user-attachments/assets/9a91905b-6a3e-454b-8817-025aa24b9e39" />

After looking at the overall season, I decided to see if there was a difference in their approach in the playoffs vs regular season. Some things that were intersted to see comparing both was how 11 peronseel dropped by about 9% and 12 personeel success rate improved by over 10%. Granted the sample size is significantly different so keep that in mind with the averages because there can be big plays that can sway the averages of YPP which is why you see 8.71 for example.

This is more of a table to see the tendencies tranfer form regular season to playoffs with the three most commonly used personeel groups. It is more difficult to compare because of the level of importance from regular season to playoffs as well as the sample size.  




