---
hide:
  - navigation
---


# **A Living Review of Symbolic Regression**

*Symbolic regression (SR) is a rapidly growing subfield of machine learning (ML) aiming to learn the analytical form of models that underlie data by searching the space of mathematical expressions. A growing interest in SR is taking place because it is naturally interpretable, i.e., it learns a transparent relationship between the input and the output, allowing for reasoning, in contrast to blackbox models learned by neural networks (NNs) where the input-output relationship is opaque and untractable.*

*This document provides a categorized list of state-of-the-art methods, datasets, and applications of SR as part of the review entitled ***Interpretable Scientific Discovery with Symbolic Regression: A Review***, which provides a technical and unified review of several research works on SR. This document's goal to list all research works so this list will continue to evolve. <!--This living review was proposed in the mentioned review in analogy with HEP ML Living Review ([link](https://iml-wg.github.io/HEPML-LivingReview/)).-->*

*The aim is to create a unified, sufficient, and complete database for materials on SR (research papers, open-source codes, datasets, useful online resources, educational materials, etc.) among different communities that have an interest in the symbolic regression research area.*

<!-- [<img src="https://s18955.pcdn.co/wp-content/uploads/2018/02/github.png" width="25"/>](https://github.com/user/repository/subscription) -->

<!-- This living review was proposed in the mentioned review in analogy with [HEP ML Living Review](https://iml-wg.github.io/HEPML-LivingReview/). The goal is to list all research works on symbolic regression, so it is expected that ***this list will continue to evolve***. The fact that a paper is listed in this document does not endorse or validate its content - that is for the community (and for peer review) to decide. -->

[![download](https://img.shields.io/badge/download-review-blue.svg)](https://arxiv.org/pdf/2211.10873.pdf)

???+ note "SR Methods"
    <div class="meta_for_parser tablespecs"
    style="font-size: 1pt;visibility:hidden" markdown>
    ##  SR Methods
    </div>

    
    | <div style="width:140px">Category</div> | <div style="width:200px">Brief description</div> | <div style="width:220px">Underlying methods</div> | <div style="width:180px">learned model</div> |
    | ---- | ------- | --- | --- |
    | Regression-based | This category presumes the model structure is a linear combination of non-linear functions. The linear method formulates the SR problem as a system of linear equations, whereas the non-linear method relies on a multi-layer perceptron (MLP). In both cases parameters are learned. | Linear SR (sparse regression) <br> Non-linear SR | System of linear equations <br> Multi-Layer Perceptron (MLP) |
    | Expression tree-based | This category treats mathematical equations as unary-binary trees whose internal nodes are mathematical operators (algebraic operators, analytical functions) and terminal nodes are constants and state variables. | Genetic programming (GP) <br> Reinforcement learning (RL) <br> Transformer neural network (TNN) | Tree structure <br> Policy <br> Seq2seq models |
    | Physics-inspired | This category takes into account the units of measurements of physical variables (so-called dimensional analysis) to constraint the search space | Deep learning <br> polynomial fit <br> brute force search | Neural network parameters <br> polynomial coefficients |
    | Mathematics-inspired| This method uses the Meijer functions | General mathematical function | parameters of the Meijer functions |


???+ note "SR Datasets"
    <div class="meta_for_parser tablespecs"
    style="font-size: 1pt;visibility:hidden" markdown>
    ##  SR Datasets
    </div>
    
    Data sets ($\mathcal{D}$) are categorized into two main groups:
    
    **Synthetic data**  for which the analytical form of the underlying model is known and used to generate data points. <br>
    Example: $f(x) = 2x^2 + \cos(x) \rightarrow \mathcal{D}=(x_i,f(x_i))_{i=1}^{n}$ for $x \in [0,1]$

     **Real-world data** for which underlying models are unknown.<br>
     
      <table>
          <thead>
              <tr>
                  <th>Type</th>
                  <th>Category</th>
                  <th>Underlying model</th>
                  <th>Benchmarks</th>
                  <th>Number of equations</th>
              </tr>
          </thead>
          <tbody>
              <tr>
                  <td rowspan=10>Synthetic data</td>
                  <td rowspan=2>Physics</td>
                  <td>Physics equations</td>
                  <td>AIFeynman</td>
                  <td>120</td>
              </tr>
              <tr>
                  <td>Ordinary differential equations</td>
                  <td>Strogatz</td>
                  <td>10</td>
              </tr>
              <tr>
                  <td rowspan=8>Mathematics</td>
                  <td rowspan=8>monomials, polynomials, <br> trigonometric, exponential, <br> logarithm, power law, etc.</td> 
                  <td>Koza</td><td>3</td>
              </tr>
              <tr><td>Keijer</td><td>15</td></tr>
              <tr><td>Vladislavleva</td><td>8</td></tr>
              <tr><td>Nguyen</td><td>12</td></tr>
              <tr><td>Korns</td><td>15</td></tr>
              <tr><td>R</td><td>3</td></tr>
              <tr><td>Jin</td><td>6</td></tr>
              <tr><td>Livermore</td><td>22</td></tr>  
              <tr>
                  <td rowspan=1>Real world data</td>
                  <td>economy, climate, commerce, etc.</td>
                  <td>NA</td>
                  <td>Penn Machine Learning Benchmarks</td>
                  <td>419</td>
              </tr>
          </tbody>
      </table>

??? note "Benchmarks"
    <div class="meta_for_parser tablespecs"
    style="font-size: 1pt;visibility:hidden" markdown>
    ##  Benchmarks
    </div>
    
      * [Contemporary Symbolic Regression Methods and their Relative Performance](https://arxiv.org/pdf/2107.14351.pdf) [![#c5f015](https://via.placeholder.com/15/c5f015/000000?text=+)`code`](https://github.com/cavalab/srbench)
      
??? note "Reviews"
    <div class="meta_for_parser tablespecs"
    style="font-size: 1pt;visibility:hidden" markdown>
    ##  Reviews
    </div>
    
      * [Interpretable Scientific Discovery with Symbolic Regression: A Review](https://arxiv.org/pdf/2211.10873.pdf)

??? "SR Applications in physics"
    <div class="meta_for_parser tablespecs"
    style="font-size: 1pt;visibility:hidden" markdown>
    ##  SR Applications
    </div>

      * [Discovering Symbolic Models from Deep Learning with Inductive Biases](https://arxiv.org/pdf/2006.11287.pdf) [![#c5f015](https://via.placeholder.com/15/c5f015/000000?text=+)`code`](https://github.com/MilesCranmer/symbolic_deep_learning) (GNN + SR)
      * [Data-driven discovery of coordinates and governing equations](https://www.pnas.org/content/pnas/116/45/22445.full.pdf) [![#c5f015](https://via.placeholder.com/15/c5f015/000000?text=+)`code`](https://github.com/kpchamp/SindyAutoencoders) (SINDY + AE)
      * [Rediscovering orbital mechanics with machine learning](https://arxiv.org/abs/2202.02306)
      * [Back to the Formula -- LHC Edition](https://arxiv.org/abs/2109.10414)
      * [SYMBA: SYMBOLIC COMPUTATION OF SQUARED AMPLITUDES IN HIGH ENERGY PHYSICS WITH MACHINE LEARNING](https://arxiv.org/pdf/2206.08901.pdf) [![#c5f015](https://via.placeholder.com/15/c5f015/000000?text=+)`code`](https://github.com/ML4SCI/SYMBAHEP)
      
