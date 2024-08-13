---
title: "Simulation of the Autonomous Maze Navigation using the NEAT Algorithm"
authors:
- admin
date: 2023-12-01T15:28:14+02:00
doi: "10.15407/pp2023.04.076"

# Schedule page publish date (NOT publication's date).
publishDate: "2023-12-01T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["2"]

# Publication name and optional abbreviated publication name.
publication: "Simulation of the autonomous maze navigation using the NEAT algorithm. Problems in programming, 2023. Vol. 4, N 1. P. 76-89."
publication_short: "Simulation of the Autonomous Maze Navigation using the NEAT Algorithm"

abstract: The article deals with the problem of finding a solution for the navigational task of navigating a maze by an autonomous agent controlled by an artificial neural network (ANN). A solution to this problem was proposed by training the controlling ANN using the method of neuroevolution of augmenting topologies (NEAT). <br/>A description of the mathematical apparatus for determining the goal-oriented objective function to measure fitness of the decision-making agent, suitable for optimizing the training of ANN in the process of neuroevolution, was given. Based on the invented objective function, a software was developed to control the neuroevolutionary process using the Python programming language.<br/>A system for simulating the behavior of an autonomous robot that can navigate through a maze using input signals from various types of sensors has been created. The simulation system allows to imitate the behavior of a physical robot in a large number of experiments in a short time and with minimal expenses.<br/>The experiments performed using the created simulation system to find the optimal values of hyperparameters, which can be used for successful training of the controlling ANN by the method of neuroevolution, are presented.<br/>Additionally, the implemented new methods of visualizing the training process are described. These methods significantly simplify the search for optimal hyperparameters of the NEAT algorithm, due to the visual demonstration of the effect of changing one or another parameter on the training process.

# Summary. An optional shortened abstract.
summary: The article deals with the problem of finding a solution for the navigational task of navigating a maze by an autonomous agent controlled by an artificial neural network (ANN). A solution to this problem was proposed by training the controlling ANN using the method of neuroevolution of augmenting topologies (NEAT).

tags:
- neuroevolution
- unsupervised-learning
- reinforcement-learning
- cooperative-robotics
- evolutionary-computation
- novelty-search
- autonomous-robotics

categories:
- artificial-neural-networks
- neuroevolution

featured: false

url_pdf: "https://pp.isofts.kiev.ua/index.php/ojs1/article/view/595/644"
url_code: "https://github.com/yaricom/goNEAT_NS"

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: 'The medium maze results for NS agent'
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects:
- goNEAT_NS


# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---
