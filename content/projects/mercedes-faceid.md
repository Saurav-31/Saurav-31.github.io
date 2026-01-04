---
title: Mercedes Pay Biometric FaceID
summary: End-to-end design and deployment of the Face Identification system for Mercedes Pay, enabling secure in-car payments.
tags:
  - Deep Learning
  - Computer Vision
  - Biometrics
  - Edge AI
date: "2025-06-01"

# Optional external link for the button (e.g. a press release or video)
# external_link: ""

image:
  caption: "Production Deployment in MBUX"
  focal_point: Smart

links:
url_code: ""
url_pdf: ""
url_slides: ""
url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""
---

**Role:** Senior Technical Lead  
**Status:** Production (Deployed in Mercedes-Benz Vehicles)

## 🚀 The Objective
Enable secure, seamless in-car payments using facial biometrics. The system needed to function as a high-security authentication layer for the **Mercedes Pay** platform, integrated directly into the MBUX head unit.

## ⚡ Technical Challenges
Automotive biometrics present unique challenges compared to mobile phones:
* **Extreme Lighting:** The model must handle direct sunlight, tunnel darkness, and rapid transitions (auto-exposure adaptation).
* **Compute Constraints:** Must run on embedded automotive hardware with strict latency and memory budgets.
* **Safety & Security:** Required defense against sophisticated 2D and 3D presentation attacks (Face Anti-Spoofing).

## 🛠️ System Architecture & Contribution
I owned the **end-to-end system design**, from algorithm conception to embedded deployment.

1.  **Face Identification Pipeline:**
    * Designed a robust identification model using **ArcFace-based objectives**.
    * Optimized for low-compute devices using mobile-friendly architectures (e.g., MobileFaceNet variants).

2.  **Anti-Spoofing (Liveness Detection):**
    * Developed a multi-modal anti-spoofing module using **RGB, IR, and Depth streams**.
    * Implemented contrastive learning strategies to handle "hard" spoof examples.
    * Designed multi-crop strategies to defend against print and video replay attacks.

3.  **Deployment & Robustness:**
    * Collaborated with hardware teams to tune camera ISP (Image Signal Processing) settings for optimal biometric performance.
    * Established data collection and annotation pipelines to cover diverse demographics and lighting conditions.

## 🏆 Impact
* **Productionized:** Successfully launched the feature for the Mercedes Pay ecosystem.
* **Security:** Achieved high TPR (True Positive Rate) at strict FAR (False Accept Rate) requirements compliant with payment security standards.
