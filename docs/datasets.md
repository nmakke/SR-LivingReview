---
hide:
  - navigation
  - toc
---

Data sets, used for model training and testing, are categorized into two main groups:

**Synthetic data**  for which the analytical form of the underlying model is known and used to generate data points. <br>
This category includes equations from physical sciences, i.e., have physical interpretation and fulfill dimensional <br> 
requirements (units of both sides of an equation match), and pure mathematical expressions.   
*Examples*:<br>
$f(x) = 2x^2 + \cos(x) \rightarrow \mathcal{D}=\{x_i,f(x_i)\}_{i=1}^{n}$ *for* $x \in [0,1]$ <br>
$f(x) = Gm_1m_2/r^2$ where $[m_1]=[m_2]=$ Kilograms, $[r]=$ meter and $G$ is gravitational constant.<br>

**Real-world data** for which the underlying model is unknown.<br>
This category includes any type of data such as climate, economics, medical, etc.

| <div style="width:100px">Category</div> | <div style="width:120px">Underlying model</div> | <div style="width:120px">Benchmark name</div> | <div style="width:100px">Reference</div> | <div style="width:100px">problems</div> | <div style="width:100px">year</div> |
| -------- | ------- | ------- | ------- | ----- | ----- | 
| Physics | Ordinary differential equations <br> Physics equations (classical mechanics, electromagnetism, <br> quantum mechanics, gravity, nuclear physics, etc. )| Strogatz <br> AIFeynman | [Strogatz repositery](https://williamlacava.com/ode-strogatz/) <br> [Feynman Database](https://space.mit.edu/home/tegmark/aifeynman.html) | 10 <br> 120 | 2011 <br> 2019 |
| <br> <br> <br> Mathematics | <br> <br> <br> monomials, polynomials, <br> trigonometric, exponential, etc.  | Koza <br> Keijer <br> Vladislavleva <br> Nguyen <br> Korns <br> R <br> Jin <br> Livermore | Koza <br> [Keijer M.](https://link.springer.com/chapter/10.1007/3-540-36599-0_7) <br> [Vladislavleva E.J. *et al.*](https://dl.acm.org/doi/10.1109/TEVC.2008.926486) <br> [Uy N.Q. *et al.*](https://link.springer.com/article/10.1007/s10710-010-9121-2) <br> [Korns M.F. ](https://link.springer.com/chapter/10.1007/978-1-4614-1770-5_8) <br> [Krawiec K., Pawlak T.](https://dl.acm.org/doi/10.1145/2463372.2463483) <br> [Jin Y. *et al.*](https://idea.edu.cn/person/guojian/assets/papers/BSR-2020.pdf) <br> [Petersen B. K. *et al.*](https://arxiv.org/abs/1912.04871) | 3 <br> 15 <br> 8 <br> 12 <br> 15 <br> 3 <br> 6 <br> 22 | 1994 <br> 2003 <br> 2009 <br> 2011 <br> 2011 <br> 2013 <br> 2019 <br> 2021 | 
| Real-world | Unkonwn underlying model | Penn Machine Learning <br> Benchmarks (PMLB) | [PMLB directory](https://epistasislab.github.io/pmlb/) | 122 | -|

| <div style="width:120px">Dataset</div> | <div style="width:100px">Expression</div> | <div style="width:100px">Variables</div> | <div style="width:140px">Training data range</div> | 
| -------- | ------- | ------- | ------- |
| Koza-1 | $x^4 + x^3 + x^2 + x$ | 1 |  U[-1, 1, 20] |
| Koza-2 | $x^5 - 2x^3 + x$	  | 1 | U[-1, 1, 20] |
| Koza-3 | $x^6 - 2x^4 + x^2$    | 1 | U[-1, 1, 20] |
| Keijzer-1 | $0.3 x \sin(2\pi x)$ | 1 | E[-1, 1, 0.1] |
| Keijzer-2 | $0.3 x \sin(2\pi x)$ | 1 | E[-2, 2, 0.1] |
| Keijzer-3 | $0.3 x \sin(2\pi x)$ | 1 | E[-3, 3, 0.1] |
| Keijzer-4 | $x^3e^{-x} \cos(x)\sin(x)(\sin^2(x)\cos(x)-1)$ | 1 | E[0, 10, 0.05] |
| Keijzer-5 | $30xz/(x-10)y^2$ | 3 | $x,z:$ U[-1,1,1000] <br> $y:$ U[1,2,1000]|
| Keijzer-6 | $\sum_1^{x}i$ | 1 | E[1, 50, 1] |
| Keijzer-7 | $\log x$ | 1 | E[1, 100, 1] |
| Keijzer-8 | $\sqrt{x}$ | 1 | E[0, 100, 1] |
| Keijzer-9 | $\mathrm{arcsinh}(x)=\log(x +\sqrt{x^2 + 1})$ | 1 | E[0, 100, 1] |
| Keijzer-10 | $x^y$ | 2 | U[0, 1, 100] |
| Keijzer-11 | $xy + \sin((x-1)(y-1))$ | 2 | U[-3, 3, 20] |
| Keijzer-12 | $x^4-x^3 +y^2/2 - y$ | 2 | U[-3, 3, 20] |
| Keijzer-13 | $6\sin(x)\cos(y)$ | 2 | U[-3, 3, 20] |
| Keijzer-14 | $8/(2+x^2+y^2)$ | 2 |  U[-3, 3, 20] |
| Keijzer-15 | $x^3/5 +y^3/2-y-x$ | 2 | U[-3, 3, 20] |
| Vladislavleva-1 | $\frac{e^{-(x-1)^2}}{1.2+(y-2.5)^2}$ | 1 | U[0.3, 4, 100] |
| Vladislavleva-2 | $e^{-x}x^3(\cos x\sin x)(\cos x \sin^2 x-1)$ | 2 | E[0.5, 10, 0.1] |
| Vladislavleva-3 | $e^{-x}x^3(\cos x\sin x)(\cos x\sin^2 x-1)(y-5)$ | 2 | $x:$E[0.05,10,0.1] <br> $y:$E[0.05,10.05,2]|
| Vladislavleva-4 | $\frac{10}{5+\sum_{i=1}^{5}(x_i-3)^2}$ | 5 | U[0.05, 6.05, 1024] |
| Vladislavleva-5 | $30(x-1)\frac{(z-1)}{y^2(x-10)}$ | 3 | $x:$ U[0.05, 2, 300] <br>  $y:$ U[1, 2, 300] <br> $z:$ U[0.05, 2, 300] |
| Vladislavleva-6 | $6\sin(x)\cos(y)$ | 2 | U[0.1, 5.9, 30] |
| Vladislavleva-7 | $(x-3)(y-3) + 2\sin((x-4)(y-4))$ | 2 | U[0.05, 6.05, 300] |
| Vladislavleva-8 | $\frac{(x-3)^4+(y-3)^3-(y-3)}{(y-2)^4+10}$ | 2 |  U[0.05, 6.05, 50]| 
| Nguyen-1 | $x^3+ x^2 + x$ | 1 | U(-1,1,20)|
| Nguyen-2 | $x^4 + x^3+ x^2 + x$| 1 |  U(-1,1,20)|
| Nguyen-3 | $x^5 + x^4 + x^3+ x^2 + x$| 1 | U(-1,1,20)|
| Nguyen-4 | $x^6 + x^5 + x^4 + x^3+ x^2 + x$ | 1 | U(-1,1,20)|
| Nguyen-5 | $\sin(x^2)\cos(x) -1$ | 1 | U(-1,1,20)|
| Nguyen-6 | $\sin(x) + \sin(x+x^2)$ | 1 | U(-1,1,20)|
| Nguyen-7 | $\log(x+1) + \log(x^2+1)$ | 1 | U(0,2,20)|
| Nguyen-8 | $\sqrt{x}$ | 1 | U(0,4,20)|
| Nguyen-9 | $\sin(x) + \sin(y^2)$ | 2 | U(-1,1,100)|
| Nguyen-10 | $2\sin(x)\cos(y)$ | 2 | U(-1,1,100)|
| Nguyen-11 | $x^{y}$ |  2|
| Nguyen-12 | $x^4 - x^3 + \frac{1}{2}y^2 - y$| 2|
| Korns-1 | $1.57 + (24.3 v)$ | 1 | U[-50, 50, 10000] |
| Korns-2 | $0.23 + 14.2\frac{v+y}{3\omega}$ | 3 | U[-50, 50, 10000] |
| Korns-3 | $-5.41 + 4.9\frac{v-x+y/w}{3\omega}$ | 4 | U[-50, 50, 10000]|
| Korns-4 | $-2.3 + 0.13\sin(z)$ | 1 | U[-50, 50, 10000] |
| Korns-5 | $3 + 2.13 \ln(\omega)$ | 1 | U[-50, 50, 10000] |
| Korns-6 | $1.3 + 0.13 \sqrt{x}$ | 1 |  U[-50, 50, 10000] |
| Korns-7 | $213.80940889(1- e^{-0.54723748542 x})$ | 1 | U[-50, 50, 10000] |
| Korns-8 | $6.87 + 11 \sqrt{7.23~x~v~\omega}$ | 3 |  U[-50, 50, 10000] |
| Korns-9 | $\frac{\sqrt{x}}{\ln(y)}\frac{e^z}{v^2}$ | 4 |  U[-50, 50, 10000] |
| Korns-10 | $0.81 + 24.3\frac{2 y+3 z^2}{4v^3+5\omega^4}$ | 4 | U[-50, 50, 10000] |
| Korns-11 | $6.87 + 11\cos(7.23 x^3)$ | 1 |  U[-50, 50, 10000] |
| Korns-12 | $2-2.1\cos(9.8 x)\sin(1.3\omega)$ | 2 | U[-50, 50, 10000] |
| Korns-13 | $32-3\frac{\tan(x)}{\tan(y)}\frac{\tan(z)}{\tan(v)}$ | 4 | U[-50, 50, 10000]|
| Korns-14 | $22-4.2(\cos(x)-\tan(y))\frac{\tanh(z)}{\sin(v)}$ | 4 | U[-50, 50, 10000] |
| Korns-15 | $12-6\frac{\tan(x)}{e^y}(\ln(z)-\tan(v))$ | 4 |  U[-50, 50, 10000]|
| R1 | $(x+1)^3/(x^2-x+1)$ | 1 | E[-1,1,20]|
| R2 | $(x^5-3x^3+1)/(x^2+1)$ | 1 | E[-1,1,20]|
| R3 | $(x^6+x^5)/(x^4+x^3+x^2+x+1)$ | 1 | E[-1,1,20]|
| Jin-1 | $2.5x^4 -1.3x^3 +0.5y^2 -1.7y$  | 2 | U(-3,3,100)|
| Jin-2 | $ 8.0x^2 + 8.0y^3 -15.0$ | 2 | U(-3,3,100)|
| Jin-3 | $ 0.2x^3 +1.5y^3 -1.2y -0.5x$ | 2 | U(-3,3,100)|
| Jin-4 | $ 1.5\exp(x) + 5.0\cos(y)$ | 2 | U(-3,3,100)|
| Jin-5 | $ 6.0\sin(x)\cos(y)$ | 2 | U(-3,3,100)|
| Jin-6 | $ 1.35xy + 5.5\sin((x-1.0)(y-1.0)$ | 2 | U(-3,3,100)|
| Livermore-1 | $1/3 + x + \sin(x^2)$ | 1 | U[-10,10,1000] |
| Livermore-2 | $\sin(x^2)\cos(x) - 2$ | 1 | U[-1,1,20]|
| Livermore-3 | $\sin(x^3)\cos(x^2) -1$ | 1 | U[-1,1,20]|
| Livermore-4 | $\log(x+1) + \log(x^2+1)+\log(x)$ | 1 | U[0,2,20]|
| Livermore-5 | $x^4 - x^3 + x^2 -y$ | 2 | U[0,1,20]|
| Livermore-6 | $4x^4 + 3x^3 + 2x^2 + x$ | 1 | U[-1,1,20]|
| Livermore-7 | $\sinh(x)$ | 1 | U[-1,1,20]|
| Livermore-8 | $\cosh(x)$ | 1 | U[-1,1,20]|
| Livermore-9 | $x^9 +x^8+x^7+x^6+x^5+x^4+x^3+x^2+x$ | 1 | U[-1,1,20]|
| Livermore-10 | $6\sin(x)\cos(y)$ | 2 | U[0,1,20]|
| Livermore-11 | $x^2y^2/(x+y)$ | 2 | U[-1,1,50]|
| Livermore-12 | $x^5/y^3$ | 2 | U[-1,1,50]|
| Livermore-13 | $x^{1/3}$ | 1 | U[0,4,20]|
| Livermore-14 | $x^3+x^2+x+\sin(x)+\sin(x^2)$ | 1 | U[-1,1,20]|
| Livermore-15 | $x^{1/5}$ | 1 | U[0,4,20]|
| Livermore-16 | $x^{2/5}$ | 1 | U[0,4,20]|
| Livermore-17 | $4\sin(x)\cos(y)$ | 2 | U[0,1,20]|
| Livermore-18 | $\sin(x^2)\cos(x) - 5$ | 1 | U[-1,1,20]|
| Livermore-19 | $x^5+x^4+x^2+x$ | 1 | U[-1,1,20]|
| Livermore-20 | $\exp(-x^2)$ | 1 | U[-1,1,20]|
| Livermore-21 | $x^8+x^7+x^6+x^5+x^4+x^3+x^2+x$ | 1 | U[-1,1,20]|
| Livermore-22 | $\exp(-0.5x^2)$ | 1 | U[-1,1,20]|
