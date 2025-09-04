---
layout: page
title: CMU Studio Project
description: Speech Emotion-Based Smart Lighting Control System
img: assets/img/need_project.png
redirect: https://github.com/GoTartans/need3
importance: 3
category: work
---

This project implements a distributed system that controls smart lighting and music playback based on emotional analysis of speech input. The system detects seven different emotions and responds with corresponding light colors and music selections. The system consists of three main components running on different devices (two Raspberry Pi and GCP instance) and uses Apache Kafka as the message broker for communication between components.

# System Architecture

The system is composed of three main components distributed across different devices:

## 1. Speech Input Node (Pi5)
- Implements `mic_to_kafka.py`
- Uses the speech_recognition to capture audio input from microphone
- Produces audio data to Kafka topic 'wav'

## 2. Processing Node (GCP Instance)
- Hosts Kafka cluster with Zookeeper and Broker
- Manages two topics: 'wav' and 'senti'
- Runs `wav_to_senti.py` which:
  - Consumes audio from 'wav' topic
  - Processes audio through ASR, Denoising, and Sentiment Analysis models
  - Produces sentiment results to 'senti' topic

## 3. Output Node (Pi6)
- Implements `kafka_to_bulb.py` 
- Uses the kasa library for smart bulb control
- Consumes sentiment data from 'senti' topic
- Creates immersive emotional experience through:
  - Smart lighting that responds to 7 different emotional states
  - Automated music selection and playback based on detected emotions
  - Synchronized audio-visual feedback system

<div class="row">
    <div class="col-sm-12 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/need3-architecture.jpg" title="System Architecture" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    High-level system architecture showing the three main components and their interactions through Kafka
</div>


