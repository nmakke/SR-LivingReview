# A living Review of Symbolic Regression

This review is created to collect references for symbolic regression methods and applications, as part of the recent paper [Interpretable Scientific Discovery with Symbolic Regression: A Review](https://arxiv.org/abs/2211.10873). It is made in analogy with "A Living Review of Machine Learning for Particle Physics" that can be found [here](https://iml-wg.github.io/HEPML-LivingReview/).

Symbolic regression is a branch of machine learning that aims to learn analytical form of underlying model in data, by searching the space of mathematical functions. A growing interest in symbolic regression is taking place in the AI community because it interpretability, which is a critical factor for a safe AI application. 

| Category | Methods | |
| -------- | ------- | ----- 
| Regression-based | Linear SR <br> Non-linear SR | System of linear equations <br> Neural network |
| Expression tree-based | Genetic programming (GP) <br> Reinforcement learning (RL) <br> Transformer neural network | tree structure <br> policy <br> sequence |
| Physics-inspired | AIFeynman | Brute force search and neural network |
| Mathematics-inspired| Metamodel | Meijer functions |

The goal of this repository is to collect references for symbolic regression. Notes will be later categorized in an as easy and useful manner as possible. 

* **Regression-based SR**
  * Linear approach
    * [Discovering governing equations from data by sparse identification of nonlinear dynamical systems](https://www.pnas.org/doi/full/10.1073/pnas.1517384113) [PDF](https://www.pnas.org/content/pnas/113/15/3932.full.pdf?with-ds=yes&source=post_page---------------------------) (SINDY)
    * [Data-driven discovery of coordinates and governing equations](https://www.pnas.org/content/pnas/116/45/22445.full.pdf), [![#c5f015](https://via.placeholder.com/15/c5f015/000000?text=+)`code`](https://github.com/kpchamp/SindyAutoencoders) (SINDY + AE)

  * Non-linear approaches
    * [AI Feynman: a Physics-Inspired Method for Symbolic Regression](https://arxiv.org/pdf/1905.11481.pdf), [![#c5f015](https://via.placeholder.com/15/c5f015/000000?text=+)`code`](https://github.com/SJ001/AI-Feynman)
    * [Integration of Neural Network-Based Symbolic Regression in Deep Learning for Scientific Discovery](https://arxiv.org/pdf/1912.04825.pdf)
    * [Symbolic regression for scientific discovery: an application to wind speed forecasting](https://arxiv.org/pdf/2102.10570.pdf)
    * [Relational inductive biases, deep learning, and graph networks](https://arxiv.org/pdf/1806.01261.pdf)
    * [Eurequa](https://link.springer.com/content/pdf/10.1007/s10710-010-9124-z.pdf)
    * [Extrapolation and learning equations](https://arxiv.org/pdf/1610.02995.pdf) (EQL)
    * [Learning Equations for Extrapolation and Control](http://proceedings.mlr.press/v80/sahoo18a/sahoo18a.pdf)(EQL_division)

* NN + SR
  * [Discovering Symbolic Models from Deep Learning with Inductive Biases](https://arxiv.org/pdf/2006.11287.pdf),[![#c5f015](https://via.placeholder.com/15/c5f015/000000?text=+)`code`](https://github.com/MilesCranmer/symbolic_deep_learning) (GNN + SR)
  * [Data-driven discovery of coordinates and governing equations](https://www.pnas.org/content/pnas/116/45/22445.full.pdf), [![#c5f015](https://via.placeholder.com/15/c5f015/000000?text=+)`code`](https://github.com/kpchamp/SindyAutoencoders) (SINDY + AE)

* Benchmark
  * [Contemporary Symbolic Regression Methods and their Relative Performance](https://arxiv.org/pdf/2107.14351.pdf)

[Discovery of Physics from Data: Universal Laws and Discrepancy Models](https://arxiv.org/pdf/1906.07906.pdf)
[Sparse dynamics for partial differential equations]()

