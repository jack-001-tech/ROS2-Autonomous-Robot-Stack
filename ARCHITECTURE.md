# ROS2 Autonomous Robot Stack Architecture

## Overview

The project follows a layered ROS2 architecture where hardware interfaces, communication bridges, perception modules, localization systems, and application logic operate as independent packages.

This separation enables reliable development and future scalability.

---

# High-Level Architecture

+-----------------------------+
|      Robot Applications     |
+-----------------------------+
              │
              ▼
+-----------------------------+
| Localization & Navigation   |
+-----------------------------+
              │
              ▼
+-----------------------------+
| Computer Vision Pipeline    |
+-----------------------------+
              │
              ▼
+-----------------------------+
| ROS2 Message Interfaces     |
+-----------------------------+
              │
              ▼
+-----------------------------+
| ESP32 / Camera Bridges      |
+-----------------------------+
              │
              ▼
+-----------------------------+
| Physical Sensors            |
+-----------------------------+

---

# Core Packages

## robot_msgs

Defines reusable ROS2 message types for:

- ToF rays
- Voxel grids
- AprilTag detections
- Structured maps

---

## esp32_bridge

Responsibilities:

- Receive UDP packets
- Validate packet structure
- Convert sensor data
- Publish ROS2 topics

---

## phone_rtsp_bridge

Responsibilities:

- Connect to RTSP stream
- Capture frames
- Convert to ROS2 Image messages

---

## apriltag_detector

Responsibilities:

- Process incoming images
- Detect AprilTags
- Estimate tag poses
- Publish detections

---

## tag_localizer

Responsibilities:

- Read tag detections
- Load known tag map
- Compute robot pose
- Publish localization results

---

# Design Goals

- Distributed communication
- Package modularity
- Easy maintenance
- High extensibility
- Hardware abstraction
- Future navigation support

---

# Source Code

The architecture described here represents the public design of the system.

Some implementation details may remain private during active development.
