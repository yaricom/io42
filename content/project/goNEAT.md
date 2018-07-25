+++
title = "Go NEAT"
date = 2018-07-25T17:55:31+03:00
draft = false

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = ["machine-learning", "artificial-neural-networks", "reinforcement-learning", "unsupervised-learning", "neuroevolution"]

# Project summary to display on homepage.
summary = "The GOLang implementation of NeuroEvolution of Augmented Topologies (NEAT) method to grow and teach Artificial Neural Networks without back propagation"

# Optional image to display on homepage.
image_preview = "projects/3/double_pole-balancing.png"

# Optional external URL for project (replaces project detail page).
external_link = "https://github.com/yaricom/goNEAT"

# Does the project detail page use math formatting?
math = false

# Does the project detail page use source code highlighting?
highlight = true

# Featured image
# Place your image in the `static/img/` folder and reference its filename below, e.g. `image = "example.jpg"`.
[header]
image = "projects/3/double_pole-balancing.png"
caption = "The classical inverted pendulum experiment"

+++

This project provides implementation of [NeuroEvolution of Augmenting Topologies](http://www.cs.ucf.edu/%7Ekstanley/neat.html) (NEAT) method written in Go language.

The Neuroevolution (NE) is an artificial evolution of Neural Networks (NN) using genetic algorithms in order to find optimal NN parameters and topology. Neuroevolution of NN may assume search for optimal weights of connections between NN nodes as well as search for optimal topology of resulting NN. The NEAT method implemented in this work do search for both: optimal connections weights and topology for given task (number of NN nodes per layer and their interconnections).
