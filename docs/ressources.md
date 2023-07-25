---
hide:
  - navigation
  - toc
---

This directory includes ready-to-use packages of symbolic regression and useful online ressources.

???+ note "Ready-to-use packages"
    <div class="meta_for_parser tablespecs"
    style="font-size: 1pt;visibility:hidden" markdown>
    ###  Genetic programming
    </div>
    
      | <div style="width:100px">Method</div> | <div style="width:90px">Category</div> | <div style="width:90px">Code</div> | <div style="width:90px">Year</div> |<div style="width:300px">Brief description</div> |
      | ---- | ------- | --- | --- | --- |
      | SINDy_AE | Mix | [URL](https://github.com/kpchamp/SindyAutoencoders) | 2019 | Formulates the SR problem as a system of linear equations built using the set of allowable operators and learns the coefficients of candidate functions using a deep autoencoder (AE) network.  This is an extendable version of the [SINDy](https://www.pnas.org/doi/epdf/10.1073/pnas.1517384113) that learns a coordinate transformation of a reduced space where the dynamics are sparsely represented. |
      | EQL$\div$ | DL (NN) | [URL](https://github.com/martius-lab/EQL) | 2018 | Consists of an end-to-end differentiable feed-forward neural network whose activation functions are algebraic operators and analytical functions instead of traditional activation functions (e.g., sigmoid, relu, softmax). This is an extendable version of the original [EQL](https://arxiv.org/abs/1610.02995) that includes the division operator as a candidate for the activation function.|
      | Eureqa | GP | [URL]() | xx | It is a closed-source code that uses genetic programming to learn mathematical expressions. It was developed in 2009 and popularized as the scientific discovery machinery but dismisses his mission.|
      | PySR | GP | [URL](https://github.com/MilesCranmer/PySR) | 2023 | Fast and parallelized symbolic regression in Python/Julia based on evolutionary algorithms (EA). Treats mathematical expressions as trees and use tournament selection.  |
      | gplearn | GP | [URL]() | xx | Koza-style symbolic regression in python.| |
      | DSR | RL | [URL](https://github.com/brendenpetersen/deep-symbolic-optimization) | 2021 | Consists of a generative RNN model of symbolic expressions trained using reinforcement learning. |
      | NeSymReS | DL (TNN) | [URL]() | 2021 | A pre-trained transformer that predicts SR models directly from the data. Predicted models are then fine-tuned and the best is returned.|
      | E2E | DL (TNN) | [URL]() | 2022 | A pre-trained transformer that predicts SR models directly from the data. Predicted models are then fine-tuned and the best is returned. |
      | $\phi$-SO | DL (RL) | [URL](https://github.com/WassimTenachi/PhySO/tree/main) | 2023 | Consists of a generative RNN model of symbolic expressions trained using reinforcement learning (DSR method) while fully leveraging physical units (of measurement) constraints in the search space.|
      | AIFeynman | Mix | [URL](https://github.com/SJ001/AI-Feynman) | 2019 | A physics-informed SR method that uses NN to learn symmetries in data (translational, rotational, vibrational) to simply the global SR problem into simpler SR subproblems. |
