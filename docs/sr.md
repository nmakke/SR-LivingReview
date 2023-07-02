---
  hide:
    - navigation
---

# SR Problem definition

Given a data set **$\mathcal{D} =(\mathbf{x}_i,y_i)_{i=1}^{n}$**, SR aims to learn the function **$f(\mathbf{x})$** such that $y_i = f(\mathbf{x}_i)$ for all data points.

Three components are required to solve the SR problem:

  * a set of allowable mathematical operators (algebraic operators, analytical functions, constants, and state variables) for function composition commonly called  *library*, e.g., $L = \{x,~\mathrm{add,~mul,~div,~sqrt,~pow,~\cos,~etc.}\}$
  * a *loss function* $l(f) = \sum_i l(f(x_i),y_i))$ <!--such as the squared difference $|f(x) - y|^2$-->
  * an optimization problem to search for the optimal solution ($f^{*}$) over the space of mathematical expressions $\mathcal{F}$ as follows: 

   $$f^{*} = \mathrm{argmin}_{f \in\mathcal{F}} l(f(\mathbf{x}))$$
