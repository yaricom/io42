---
title: UkrPROG 2024 paper presentation
event: 14th International Scientific and Practical Programming Conference, UkrPROG 2024, Kyiv, Ukraine
event_url: https://iss.nas.gov.ua/event/ukrprog-2024-15

location: 40, Academician Glushkov avenue, Kyiv, Ukraine
address:
  street: 40, Academician Glushkov avenue
  city: Kyiv
  postcode: "03187"
  country: Ukraine

summary: I presented my research paper \"Application of the coevolution strategy to solve the problem of autonomous navigation through the maze\"
abstract: "This study explores the use of coevolutionary methods to address the challenge of navigating through complex mazes using autonomous agents controlled by artificial neural networks (ANNs). It underscores a critical impediment to algo-rithmic optimization: the close interdependence between the task's goal and the objective function used for optimal so-lution discovery. The task's goal is clear—identify the most efficient route through the maze. However, the objective function's formulation is more complex. In complex maze layouts, numerous deceptive areas may appear proximate to the exit but culminate in dead ends. Consequently, an elementary objective function that merely gauges the proximity to the exit can encounter numerous local optima within this deceptive search space, hindering the search for optimal so-lution. As maze complexity increases, such an objective function inevitably becomes ensnared in a local optimum, ren-dering the navigation issue unsolvable.</br>
To counteract this, the study proposes a coevolution strategy involving a population of decision-making agents and a population of objective function candidates. This approach diverges from prior research by incorporating the NEAT algorithm to steer the coevolution of both populations. Additionally, the Novelty Search (NS) method was sug-gested to optimize the search within the potential solution space, favoring the most novel solutions.</br>
The paper details the mathematical framework for crafting the objective function template, which integrates the novelty value of the discovered solution and its distance from the maze's exit. This framework serves as the foundation for defining the genomes of the organisms — candidates for the objective functions.</br>
For comparison with preceding works, an experiment was conducted to evaluate the efficacy of the proposed coevolution method in resolving the problem of navigation within a complex maze environment.
"

# Talk start and end times.
#   End time can optionally be hidden by prefixing the line with `#`.
date: "2024-05-14T10:15:00-03:00"
date_end: "2024-05-14T10:30:00-03:00"
all_day: false

# Schedule page publish date (NOT talk date).
publishDate: "2024-05-15T00:00:00Z"

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
url_slides: "files/ukrpog2024/UkrPROG2024-slides.pdf"
# url_poster: "files/icict2024/75_CC.pdf"
# url_video: "https://youtu.be/1jhcr6DWQIw "
url_code: "https://github.com/yaricom/goNEAT_NS"

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
projects: 
  - goNEAT_NS

# Enable math on this page?
math: false
---
