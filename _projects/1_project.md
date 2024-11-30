---
layout: page
title: Beam Profiler
description: Low Cost, SBC, Data Collection & Analysis
img: assets/img/beamprofiler_main_image.jpg
importance: 1
category: work
related_publications: true
---

Introducing the **Laser Beam Profiler**—a comprehensive solution for capturing, analyzing, and visualizing laser beam profiles using low-cost hardware and efficient software integration.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/beamprofiler_setup.jpg" title="Beam Profiler Setup" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/beamprofiler_ir_image.jpg" title="Infrared Image Capture" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/beamprofiler_noir_image.jpg" title="No Infrared Image Capture" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    **Left**: The hardware setup integrating the camera with adjustable parameters. **Middle**: Captured Infrared (IR) image. **Right**: Captured No Infrared (NoIR) image for comparison.
</div>

### Project Main Features

#### Hardware Control

- **Camera Integration**: Connect to a camera with control over integration time, gain, and pixel format. This allows precise adjustments to capture high-quality images suitable for analysis.

#### Image Acquisition and Processing

- **IR and NoIR Image Capture**: Capture and compare Infrared (IR) and No Infrared (NoIR) images to analyze differences in laser beam profiles.
- **Image Processing**: Highlight differences between IR and NoIR images using thresholds and ratios, handling edge cases gracefully to ensure accurate results.
- **Live IR Processing**: Real-time processing of live IR images with adjustable thresholds and color mapping for immediate visualization.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/beamprofiler_live_processing.jpg" title="Real-time Image Processing" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Real-time processing of IR images with adjustable thresholds and color mapping.
</div>

#### Data Visualization

- **Image Display**: Uses PyQtGraph for real-time image display with custom colormaps, providing an interactive visualization experience.
- **Statistical Analysis**: Compute and display image statistics, including mean, median, standard deviation, and more, for both the entire image and regions of interest (ROI).
- **ROI Selection and Analysis**: ROI selection with dedicated statistics, enabling focused analysis on specific areas of the beam profile.

#### User Interface (GUI)

- **Interactive Controls**: Start/stop streaming, capture images, toggle dark mode, set parameters, and adjust thresholds seamlessly through a user-friendly interface.
- **Tabbed Interface**: Organize functionalities into tabs for easy navigation and enhanced user experience.
- **Status Updates**: Display camera information and current settings, keeping users informed about the system's state.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/beamprofiler_ui.jpg" title="User Interface" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The intuitive user interface with interactive controls and real-time updates.
</div>

#### Data Saving and Export

- **Data Saving**: Save captured frames, images, ROI data, and statistics in a timestamped directory for easy retrieval and analysis.
- **Notes and Documentation**: Allow users to add notes to sessions, aiding in documentation and future reference.

#### Threading and Performance

- **Multithreading**: Use separate threads for camera control and image processing to maintain UI responsiveness and ensure smooth operation.
- **Thread Safety**: Ensure safe access to shared resources, preventing data corruption and crashes.

### Technical Highlights

The Laser Beam Profiler is built using Python and leverages the PyQt framework for the graphical user interface. It integrates advanced image processing libraries to perform real-time analysis and visualization.

- **PyQtGraph Integration**: For high-performance visualization, the application uses PyQtGraph, allowing for smooth real-time image display and interaction.
- **Thread Management**: Implements Python's threading capabilities to separate the camera capture process from image processing and UI updates, ensuring efficient use of system resources.
- **Custom Colormaps**: Develop custom colormaps to enhance the visualization of laser beam profiles, aiding in better interpretation of data.

### Applications

This project is ideal for:

- **Research Laboratories**: Where precise measurement and analysis of laser beams are required.
- **Educational Institutions**: As a teaching tool for optics and photonics courses.
- **Industrial Settings**: For quality control and monitoring of laser systems.

### Future Work

- **Extended Hardware Support**: Incorporate support for additional camera models and hardware components.
- **Advanced Analysis Tools**: Implement features such as beam diameter calculation, divergence measurement, and Gaussian fitting.
- **Remote Access**: Develop capabilities for remote operation and monitoring over a network.

### Conclusion

The Laser Beam Profiler project provides a comprehensive, low-cost solution for laser beam analysis, combining powerful software features with accessible hardware integration.

---
