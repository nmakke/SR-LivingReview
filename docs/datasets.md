---
hide:
  - navigation
---

Data sets are categorized into two main groups:

**Synthetic data**  for which the analytical form of the underlying model is known and used to generate data points. <br>
Example: $f(x) = 2x^2 + \cos(x) \rightarrow \mathcal{D}=\{x_i,f(x_i)\}_{i=1}^{n}$ *for* $x \in [0,1]$ <br>

**Real-world data** for which the underlying model is unknown.<br>

| <div style="width:100px">Category</div> | <div style="width:100px">Underlying model</div> | <div style="width:100px">Benchmark name</div> | <div style="width:100px">Reference</div> | <div style="width:100px">problems</div> | <div style="width:100px">year</div> |
| -------- | ------- | ------- | ------- | ----- | ----- | 
| Physics | Ordinary differential equations <br> Physics equations (classical mechanics, electromagnetism, <br> quantum mechanics, gravity, nuclear physics, etc. )| Strogatz <br> AIFeynman | [Strogatz repositery](https://williamlacava.com/ode-strogatz/) <br> [Feynman Database](https://space.mit.edu/home/tegmark/aifeynman.html) | 10 <br> 120 | 2011 <br> 2019 |
| <br> <br> <br> Mathematics | <br> <br> <br> monomials, polynomials, <br> trigonometric, exponential, etc.  | Koza <br> Keijer <br> Vladislavleva <br> Nguyen <br> Korns <br> R <br> Jin <br> Livermore | Koza <br> [Keijer](https://link.springer.com/chapter/10.1007/3-540-36599-0_7) <br> [Vladislavleva *et al.*](https://dl.acm.org/doi/10.1109/TEVC.2008.926486) <br> [Uy *et al.*](https://link.springer.com/article/10.1007/s10710-010-9121-2) <br> [Korns](https://link.springer.com/chapter/10.1007/978-1-4614-1770-5_8) <br> [Krawiec *et al.*](https://dl.acm.org/doi/10.1145/2463372.2463483) <br> [Jin *et al.*](https://idea.edu.cn/person/guojian/assets/papers/BSR-2020.pdf) <br> [Petersen *et al.*](https://arxiv.org/abs/1912.04871) | 3 <br> 15 <br> 8 <br> 12 <br> 15 <br> 3 <br> 6 <br> 22 | 1994 <br> 2003 <br> 2009 <br> 2011 <br> 2011 <br> 2013 <br> 2019 <br> 2021 | 
| Real-world | - | Penn Machine Learning <br> Benchmarks (PMLB) | [PMLB directory](https://epistasislab.github.io/pmlb/) | 122 | -|
