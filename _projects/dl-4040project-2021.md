---
layout:      project
title:       A New Backbone for Hyperspectral Image Construction and Improvement based on Mask Mixture Training and Energy Normalization
date:        01 Nov 2021
image:
  path:       /assets/img/projects/SSI-ResU-Net.png
  srcset:
    1920w:   /assets/img/projects/SSI-ResU-Net.png
    960w:    /assets/img/projects/SSI-ResU-Net@0,5x.png
    480w:    /assets/img/projects/SSI-ResU-Net@0,25x.png
caption:     "We implemented mask mixture training and energy normalization. Those two changes have been proved to successfully improve the robustness of the SSI-ResU-Net. Besides, a combination of those two modifications can further improve the generalizing ability of SSI-ResU-Net."
description: >
    "We implemented mask mixture training and energy normalization. Those two changes have been proved to successfully improve the robustness of the SSI-ResU-Net. Besides, a combination of those two modifications can further improve the generalizing ability of SSI-ResU-Net. "
links:
  - title:   Paper
    url:     /papers/E4040.2021Fall.YZJH.report.ys3493.zy2501.jl5999.pdf
  - title:   GitHub
    url:     https://github.com/JiaweiLu1999/E4040-Final-Project-21Fall
featured:    true
---

- **Abstract**

The study of 3D hyperspectral image (HSI) reconstruction refers to the inverse process of snapshot compressive imaging when the optical system, e.g., the coded aperture snapshot spectral imaging (CASSI) system, captures the 3D spatial-spectral signal and encodes it to a 2D measurement. Although numerous neural networks have been built for end-to-end reconstruction, those previous works have a hard time balancing among performance, efficiency (training and inference time), and feasibility (the ability to restore high-resolution HSI on limited GPU memory). 

In this work, we try to solve this challenge by creatively proposing SSI-ResU-Net, Spatial/Spectral Invariant Residual U-Net.  The SSI-ResU-Net makes several modifications compared to U-Net: scale/spectral-invariant learning, and nested residual learning.  Benefiting from these updates,  the SSI-ResU-Net can achieve a trade-off between performance, efficiency, and feasibility. Apart from that, mask mixture training and energy normalization are integrated into the process of generating measurements to increase the ability to generalize for SSI-ResU-Net. The dataset of this work can be found at [here](https://www1.cs.columbia.edu/CAVE/databases/multispectral/).