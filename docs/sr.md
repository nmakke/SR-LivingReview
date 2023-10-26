---
  hide:
    - navigation
---

# Symbolic regression

SR is the task of learning an interpretable model using AI-based techniques. 

Note that AI-based models are often uninterpretable, meaning that the learned model is a formula that is either too complicated for any human to understand or proprietary, i.e., it is very hard to understand its inner workings and only its developers know the secrets of its formula. 
SR folds in the category of interpretable AI because it aims to learn clear, transparent, and analytical expressions of underlying models. 

# SR Problem definition

Given a data set **$\mathcal{D} =\{\mathbf{x}_i,y_i\}_{i=1}^{n}$** where **$\mathbf{x}_i \in \mathbb{R}^{d}$**, the objective is to learn the function **$f(\mathbf{x})$** such that $y_i = f(\mathbf{x}_i) ~~\forall ~~i$.

Three components are required to solve the SR problem:

  * a set of allowable mathematical operators, among which are algebraic operators $\{+, -, \times, \div \}$,  analytical functions $\{\cos,\sin,\tan,\exp,\log,\mathrm{pow},\mathrm{sqrt},\mathrm{etc}\}$), constants $c$, and state variables $x$ for function composition commonly called  ***library*** $L$
  * a ***loss function*** $l(f) = \sum_i l(f(x_i),y_i))$ <!--such as the squared difference $|f(x) - y|^2$-->
  * an optimization problem to search for the optimal solution ($f^{*}$) over the space of mathematical expressions $\mathcal{F}$ as follows:<be>
  $f^{*} = \mathrm{argmin}_{f \in\mathcal{F}} l(f(\mathbf{x}))$


# Challenges

- SR is an NP-hard problem  (Virgolin & Pissis 2022).
The number of mathematical expressions grows exponentially with the number of features.
Suppose the target analytic expression has a length of 35 symbols and that the library consists of 15 different variables or operations (e.g., x, +, −, ×, /,sin, log, ...) to choose from for each symbol.
A naive brute-force attempt to fit the dataset might then have to consider up to $15^{30]=1.9 10^{35}$ trial solutions, which is obviously very challenging.
The obvious conclusion one draws from these considerations is that symbolic regression requires one to develop highly efficient strategies to prune poor guesses.

- Discrete nature of its search space
The optimization problem in SR is defined over the space of mathematical expressions, which is discrete. 
<!--- SR has been introduced by Gerwin D., Langley P., and Falkenhainer B.C. in independent research works back in 1970 aiming to redisccover empirical laws.-->
<!--- At a later stage, SR was proposed by Koza as an evolutionary algorithm that represents mathematical expressions as unary-binary trees. -->
