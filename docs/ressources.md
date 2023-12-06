---
hide:
  - navigation
  - toc
---

This directory includes open source codes of SR methods and useful online resources.

???+ note "Open source codes"
    <div class="meta_for_parser tablespecs"
    style="font-size: 1pt;visibility:hidden" markdown>
    ###  Genetic programming
    </div>

      For method category, we use: EA=EVOLUTIONARY ALGORITHM (E.G., GP), DL=DEEP LEARNING, MIX=COMBINATION OF MULTIPLE CLASSES.
    
      | <div style="width:100px">Method</div> | <div style="width:90px">Category</div> | <div style="width:90px">Code</div> |  <div style="width:100px">Implementation</div> | <div style="width:90px">Year</div> |<div style="width:400px">Brief description</div> |
      | ---- | ------- | --- | --- | --- | --- |
      | SINDy_AE | Mix | [URL](https://github.com/kpchamp/SindyAutoencoders) | Python | 2019 | Formulates the SR problem as a system of linear equations built using the set of allowable operators and learns the coefficients of candidate functions using a deep autoencoder (AE) network.  This is an extendable version of the [SINDy](https://www.pnas.org/doi/epdf/10.1073/pnas.1517384113) that learns a coordinate transformation of a reduced space where the dynamics are sparsely represented. |
      | EQL$\div$ | DL (NN) | [URL](https://github.com/martius-lab/EQL) | Python | 2018 | A fully differentiable shallow neural network with non-linear activation functions (e.g., algebraic operators and analytical functions) instead of traditional ones (e.g., sigmoid, relu, softmax, etc.). This is an extendable version of the original [EQL](https://arxiv.org/abs/1610.02995) that includes the division among candidate activation functions.|
      | Eureqa | EA | [URL]() | | 2009 | It is a closed-source code that uses genetic programming to learn mathematical expressions. It was developed in 2009 and popularized as the scientific discovery machinery but dismisses its mission.|
      | PySR | EA | [URL](https://github.com/MilesCranmer/PySR)  | Pyhton/Julia | 2023 | Fast and parallelized symbolic regression in Python/Julia based on evolutionary algorithms (EA). Treats mathematical expressions as trees and uses tournament selection.  |
      | PSTree | EA | [URL](https://github.com/hengzhe-zhang/PS-Tree) | Python | 2022 | Consists of an automated piece-wise non-linear regression method based on decision tree and genetic programming techniques. |
      | gplearn | EA | [URL](https://gplearn.readthedocs.io/en/stable/intro.html#transformer) | Pyhton | - | Koza-style symbolic regression in python. It includes a **SymbolicRegressor**, **SymbolicClassifier**, and **SymbolicTransformer** for different tasks. |
      | Operon | EA | [URL](https://github.com/heal-research/operon) | C++ | 2020 | GP-based | 
      | DSR | Mix | [URL](https://github.com/brendenpetersen/deep-symbolic-optimization) | Pyhton  | 2021 | Consists of a generative RNN model of symbolic expressions trained using reinforcement learning. |
      | NeSymReS | DL (TNN) | [URL](https://github.com/SymposiumOrganization/NeuralSymbolicRegressionThatScales/tree/main) | Pyhton | 2021 | A pre-trained transformer that predicts SR models directly from the data. Predicted models are then fine-tuned and the best is returned.|
      | E2ET | DL (TNN) | [URL](https://github.com/pakamienny/e2e_transformer/tree/main) | Pyhton | 2022 | A pre-trained transformer that predicts SR models directly from the data. Predicted models are then fine-tuned and the best is returned. |
      | $\phi$-SO | DL (RL) | [URL](https://github.com/WassimTenachi/PhySO/tree/main) | Python | 2023 | Consists of a generative RNN model of symbolic expressions trained using reinforcement learning (DSR method) while fully leveraging physical units (of measurement) constraints in the search space at two levels, external (*in situ physical units constraints*) and internal (during RNN training).|
      | AIFeynman | Mix | [URL](https://github.com/SJ001/AI-Feynman) | Pyhton  | 2019 | A physics-informed SR method that uses NN to learn symmetries in data (translational, rotational, vibrational) to simply the global SR problem into simpler SR subproblems. |
      | SRBench | - | [URL](https://github.com/cavalab/srbench) | Python | 2021 | A benchmark consisting of 14 SR methods (among which DSR, BSR, AIFeynman, and FFX are non-EA-based methods). |
      | uDSR | Mix | [URL](https://github.com/brendenpetersen/deep-symbolic-optimization) | Python | 2022 | A unified SR framework that includes AIFeynamn, DSR, linear model (LM), large-scale pre-training (LSPT), and GP altogether. This method takes the strength of each class of symbolic regression. |
