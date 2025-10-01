---
layout: page
title: Fly-Scan System
description: An advanced, high-speed data acquisition system for capturing detailed optical component characteristics using continuous motion.
img: 
importance: 2
category: work
related_publications: false
---

The Fly-Scan System is an advanced data acquisition platform designed for high-resolution scientific and industrial measurements. It acquires data "on the fly" by synchronizing a high-precision motion controller with a sensitive data acquisition module, enabling dramatically faster and more detailed measurements compared to traditional stop-and-measure techniques.

The system is built on three core, perfectly synchronized building blocks: a motion controller, a data acquisition unit, and a hardware-based synchronization conductor.

### System Architecture

**1. Motion Control (The Mover)**

The physical heart of the system is a **Zaber RSW-E Rotation Stage**, which rotates optical components with high precision.
- **Functionality**: A stepper motor turns the platform at a constant, controlled velocity between a defined start and end angle.
- **Key Feature**: An integrated high-resolution motor encoder tracks the motor's rotation with extreme accuracy. This encoder is crucial for generating the trigger signal that drives the entire system, ensuring each data point is tied to a precise angular position.

**2. Data Acquisition (The Measurer)**

This sensory part of the system converts light into a digital signal for analysis.
- **Photodetector**: A **Thorlabs PDA100A2 Photodetector** acts as the "eye," converting incident light from a laser into a proportional analog voltage. An internal amplifier ensures the signal is strong enough for accurate measurement.
- **DAQ**: A **National Instruments USB-6211 DAQ** bridges the analog detector and the digital computer. Its Analog-to-Digital Converter (ADC) measures the voltage from the photodiode and sends a stream of digital data to the host computer for storage and real-time plotting.

**3. Synchronization (The Conductor)**

The most critical part of the system is the hardware triggering mechanism, which ensures perfect timing between movement and measurement. This architecture removes the uncertainties of software-based timing.

The process for acquiring each data point is as follows:
1.  **Motion**: The Zaber stage rotates by a pre-defined micro-step (e.g., 0.00025 degrees).
2.  **Trigger Generation**: The Zaber's encoder detects this movement and instantly toggles the voltage on a digital output pin, creating an electrical trigger pulse.
3.  **Synchronization Signal**: The pulse is sent via a direct hardware connection to a Programmable Function Interface (PFI) pin on the NI DAQ.
4.  **Hardware-Timed Acquisition**: The Python control software pre-configures the NI DAQ to operate in a hardware-timed mode. It waits in an armed state for the trigger pulse from the Zaber stage instead of using its own internal clock.
5.  **Measurement**: The instant the DAQ detects the trigger pulse, its ADC takes a single voltage measurement from the photodiode.
6.  **Repeat**: The DAQ immediately re-arms and waits for the next pulse. This cycle repeats thousands of times per second, creating a high-density data stream.

### Software and Backend

- **Control & Analysis**: The entire system is orchestrated by a **Python** application. This software is responsible for configuring the Zaber stage's motion profile, arming the NI DAQ's hardware trigger, and processing the incoming data stream in real-time.
- **Data Handling**: The stream of measurements is saved to the computer, often into structured file formats (like HDF5 or CSV) that pair each voltage reading with its corresponding angular position. This creates a clean, high-resolution dataset ready for analysis and visualization.
- **GUI**: A graphical user interface, likely built with a framework like PyQt or a web-based dashboard, allows the operator to configure scan parameters, monitor data acquisition live, and perform post-scan analysis.

This hardware-timed architecture guarantees that every data sample corresponds perfectly to a specific physical angle, enabling the creation of extremely accurate and high-resolution maps of an optical component's properties.
