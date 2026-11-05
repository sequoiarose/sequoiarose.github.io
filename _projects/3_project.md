---
layout: page
title: Effect of Bomb Threats on Voter Turnout
description:
img: assets/img/georgia-turnout-2020-2024.png
importance: 2
category: PhD Research
related_publications: true
---

In the 2024 general election, bomb threats disrupted polling places across Georgia, USA, prompting several counties to extend voting hours in response. Working with Professor Philip Stark, I used non-parametric, Monte Carlo permutation tests to evaluate whether extending polling hours actually compensated for the disruption, testing for evidence of a measurable effect on the in-person day-of voter turnout in affected precincts.

Results found statistically significantly lower turnout in DeKalb County and a non-significant difference in Fulton. Ultimately these results indicate that extending polling hours do not compensate for poll closures due to threats.

{% include figure.liquid path="assets/img/georgia-turnout-2020-2024.png" class="img-fluid rounded z-depth-1" alt="Two scatter plots comparing the 2020 and 2024 relative in-person turnout statistic for DeKalb precincts and Fulton polling sites, with threatened locations marked by orange crosses" caption="Relative in-person turnout statistic in 2020 vs. 2024 for DeKalb precincts and Fulton polling sites. Orange crosses mark locations with credible bomb threats; points below the line had higher relative in-person turnout in 2024 than in 2020. From the BSTARS 2025 poster." zoomable=true %}

The code and data for this analysis are available in the [georgia-2024-election repository](https://github.com/sequoiarose/georgia-2024-election), with the paper presented at E-Vote-ID 2025 and available here {% cite andrade2025extending %}. A poster presented at BSTARS is available [here](/assets/pdf/BSTARS_2025_Sequoia.pdf). The results were also presented in a panel at the ESRA conference in June 2026.
