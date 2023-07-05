---
hide:
  - navigation
---

Symbolic regression (SR) methods are grouped into different categories to be most useful, as summarized in the table.<br>
Below you find the list of SR methods for each category.
<!--**Regression-based** SR methods assume a predefined model structure. In this category, the linear approach formulates the SR problem as a system of linear equations, whereas the non-linear approach relies on multi-layer perceptron (MLP) to solve it. In both cases, the models' parameters are learned.<be>-->
<!-- ´**Expression tree-based** SR methods treat mathematical equations as unary-binary tree whose internal nodes are mathematical operators (algebraic operators $\{+, -, \times, \div\}$,  analytical functions $\{\cos,\sin,\tan,\exp,\log,\mathrm{sqrt},\mathrm{etc}\}$) and terminal nodes are constants and state variables. This category comprises GP-based SR, RL-based SR, and TNN-based SR.<br>-->
<!--  **Other SR approaches** category includes methods inspired by other disciplines, such as physics and mathematics, to solve the SR problem.-->

<!-- | Category | Description | Methods | learned model |-->
| <div style="width:130px">Category</div> | <div style="width:200px">Description</div> | <div style="width:200px">Methods</div> | <div style="width:180px">learned model</div> |
| ---- | ------- | --- | --- |
| Regression-based | This category assumes a predefined model structure and learns only parameters. The linear approach formulates the SR problem as a system of linear equations, whereas the non-linear approach relies on multi-layer perceptron (MLP) to solve it. | Linear SR (sparse regression) <br> Non-linear SR | System of linear equations <br> Deep Neural Network (DNN) |
| Expression tree-based | This category treats mathematical equations as unary-binary trees whose internal nodes are mathematical operators (algebraic operators and  analytical functions) and terminal nodes are constants and state variables. | Genetic programming (GP) <br> Reinforcement learning (RL) <br> Transformer neural network (TNN) | Tree structure <br> Policy <br> Seq2seq models |
| Physics-inspired | This category uses units of measurements of input features (so-called dimensional analysis) | Deep learning (including many tools) & polynomial fit & brute force search | Neural network for symmetries (translational, rotational) |
| Mathematics-inspired| This method uses the Meijer functions | Metamodel | parameters of the Meijer functions |

## Regression-based SR
  
???+ note "Linear approach"
    <div class="meta_for_parser tablespecs"
    style="font-size: 1pt;visibility:hidden" markdown>
    ###  Linear approach
    </div>
    
    * [Discovering governing equations from data by sparse identification of nonlinear dynamical systems](https://www.pnas.org/content/pnas/113/15/3932.full.pdf?with-ds=yes&source=post_page---------------------------)[[DOI]](https://www.pnas.org/doi/full/10.1073/pnas.1517384113) (SINDY)
    * [Sparse identification of nonlinear dynamics for rapid model recovery](https://arxiv.org/pdf/1803.00894.pdf)[[DOI]](https://pubs.aip.org/aip/cha/article/28/6/063116/1059339/Sparse-identification-of-nonlinear-dynamics-for)
    * [Data-driven discovery of coordinates and governing equations](https://www.pnas.org/content/pnas/116/45/22445.full.pdf) [[DOI]](https://www.pnas.org/doi/10.1073/pnas.1906995116) [![#c5f015](https://via.placeholder.com/15/c5f015/000000?text=+)`code`](https://github.com/kpchamp/SindyAutoencoders) (SINDY_AE)
    
???+ note "Non-linear approaches"
    <div class="meta_for_parser tablespecs"
    style="font-size: 1pt;visibility:hidden" markdown>
    ###  Non-linear approach
    </div>
    
    * [AI Feynman: a Physics-Inspired Method for Symbolic Regression](https://arxiv.org/pdf/1905.11481.pdf) [[DOI]](https://www.science.org/doi/10.1126/sciadv.aay2631) [![#c5f015](https://via.placeholder.com/15/c5f015/000000?text=+)`code`](https://github.com/SJ001/AI-Feynman) (AIFeynman)
    * [Integration of Neural Network-Based Symbolic Regression in Deep Learning for Scientific Discovery](https://arxiv.org/pdf/1912.04825.pdf)
    * [Symbolic regression for scientific discovery: an application to wind speed forecasting](https://arxiv.org/pdf/2102.10570.pdf)
    * [Relational inductive biases, deep learning, and graph networks](https://arxiv.org/pdf/1806.01261.pdf)
    * [Extrapolation and learning equations](https://arxiv.org/pdf/1610.02995.pdf) (EQL)
    * [Learning Equations for Extrapolation and Control](http://proceedings.mlr.press/v80/sahoo18a/sahoo18a.pdf)(EQL_division)

## Expression tree-based SR

???+ note "Genetic programming"
    <div class="meta_for_parser tablespecs"
    style="font-size: 1pt;visibility:hidden" markdown>
    ###  Genetic programming
    </div>

       * [Eurequa](https://link.springer.com/content/pdf/10.1007/s10710-010-9124-z.pdf)
       * [PySR: High-Performance Symbolic Regression in Python and Julia](https://github.com/MilesCranmer/pysr)
       * Genetic programming as a means for programming computers by natural selection [[DOI]](https://link.springer.com/article/10.1007/BF00175355)
       * Order of Nonlinearity as a Complexity Measure for Models Generated by Symbolic Regression via Pareto Genetic Programming [[DOI]](https://ieeexplore.ieee.org/document/4632147)
       * Improving Symbolic Regression with Interval Arithmetic and Linear Scaling [[DOI]](https://link.springer.com/chapter/10.1007/3-540-36599-0_7)
       * Accuracy in Symbolic Regression [[DOI]](https://link.springer.com/chapter/10.1007/978-1-4614-1770-5_8)
       * Semantically-based crossover in genetic programming: application to real-valued symbolic regression [[DOI]](https://link.springer.com/article/10.1007/s10710-010-9121-2)

???+ note "Reinforcement learning"
    <div class="meta_for_parser tablespecs"
    style="font-size: 1pt;visibility:hidden" markdown>
    ###  Reinforcement learning
    </div>

    * [Deep symbolic regression: Recovering mathematical expressions from data via risk-seeking policy gradients](https://arxiv.org/abs/1912.04871) [[DOI]](https://openreview.net/forum?id=m5Qsh0kBQG) [![#c5f015](https://via.placeholder.com/15/c5f015/000000?text=+)`code`](https://github.com/brendenpetersen/deep-symbolic-optimization)(DSR)
    * [Symbolic Regression via Neural-Guided Genetic Programming Population Seeding](https://arxiv.org/abs/2111.00053) [[DOI]](https://proceedings.neurips.cc/paper/2021/hash/d073bb8d0c47f317dd39de9c9f004e9d-Abstract.html)[![#c5f015](https://via.placeholder.com/15/c5f015/000000?text=+)`code`](https://github.com/brendenpetersen/deep-symbolic-optimization) (DSR)
    * [Physical Symbolic Optimization](https://arxiv.org/pdf/2303.03192.pdf) [![#c5f015](https://via.placeholder.com/15/c5f015/000000?text=+)`code`](https://github.com/WassimTenachi/PhySO/tree/main) ($\phi$-SO)
    
???+ note "Transformer neural network"
    <div class="meta_for_parser tablespecs"
    style="font-size: 1pt;visibility:hidden" markdown>
    ###  Transformer neural network
    </div>

    * [End-to-end symbolic regression with transformers](https://arxiv.org/abs/2204.10532) [![#c5f015](https://via.placeholder.com/15/c5f015/000000?text=+)`code`](https://github.com/facebookresearch/symbolicregression)
    * [Neural Symbolic Regression that Scales](https://arxiv.org/abs/2106.06427) [![#c5f015](https://via.placeholder.com/15/c5f015/000000?text=+)`code`](https://github.com/SymposiumOrganization/NeuralSymbolicRegressionThatScales) (NeSymReS)
    * [A Generative Transformer Model for Symbolic Regression](https://arxiv.org/pdf/2106.14131.pdf) [![#c5f015](https://via.placeholder.com/15/c5f015/000000?text=+)`code`](https://github.com/mojivalipour/symbolicgpt) (SymbolicGPT)
    * [SYMBA: SYMBOLIC COMPUTATION OF SQUARED AMPLITUDES IN HIGH ENERGY PHYSICS WITH MACHINE LEARNING](https://arxiv.org/pdf/2206.08901.pdf) [![#c5f015](https://via.placeholder.com/15/c5f015/000000?text=+)`code`](https://github.com/ML4SCI/SYMBAHEP) (SYMBA)

## Other SR approaches

???+ note "Physics-inspired"
    <div class="meta_for_parser tablespecs"
    style="font-size: 1pt;visibility:hidden" markdown>
    ###  Physics-inspired
    </div>

    * [AI Feynman: a Physics-Inspired Method for Symbolic Regression](https://arxiv.org/pdf/1905.11481.pdf) [[DOI]](https://www.science.org/doi/10.1126/sciadv.aay2631) [![#c5f015](https://via.placeholder.com/15/c5f015/000000?text=+)`code`](https://github.com/SJ001/AI-Feynman)
    * [Physical Symbolic Optimization](https://arxiv.org/pdf/2303.03192.pdf) [![#c5f015](https://via.placeholder.com/15/c5f015/000000?text=+)`code`](https://github.com/WassimTenachi/PhySO/tree/main) ($\phi$-SO)

???+ note "Mathematics-inspired"
    <div class="meta_for_parser tablespecs"
    style="font-size: 1pt;visibility:hidden" markdown>
    ###  Mathematics-inspired
    </div>

    * [Demystifying Black-box Models with Symbolic Metamodels](https://www.vanderschaar-lab.com/papers/NIPS2019_DBM.pdf) [[DOI]](https://papers.nips.cc/paper_files/paper/2019/hash/567b8f5f423af15818a068235807edc0-Abstract.html) [![#c5f015](https://via.placeholder.com/15/c5f015/000000?text=+)`code`](https://github.com/vanderschaarlab/mlforhealthlabpub/tree/main/alg/symbolic_metamodeling)

???+ note "Computational approach"
    <div class="meta_for_parser tablespecs"
    style="font-size: 1pt;visibility:hidden" markdown>
    ###  Computational approach
    </div>

    * [Distilling Free-Form Natural Laws from Experimental Data](https://www.science.org/doi/10.1126/science.1165893)
