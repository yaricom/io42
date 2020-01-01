---
title: SSVEP Brain Hash Function
summary: Our goal is to create Brain Hash Algorithm able to produce robust distinction between EEG signals of different humans under electro-physiological visual feedback based on steady-state visually evoked potential (SSVEP). It can be applied at variety of tasks from user authentication at online web services to user identification for physical access control systems.
tags:
- brain-computer-interface
date: "2017-08-03T18:25:34+03:00"

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  caption: The electro-physiological visual feedback screen
  focal_point: Smart

url_pdf: "https://arxiv.org/pdf/1708.01167"
url_preprint: "https://arxiv.org/abs/1708.01167"
url_code: "https://github.com/yaricom/brainhash"
url_source: "https://www.researchgate.net/project/Brain-Hash-Function"

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""
---

This project had a goal to research if steady-state visually evoked potential (SSVEP) can be used to create Brain Hash Function Algorithm able to distinguish between unique footprints of each individual brain under specific visual stimulation with electro-physiological visual feedback based on consumer-grade EEG monitoring device.

The project scope consist of two major parts:

1. Implementation of electro-physiological visual feedback system based on consumer-grade EEG monitoring device. It should perform monitoring of EEG signals in real time and perform preprocessing of received raw EEG signal.

2. Implementation of advance machine-learning pipeline to automatically extract important features from data stream and perform classification of encoded features. It should perform confident classification of the collected EEG data in order to (a) reliably distinguish signal from noise and (b) reliably distinguish between EEG records collected from different human participants.

The project timeline and results can be found at: [ResearchGate](https://www.researchgate.net/project/Brain-Hash-Function)
