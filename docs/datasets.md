---
hide:
  - navigation
  - toc
---

Data sets ($\mathcal{D}$) are categorized into two main groups:

**Synthetic data**  for which the analytical form of the underlying model is known and used to generate data points. <br>
Example: $f(x) = 2x^2 + \cos(x)$<br>
For $x \in [0,1] \rightarrow \mathcal{D}=(x_i,f(x_i))_{i=1}^{n}$. <br>

**Real-world data** for which the underlying model is unknown.<br>

| Category | Underlying model   | Reference | Number of problems | year |
| -------- | ------- | ------- | ------- | ----- 
| Physics | Ordinary differential equations <br> Physics equations (gravity, electromagnetic nuclear, etc. )| [Strogatz repositery](https://williamlacava.com/ode-strogatz/) <br> [Feynman Database](https://space.mit.edu/home/tegmark/aifeynman.html) | 10 <br> 120 | 2011 <br> 2019 |
| <br> <br> <br> Mathematics | <br> <br> <br> monomials, polynomials, <br> trigonometric, exponential, etc.  | Koza <br> Keijer <br> Vladislavleva <br> Nguyen <br> Korns <br> R <br> Jin <br> [Livermore](https://arxiv.org/abs/1912.04871) | 3 <br> 15 <br> 8 <br> 12 <br> 15 <br> 3 <br> 6 <br> 22 | 1994 <br> 2003 <br> 2009 <br> 2011 <br> 2011 <br> 2013 <br> 2019 <br> 2021 |
| Real-world | Penn Machine Learning Benchmarks (PMLB) | [Ref](https://epistasislab.github.io/pmlb/) | 122 | -|
