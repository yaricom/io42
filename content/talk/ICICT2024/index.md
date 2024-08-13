---
title: ICICT 2024 paper presentation
event: 9th International Congress on Information and Communication Technology, London, United Kingdom
event_url: https://icict.co.uk/home.php

location: America Square Conference Centre, London, United Kingdom
address:
  street: 1 America Square, 17 Crosswall
  city: London
  region: City of London
  postcode: 'EC3N 2LB'
  country: United Kingdom

summary: I presented my research paper \"Design of cluster-computing architecture to improve training speed of the Neuroevolution algorithm\"
abstract: In this paper, we review the key features and major drawbacks of the Neuroevolution of Augmenting Topologies (NEAT) algorithm, such as slow training speed that limits its area of application. The main reason for the performance issues of the NEAT algorithm is the huge number of calculations required at the end of each epoch to estimate the fitness of each organism in the population. We propose a software system architecture that can be implemented to solve NEAT performance problems based on Ray cluster-computing framework. Finally, we demonstrate how fitness estimation computations can be distributed across stateless distributed workers deployed either on-premise or in the cloud using Ray framework.

# Talk start and end times.
#   End time can optionally be hidden by prefixing the line with `#`.
date: "2024-02-22T16:15:00-08:00"
date_end: "2024-02-22T16:30:00-08:00"
all_day: false

# Schedule page publish date (NOT talk date).
publishDate: "2024-02-22T00:00:00Z"

authors: 
- admin

tags:
- neuroevolution

# Is this a featured talk? (true/false)
featured: true

image:
  caption: ''
  focal_point: Right

# url_pdf: "files/icict2024/75.pdf"
url_slides: "files/icict2024/icict_2024_presentation.pdf"
url_poster: "files/icict2024/75_CC.pdf"
url_video: "https://youtu.be/1jhcr6DWQIw "
url_code: "https://github.com/yaricom/goNEAT"

# Markdown Slides (optional).
#   Associate this talk with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []

# Enable math on this page?
math: false
---
