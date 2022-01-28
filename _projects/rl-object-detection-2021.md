---
layout:      project
title:       Improvements of Active Object Localization with Deep Reinforcement Learning
date:        10 Nov 2021
image:
  path:       /assets/img/projects/rl-object-detection-2021.jpg
  srcset:
    1920w:   /assets/img/projects/rl-object-detection-2021.jpg
    960w:    /assets/img/projects/rl-object-detection-2021@0,5x.jpg
    480w:    /assets/img/projects/rl-object-detection-2021@0,25x.jpg
caption:     "In this project, we proposed several improvement in four aspects, including using advanced CNNs to generate state representation, 
    defining more flexible action spaces, changing reward function to avoid undesired activity in agent and using mask instead cross for multiple objects."
description: >
    "In this project, we proposed several improvement in four aspects, including using advanced CNNs to generate state representation, 
    defining more flexible action spaces, changing reward function to avoid undesired activity in agent and using mask instead cross for multiple objects."
links:
  - title:   Paper
    url:     /papers/E6885_Final_Project.pdf
  - title:   GitHub
    url:     https://github.com/JiaweiLu1999/DRL-Object-Detection
featured:    true
---

- **Abstract**

Object localization is a research area with wide range of application scenarios, which has been extensively explored. However, there is a trend to incorporate deep reinforcement learning recently because it is believed to conform better to natural object searching process by human. Although several previous works have built a concrete basis by defining state, action and reward, there is still much field to explore for higher efficiency and accuracy. 

In this paper, we proposed several improvement in four aspects, including using advanced CNNs to generate state representation, defining more flexible action spaces, changing reward function to avoid undesired activity in agent and using mask instead cross for multiple objects. All these improvements are tested with extensive experiments and proved its effectiveness. They are also flexible enough to get incorporated into other works to achieve even higher performance.