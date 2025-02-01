---
layout: page
title: Beam Profiler
description: Low Cost, Multiplatform, SBC, Data Collection & Analysis
img: assets/img/live_heatmap.png
importance: 1
category: work
related_publications: false
---

Introducing a versatile and high-performance Beam Profiler designed for flexibility and efficiency. Below is an in-depth look at its core features and capabilities, complete with images that showcase its potential in action.

<div class="row justify-content-sm-center" style="display: flex; align-items: flex-start;">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/tec_control.png" title="TEC Integration" style="height: 300px; width: auto;" class="rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/3D_heatmap.png" title="3D Heatmap" style="height: 300px; width: auto;" class="rounded z-depth-1" %}
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

The Laser Beam Profiler is an innovative, multiplatform solution that operates seamlessly on Linux and Windows systems, supporting both ARM64 and x86 architectures. Designed to adapt to diverse use cases, it blends cutting-edge features with intuitive usability. It offers hardware control with camera integration, effortlessly connecting to various cameras using open-source and proprietary APIs, and provides full control over camera settings to achieve optimal image capture in any scenario. Additionally, it includes control for multiple Thermoelectric Cooler (TEC) devices, enabling precise thermal profiling and analysis of laser temperature characteristics.

In terms of image acquisition and processing, the profiler captures pristine raw images using both monochrome and color cameras. It applies advanced, non-destructive transformations alongside vibrant heatmaps to aid in interpretation while safeguarding data integrity. Comprehensive statistics enhance analysis effectiveness. Real-time processing allows on-the-fly adjustments with responsive live image processing, featuring color mapping, customizable regions of interest (ROI), and more, delivering actionable insights instantaneously.

<div class="row justify-content-sm-center" style="display: flex; align-items: flex-start;">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/camera_integration.png" title="Camera Integration" style="height: 300px; width: auto;" class="rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/config.png" title="ROI Selection" style="height: 300px; width: auto;" class="rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left: Showcasing camera integration. Right: Highlighting configuration options.
</div>

For data visualization, it leverages PyQtGraph for real-time visualization, offering customizable colormaps for improved clarity. It includes robust statistical tools for analyzing entire images or specific regions, ensuring informed decision-making.

The user-friendly interface features interactive controls that allow fine-tuning of settings such as streaming, image capture, laser temperature adjustments, dark mode toggling, and more, all with a few clicks. Organized navigation with a tabbed interface neatly groups functions, ensuring a smooth workflow. Live status updates and logging keep users informed at all times.

For data saving and export, the profiler offers intelligent data management by capturing and storing images, ROIs, and related metadata in timestamped directories for easy retrieval. Experiments can be automatically uploaded to a centralized cloud database, complete with tags and advanced search capabilities, so users may revisit past data effortlessly. It supports the addition of experimental notes and tags, enhancing traceability and documentation. Configuration flexibility allows saving and loading customized configurations to quickly adapt to different experiments and hardware setups.

Performance optimization is achieved through multithreading, ensuring a responsive user experience by separating tasks like camera control and image processing into dedicated threads. Rock-solid thread safety guarantees smooth, error-free operation even during concurrent tasks.

The Beam Profiler combines high functionality with effortless usability and low cost. Its advanced architecture delivers compatibility across platforms, superior performance, and a user-focused experience, making it an essential tool for beam profiling.
