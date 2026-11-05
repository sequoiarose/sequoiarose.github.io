---
layout: page
title: Prescribed Burn Efficacy in the Changing California Climate
description: Prescribed Burn Efficacy in the Changing California Climate
img: assets/img/rx-burns-wildfire-map.png
importance: 2
category: Master's Thesis
related_publications: true
---

With climate change-driven large, destructive wildfires becoming more frequent,
especially in California, using data to identify effective or ineffective prevention
strategies, such as prescribed burns, can inform future prevention strategies. In this
work, we present a statistical analysis on a new dataset created by fusing wildfire,
prescribed fire, and climate data. Descriptive and inferential statistics, time series
analysis, and regression analysis are applied to the dataset to analyze if prescribed
burns are associated with reduced wildfire size while accounting for climate variables.
When grouped across the entire state with a monthly time scale, results indicate
prescribed burns do not impact the number of wildfire acres burned. However,
the impact of prescribed burns is significant when considering individual fires, even
when controlling for climate variables. Climate variables have a stronger impact on
wildfire size, though prescribed burns are associated with slightly smaller wildfires {% cite andrade2024statistical %}.

{% include figure.liquid path="assets/img/rx-burns-wildfire-map.png" class="img-fluid rounded z-depth-1" alt="Four maps of California, each showing one year of prescribed burns in blue and the wildfires of the following three years in red, orange, and yellow" caption="Prescribed burns (blue) and the wildfires that followed them over the next three years (red, orange, yellow), sized by area burned. Each panel starts from one year of prescribed burns." zoomable=true %}

The full thesis, presentation, and reproducible code is available in the [rx_burns_wildfires repository](https://sequoiarose.github.io/rx_burns_wildfires/).
