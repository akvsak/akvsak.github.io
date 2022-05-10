---
title: "Latex testing"
category: tech
tags: 
 - general
 - latex
mathjax: true
--- 




This 100em is 
<img src="https://render.githubusercontent.com/render/math?math=e^{i \pi} = -1" width="100em" height=auto /> <br/>
This 90em is 
<img src="https://render.githubusercontent.com/render/math?math=e^{i \pi} = -1" width="90em" height=auto /> <br/>
This 80em is 
<img src="https://render.githubusercontent.com/render/math?math=e^{i \pi} = -1" width="80em" height=auto /> <br/>
This 70em is 
<img src="https://render.githubusercontent.com/render/math?math=e^{i \pi} = -1" width="70em" height=auto /> <br/>

$$
\begin{aligned}
  & \phi(x,y) = \phi \left(\sum_{i=1}^n x_ie_i, \sum_{j=1}^n y_je_j \right)
  = \sum_{i=1}^n \sum_{j=1}^n x_i y_j \phi(e_i, e_j) = \\
  & (x_1, \ldots, x_n) \left( \begin{array}{ccc}
      \phi(e_1, e_1) & \cdots & \phi(e_1, e_n) \\
      \vdots & \ddots & \vdots \\
      \phi(e_n, e_1) & \cdots & \phi(e_n, e_n)
    \end{array} \right)
  \left( \begin{array}{c}
      y_1 \\
      \vdots \\
      y_n
    \end{array} \right)
\end{aligned}
$$

This is the end of the test1.

The following is a math block:

$$ 5 + 5 $$

But next comes a paragraph with an inline math statement:

\$$ 5 + 5 $$

End of another test2.

$$ x_t $$ and $$\theta_t$$

$$\sum_{x_i < x_k} w_i < \frac{1}{2}$$

and

$$\sum_{x_i > x_k} w_i \le \frac{1}{2}.$$

### Logistic regression functions

I use the naming conventions of the Ng course. The logistic regression model is such that we want the hypothesis to be within the bounds 0 and 1.

$$ 0 \leq h_{\theta}(x) \leq 1 $$

If $$ h_{\theta}(x) = g(\theta^Tx) $$ and $$ g(z) = \frac{1}{1 + exp(-z)}\ $$ then

$$ h_{\theta}(x) = \frac{1}{1 + exp(-\theta^Tx)} $$

The objective will be to determine the parameters $$ \theta $$.

To do this, we will minimize the logistic regression cost function

$$ J(\theta) = \frac{1}{m} \sum_{i=1}^{m}[-y^{(i)}\log(h_{\theta}(x^{(i)}))-(1-y^{(i)})\log(1-h_{\theta}(x^{(i)}))] $$

The gradient equation is $$ \frac{\partial J(\theta)}{\partial \theta_{j}} = \frac{1}{m} \sum_{i=1}^{m}(h_{\theta}(x^{(i)}))-y^{(i)})x^{(i)}_{j} $$

### Determine the decision boundary linear equation.

From the lectures: $$ h_{\theta}(x) = g(\theta^Tx) \geq 0.5 $$ when $$ \theta^Tx \geq 0 $$.

In the case of two features:

$$ h_{\theta}(x) = g(\theta_{0} + \theta_{1}x_{1} + \theta_{2}x_{2}) $$

Therefore: $$ \theta_{0} + \theta_{1}x_{1} + \theta_{2}x_{2} \geq 0 $$

We can re-arrange to solve for the linear equation: $$ x_{2} = \frac{-\theta_{1}x_{1} - \theta_{0}}{\theta_{2}}\ $$

### The logistic regression cost function with L2 regularization as taught in the ML course is

$$ J(\theta) = \frac{1}{m} \sum_{i=1}^{m}[-y^{(i)}\log(h_{\theta}(x^{(i)}))-(1-y^{(i)})\log(1-h_{\theta}(x^{(i)}))] + \frac{\lambda}{2m}\sum_{j=1}^{n}\theta^2_{j} $$

[Home](/) or [random post](/random)