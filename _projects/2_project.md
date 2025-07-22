---
layout: page
title: WISE AR UI/UX Platform Development for Smartglasses
description: Develop a real-time hand tracking system on Smartglasses for natural interaction
img: assets/img/Figure1.png
importance: 2
category: work
related_publications: true
---

Contributed to the development of WISE (Wearable Interface for Sustainable Enhancement) UI/UX, an intuitive smartglass interface designed to adapt to individual users and dynamic environments, ultimately empowering proactive personal growth. As part of this project, I proposed a 3D hand tracking system capable of estimating the user's dynamic hand pose and recognizing hand-based inputs in complex real-world settings.


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Figure1.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Visualization of reconstructed hand mesh with our method from Hololens2 RGB input. The hand mesh is rendered in the off-loaded server.
</div>



## Project Scope and Collaboration

Led the development of tracking and interaction technologies, enabling natural hand-based interactions with smartglasses in everyday settings. The overarching goal was to create a “magical,” intuitive smart glasses experience—usable anytime, anywhere—through a dynamic interface that adapts to user attention, intention, and context. My work focused on integrating a full understanding of users' hand interaction, real-time pose estimation, and adaptive input methods, culminating in a holistic AR UI/UX platform. 



## Technical Approach

Our goal is to propose a hand tracking system in HMD by estimating a set of hand pose joints and mesh vertices, given an input RGB image and joint pose prediction from the previous frame. To fully utilize the given information, we designed a two-stage structured approach. In the first stage, we extract a feature map from the input image and estimate coarse pose through adaptive-GCN based module. In the second stage, we refine the prediction by using the regressed coarse pose and the adaptive temporal pose feature induced from the latent feature map in the intermediate stage and the information of the previous frame.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Figure2.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Schematic of proposed system
</div>

To overcome the challenge of deploying a deep learning network onto the HPU of the Hololens 2, we devised the offloading framework. The image data captured from the Hololens 2 is transmitted to a server and processed by our system to predict the hand pose, and only the predicted hand pose data is sent back to the Hololens 2.


<div class="row">
    <div class="col-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Figure4.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Diagram of Offloading framework for HMD
</div>


## Performance

Quantitative results with the official test set of the FreiHAND dataset show close to state-of-the-art performance. Note that we perform the test assuming a zero value for all previous poses, as the FreiHAND is non-sequential. In other words, our method demonstrated notable accuracy even in the absence of temporal information, indicating its robustness in scenarios such as re-initialization due to tracking failure.

In the proposed offloading framework, we evaluated the average latency for each step, as shown in the figure(right). As we processed the latest image received on the server, the framerate perceivable by users remains consistent with the reported latency at 34.3 FPS. Furthermore, additional experiments showed that WiFi specifications and connection environment directly influence data transmission and reception latency. Hence, it is expected that the overall framerate of the proposed module will increase in the future with improved communication environments.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Figure5.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Figure6.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    (left) Comparison of 3D PCK on FreiHAND (right) Diagram of the latency for each step within our HMDServer offloading framework
</div>



<div class="row">
    <div class="col-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Figure7.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Qualitative results on FreiHAND and DexYCB
</div>


<div class="row">
    <div class="col-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Figure9.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Visual results on Hololens2 viewpoint. The scene is captured on Hololens2, and hand mesh is rendered in the off-loaded server.
</div>


## Reference

    ---
    @article{cho2024temporally,
    title={Temporally enhanced graph convolutional network for hand tracking from an egocentric camera},
    author={Cho, Woojin and Ha, Taewook and Jeon, Ikbeom and Jeon, Jinwoo and Kim, Tae-Kyun and Woo, Woontack},
    journal={Virtual Reality},
    volume={28},
    number={3},
    pages={143},
    year={2024},
    publisher={Springer}
    }
    ---