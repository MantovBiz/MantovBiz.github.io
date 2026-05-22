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

<img width="100" height="200" alt="Personnel Groupings Chart" src="https://github.com/user-attachments/assets/43a6524f-ff83-4a97-9637-3f01afb9d3c7" />

For example, **11 personnel** means 1 RB, 1 TE, and 3 WRs. **12 personnel** means 1 RB, 2 TEs, and 2 WRs.

<img width="733" height="490" alt="chi_offense_personnel" src="https://github.com/user-attachments/assets/635935e0-6520-4195-8fa5-dde789fe9ca6" />

The Chicago Bears were a heavy 11-personnel team with 663 of their plays being run in that group, followed by 428 plays in 12 personnel and 120 in 13 personnel. After seeing those numbers, I decided to look into the snap counts of the tight ends using PFF. Kmet had 768, Loveland had 701, Smythe had 293, and Carlson had 14, which amounts to 1,776. After adding up the plays from R, it came out to be (1×685) + (2×439) + (3×122) = 1,929 total TE snaps. That is a significant difference, and it is important to note that PFF states snap counts are unofficial. Looking further into this, I learned that offensive linemen can line up as one of the tight ends. This is typically done in short-yardage situations to bring a bigger body to the line of scrimmage. It does not happen very often, hence the 153-snap difference between tight end snap counts and the overall personnel group totals. Context matters a lot if we want to understand the bigger picture.

The Chicago Bears' 12-personnel grouping had the highest success rate at 46.96% (minimum of 10 plays) and the most yards per play at 6.04. The two most prominent tight ends were Cole Kmet and Colsten Loveland, and there was draft capital behind Loveland as the 10th overall pick. Ben Johnson selected him with the intention of using him, which they did throughout the course of the season.

### Regular Season vs Playoffs
<img width="774" height="799" alt="chi_offense_reg_vs_playoffs" src="https://github.com/user-attachments/assets/9a91905b-6a3e-454b-8817-025aa24b9e39" />

After looking at the overall season, I wanted to see if there was a difference in their approach in the playoffs versus the regular season. A few things stood out: 11 personnel usage dropped by about 9%, and the 12-personnel success rate improved by over 10%. That said, the sample sizes are significantly different, so keep that in mind when looking at the averages because a few big plays can skew the yards per play, which is wh you see a number like 8.71.

This table is more of a look at how tendencies transferred from the regular season to the playoffs across the three most commonly used personnel groups. A direct comparison is difficult given both the difference in sample size and the elevated stakes of playoff football.



