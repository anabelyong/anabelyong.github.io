---
layout: default
title: ML Posts
---

# My thoughts and opinions for Bayesian Machine Learning. 
I want to document my journey in Machine Learning where I stamp interesting frameworks and why I find them interesting. 
A reminder to self: Great ideas do not come from nowhere. They are derived from fundamental concepts, collaboration, and lots of trial and error. 

## 10/11/2025: Probabilistic Circuits (why Tractable Inference?)
A generative model encodes a joint distribution $p(X)$ over many variables $X$. Even answering a simple equestion like "What is the probability that it is raining today  and Anabel is going to eat hotpot soup?" requires computing a marginal probability: $p(E=e) = \sum_H p(e,H)$ where $E$ is an observed event and $H$ represents all other hidden variables. For general graphical models, this summation is \#P-hard, meaning it is computationally intractable in the worst case.

This motivates the design of tractable model classes - models for which inference is guaranteed to be efficient. I attempt to summarise key ideas in my notes below on Probabilistic Circuits, a line of work driven by Guy van der Broeck and collaborators that advances tractable, rather than approximante, probabilistic inference. Here are the resources: 
- **UCLA StarAI Lab's 3 hour Lecture:** The first two hours of this provides a great introduction to PCs (if you have a nice intuition on probability on marginals and conditionals). [YOUTUBE Video](https://www.youtube.com/watch?v=2RAG5-L9R70)
- **Anji Liu's Notebook Tutorials:** Am personally still navigating this PyJuice framework myself. [PyJuice Tutorials](https://tractables.github.io/pyjuice/getting-started/tutorials/01_train_pc.html#sphx-glr-getting-started-tutorials-01-train-pc-py)
- **My notes on PCs:** [Anabel's Introduction to PCs](/documents/prob_circ_notes.pdf)
- **Relevant Concepts:** [Logic Gates](https://www.geeksforgeeks.org/digital-logic/introduction-of-logic-gates/) (useful to know AND/OR/XOR nodes), [Sum-Product Networks (SPNs)](https://proceedings.mlr.press/v28/gens13.html). 


## 31/10/2025: Bayesian Optimal Experimental Design (why Expected Information Gain?)
I wanted to investigate the origin story for [InfoBAX](https://arxiv.org/abs/2104.09460), have a short introduction on BOED. How and why the ideas of info-theoretic BO came around. 
**Useful Resources:**
- **Bayesian Optimal Experimental Design notes:** Desi Ivanova does a great simple introduction and visualization to BOED. Here: [Desi's 7 min Read](https://desirivanova.com/post/boed-intro/)
- **InfoBAX:** Willie Neiswanger does a great talk on InfoBAX I really loved. Here: [Willie Neiswanger's Presentation](https://stanford.zoom.us/rec/share/1ASiyhRzE34CVbW3-2oiwJqBc69RnDe6QlVuwVxY6hui_mJDBV3_5rkD-j7zirWD.tF6pyVfWGcbpa_5C)
- **My thoughts on InfoBAX:** [InfoBAX_insights](/documents/InfoBAX_insights.pdf)
- **Relevant Concepts:** [Lindley's EIG](https://projecteuclid.org/euclid.aoms/1177728069), [Hennig's Entropy Search](https://arxiv.org/abs/1112.1217), [Krause's Mutual Information Maximization](https://jmlr.org/papers/v9/krause08a.html), [A Geneticist's Approximate Bayesian Computation demonstration](https://pubmed.ncbi.nlm.nih.gov/10605120/).

