# ROS2 Autonomous Robot Stack

## Overview

ROS2 Autonomous Robot Stack is a modular robotics software framework designed to provide scalable perception, communication, localization, and sensor integration capabilities for autonomous robotic systems.

The project follows a distributed ROS2 architecture where independent nodes communicate through standardized interfaces, enabling flexible development and future expansion.

---

# Objectives

- Build a modular robotics software stack.
- Enable ESP32 integration with ROS2.
- Support real-time sensor communication.
- Process live camera streams.
- Perform visual localization using AprilTags.
- Maintain scalable package-based architecture.

---

# Key Features

- ROS2 package-based architecture
- Custom ROS2 message definitions
- ESP32 UDP communication bridge
- RTSP camera streaming
- AprilTag detection pipeline
- Tag-based localization
- Structured map interfaces
- Distributed node communication
- Modular software design

---

# System Architecture

ESP32 Devices

↓

UDP Bridge

↓

ROS2 Communication Layer

↓

Perception Nodes

↓

Localization Nodes

↓

Mapping & Navigation

↓

Robot Applications

---

# Major Components

## robot_msgs

Provides custom ROS2 interfaces for:

- ToF ray data
- Voxel maps
- Tag detections
- Structured maps

---

## esp32_bridge

Receives UDP packets from ESP32 hardware and converts them into ROS2-compatible messages.

---

## phone_rtsp_bridge

Streams RTSP video into ROS2 image topics for downstream computer vision processing.

---

## apriltag_detector

Detects AprilTags from incoming camera frames and estimates tag poses.

---

## tag_localizer

Uses AprilTag detections and known map information to estimate robot position within the environment.

---

# Technology Stack

## Languages

- Python

## Robotics

- ROS2

## Embedded Systems

- ESP32

## Computer Vision

- OpenCV
- AprilTag

## Networking

- UDP
- RTSP

## Communication

- ROS2 Topics
- Custom Message Interfaces

---

# Design Principles

- Modularity
- Scalability
- Separation of concerns
- Extensibility
- Reusability
- Distributed architecture

---

# Repository Notice

This repository documents the project architecture and engineering concepts.

Some implementation components may remain private during active development.

For collaboration opportunities or technical discussions:

Email:
nandnarnandanr1234@gmail.com
