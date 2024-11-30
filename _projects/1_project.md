---
layout: page
title: Beam Profiler
description: Low Cost, SBC, Data collection & Analysis
img: assets/img/beamprofiler_main_image.jpg
importance: 1
category: work
related_publications: true
---

Below, you'll find an in-depth look at its core features and capabilities, with images to help illustrate its power and versatility.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/1.jpg" title="Hardware Integration" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/3.jpg" title="Data Visualization" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="User Interface" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The images show: On the left, TEC control; in the middle, camera integration; and on the right, data visualization and real-time image statistics.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="Image Processing" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This image illustrates a live heatmap, visually representing intensity differences for easy analysis.
</div>

The Laser Beam Profiler is designed to provide a cost-effective yet highly efficient solution for capturing and analyzing laser beam properties. With its flexible software architecture, it delivers a powerful set of features:

- **Hardware Control**:
  - *Camera Integration*: The profiler seamlessly connects to a variety of cameras, using open source and proprietary APIs, with adjustable settings for all camera features to ensure optimal image capture.
  - *TEC Integration*: The profiler can control multiple TEC (Thermoelectric Cooler) devices to analyze temperature-related characteristics of the laser.
- **Image Acquisition and Processing**:
  - *Image Processing*: Captures high-quality raw images using both monochrome and color cameras. It applies non-destructive transformations and sophisticated heatmaps to enhance visual analysis while preserving the original data integrity. Furthermore, it generates comprehensive statistics, offering insights that make image analysis more effective and precise.
  - *Live Processing*: The system supports real-time image processing, allowing for instant visual analysis with adjustable thresholds and adaptable color mapping to easily distinguish differences across various regions. Additionally, users can define regions of interest (ROI) for focused analysis, enabling targeted insights into specific areas while maintaining a smooth and intuitive user experience.
  
<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/6.jpg" title="Live Processing Display" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/11.jpg" title="ROI Selection" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The left image showcases different real-time image adjustments, while the right image focuses on camera configuration settings.
</div>

- **Data Visualization**:
  - *Image Display*: Uses PyQtGraph for real-time image visualization, featuring custom colormaps for greater clarity.
  - *Statistical Analysis*: Provides a full statistical breakdown of captured images, including detailed region-specific information (ROI analysis).

- **User Interface (GUI)**:
  - *Interactive Controls*: Easily control settings such as streaming, capturing images, changing laser housing temperature, toggling dark mode, and adjusting processing thresholds.
  - *Tabbed Interface*: Features are grouped into intuitive tabs, making navigation simple and efficient.
  - *Status Updates*: Displays the current camera settings and status information in real time.

- **Data Saving and Export**:
  - *Data Saving*: All captured data, including images, ROI data, program settings, and relevant statistics, can be saved in a timestamped directory for future reference.
  - *Notes and Documentation*: Users can add notes to their sessions, improving traceability and documentation.
  - *Configurations*: Allows for saving and loading of any number of configurations.

- **Threading and Performance**:
  - *Multithreading*: To maintain the UI's responsiveness, separate threads are used for camera control and image processing.
  - *Thread Safety*: Ensures safe access to shared resources, which is crucial for avoiding issues in concurrent operations.

The Laser Beam Profiler is a sophisticated yet user-friendly tool, designed to make beam profiling accessible without compromising on the quality of data or the efficiency of the workflow. 