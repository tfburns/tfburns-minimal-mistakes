---
title: "Simplicial Hopfield networks"
excerpt: "Without increasing the total number of parameters, we improve the memory capacity of associative memory networks by adding setwise connections embedded in a simplicial complex."

author_profile: true
share: true
comments: false
related: true

show_date: true
date: 2023-01-20

header:
  teaser: /assets/images/research/BurnsFukaiICLR2023/diagram-th.png
  overlay_image: /assets/images/research/BurnsFukaiICLR2023/diagram.png
  overlay_filter: 0.5
  actions:
  - label: "PDF"
    url: "https://openreview.net/forum?id=_QLsH8gatwx"
  - label: "X thread"
    url: "https://x.com/tfburns/status/1631182727147048960"
  - label: "Talk"
    url: "https://www.youtube.com/watch?v=dlg2L4yXWak"
  - label: "Press release"
    url: "https://www.oist.jp/news-center/news/2023/3/7/what-makes-neural-network-remember"

categories:
  - Transformers & associative memory
---

Neurons in the brain take on wonderous and sophisticated shapes, stretching and crawling between one another to each make thousands of connections. Mediated by a ballet of biochemistry, they use brief electrical impulses to pass signals between each other at these connections. These impulses vary in size, electrical charge, timing, and even location on the neuron. And because these impulses are so brief while at the same time being so various in type, space, and time, our brains have evolved to become biological supercomputers capable of learning and becoming experts in many tasks while keeping energy consumption low. Our challenge is to discover and understand the algorithms and principles behind this complexity. 

Many previous computational models of memory have been produced with various levels of biological complexity. In this work, we focused on one understudied piece of the puzzle: setwise connections. Drawing inspiration from biology, we extended an associative memory network (sometimes also called a Hopfield network) by replacing pairwise connections between neurons with sparse, group connections to better reflect how neurons and other cells wire up in the brain. In doing so, we found the network can successfully store and recall more memories.

The way associative memory networks store memories as patterns of weighted connections between different neurons in the system. The network is “trained” to encode these patterns, and then we test its memory of them by presenting a series of blurry or incomplete patterns to see if the network can recognise them as one it already knows. In classical networks, however, neurons in the model connect reciprocally to form a series of “pairwise” connections. Pairwise connections represent how two neurons connect at a synapse, a connection point between neurons in the brain. But in reality, neurons have intricate branched structures called dendrites that provide multiple points for connection; evidence from neuroscience studies indicates the brain uses this much more complex arrangement of connections to perform more sophisticated computations. Additionally, connections of various orders between neurons are also modulated by other cell types, such as astrocytes.

Altogether, this work indicates the computational affordances of structures such as dendrites and astrocytes in biological neural networks in memory systems could be immense. It also offers new inspiration for Transformers’ attention mechanisms, an important component in modern AI systems such as ChatGPT.

Thank you to my co-author, Tomoki Fukai at OIST, for his support and guidance in this project and throughout my PhD studies.