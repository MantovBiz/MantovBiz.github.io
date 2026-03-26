---
layout: post
title: "Breaking Down the Chicago Bears Formations for the 2025/2026 Season"
date: 2026-03-13
categories: [research]
tags: [NFL, Chicago Bears]
---

In this article, I will be looking at the different defensive formations and personnel groupings the Chicago Bears used in the 2025 NFL season. I will be breaking down the regular season and postseason data using play-by-play data from nflverse. The goal is to break down what formations the Bears used on both sides of the ball and get a better understanding of their identity. The full R code used to produce the tables below is available [here](https://github.com/MantovBiz/NFL-fast-R-Data-Visualizations-and-Breakdowns/tree/main/Chicago-Bears/2025)

---

## Terminology

Here are some football terms that will be mentioned throughout the article.

**EPA (Expected Points Added)** measures how much a play helped or hurt a team relative to what was expected given the down, distance, and field position. A positive EPA means the play outperformed expectations; a negative EPA means it didn't.

**Success Rate** is the percentage of plays that gained enough yards to be considered "successful" — typically 40% of needed yards on first down, 60% on second down, and 100% on third or fourth down.

**Yards Per Play (YPP)** is the average yards gained per play. On defense, this is known as Yards Per Attempt (YPA) since it applies only to pass plays.

---

## Offense

### Playcaller and Roster

**Offensive Coordinator:** Ben Johnson

| Position | Players |
|---|---|
| QB | Caleb Williams, Tyson Bagent, Case Keenum |
| RB | D'Andre Swift, Kyle Monangai |
| WR | DJ Moore, Rome Odunze,  |
| TE | Colston Loveland, Cole Kmet |

---

### Personnel Groups

NFL offensive personnel is described using a two-digit shorthand based on the number of running backs and tight ends on the field. The first digit represents the number of RBs (including fullbacks), and the second represents the number of TEs. The remaining skill players are wide receivers.

![Personnel Groupings Chart](https://github.com/user-attachments/assets/43a6524f-ff83-4a97-9637-3f01afb9d3c7)

For example, **11 personnel** means 1 RB, 1 TE, and 3 WRs. **12 personnel** means 1 RB, 2 TEs, and 2 WRs, a heavier look often used in run-heavy situations or play-action.

<img width="1466" height="980" alt="chi_offense_personnel" src="https://github.com/user-attachments/assets/635935e0-6520-4195-8fa5-dde789fe9ca6" />
