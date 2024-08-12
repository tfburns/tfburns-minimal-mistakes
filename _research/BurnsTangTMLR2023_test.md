---
title: "Detecting danger in gridworlds using Gromov's Link Condition"
excerpt: "By representing all possible configurations of multi-agent gridworlds as a single geometric space, we show positive curvature detects potential collisions."

author_profile: true
share: true
comments: false
related: true

show_date: true
last_modified_at: 2024-08-11T00:00:00+01:00

read_time: true
words_per_minute: 200
categories:
  - AI interpretability & evaluation
---

![gif](/tfburns-minimal-mistakes/assets/images/research/BurnsTangTMLR2023/koala-ball-playing.gif)

In physics, spacetime is a geometric object which represents the three dimensions of space and the single dimension of time. Gravitational force is represented in this geometric object by its curvature. Can we do something similar in AI? For example, can we represent typical AI environments using a single geometric object? And if we could, what would its properties tell us?

Introducing tools from geometric group theory and combinatorics to the AI community, my co-author Robert Tang and I demonstrate a proof-of-concept via simple gridworld environments.

Gridworlds have been long-utilised in AI research, particularly in reinforcement learning, which itself has been used to successfully beat world-champions in board games like chess and Go and video games like StarCraft and DOTA 2. Gridworlds provide simple yet scalable models for potential real-world applications, e.g., safely coordinating the movements of self-driving cars or warehouse robots. A gridworld is made up of square cells, arranged in a grid, where cells can be occupied or not. In our gridworlds, cells can be occupied by a single agent (a koala) or object (a beach ball).

Starting at a chosen state in the gridworld – a specified arrangement of the agent(s) and object(s) in the gridworld – we explore all allowable actions. We allow two such actions: Move, letting an agent move to an adjacent empty cell; and Push/Pull, letting an agent push or pull an object in a straight line.

When we repeat this process enough times, we can generate the state complex. State complexes represent all possible configurations of a system as a single geometric object, which means we can study them using mathematical tools from geometry (shapes of things), topology (shapes of space), and combinatorics (counting and combining things). In the state complex, a ‘state’ of the gridworld is represented by a node, and if a state is reachable by another state, then we connect their nodes with a line. In the example below, orange lines are due to Push/Pull and maroon lines are due to Move.

![png](/tfburns-minimal-mistakes/assets/images/research/BurnsTangTMLR2023/staircase_v3_whitebg.PNG)

The main contribution of our work is a modification to the original method of constructing state complexes, which more naturally captures the relative movements of the agents. With this modification, the state complexes may exhibit new geometric defects, specifically: a change in curvature. However, we prove this can only happen under very specific circumstances. And, serendipitously, we discover these circumstances occur exactly when the agents could potentially collide!

Even though we didn’t seek out to detect potential collisions, our geometric object naturally captures critical safety information.

This result provides a new method for seeking guaranteed safety limitations in AI environments with single or multiple agents – and they needn’t be koalas, they could be self-driving cars taking you to work or warehouse robots fulfilling your Amazon delivery. More importantly, and more broadly, our result opens new ways for recasting and analysing AI problems as geometric ones.

Thank you to my co-author, Robert Tang at XJTLU, and to Anastasiia Tsvietkova at the Institute for Advanced Study and Rutgers University - Newark for supporting me as a rotation student in the Topology and Geometry of Manifolds Unit at OIST.
