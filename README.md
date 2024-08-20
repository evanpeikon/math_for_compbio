This repository contains a series of math tutorials for computational biology and bioinformatics. Upon completion, it will be broken into three sections: calculus, linear algebra, and ordinary differential equations. 

# 📚 Calculus 
## Techniques of Differentiation

### Fundamentals
- Differentiation is the process of finding derivatives. Differentiation is an operation that transforms a function $f$ into a new function $f'$. When the independent variable is $x$, the differentiation operation is denotes as $\frac{d}{dx}[ ]$, which can be read as the derivative with respect to $x$. According to the **power rule**, if $n$ is a posiitive integer, then... $\frac{d}{dx}[x^n] = nx^{n-1}$.
  - For example... $\frac{d}{dx}[x^5]= 5x^4$, $\frac{d}{dx}[2x^3]=6x^2$, and $\frac{d}{dx}[4x^1]=4$

- If $c$ is a constant and the function $f$ is differentiable at $x$, then so is $$cf$ and $(cf)'(x) = cf'(x)$. Thus, $\frac{d}{dx}[cf(x)]=c \frac{d}{dx}[f(x)]$
  - For example, $\frac{d}{dx}[x^8] = \frac{d}{dx}[4x^8] = 32x^7$ and $2\frac{d}{dx}[x^2] = \frac{d}{dx}[2x^2] = 4x$

### Addition and Subtraction
- If $f$ and $g$ are both differentiable at $x$, so is $f+g$. Thus, $\frac{d}{dx}[f(x)+g(x)]= \frac{d}{dx}[f(x)] + \frac{d}{dx}[g(x)]$.
  - For example, $\frac{d}{dx}[2x+x^3]= \frac{d}{dx}[2x] + \frac{d}{dx}[x^3] = 2 + 3x^2$
- Additionally, is $f$ and $g$ are both differentiable at $x$, so is $f-g$. Thus, $\frac{d}{dx}[f(x)-g(x)]= \frac{d}{dx}[f(x)] - \frac{d}{dx}[g(x)]$.
  - For example, $\frac{d}{dx}[3x-2x]= \frac{d}{dx}[3x] + \frac{d}{dx}[2] = 3-2 = 1$

 ### Multiplication and Division
- If $f$ and $g$ are both differentiable at $x$, so is the product of $f$ and $g$, $f⋅g$. According to the **product rule**, $\frac{d}{dx}[f(x)⋅g(x)] = f(x)\frac{d}{dx}[g(x)] + g(x)\frac{d}{dx}[f(x)]$.
  - For example, $\frac{d}{dx}[(4x^2-1)(7x^3+x)]= (4x^2-1)\frac{d}{dx}[7x^3+x] + (7x^3+x)\frac{d}{dx}[4x^2-1] = (4x^2-1)(21x^2+1) + (7x^3+x)(8x) = 140x^4 - 9x^2 -1$
- If f and g are differentiable at x and g(x)≠0, then $\frac{f}{g}$ is differentiable and $\frac{d}{dx} [\frac{f(x)}{g(x)}] = \frac{g(x)\frac{d}{dx}[f(x)] - f(x)\frac{d}{dx}[g(x)]}{[g(x]^2}$

## The Chain Rule
- Given the functions $f$ and $g$, we can find the composition, $f∘g$, which is expressed as $(f∘g)(x) = f(g(x))$. For example, if $f(x)=sinx$ and $g(x)=x^2-1$, $f(g(x))=sin(x^2-1)$.
- To solve these types of problems we introduce the variable $u=g(x)$, such that $f(g(x)) = f(u)$. Using the previous example, if $u=x^2-1$, then $f(u)=sin(u)$.
- Now, if we want the derivative of functions like $y=sin(x^2-1)$ we say that $\frac{dy}{dx} = \frac{dy}{du} ⋅ \frac{du}{dx} = \frac{d}{du}[ ] ⋅ \frac{d}{dx}[ ]$
  - For example, $\frac{dy}{dx} = \frac{dy}{du} ⋅ \frac{du}{dx} = \frac{d}{du}[sin(u)] ⋅ \frac{d}{dx}[x^2-1] = cos(u) ⋅ 2x = 2xcos(u)$. Now, since $u=x^2-1$, we can substitute in $u$ to get the final solution $2xcos(x^2-1)$. 
- Let's try another example... find $\frac{d}{dx} [4cos(x^3)]$. First, we say $y=4cos(x^3)$ and $u=x^3$, so $y=4cos(u)$. Now, to solve this we say $\frac{dy}{dx} = \frac{d}{du}[4cos(u)] ⋅ \frac{d}{dx}[x^3] = -4sin(u) ⋅ 3x^2 = -12x^2sin(u) = -12x^2sin(x^3)$

## Rolle's Theorem (Mean Value Theorem)
- Between any two points on a well-behaved curve $y=f(x)$ where the curve crosses the x-axis, there is atleast one point $b$ where the tangent to the curve is horizontal.
- Thus, if the function $f$ is differentiable between the points on the x-axis $(a,c)$ and is continous on the points $[a,c]$, then at atleast one point $b$... $f(b)' = \frac{f(c)-f(a)}{c-a}$
- Now, here's how we find $b$:
  1. First, find $f(a)$ and $f(c)$
  2. Next, find $f'(x)$, which is the derivative of $f(x)$
  3. Plug variables from 1 and 2 into the forumula $f(b)' = \frac{f(c)-f(a)}{c-a}$
  4. Solve for $b$ and select points that fall within [a,c]
- Let's try an example... let $f(x)=x^3+1$ and show it satifies the mean value theorem on [1,2]
  - $f(a) = 1^3+1=2$ and $f(c)=2^3+1=9$
  - Now, $f'(x)= \frac{d}{dx}[x^3+1] = 3x^2$
  - 3b^2 = \frac{9-2){2-1} = 7$
  - If $3b^2=7$, then $b^2=\frac{7}{3}$ and thus, $b= \sqrt{\frac{7}{3}}$ and $-\sqrt{\frac{7}{3}}$. However, only the first of those two solutions falls within the range [1,2], fulfiling the mean value theorem.
 
## Anti-Differentiation (Integration)
- Integration is the process of finding anti-derivatives. If $\frac{d}{dx}[F(x)]=f(x)$, then functions of the form $F(x)+c$ are anti-derivatives of $f(x)$. We denote this relationship as $\int f(x)dx = F(X)+c$.
  - For example, $\frac{x^3}{3}$,  $\frac{x^3}{3}+2$, and  $\frac{x^3}{3}-π$ are all anti-derivatives of the function $f(x)=x^2$ since $\frac{d}{dx}[\frac{x^3}{3}] = \frac{d}{dx}[\frac{x^3}{3}+2] = \frac{d}{dx}[\frac{x^3}{3}-π] = x^2$
- Furthermore, if we differentiate the anti-derivative of a function, $f(x)$, we get $f(x)$ back again... $\frac{d}{dx}[\int f(x)dx] = \frac{d}{dx}[F(x)] = f(x)$.
  - For example, $\frac{d}{dx}[\int 2x^2dx] = \frac{d}{dx}[\frac{2x^3}{3}] = \frac{6x^2}{3} = 2x^2$

## Integration by u-Substitution
- $u$-substitution can turn complex integration problems into simpler ones. If we want to evaluate a complex integral $\int h(x)dx$ we can say that $\int h(x)dx = \int f(g(x))g'(x)dx = \int[f(u)\frac{du}{dx}]dx = F(u)+c$ where $u=g(x)$ and $\frac{du}{dx} = g'(x)$.
- Now, to solve these problems follow these steps:
  1. Start with problem is $\int f(g(x))g'(x)dx$ form
  2. Make a choice for $u=g(x)$
  3. Make a choice for $\frac{du}{dx} = g'(x)$, then find $du$ which is $du= g'(x)dx$.
  4. Sub $u=g(x)$ and $du=g'(x)dx$ into the problem, such that it is in the form $\int f(u)du$
  5. Evaluate the resultant integral from step 4, then sub $g(x)$ back in for $u$
- Let's try an example... $\int (x^2+1)^{50} ⋅ 2xdx$
  - Now, we say $u=x^2+1$ and $\frac{du}{dx}=2x}, so $du=2xdx$
  - The after substitution, the resultant integral is $\int (u)^{50}⋅du$
  - After evaluating the integral we get $\frac{u^{51}}{51}+c$, then after substituting $g(x)$ back in we get $\frac{(x^2+1)^{51}}{51}+c$

## Definite Integrals
- If $f$ is continous on [a,b] and if $F$ is the anti-derivative of $f$ on [a,b], then $\int^{b}_{a} f(x)dx = F(x)]_a^b = F(b)-F(a)$
  - Evaluate $\int^{2}_{1} xdx$
    - $\int^{2}_{1}xdx = \frac{x^2}{2}]_1^2 = \frac{2^2}{2} - \frac{1^2}{2} = \frac{4}{2} - \frac{1}{2} = \frac{3}{2}$
- Properies of the definite integral...
  - If $a$ is in the domain of $f$, then $\int^{a}_{a} f(x)dx = 0$ because there is no area under th e curve $y=f(x)$ above the x-axis.
    - For example, $\int^{5}_{5} x^4dx = 0$

If $b<a$ and $f$ is integrable on $[a,b]$, then ...
$\int^{b}_{a} f(x)dx = - \int^{a}_{b} f(x)dx$

ex)
$\int^{0}_{4} xdx = - \int^{4}_{0} xdx = - \frac{x^2}{2}}_{0}_{4} = -8$
