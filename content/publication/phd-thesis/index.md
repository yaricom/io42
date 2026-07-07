---
title: "PhD Thesis: Optimization of Neural Network Topology Based on Neuroevolutionary Algorithms Using Distributed Parallel Computations."
authors:
- admin
date: 2026-04-22T15:28:14+02:00
doi: "10.13140/RG.2.2.21655.33443"
url_preprint: "https://svr.naqa.gov.ua/#/defense/11998"

# Schedule page publish date (NOT publication's date).
publishDate: "2026-04-22T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["7"]

# Publication name and optional abbreviated publication name.
publication: "Optimization of Neural Network Topology Based on Neuroevolutionary Algorithms Using Distributed Parallel Computations. –Qualification scientific work, manuscript rights."
publication_short: "Optimization of Neural Network Topology Based on Neuroevolutionary Algorithms Using Distributed Parallel Computations."

abstract: The dissertation is submitted in partial fulfillment of the requirements for the degree of Doctor of Philosophy (PhD) in the specialty 122 – “Computer Sciences”. The research was carried out at the Institute of Software Systems of the National Academy of Sciences of Ukraine.<br/>The dissertation is devoted to solving a relevant scientific and applied problem of improving the performance (speed) of artificial neural network (ANN) topology construction using the NEAT neuroevolutionary algorithm by optimizing the fitness evaluation stage through the application of parallel computing techniques.<br/>Neuroevolutionary algorithms, like other genetic algorithms, are based on the concept of evolutionary development of a population of organisms encoding the topology and/or weight coefficients of a neural network. To maintain the evolutionary process, each organism in the population must be evaluated by a selected fitness function at every evolutionary epoch. Typically, the fitness function relies on parameters obtained by simulating a practical task that each organism in the population must solve. Classical software models for managing the evolutionary process in neuroevolutionary algorithms perform such simulations sequentially for each organism before generating the next population. This approach has a significant negative impact on algorithm performance, since practical task simulation usually requires substantial computational resources and execution time. As a result, the total computation time grows proportionally to the population size, leading to a considerable loss of efficiency and limiting the applicability of neuroevolutionary algorithms to real-world problems involving complex simulations of physical environments. This limitation is particularly critical given that neural network topologies obtained via neuroevolution are typically optimal and energy-efficient, making them suitable for deployment on resource-constrained devices such as autonomous robotic platforms and unmanned aerial vehicles.<br/>The described performance issue can be mitigated by employing modern software tools that enable parallel execution of task simulations in a distributed computational environment. This dissertation proposes a software-based approach for utilizing distributed parallel computations at the stage of practical task simulation used for fitness evaluation in neuroevolutionary algorithms.


# Summary. An optional shortened abstract.
summary: This dissertation, submitted in partial fulfillment of the PhD degree in Computer Science, focuses on improving the performance of the NEAT neuroevolutionary algorithm by accelerating the fitness evaluation stage through distributed parallel computing. Since evaluating each neural network in a population is computationally expensive and traditionally performed sequentially, it becomes the main performance bottleneck. The proposed approach enables parallel execution of fitness evaluations across distributed computing resources, significantly reducing computation time, improving scalability, and extending the applicability of neuroevolutionary algorithms to complex real-world tasks, including autonomous robotics and unmanned aerial vehicles.

tags:
- neuroevolution
- unsupervised-learning
- reinforcement-learning
- evolutionary-computation
- distributed computing
- formal model
- optimal strategy

categories:
- artificial-neural-networks
- neuroevolution
- NEAT

featured: true

url_pdf: "/files/phd_thesis/Omelianenko_Iaroslav_PhD_thesis.pdf"

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: 'Three-dimensional dependence of the total evolution time on the population size N and the number of workers p, with the Pareto-optimal region  highlighted (within 5% of the minimum evolution time for each population size).'
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects: []


# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---
