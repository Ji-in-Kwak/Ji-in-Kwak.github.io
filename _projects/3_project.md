---
layout: page
title: CMU Studio Project
description: Speech Emotion-Based Smart Lighting Control System
img: assets/img/need_project.png
importance: 3
category: work
---

## Project Overview

**Role:** Sentiment analysis developement and Kafka system implementation

**Period:** 2022.09 - 2023.02

**Location:** Carnegie Mellon University


This project implements a distributed system that controls smart lighting and music playback based on emotional analysis of speech input. The system detects seven different emotions and responds with corresponding light bulb colors and music recommendations. The system consists of three main components running on different devices and uses Apache Kafka as the message broker for communication between components.

### Project Github Repository
**Repository:** [GitHub - NEED Project](https://github.com/GoTartans/need3)



## System Architecture

The system is composed of three main modules, each running on separate devices and communicating via Apache Kafka:

- **Speech Input:** Captures live audio from the user through a microphone using Automatic Speech Recognition (ASR) and Speech to Text (STT), providing processed audio data for emotion analysis.
- **Emotion Recognition:** Processes the captured speech to identify one of seven emotional states using semantic analysis techniques.
- **Smart Lighting & Music Control:** Adjusts lighting colors and music playback in real time, creating an environment that matches the detected emotion.

Two Raspberry Pi devices and a Google Cloud Platform (GCP) instance collaborate to enable distributed processing and seamless control. This architecture allows for scalable, responsive smart environment management based on user emotions.

<div class="row">
    <div class="col-sm-12 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/need_project.png" title="System Architecture" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    System architecture showing the main components and their interactions through Kafka
</div>


