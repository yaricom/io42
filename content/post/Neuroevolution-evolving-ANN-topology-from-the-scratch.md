+++
title = "Neuroevolution - Evolving Artificial Neural Networks Topology From the Scratch"
date = 2018-07-25T13:55:17+03:00
draft = false

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["Iaroslav Omelianenko"]

# Tags and categories
# For example, use `tags = []` for no tags, or the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = ["neuroevolution", "artificial-neural-networks", "machine-learning", "reinforcement-learning"]
categories = ["machine-learning", "reinforcement-learning"]

# Featured image
# Place your image in the `static/img/` folder and reference its filename below, e.g. `image = "example.jpg"`.
# Use `caption` to display an image caption.
#   Markdown linking is allowed, e.g. `caption = "[Image credit](http://example.org)"`.
# Set `preview` to `false` to disable the thumbnail in listings.
[header]
image = "posts/1/neuroevolution-evolving-ANNs-feature.jpg"
caption = "The ANN graph representation"
preview = true


+++

The most popular method of [Artificial Neural Networks](https://en.wikipedia.org/wiki/Artificial_neural_network) (ANN) training -at the time of this essay writing - is to use some form of Gradient Descent (GD) combined with error back propagation w.r.t. objective function defining our learning goal. This methodology was invented about 30 years ago by [Geoffrey Hinton](https://en.wikipedia.org/wiki/Geoffrey_Hinton) and become a foundation of all modern research activities in the [Deep Machine Learning](https://en.wikipedia.org/wiki/Deep_learning) (ML) and the [Artificial Intelligence](https://en.wikipedia.org/wiki/Artificial_intelligence) (AI). But despite the fact that it gives immense power in areas of pattern recognition ([feature or representation learning](https://en.wikipedia.org/wiki/Feature_learning)) it has considerable weakness:

* the network topology must be fully hand-engineered before training starts and only connection weights encapsulate learned knowledge, the network topology remain the same
* as a result it may introduce oversatturated neural units which don not take part in the training/inference process but simply consuming comptunig resources
* special methodic must be applied to avoid sticking into local optima such as L1/L2-norm, dropout regularizations, etc
* exploding or diminishing learning gradient issues during back/forward propagation
* implemented solutions can generalize only in the narrow scope learned from provided training samples

***

To overcome some of the drawbacks of GD-based training it was proposed to use alternative methods to train/evolve neural networks with group of algorithms inspired by natural selection and genetic evolution. It was given name [Genetic Algorithms](https://en.wikipedia.org/wiki/Genetic_algorithm) (GA) to address the source of inspiration and due to its attempt to mimic natural process of genetic mutations, crossover and selection, while trying to solve objective function optimization problem. There are many types of such algorithms was invented during last years.

{{< figure src="img/posts/1/crossover_mutation.png" title="The example of Crossover and Mutation in GA ([image source](http://www.abrandao.com/2015/01/simple-php-genetic-algorithm/))" >}}

But my main interest in this essay is to present a kind of GA which can be applied to evolve ANNs from the most simple forms to the complex ones in order to find objective function optimization solution not only by changing weights of connections between neural units, but by evolving the topology of network graph itself.

***

I would like to consider [Neuroevolution of Augmented Topologies](http://www.cs.ucf.edu/~kstanley/neat.html) (NEAT) algorithm invented by [Kenneth O. Stanley](http://www.cs.ucf.edu/~kstanley/) as part of his [Phd Thesis](http://nn.cs.utexas.edu/keyword?stanley:phd04) in years 2002-2004. With this method of ANN evolution, search for complex solutions made feasible through graduate complexification of network topology. By starting with minimal ANN the NEAT is more likely to find efficient and robust solution, avoiding sticking at the local optima as in cases with other GA methods which starts with elaborated network graphs and mutate them during training.

With NEAT method, the training starts with very simple ANNs topology comprising of only input, output and bias neural units - no hidden units introduced at the beginning. Thus it ensures, that the system searches for the solution in the lowest-dimensional weight space possible over the course of all generations. The goal is not to minimize only final product, but all intermediate networks along the way as well. This idea is they key to gaining an advantage from the evolution of topology: it allows us to minimize the search space, resulting in dramatic performance gains.

{{< figure src="img/posts/1/genotype-phenotype-mapping.png" title="A genotype to phenotype mapping example. A genotype is depicted that produces the shown phenotype." >}}

There are two main types of structural mutations present in the NEAT algorithm: adding the connection between nodes or adding the new node. When mutation is performed, the new added gene (connection gene or node gene) will be assigned with increasingly incremented *innovation number*.

{{< figure src="img/posts/1/types-of-structural-mutations.png" title="In adding a connection, a single new connection gene is added to the end of the genome and given the next available innovation number. In adding a new node, the connection gene being split is disabled, and two new connection genes are added to the end the genome. The new node is between the two new connections." >}}

Through mutation, the genomes in NEAT will gradually get larger. Genomes of varying sizes will result, sometimes with different connections (genes) at the same positions.

There is an unexploited information in evolution, that tells us exactly which genes match up with which genes between *any* individuals in a topologically diverse population. That information is the historical origin of each gene. Two genes with the same historical origin must represent the same structure (although possibly with different weights), since they are both derived from the same ancestral gene of some point in the past. Thus, all the system needs to do, in order to know which genes line up with which, is to keep track of the historical origin of every gene in the population’s genome.

Luckily for us, the *innovation numbers* incrementally assigned to the genes during genome mutations is a kind of *historical markers* to use for tracking chronology of structural genome mutations. At the same time, during crossover (mating), the offsprings will inherit the same innovation numbers of genes in the parents genome. Thus, innovation number of particular gene will never change, allowing tracking of historical origin of every gene throughout evolution.

The historical markers give NEAT a power to track which genes match up with which. Thus, during the crossover, system will know exactly how to lineup genes from genomes of both parents. The genes with matching innovation numbers will be called *matching* genes. Genes that do not match are either *disjoint* or *excess*, depending on whether they occur within or outside the range of the other parent’s innovation numbers. They represent structure that is not present in the other parent’s genome. When composing the offspring, genes are randomly chosen from either parent at matching genes, whereas all excess or disjoint genes are always included from the more fit parent. This way, historical markings allow NEAT to perform crossover using linear genomes encoding without the need for expensive topological analysis.

{{< figure src="img/posts/1/crossover-using-linear-genomes-encoding.png" title="During the crossover, the offspring genes are randomly chosen from matching genes of either parent and disjoint/excess genes taken from most fit parent. All diagrams from original [NEAT paper](http://nn.cs.utexas.edu/?stanley:gecco02b), highly recommended reading!" >}}

Using proposed method the population of organisms can evolve diverse topologies, but it happens that such population can not evolve and maintain *topological innovations* on its own. The smaller structures optimize faster than larger structures. Thus by adding new nodes and connections to some topology we artificially reduce it’s chances for survival. The freshly augmented topologies usually experience initial decrease in the fitness, even though the innovations they represent may be resulting in winning solution in the long run.

This can be solved by introducing *speciation* to the population which additionally limits range of organisms that can mate. With speciation it’s possible to organize crossover in such a way that organisms will compete only in narrow niches instead of all population in general. The idea is to divide the population such that similar topologies are in the same species.

***

With all specific tweaks to general GA introduced with NEAT it's possible to build complex ANNs to solve control optimization problems among other unsupervised learning problems. Due to specifics of ANN topology augmentation through complexification and speciation found solutions tends to be performance optimized from the train as well as from the inference point of view. The resulting ANNs topology grows exactly to match problem to be solved without any excess layers of hidden units introduced with traditional approach of ANN's topology hand-engineering.

Due to this it's possible to build complex ensembles of specific ANNs to solve most complex problems arising when attempting to build AI systems. Such ensembles of highly specialized small ANNs can be combined in a way as neural networks combined in the human brain, where each specific part responsible for the processing of particular stimulus or specialized activity.

Another application of ANNs ensembles is to create solvers for imperfect information games by applying sub-game solving strategy proposed in this [research paper](https://arxiv.org/abs/1705.02955).

***

There are exists number of implementations of NEAT algorithm in [diverse programming languages](http://eplex.cs.ucf.edu/neat_software/).

The author also provided his own implementation of NEAT in GO programming language with extended verification benchmarks: XOR, single-, and double-pole balancing. The source code of the implementation is available at GitHub: https://github.com/yaricom/goNEAT

The associated research project can be found at ResearchGate: https://www.researchgate.net/project/NeuroEvolution-of-Augmented-Topologies

> The original article was posted by author at Medium: [Neuroevolution - evolving Artificial Neural Networks topology from the scratch](https://medium.com/@io42/neuroevolution-evolving-artificial-neural-networks-topology-from-the-scratch-d1ebc5540d84)
