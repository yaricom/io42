---
title: "Design of cluster-computing architecture to improve training speed of the Neuroevolution algorithm"
authors:
- admin
date: 2024-08-10T16:15:00-00:00
doi: "10.1007/978-981-97-3556-3_32"

# Schedule page publish date (NOT publication's date).
publishDate: "20124-02-22T16:15:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["1"]

# Publication name and optional abbreviated publication name.
publication: "Design of Cluster-Computing Architecture to Improve Training Speed of the Neuroevolution Algorithm. In: Yang, XS., Sherratt, S., Dey, N., Joshi, A. (eds) Proceedings of Ninth International Congress on Information and Communication Technology. ICICT 2024. Lecture Notes in Networks and Systems. Singapore, Springer, 2024. Vol. 1012"
publication_short: "Design of Cluster-Computing Architecture to Improve Training Speed of the Neuroevolution Algorithm."

abstract: In this paper, we review the key features and major drawbacks of the Neuroevolution of Augmenting Topologies (NEAT) algorithm, such as slow training speed that limits its area of application. The main reason for the performance issues of the NEAT algorithm is the huge number of calculations required at the end of each epoch to estimate the fitness of each organism in the population. We propose a software system architecture that can be implemented to solve NEAT performance problems based on Ray cluster-computing framework. Finally, we demonstrate how fitness estimation computations can be distributed across stateless distributed workers deployed either on-premise or in the cloud using [Ray framework](https://www.ray.io).

# Summary. An optional shortened abstract.
summary: ""

tags:
- neuroevolution

featured: true

url_pdf: "https://link.springer.com/chapter/10.1007/978-981-97-3556-3_32"
url_code: "https://github.com/yaricom/goNEAT"

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: ''
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
