---
layout: page
title: Smoke and Cloud Image Segmentation
description:
img: assets/img/smoke-cloud.jpg
importance: 3
category: NASA Research
related_publications: true
---

Advanced satellite data is increasingly used for wildfire detection and monitoring, yet near real-time hotspot data products from the GOES-R series often have low confidence due to aerosol contamination. Since aerosol contamination impacts the confidence of the GOES-R hot spot detection algorithm, regardless of contamination from fire-indicating smoke or false positive-indicating clouds, differentiating smoke from cloud has the potential to improve the accuracy of real-time hot spot detection. The primary contribution of this paper is a multi-class smoke and cloud segmentation model that classifies smoke, cloud, and neither pixels from GOES-R true color images in a real-time application. When selecting the final model, we perform an experiment to examine the impact self-supervised learning has on different model architectures. The final model is a U-Net model pre-trained on over 10,000 images using Barlow Twins self-supervised learning and fine-tuned using supervised learning, which exhibits comparable performance to the larger and slower ResUnet model. Our model improves upon existing satellite-based smoke segmentation, with 85% accuracy and 68% mean intersection-over-union on the test set. The model is deployed in an Open Data Integration for wildfire management (ODIN) application, allowing for real-time smoke and cloud detection to improve situational awareness regarding smoke location. From real-time image import to smoke-cloud segmentation display in the browser, the total run time is approximately 74 s, with 52 s total from the segmentation model pipeline {% cite andrade2025smoke %}.

The smoke-cloud segmentation model is [open-source on Hugging Face](https://huggingface.co/sequoiaandrade/Smoke-Cloud-Segmentation-RACE-ODIN), as well as the [labeled training dataset](https://huggingface.co/datasets/sequoiaandrade/Smoke-Cloud-Segmentation-RACE-ODIN-Data), [model training code](https://github.com/sequoiarose/smoke-segmentation), and [ODIN code](https://nasarace.github.io/race-odin/). Early results were presented at AGU 2024 {% cite andrade2024improving %}.

{% include figure.liquid path="assets/img/smoke-cloud.jpg" title="Smoke vs. cloud classification" class="img-fluid rounded z-depth-1" caption="Example output from the smoke/cloud classifier." zoomable=true %}
