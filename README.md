# A living Review of Symbolic Regression

This note aims to collect references for symbolic regression (SR) [methods](#methods) and [datasets](#datasets) as part of the recent [review](https://arxiv.org/abs/2211.10873) entitled "**Interpretable Scientific Discovery with Symbolic Regression: A Review**". The latter review SR methods and state-of-the-art applications of SR, along with existing datasets usually used in testing SR methods, and discusses their main strength and weakness.

<!-- [<img src="https://s18955.pcdn.co/wp-content/uploads/2018/02/github.png" width="25"/>](https://github.com/user/repository/subscription) -->

**A living review for symbolic regression is first** proposed in the mentioned review in analogy with "A Living Review of Machine Learning for Particle Physics" which can be found [here](https://iml-wg.github.io/HEPML-LivingReview/). The goal is to list all research works on symbolic regression so it is expected that ***this list will continue to evolve***. The fact that a paper is listed in this document does not endorse or validate its content - that is for the community (and for peer-review) to decide.

Symbolic regression is an emerging branch of machine learning that aims to learn analytical form of underlying model in data, by searching the space of mathematical functions. A growing interest in symbolic regression is taking place in the AI community because it pomotes interpretability, which is a critical factor for a safe AI application.

## Methods 
The symbolic regression problem can be approached and solved in different manners, depending on the way the target mathematical expression f(x) is defined. References (for SR) are categorized in an as easy and useful manner as possible, with a summary given in the table below. 

| Category | Methods | learned model |
| -------- | ------- | ----- 
| Regression-based | Linear SR <br> Non-linear SR | System of linear equations <br> Deep Neural Network |
| Expression tree-based | Genetic programming (GP) <br> Reinforcement learning (RL) <br> Transformer neural network (TNN) | tree structure <br> policy <br> sequence |
| Physics-inspired | AIFeynman | Brute force search and neural network |
| Mathematics-inspired| Metamodel | Meijer functions |

<!-- the model has a pre-defined form such as a linear combination of non-linear functions or a neural network<br> the problem reduces to learning the parameters of the model
mathematical equations are treated as <br> unary-binary trees, which can be written in polish notation as sequences of symbolic representations |
 -->
 
* **Regression-based SR**
  
  * Linear approach
    * [Discovering governing equations from data by sparse identification of nonlinear dynamical systems](https://www.pnas.org/content/pnas/113/15/3932.full.pdf?with-ds=yes&source=post_page---------------------------)[[DOI]](https://www.pnas.org/doi/full/10.1073/pnas.1517384113) (SINDY)
    * [Data-driven discovery of coordinates and governing equations](https://www.pnas.org/content/pnas/116/45/22445.full.pdf) [[DOI]](https://www.pnas.org/doi/10.1073/pnas.1906995116) [![#c5f015](https://via.placeholder.com/15/c5f015/000000?text=+)`code`](https://github.com/kpchamp/SindyAutoencoders) (SINDY + AE)
    
  * Non-linear approaches
    * [AI Feynman: a Physics-Inspired Method for Symbolic Regression](https://arxiv.org/pdf/1905.11481.pdf) [[DOI]](https://www.science.org/doi/10.1126/sciadv.aay2631) [![#c5f015](https://via.placeholder.com/15/c5f015/000000?text=+)`code`](https://github.com/SJ001/AI-Feynman)
    * [Integration of Neural Network-Based Symbolic Regression in Deep Learning for Scientific Discovery](https://arxiv.org/pdf/1912.04825.pdf)
    * [Symbolic regression for scientific discovery: an application to wind speed forecasting](https://arxiv.org/pdf/2102.10570.pdf)
    * [Relational inductive biases, deep learning, and graph networks](https://arxiv.org/pdf/1806.01261.pdf)
    * [Extrapolation and learning equations](https://arxiv.org/pdf/1610.02995.pdf) (EQL)
    * [Learning Equations for Extrapolation and Control](http://proceedings.mlr.press/v80/sahoo18a/sahoo18a.pdf)(EQL_division)

* **Expression tree-based approaches** 

  * Genetic programming
       * [Eurequa](https://link.springer.com/content/pdf/10.1007/s10710-010-9124-z.pdf)
       * [PySR: High-Performance Symbolic Regression in Python and Julia](https://github.com/MilesCranmer/pysr)
       * Genetic programming as a means for programming computers by natural selection [[DOI]](https://link.springer.com/article/10.1007/BF00175355)
       * Order of Nonlinearity as a Complexity Measure for Models Generated by Symbolic Regression via Pareto Genetic Programming [[DOI]](https://ieeexplore.ieee.org/document/4632147)
       * Improving Symbolic Regression with Interval Arithmetic and Linear Scaling [[DOI]](https://link.springer.com/chapter/10.1007/3-540-36599-0_7)
       * Accuracy in Symbolic Regression [[DOI]](https://link.springer.com/chapter/10.1007/978-1-4614-1770-5_8)
       * Semantically-based crossover in genetic programming: application to real-valued symbolic regression [[DOI]](https://link.springer.com/article/10.1007/s10710-010-9121-2)

  * Reinforcement learning
    * [Deep symbolic regression: Recovering mathematical expressions from data via risk-seeking policy gradients](https://arxiv.org/abs/1912.04871) [[DOI]](https://openreview.net/forum?id=m5Qsh0kBQG) [![#c5f015](https://via.placeholder.com/15/c5f015/000000?text=+)`code`](https://github.com/brendenpetersen/deep-symbolic-optimization)
    * [Symbolic Regression via Neural-Guided Genetic Programming Population Seeding](https://arxiv.org/abs/2111.00053) [[DOI]](https://proceedings.neurips.cc/paper/2021/hash/d073bb8d0c47f317dd39de9c9f004e9d-Abstract.html)[![#c5f015](https://via.placeholder.com/15/c5f015/000000?text=+)`code`](https://github.com/brendenpetersen/deep-symbolic-optimization)
    * [Physical Symbolic Optimization](https://arxiv.org/pdf/2303.03192.pdf) [![#c5f015](https://via.placeholder.com/15/c5f015/000000?text=+)`code`](https://github.com/WassimTenachi/PhySO/tree/main)
    
  * Transformer neural network
    * [End-to-end symbolic regression with transformers](https://arxiv.org/abs/2204.10532) [![#c5f015](https://via.placeholder.com/15/c5f015/000000?text=+)`code`](https://github.com/facebookresearch/symbolicregression)
    * [Neural Symbolic Regression that Scales](https://arxiv.org/abs/2106.06427) [![#c5f015](https://via.placeholder.com/15/c5f015/000000?text=+)`code`](https://github.com/SymposiumOrganization/NeuralSymbolicRegressionThatScales)
    * [SymbolicGPT: A Generative Transformer Model for Symbolic Regression](https://arxiv.org/pdf/2106.14131.pdf) [![#c5f015](https://via.placeholder.com/15/c5f015/000000?text=+)`code`](https://github.com/mojivalipour/symbolicgpt)
    * [SYMBA: SYMBOLIC COMPUTATION OF SQUARED AMPLITUDES IN HIGH ENERGY PHYSICS WITH MACHINE LEARNING](https://arxiv.org/pdf/2206.08901.pdf) [![#c5f015](https://via.placeholder.com/15/c5f015/000000?text=+)`code`](https://github.com/ML4SCI/SYMBAHEP)

* **Physics-inspired**

  * [AI Feynman: a Physics-Inspired Method for Symbolic Regression](https://arxiv.org/pdf/1905.11481.pdf) [[DOI]](https://www.science.org/doi/10.1126/sciadv.aay2631) [![#c5f015](https://via.placeholder.com/15/c5f015/000000?text=+)`code`](https://github.com/SJ001/AI-Feynman)

* **Mathematics-inspired**

  * [Demystifying Black-box Models with
Symbolic Metamodels](https://www.vanderschaar-lab.com/papers/NIPS2019_DBM.pdf) [[DOI]](https://papers.nips.cc/paper_files/paper/2019/hash/567b8f5f423af15818a068235807edc0-Abstract.html) [![#c5f015](https://via.placeholder.com/15/c5f015/000000?text=+)`code`](https://github.com/vanderschaarlab/mlforhealthlabpub/tree/main/alg/symbolic_metamodeling)

* **Computational approach**

    * [Distilling Free-Form Natural Laws from Experimental Data](https://www.science.org/doi/10.1126/science.1165893)


## Applications

  * Physics   
    * [Discovering Symbolic Models from Deep Learning with Inductive Biases](https://arxiv.org/pdf/2006.11287.pdf) [![#c5f015](https://via.placeholder.com/15/c5f015/000000?text=+)`code`](https://github.com/MilesCranmer/symbolic_deep_learning) (GNN + SR)
    * [Data-driven discovery of coordinates and governing equations](https://www.pnas.org/content/pnas/116/45/22445.full.pdf) [![#c5f015](https://via.placeholder.com/15/c5f015/000000?text=+)`code`](https://github.com/kpchamp/SindyAutoencoders) (SINDY + AE)
    * [Rediscovering orbital mechanics with machine learning](https://arxiv.org/abs/2202.02306)
    * [Back to the Formula -- LHC Edition](https://arxiv.org/abs/2109.10414)
    * [SYMBA: SYMBOLIC COMPUTATION OF SQUARED AMPLITUDES IN HIGH ENERGY PHYSICS WITH MACHINE LEARNING](https://arxiv.org/pdf/2206.08901.pdf) [![#c5f015](https://via.placeholder.com/15/c5f015/000000?text=+)`code`](https://github.com/ML4SCI/SYMBAHEP)
  
* Benchmark
  * [Contemporary Symbolic Regression Methods and their Relative Performance](https://arxiv.org/pdf/2107.14351.pdf) [![#c5f015](https://via.placeholder.com/15/c5f015/000000?text=+)`code`](https://github.com/cavalab/srbench)

<!-- [Discovery of Physics from Data: Universal Laws and Discrepancy Models](https://arxiv.org/pdf/1906.07906.pdf)
[Sparse dynamics for partial differential equations]() -->

## Datasets

Data sets can be categorized into two main groups:

**Synthetic data**  for which analytical form of underlying model is known, and used to generate data points. <br>
Example: $f(x) = 2x^2 + \cos(x)$, $x \in [0,1] \rightarrow \mathcal{D}=(x_i,f(x_i))_{i=1}^{n}$

**Real-world data** for which underlying model is unknown.<br>
$\mathcal{D}=(x_i,y_i)_{i=1}^{n}$ 

| Category | reference | # equations | year |
| -------- | ------- | ------- | ----- 
| Physics-related | [Strogatz repositery](https://williamlacava.com/ode-strogatz/) <br> [Feynman Database](https://space.mit.edu/home/tegmark/aifeynman.html) | 10 <br> 120 | 2011 <br> 2019 |
| Mathematics-related | Koza <br> Keijer <br> Vladislavleva <br> Nguyen <br> Korns <br> R <br> Jin <br> [Livermore](https://arxiv.org/abs/1912.04871) | 3 <br> 15 <br> 8 <br> 12 <br> 15 <br> 3 <br> 6 <br> 22 | 1994 <br> 2003 <br> 2009 <br> 2011 <br> 2011 <br> 2013 <br> 2019 <br> 2021 |
| Real-world problems | [link](https://epistasislab.github.io/pmlb/) | 









