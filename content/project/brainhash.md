+++
title = "SSVEP Brain Hash Function"
date = 2017-08-03T18:25:34+03:00
draft = false

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = ["brain-computer interface", "machine-learning", "deep-learning"]

# Project summary to display on homepage.
summary = "Our goal is to create Brain Hash Algorithm able to produce robust distinction between EEG signals of different humans under electro-physiological visual feedback based on steady-state visually evoked potential (SSVEP). It can be applied at variety of tasks from user authentication at online web services to user identification for physical access control systems."

# Optional image to display on homepage.
image_preview = "wisp_screen.png"

# Optional external URL for project (replaces project detail page).
external_link = ""

# Does the project detail page use math formatting?
math = false

# Does the project detail page use source code highlighting?
highlight = false

# Featured image
# Place your image in the `static/img/` folder and reference its filename below, e.g. `image = "example.jpg"`.
[header]
image = "wisp_screen.png"
caption = "The electro-physiological visual feedback screen"

+++

This project had a goal to research if steady-state visually evoked potential (SSVEP) can be used to create Brain Hash Function Algorithm able to distinguish between unique footprints of each individual brain under specific visual stimulation with electro-physiological visual feedback based on consumer-grade EEG monitoring device.

The project scope consist of two major parts:

1. Implementation of electro-physiological visual feedback system based on consumer-grade EEG monitoring device. It should perform monitoring of EEG signals in real time and perform preprocessing of received raw EEG signal.

2. Implementation of advance machine-learning pipeline to automatically extract important features from data stream and perform classification of encoded features. It should perform confident classification of the collected EEG data in order to (a) reliably distinguish signal from noise and (b) reliably distinguish between EEG records collected from different human participants.

The project timeline and results can be found at: [ResearchGate](https://www.researchgate.net/project/Brain-Hash-Function)
