---
layout: page
title: Beam Profiler
description: Low Cost, Multiplatform, SBC, Data Collection & Analysis
img: assets/img/beamprofiler_main_image.jpg
importance: 1
category: work
related_publications: true
---

A versatile, high-performance beam profiler built for flexibility and efficiency. Below, you'll find an in-depth look at its core features and capabilities, complete with images to showcase its potential in action.

<div class="row" style="display: flex; align-items: flex-start;">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/tec_control.png" title="TEC Integration" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/3D_heatmap.png" title="3D Heatmap" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The images showcase: TEC control on the left, and live mesh heatmap on the right.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/live_heatmap.png" title="Image Processing" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    A live heatmap representation, highlighting intensity variations for deeper analysis.
</div>

The Laser Beam Profiler is an innovative, multiplatform solution that works seamlessly on Linux and Windows systems, with support for both ARM64 and x86 architectures. Designed to adapt to diverse use cases, it blends cutting-edge features with intuitive usability:

- **Hardware Control**:
  - *Camera Integration*: Effortlessly connects to various cameras using open-source and proprietary APIs. Offers full control over camera settings to achieve optimal image capture for any scenario.
  - *TEC Integration*: Includes control for multiple Thermoelectric Cooler (TEC) devices, enabling precise thermal profiling and analysis of laser temperature characteristics.
  
- **Image Acquisition and Processing**:
  - *High-Fidelity Image Processing*: Captures pristine raw images using both monochrome and color cameras. Applies advanced, non-destructive transformations, alongside vibrant heatmaps, to aid in interpretation while safeguarding data integrity. Comprehensive statistics enhance analysis effectiveness.
  - *Real-Time Processing*: Enables on-the-fly adjustments with responsive live image processing. Features include color mapping, customizable regions of interest (ROI), and more, delivering actionable insights instantaneously.

<div class="row justify-content-sm-center" style="display: flex; align-items: flex-start;">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/camera_integration.png" title="Camera Integration" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/config.png" title="ROI Selection" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left: Showcasing camera integration. Right: Highlighting configuration options.
</div>

- **Data Visualization**:
  - *Enhanced Image Display*: Leverages PyQtGraph for real-time visualization, offering customizable colormaps for improved clarity.
  - *Comprehensive Analytics*: Includes robust statistical tools for analyzing entire images or specific regions, ensuring informed decision-making.

- **User-Friendly Interface**:
  - *Interactive Controls*: Fine-tune settings such as streaming, image capture, laser temperature adjustments, dark mode toggling, and more, all with a few clicks.
  - *Organized Navigation*: Features a tabbed interface to neatly group functions, ensuring a smooth workflow.
  - *Real-Time Feedback*: Live status updates and logging keep users informed at all times.

- **Data Saving and Export**:
  - *Intelligent Data Management*: Captures and stores images, ROIs, and related metadata in timestamped directories for easy retrieval.
  - *Cloud Integration*: Experiments can be automatically uploaded to a centralized cloud database, complete with tags and advanced search capabilities, so users may revisit past data effortlessly.
  - *Detailed Experimental Notes and Tags*: Supports the addition of experimental notes and Tags, enhancing traceability and documentation.
  - *Configuration Flexibility*: Save and load customized configurations to quickly adapt to different experiments and hardware configurations.

- **Performance Optimization**:
  - *Multithreading Mastery*: Ensures a responsive user experience by separating tasks like camera control and image processing into dedicated threads.
  - *Rock-Solid Thread Safety*: Guarantees smooth, error-free operation even during concurrent tasks.

The Beam Profiler goes beyond the ordinary, combining high functionality with effortless usability and low-cost. Its advanced architecture delivers compatibility across platforms, superior performance, and a user-focused experience—making it the ultimate tool for beam profiling.
