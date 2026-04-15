---
layout: page
title: 2023 AI Training Dataset Construction Project
description: Heading a collaborative project with multiple companies to construct a comprehensive Hand-Object Interaction dataset.
img: assets/img/dense.png
importance: 1
category: work
related_publications: true
---

From March to December 2023, I led a national AI training data initiative organized by the National Information Society Agency of Korea (NIA). This ambitious project focused on building a world-class dataset for hand-object interaction, with contributions from three industry partners and KAIST.


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/HardwareSetup.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/dense.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    (left) Multi-camera studio setup (right) Structure of HOGraspNet. It captures diverse hand-object grasping at 4 different viewpoints. Example RGB images (A) and depth images (B) are shown, while the fitted hand and object meshes are visualized in (C) and (D). (E) shows the contact map.
</div>



## Project Scope and Collaboration

This was a comprehensive end-to-end R&D project encompassing:
- Data collection using a multi-view camera system
- Data annotation with custom-built toolkits and frameworks
- Rigorous verification and validation, including AI model development

As the project lead, I guided the overall planning and execution, directly implemented core processing methods, and coordinated collaboration across all partners—from technical roles to data sharing protocols.

## Technical Approach & Implementation

Key accomplishments include:
- Designing and establishing a multi-view camera studio tailored for dataset capture
- Defining dataset details, participant guidelines, and collection protocols
- Developing custom error filtering and sampling toolkits for data refinement
- Implementing an optimization framework to extract accurate 3D poses from RGB-Depth data
- Generating precise ground-truth via iterative mesh-based rendering workflows including hybrid verification step



<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/AnnotationDiagram.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Automatic annotation pipeline.
</div>



## Quality Control & Validation

To maximize data quality:
- Utilized a bootstrapping approach to reject the outlier pseudo GT keypoints
- Fine-tuned the segmentation model per object with our manually annotated segmentation masks
- Conduct both automatic and manual verification steps to further filter out the noisy annotations


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/segmentation_examples.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Examples of our pseudo GT segmentation masks.
</div>


## Role & Impact
As the general lead, I navigated both technical and organizational challenges—solving engineering problems while driving efficient communication between companies.
The project was successfully completed within a short timeline thanks to cohesive teamwork and agile execution. This hands-on experience in large-scale AI data construction and multi-stakeholder coordination has become a cornerstone of my skillset for future endeavors.


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/AllSample_filtered.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Diverse samples in HOGraspNet (best viewed with zoom-in). HOGraspNet captures all hand-object grasp taxonomies with high-quality 3D annotations.
</div>

## Cite

    ---
    @inproceedings{cho2024dense,
    title={Dense hand-object (ho) graspnet with full grasping taxonomy and dynamics},
    author={Cho, Woojin and Lee, Jihyun and Yi, Minjae and Kim, Minje and Woo, Taeyun and Kim, Donghwan and Ha, Taewook and Lee, Hyokeun and Ryu, Je-Hwan and Woo, Woontack and others},
    booktitle={European Conference on Computer Vision},
    pages={284--303},
    year={2024},
    organization={Springer}
    }
    ---