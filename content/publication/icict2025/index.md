---
title: "Parallel Fitness Scores Evaluation to Improve Training Speed of the NEAT Algorithm Using GO Routines"
authors:
- admin
date: 2025-11-08T16:15:00-00:00
doi: "10.1007/978-981-96-6938-7_17"

# Schedule page publish date (NOT publication's date).
publishDate: "2025-11-08T16:15:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["1"]

# Publication name and optional abbreviated publication name.
publication: "Parallel Fitness Scores Evaluation to Improve Training Speed of the NEAT Algorithm Using GO Routines. In: Yang, XS., Sherratt, R.S., Dey, N., Joshi, A. (eds) Proceedings of Tenth International Congress on Information and Communication Technology. ICICT 2025. Lecture Notes in Networks and Systems, vol 1441. Springer, Singapore."
publication_short: "Design of Cluster-Computing Architecture to Improve Training Speed of the Neuroevolution Algorithm."

abstract: Neuroevolution algorithms need to evaluate at the end of each epoch the fitness scores of each organism in a population of solvers within the problem space where a solution is sought. This evaluation often involves running complex environmental simulations, which can significantly slow down the training speed if done sequentially. This work proposes a solution that utilizes the inherent capabilities of the Go programming language to run complex simulations in local parallel processes (routines). The efficiency of this proposed solution is compared to sequential evaluation using two classic reinforcement learning experiments, specifically single and double-pole balancing. Direct comparisons indicate that the proposed solution is up to five times faster than the sequential approach when complex environmental simulations are required for objective function evaluation.

# Summary. An optional shortened abstract.
summary: ""

tags:
- neuroevolution

featured: true

url_pdf: "/files/icict2025/flyer_978-981-96-6938-7.pdf"
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
