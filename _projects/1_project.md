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

## Project Scope and Collaboratio

This was a comprehensive end-to-end R&D project encompassing:
    - Data collection using a multi-view camera system
    - Data refinement and processing with custom-built toolkits and frameworks
    - Rigorous verification and validation, including AI model development
As the project lead, I guided the overall planning and execution, directly implemented core processing methods, and coordinated collaboration across all partners—from technical roles to data sharing protocols.

## Technical Approach & Implementation
Key accomplishments include:
- Designing and establishing a multi-view camera studio tailored for dataset capture
- Defining dataset scale, participant guidelines, and collection protocols
- Developing custom error filtering and sampling toolkits for data refinement
- Implementing an optimization framework to extract 3D models and poses from RGB-D data
- Generating precise ground-truth via iterative mesh-based rendering workflows

## Quality Control & Validation
To maximize data quality:
- Built a vision-based auto-inspection tool
- Designed a dual-stage review system using crowdsourcing
- Created robust inspection criteria and guidelines
For dataset validation, I took part in developing an AI model, defining evaluation tasks, and implementing a hand pose estimation algorithm that demonstrated the dataset’s effectiveness.

## Role & Impact
As the general lead, I navigated both technical and organizational challenges—solving engineering problems while driving efficient communication between companies.
The project was successfully completed within a short timeline thanks to cohesive teamwork and agile execution. This hands-on experience in large-scale AI data construction and multi-stakeholder coordination has become a cornerstone of my skillset for future endeavors.


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/HardwareSetup.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/dense.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Caption photos easily. On the left, a road goes through a tunnel. Middle, leaves artistically fall in a hipster photoshoot. Right, in another hipster photoshoot, a lumberjack grasps a handful of pine needles.
</div>



<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/AnnotationDiagram.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This image can also have a caption. It's like magic.
</div>



<!-- To give your project a background in the portfolio page, just add the img tag to the front matter like so:

    ---
    layout: page
    title: project
    description: a project with a background image
    img: /assets/img/12.jpg
    ---


You can also put regular text between your rows of images, even citations {% cite einstein1950meaning %}.
Say you wanted to write a bit about your project before you posted the rest of the images.
You describe how you toiled, sweated, _bled_ for your project, and then... you reveal its glory in the next row of images.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    You can also have artistically styled 2/3 + 1/3 images, like these.
</div>

The code is simple.
Just wrap your images with `<div class="col-sm">` and place them inside `<div class="row">` (read more about the <a href="https://getbootstrap.com/docs/4.4/layout/grid/">Bootstrap Grid</a> system).
To make images responsive, add `img-fluid` class to each; for rounded corners and shadows use `rounded` and `z-depth-1` classes.
Here's the code for the last row of images above:

{% raw %}

```html
<div class="row justify-content-sm-center">
  <div class="col-sm-8 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm-4 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
```

{% endraw %} -->
