---
layout: page
title: Animaker Project Portfolio
description: 
img: assets/img/animaker-logo.png
importance: 2
category: work (proprietary)
---

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vRZPtOS8dfX_KjMea41Gb1cjJiHMvFrSpXxsX67IMwJc6VLoYhvn_kFbCwThLUN-Trw99BHq5JaOkTC/pubembed?start=true&loop=true&delayms=3000" frameborder="0" width="960" height="569" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>


## A. Talking-Head Video (AI Lip Sync of Animated Characters, Expressions, and Actions)

**Link:** [https://www.steve.ai/](https://www.steve.ai/)  
**Role:** Research Engineer at Animaker

### Project Inception

The existing lip sync feature for animated characters lacked realism and dynamic adaptability to voiceovers, making them less human-like.

### Challenges Faced

1. Identifying the right model to generate realistic lip movements that could be transformed into animated characters.
2. Model optimization and performance – improving inference speed, throughput/latency, and GPU consumption.

### Roles and Responsibilities

#### 1. PoC (Proof of Concept) Phase

- Conducted research and literature review on lip sync techniques.
- Identified and analyzed relevant research papers for implementation.
- Evaluated implementation results and guided further improvements.

#### 2. Production Deployment Phase

- Model Optimization – enhanced efficiency for deployment.
- Model Inference – ensured accurate and efficient execution.
- Latency & Throughput Optimization – improved performance for real-time processing.
- Scalability on AWS GPU – optimized the model for large-scale deployment.
- Containerization – created Docker images and managed containerization.
- API Development – developed APIs and integrated them with the backend.
- Deployment & Scalability – ensured system-wide scalability and efficient resource utilization.

### Technologies Used

- **GPU Hardware:** AWS GPU instances
- **Model Optimization:** **Knowledge Distillation (Teacher-Student Training)**
- **Containerization:** Docker

### Project Impact

1. Achieved realistic lip sync for animated characters in sync with voiceovers.
2. Enabled adoption across business verticals – L&D, marketing, and content creation, supporting Talking-Head videos and conversational videos.
3. Model Optimization **(Knowledge Distillation)** led to ~60% improvement in inference speed, enabling real-time processing.
4. Reduced model size to 1.1GB on GPU RAM, increasing model workers and enabling parallel processing.
5. Significant AWS GPU cost savings through optimized resource utilization.
6. High adoption rate – with a 15M+ daily user base, an average of ~250 projects of this category are downloaded daily.
7. Scalable and future-proof – the model can be adapted for any existing or future animated character designed at Animaker.

-------------------------------------------------

## B. Text to GenAI Video

**Link:** [https://www.steve.ai/](https://www.steve.ai/)  
**Role:** Research Engineer at Animaker

### Challenges Faced

1. Deployment on AWS GPU instances – optimizing for faster inference and higher throughput.
2. Load balancing and scalability – ensuring the model scales efficiently with increasing demand.

### Solutions Implemented

1. Utilized Segmind/SSD-1B model – a 50% smaller distilled version of SDXL, achieving a 60% speedup while maintaining high-quality text-to-image generation.
2. Integrated Tiny AutoEncoder for Stable Diffusion – reduced computational overhead while preserving output quality.
3. Optimized model inference using HuggingFace Diffusion Pipeline – improved efficiency and streamlined processing.

### Technologies Used

- **Stable Diffusion Text-to-Image Model:** SDXL1.0
- **Segmind/SSD-1B Model:** optimized, distilled version of SDXL
- **Tiny AutoEncoder for Stable Diffusion**
- **HuggingFace Diffusion Pipeline** with optimization steps
- **GPU Hardware:** AWS GPU instances
- **Containerization:** Docker

### Project Impact

1. Successfully launched in Steve.ai (Steve 2.0) on Product Hunt as a key AI-powered feature.
2. Second highest category in terms of projects created and exported since launch.
3. With a 15M+ daily user base, an average of ~1,500 projects of this category are generated daily.
4. Model optimizations and use of distilled/tiny models led to:
    - Reduced AWS costs
    - Faster inference and higher throughput
    - Scalable solutions to support increasing load
