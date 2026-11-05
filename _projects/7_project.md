---
layout: page
title: Wildfire Response Systems Modeling
description: Simulating wildfire response to measure how drones and UAS traffic management affect performance and resilience
img: assets/img/smart-stereo-fire-progression.png
importance: 4
category: NASA Research
related_publications: true
---

Aerial firefighting still relies largely on radio-based coordination, which limits how well crews and aircraft can share information
about a fire. NASA's Scalable Traffic Management for Emergency Response Operations (STEReO) project explored using Unmanned Aerial
Systems (UAS) and UAS Traffic Management (UTM) to improve this coordination. Before these technologies are adopted, though, it matters
whether their benefits actually outweigh the new hazards they introduce.

As part of the System Modeling and Analysis of Resiliency in STEReO (SMARt-STEReO) project at NASA Ames Research Center, I helped build
a dynamic simulation of wildfire response using [fmdtools](https://github.com/nasa/fmdtools), NASA's open-source Python library for
modeling, simulating, and analyzing the resilience of complex systems. The model combines grid-based fire propagation with
surveillance and communication, response planning, and mitigation actions by ground crews and aerial assets, and represents both
current operations and STEReO's proposed concepts {% cite walsh2020smart hulse2020smart %}.

{% include figure.liquid path="assets/img/smart-stereo-fire-progression.png" class="img-fluid rounded z-depth-1" alt="Three snapshots of the SMARt-STEReO simulation grid at time steps 0, 10, and 20, showing a fire spreading from the center while firelines are built around the edges" caption="Fire progression in the SMARt-STEReO simulation at time steps 0, 10, and 20 (eight minutes each). Color shows time-to-ignition; black dots are completed fireline, triangles are ground crews and surveillance aircraft. From Andrade & Hulse (2022)." zoomable=true %}

Simulating the model over many scenarios, I used statistical tests (t-tests and ANOVA) to compare current operations against UAS-enabled
response. Adding UAS reduced the number of acres burned and improved the system's resilience to faults {% cite andrade2021smartstereo %}.
In a follow-up study, we evaluated how improved communications and surveillance affect fire containment and ground crew injuries,
under both existing and newly introduced fault scenarios. These improvements increased containment and reduced injuries across
single-fault scenarios, making the system more resilient overall, but the benefits could be negated if the new communications
infrastructure is prone to full-scale outages {% cite andrade2022evaluation %}.

The SMARt-STEReO model was later paired with the [MIKA]({{ '/projects/6_project/' | relative_url }}) natural language processing toolkit to support hazard
analysis for NASA's wildfire response safety demonstrations {% cite andrade2022supporting %}.
