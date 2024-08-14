---
title: "Classic Hebbian learning endows feed-forward networks with sufficient adaptability in challenging reinforcement learning tasks"
excerpt: "Reinforcement learning agents can suffer from inadaptability post-optimization. Training using Hebbian learning, however, partly corrects this, and here I discuss potential imporvements which could arise from taking even further inspiration from biology."

author_profile: true
share: true
comments: false
related: true

show_date: true
date: 2021-05-28

header:
  teaser: /assets/images/research/BurnsJNeurophysiol2023/JNeurophysiol-logo-th.png
  overlay_image: /assets/images/research/BurnsJNeurophysiol2023/JNeurophysiol-logo.jpg
  overlay_filter: 0.5
  actions:
  - label: "PDF"
    url: "/assets/pdfs/Burns-JME-2023.pdf"
  - label: "BibTex"
    url: "/assets/bibtexs/Burns-JME-2023.bib"

categories:
  - Transformers & associative memory
---

A common pitfall of current reinforcement learning agents implemented in computational models is in their inadaptability post-optimization. Recent work demonstrates how such adaptability may be salvaged in artificial feed-forward networks by optimizing coefficients of classic Hebbian rules to dynamically control the networks’ weights instead of optimizing the weights directly. Although such models fail to capture many important neurophysiological details, allying the fields of neuroscience and artificial intelligence in this way bears many fruits for both fields, especially when computational models engage with topics with a rich history in neuroscience such as Hebbian plasticity. Here I discuss how taking more inspiration from neuroscience may further improve these models further, such as via altering the neuron and network structure, dynamic and intrinsic output values of neurons, and distributions of plasticity and learning rules.