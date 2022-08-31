---
layout: page
title: Knowledge Proliferation in Academic Documents
description: Understand important concepts in academic documents and link them to authors, publications, and each other. My work focuses on understanding important keyphrases in research articles.
img: /assets/img/keyphrase.png
---

<br />

To understand knowledge proliferation, we first need to understand what are important keyphrases in research documents. In the past, all work in keyphrase extraction is based on ideas derived from information theory - something is important if it is uncertain in a particular context, given some background knowledge. We look at importance from a completely different perspective, which is based on the <b>impact on downstream applications</b>. 

<br />

### Method

<br />

We extract candidate phrases from a research article, which is the set of all noun phrases. We then train a model to perform auxiliary tasks like Topic Prediction, Open Review User Keywords Prediction, Summarization and Representation Learning to learn importance attribution. We then use the influence scores to rerank keyphrases. The main idea is that a phrase is <i>important</i> if it influences a downstream task's prediction.
