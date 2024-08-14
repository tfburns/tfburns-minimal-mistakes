---
title: "A Bergson-Inspired Adaptive Time Constant for the Multiple Timescales Recurrent Neural Network Model"
excerpt: "Cognitive neurorobotics using recurrent neural networks and naturalistic time-series data."

author_profile: true
share: true
comments: false
related: true

show_date: true
date: 2018-10-1

header:
  teaser: /assets/images/research/BurnsetalJNNS2018/screengrab-th.png
  overlay_image: /assets/images/research/BurnsetalJNNS2018/screengrab.PNG
  overlay_filter: 0.5
  actions:
  - label: "PDF"
    url: "/assets/pdfs/Burns-etal-JNNS-2018.pdf"
  - label: "BibTex"
    url: "/assets/bibtexs/Burns-etal-JNNS-2018.bib"
  - label: "GitHub"
    url: "https://github.com/oist-cnru/mouse_drawing_app"

categories:
  - Robotics & RNNs
---

For this project, it was important to use naturalistic yet low-dimensional data. For this purpose, I built a simple GUI application in Python to generate and collect 2D mouse input data (available on [GitHub](https://github.com/oist-cnru/mouse_drawing_app)).

![jpg](/tfburns-minimal-mistakes/assets/images/research/BurnsetalJNNS2018/figure1.jpg)

I then used these data as training inputs to various recurrent neural networks (RNNs), and also adapted them for use in robotic arms, circumventing the inverse kinematics problem by interpolating joint-angles (within some safety bounds) between the four corners of a a 2D plane.

![jpg](/tfburns-minimal-mistakes/assets/images/research/BurnsetalJNNS2018/figure2.jpg)

We can then interact with the learnt behaviour physcally via compliant robots and see what happened when humans intervened and 'pushed' them into different patterns. Animations below showing some of the 2D patterns as learnt by an RNN.

![gif](/tfburns-minimal-mistakes/assets/images/research/BurnsetalJNNS2018/circle.gif)

![gif](/tfburns-minimal-mistakes/assets/images/research/BurnsetalJNNS2018/figure-of-8.gif)

With this data and training, we then introduced an adaptive time constant for the multiple timescales recurrent neural network (MTRNN) inspired by the work of philosopher Henri Bergson (1859-1941). Observed variations in the recent activity of MTRNN neurons is used to adapt the time constant. We analysed how the time constant adapts in response to neuronal activity for a simple one-dimensional function-fitting task.

This work was completed during the first, 4-month research unit rotation of my PhD. It was completed in the lab of Jun Tani, with a lot of mentorship and suport from the other lab members, especially Fabien C. Y. Benureau, who was a post-doc in the lab. I sincerely thank them for all their support.