---
layout: page
title: Natural Language Processing for Aviation Safety Management
description: NLP tools for knowledge discovery from aerospace safety reports, built at NASA Ames Research Center
img: assets/img/mika-architecture.png
importance: 3
category: NASA Research
related_publications: true
---

Engineers and safety analysts sit on decades of incident reports, accident investigations, and lessons-learned documents, but this
knowledge lives in unstructured narrative text that is slow to search and hard to analyze at scale. At NASA Ames Research Center, I
helped develop the [Manager for Intelligent Knowledge Access (MIKA)](https://github.com/nasa/mika), an open-source Python toolkit
that applies natural language processing to these documents to support design-time risk analysis and safety assurance
{% cite andrade2023mika %}.

MIKA has two main components. The **knowledge discovery** module extracts structured information from narrative reports using
topic modeling, custom named-entity recognition, and hazard trend analysis. The **information retrieval** module provides semantic
search over document collections with a bi-encoder/cross-encoder pipeline {% cite walsh2022semantic %}. Both are built on BERT
language models, including two I developed:

- **[SafeAeroBERT](https://huggingface.co/NASA-AIML/MIKA_SafeAeroBERT)** is a BERT model further pre-trained on over 350,000 Aviation
  Safety Reporting System (ASRS) and National Transportation Safety Board (NTSB) reports, roughly 1 billion tokens of aviation safety
  text. On contributing-factor classification it outperformed general-purpose BERT and SciBERT on procedure- and weather-related
  factors {% cite andrade2023safeaerobert %}.
- **[MIKA BERT FMEA NER](https://huggingface.co/NASA-AIML/MIKA_BERT_FMEA_NER)** is a named-entity recognition model fine-tuned on
  annotated NASA Lessons Learned reports to extract failure causes, failure modes, effects, control processes, and recommendations,
  the building blocks of a Failure Modes and Effects Analysis (FMEA). I applied it to survey mishaps involving uncrewed aircraft in
  wildfire response {% cite andrade2022what %}.

{% include figure.liquid path="assets/img/mika-architecture.png" class="img-fluid rounded z-depth-1" alt="Tree diagram of the MIKA toolkit: data, knowledge discovery, information retrieval, and utility modules, plus examples and trained models" caption="Overview of the MIKA toolkit architecture, from Andrade & Walsh (2023)." zoomable=true %}

Using MIKA, I developed the Hazard Extraction and Analysis of Trends (HEAT) framework for identifying hazards and their trends in
wildfire emergency response reports {% cite andrade2021wildfire andrade2023machine %}, and extended it to NLP-enabled quantitative
risk analysis of aerial wildfire operations {% cite andrade2022machine andrade2024natural %}. The toolkit has also been used to build
failure taxonomies for the early design of complex engineered systems {% cite andrade2021knowledge andrade2023discovering %}.

MIKA can be installed with `pip install nasa-mika`. Documentation and source code are available in the
[MIKA GitHub repository](https://github.com/nasa/mika), and the trained models are hosted on
[NASA-AIML's Hugging Face page](https://huggingface.co/NASA-AIML).
