This repository contains a series of math tutorials for computational biology and bioinformatics. 

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

### The Chain Rule
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
 
## Integration / Indefinite Integrals 
- Integration is the process of finding anti-derivatives. If $\frac{d}{dx}[F(x)]=f(x)$, then functions of the form $F(x)+c$ are anti-derivatives of $f(x)$. We denote this relationship as $\int f(x)dx = F(X)+c$.
  - For example, $\frac{x^3}{3}$,  $\frac{x^3}{3}+2$, and  $\frac{x^3}{3}-π$ are all anti-derivatives of the function $f(x)=x^2$ since $\frac{d}{dx}[\frac{x^3}{3}] = \frac{d}{dx}[\frac{x^3}{3}+2] = \frac{d}{dx}[\frac{x^3}{3}-π] = x^2$
- Furthermore, if we differentiate the anti-derivative of a function, $f(x)$, we get $f(x)$ back again... $\frac{d}{dx}[\int f(x)dx] = \frac{d}{dx}[F(x)] = f(x)$.
  - For example, $\frac{d}{dx}[\int 2x^2dx] = \frac{d}{dx}[\frac{2x^3}{3}] = \frac{6x^2}{3} = 2x^2$

### Integration by u-Substitution
- $u$-substitution can turn complex integration problems into simpler ones. If we want to evaluate a complex integral $\int h(x)dx$ we can say that $\int h(x)dx = \int f(g(x))g'(x)dx = \int[f(u)\frac{du}{dx}]dx = F(u)+c$ where $u=g(x)$ and $\frac{du}{dx} = g'(x)$.
- Now, to solve these problems follow these steps:
  1. Start with problem is $\int f(g(x))g'(x)dx$ form
  2. Make a choice for $u=g(x)$
  3. Make a choice for $\frac{du}{dx} = g'(x)$, then find $du$ which is $du= g'(x)dx$.
  4. Sub $u=g(x)$ and $du=g'(x)dx$ into the problem, such that it is in the form $\int f(u)du$
  5. Evaluate the resultant integral from step 4, then sub $g(x)$ back in for $u$
- Let's try an example... $\int (x^2+1)^{50} ⋅ 2xdx$
  - Now, we say $u=x^2+1$ and $\frac{du}{dx}=2x$, so $du=2xdx$
  - The after substitution, the resultant integral is $\int (u)^{50}⋅du$
  - After evaluating the integral we get $\frac{u^{51}}{51}+c$, then after substituting $g(x)$ back in we get $\frac{(x^2+1)^{51}}{51}+c$

### Techniques of Integration 
- Additional techniques of integration are as follows:
  1. $\int dx= x+c$
  2. $\int adx = ax+c$
  3. $\int x^r dx = \frac{x^{r+1}}{r+1} + c$, $r≠1$
  4. $\int \frac{1}{x} = ln|x|+c$
  5. $\int e^xdx = e^x+c$
  6. $\int a^xdx = \frac{a^x}{ln(a)} +c$
 
### Integration by Parts
- Integration by parts is a technique for evaluating integrals that do not fit basic formulas. The formula for integration by parts allows one ot reduce complex integration problems into easier ones and is defined as $\int f(x)g'(x)dx = f(x)g(x) - \int g(x)f'(x)dx$
- Here's how to solve the eqution above...
  1. Write the equation in $\int f(x)g'(x)dx$ form
  2. Identify $f(x)$, then say $f(x)=u$
  3. Calculate $f'(x)$, then say $f'(x)(dx) = du$
  4. Identify $g'(x)$ and say $g'(x)dx = dv$
  5. Now, calcualte $g(x)$ and say $g(x)=v$
  6. Write $\int (u)(dv) = (u)(v) - \int (v)(du)$ or for definite integrals write $\int^{b}_{a} (u)(dv) = (u)(v)]_b^a - \int^{b}_a (v)(du)$
  7. Plug variables back into formula from 6, then evaluate.
- For example, evaluate $\int xe^xdx$
  - First, we say $f(x) = x$, so $x=u$
  - Then, we find $f'(x)$, which is 1, so $f'(x)dx= 1dx$
  - Next, we say $g'(x) = e^x$, so $e^xdx = dv$
  - Then we calculate $g(x)$ and get $e^x=v$
  - After substiution into the formula  $\int (u)(dv) = (u)(v) - \int (v)(du)$ we get $\int xe^xdx = xe^x - \int e^xdx = xe^x - e^x +c$

## Definite Integrals
- If $f$ is continous on [a,b] and if $F$ is the anti-derivative of $f$ on [a,b], then $\int^{b}_{a} f(x)dx = F(x)]_a^b = F(b)-F(a)$
  - Evaluate $\int^{2}_{1} xdx$
    - $\int^{2}_{1}xdx = \frac{x^2}{2}]_1^2 = \frac{2^2}{2} - \frac{1^2}{2} = \frac{4}{2} - \frac{1}{2} = \frac{3}{2}$

### Properies of The Definite Integral...
- If $a$ is in the domain of $f$, then $\int^{a}_{a} f(x)dx = 0$ because there is no area under th e curve $y=f(x)$ above the x-axis.
  - For example, $\int^{5}_{5} x^4dx = 0$
- If b<a and $f$ is integrable on [a,b], then $\int^{b}_{a} f(x)dx = - \int^{a}_b f(x)dx$
  - For example, $\int^{0}_{4} xdx = - \int^{4}_0 xdx = -\frac{x^2}{2}]_0^4 = -8$
- If $f$ is continous and non-negative on $[a,b]$ and if $c$ is a point between $a$ and $b$, then the area under $y=f(x)$ over $[a,b]$ can be split into two parts, $a$ to $c$ and $c$ to $b$. Thus, $\int^{b}_{a} f(x)dx = \int^{c}_a f(x)dx + \int^{b}_c f(x)dx$
   - For example, evaluate $\int{6}_{0} f(x)dx$ where $fx(x) = x^2$ when $x<=2$ and $f(x)= 3x-2$ when $x>=2$.
    - To solve we say $\int^{2}_{0} x^2dx + \int^{6}_2 3x-2dx = \frac{x^3}{3}]_0^2 + \frac{3x^2}{2}-2x]_2^6 = \frac{128}{3}$
     
### U-Substitution for Definite Integrals
- U-substitution also works for definite integrals. Now, to solve these problems follow these steps:
  1. Start with problem is $\int^{b}_{a} f(g(x))g'(x)dx$ form
  2. Make a choice for $u=g(x)$
  3. Make a choice for $\frac{du}{dx} = g'(x)$, then find $du$ which is $du= g'(x)dx$.
  4. Sub $u=g(x)$ and $du=g'(x)dx$ into the problem, such that it is in the form $\int f(u)du$
  5. Evaluate the resultant integral from step 4, then sub $g(x)$ back in for $u$
- For example, evaluate $\int^{2}_{0} 2x(x^2+1)^3dx$
  - First, we say $u=(x^2+1)$
  - Next, we say $\frac{du}{dx} = 2x$, so $du= 2xdx$
  - Following substitution we get $\int^{2}_{0} (u)^3du$
  - After evaluating integral we get $\frac{u^4}{4}]_0^2 = \frac{(x^2+1)^4}{4}]_0^2 = \frac{(2^2+1)^4}{4} - \frac{(0^2+1)^4}{4} = \frac{625}{4} - \frac{1}{4} = 156$

### Mean Value Theorem For Definite Integrals 
 - If $f$ is continous on a closed interval $[a,b]$, there is a number between the minimum $(m)$ and maximum $(M)$ value of the function representing an arithmatic average. The mean value of $f$ on $[a,b]$ is defined as $f_{avg} = \frac{1}{b-a} ⋅ \int^{b}_{a} f(x)dx$
  - For example, find the average value of the function $f(x) = x^2$ on $[1,4]$
    - $f_{avg} = \frac{1}{4-1} ⋅\int^{4}_{1} x^2dx = \frac{1}{3} ⋅ \frac{x^3}{3}]_1^4 = \frac{1}{3} ⋅ 21= 7$
   
### Area Between Two Curves
- If $f$ and $g$ are continous functions where $f(x)>g(x)$ for all $x$ on $[a,b]$, we can find the area bounded above by $f(x)$,  below by $g(x)$, and on the sides by $x=a$ and $x=b$ with the following formula: $A = \int^{b}_{a} f(x)dx - \int^{b}_a g(x)dx = \int^{b}_a [f(x)-g(x)]$.
  - For example...  find the area bounded above by $y=x+6$, below by $y=x^2$, and on the sides by $x=0$ and $x=2$.
    - $\int^{2}_{0} x+6dx - \int^{2}_0 x^2dx = \int^{2}_0 [x+6-x^2] dx = \frac{x^2}{2} + 6x - \frac{x^3}{3}]_0^2 = (\frac{2^2}{2} + 12 -  \frac{2^3}{3}) - (\frac{0^2}{2} + 0 -  \frac{0^3}{3})  = \frac{34}{3}$

## Natural Logarithms
- The integral $\int^{x}_1 \frac{1}{t} dt$ is called the natural logarithm of $x$ and is denoted by the symbol $ln$. Thus, $ln(x) = \int^{x}_1 \frac{1}{t}dt$
- Since $ln(x) = \int^{x}_1 \frac{1}{t}dt$, we can say that $lnx$ is the antiderivative of $\frac{1}{x}$ and $lnx$ equals 0 when $x=1$. Thus, $\frac{d}{dx}[lnx] = \frac{1}{x}$.
  - For example, $\frac{d}{dx}[ln2] = \frac{1}{2}$
- For more complex derivatives of natural logaritms we can use the chain rule, which states $\frac{d}{dx}[lnu] = \frac{d}{du}[lnu] ⋅ \frac{du}{dx} = \frac{1}{u} ⋅ \frac{d}{dx}[ ]$
  - For example, $\frac{d}{dx}[lnx^2] = \frac{d}{du}[lnx^2] ⋅ \frac{du}{dx} = \frac{1}{x^2} ⋅ \frac{d}{dx}[x^2] = \frac{1}{x^2} ⋅ 2x = \frac{2}{x}$
- The same concepts apply for integration as well. For example, evaluate $\int \frac{3x^2}{x^3+5}$ using $u$-substitution
  - First, we can re-write $\int \frac{3x^2}{x^3+5}$ as $\int \frac{1}{x^3+5} 3x^2dx$
  - Then, we say $u=x^3+5$
  - Next, we say $\frac{du}{dx} = 3x^2$, so $du = 3x^2dx$
  - Following substiution we get $\int \frac{1}{u} dx$
  - After evaluating the integral we get $lnu+c$ and upon substituing $u$ back in the result is $ln|x^3+5|+c$
 
### Properties of Natural Logarithms
- For any positive numbers $a$ and $b$ and any rational numbenr $r$....
  1. $ln(ab) = ln(a) + lb(b)$
  2. $ln(\frac{a}{b}) = ln(a)-ln(b)$
  3. $ln(a)^r = rln(a)
  4. $ln(\sqrt{a}) = \frac{1}{2} ln(a)$
  5. $ln(\frac{1}{b}) = -ln(b)$

### The Functions $e^x$ and $a^x$
- $e^x$ is called the exponential function and has a special property where it can undo the natural logarithm and vice versa. Thus, $ln(e^x)=x$ and $e^{lnx} = x$
  - For example, $ln(e^2)=2$ and $e^{ln2}=2$
- Additionally, if $a$ is a positive real number and $k$ is any real number, then...
  1. $a^k = e^{kln(a)}$
  2. $\frac{d}{dx}[a^x] = a^xln(a)$
  3. $\frac{d}{dx}[e^x] = e^x$
  4. $\frac{d}{dx}[a^u] = a^u ln(a)⋅\frac{du}{dx}[ ]$
  5. $\frac{d}{dx}[e^u] = e^u ⋅\frac{du}{dx}[ ]$
  6. $\int a^xdx = \frac{a^x}{ln(a)}+c$
  7. $int\ e^xdx = e^x +c$
 
## First Order Partial Derivatives
- For function of $x$ and $y$, we can find partial derivative $f_{x}(x_0, y_0)$ by holding $y$ constant and differentiating with respect to $x$ and $f_{y}(x_0, y_0)$ by holdong $x$ constant and differentiating with respect to $y$.
- For example, if $f(x,y) = 2x^3y^2+2y+4x$, find $f_{x}(1,2)$ and $f_{y}(1,2)$
  - First, $f_{x}(x,y) = 6x^2y^2+4$, so $f_{x}(1,2) = 6(1)^2(2)^2+4=28$
  - Second, $f_{y}(x,y) = 4x^3y+2$, so $f_{y}(1,2)= 4(1)^3(2)+2=10$
- $f_{x}(x_0, y_0)$ is also denoted as $\frac{∂f}{∂x}$ and $f_{y}(x_0, y_0)$ is $\frac{∂f}{∂y}$. If the independent variable $z=f(x,y)$ is introduced, we use the following symbols instead: $\frac{∂z}{∂x}$ and $\frac{∂z}{∂y}$
  - For example, $z=x^4sin(xy^3)$. Find  $\frac{∂z}{∂x}$ and $\frac{∂z}{∂y}$
    - $\frac{∂z}{∂x}$ = $\frac{∂}{∂x}[x^4sin(xy^3)] = x^4\frac{∂}{∂x}[sin(xy^3)] + sin(xy^3)\frac{∂}{∂x}[x^4]= x^4cos(xy^3)y^3+sin(xy^3)(4x^3)= x^4y^3cos(xy^3)+4x^3sin(xy^3)$
    - $\frac{∂z}{∂y}$ = $\frac{∂}{∂y}[x^4sin(xy^3)] = x^4\frac{∂}{∂y}[sin(xy^3)] + sin(xy^3)\frac{∂}{∂y}[x^4]= x^4cos(xy^3)3xy^2+sin(xy^3)(0)= 3x^5y^2cos(xy^3)$

## Partial Integrals 
- A partial integral is the inverse of a partial derivative. $\int^{b}_{a} f(x,y)dx$ is a partial integral with respect to $x$ and is evaluated by holding $y$ constant and integrating with repect to $x$.
  - For example, $\int^{1}_{0} xy^2dx = \frac{x^2 y^2}{2}]_0^1= \frac{1^2 y^2}{2} - \frac{0^2 y^2}{2} = \frac{y^2}{2}$
- On the other hand, $\int^{b}_{a} f(x,y)dy$ is a partial integral with repect to $y$ and is evaluated by holding $x$ constant and integrating with respect to $y$.
  - For example, $\int^{1}_{0} xy^2dy = \frac{x y^3}{3}]_0^1 = \frac{x 1^3}{3} - \frac{x 0^3}{3} = \frac{x}{3}$

## Second, Third, and Fourth Order Partial Derivatives
- Since the partial derivatives $\frac{∂z}{∂x}$ and $\frac{∂z}{∂y}$ are functions of $x$ and $y$, each can in turn have partial derivatives, giving rise to four possible second order partial derivaive:
  1. $f_{xx} = \frac{∂^2f}{∂x^2} = \frac{∂}{∂x}[\frac{∂f}{∂x}]$
  2. $f_{yy} = \frac{∂^2f}{∂y^2} = \frac{∂}{∂y}[\frac{∂f}{∂y}]$
  3. $f_{xy} = \frac{∂^2f}{∂y∂x} = \frac{∂}{∂y}[\frac{∂f}{∂x}]$
  4. $f_{yx} = \frac{∂^2f}{∂x∂y} = \frac{∂}{∂x}[\frac{∂f}{∂y}]$
- For example, find the second order partial derivatives of $f(x,y)= x^2y^3+x^4y$
  - $f_{xx}= \frac{∂}{∂x}[\frac{∂f}{∂x}] = \frac{∂}{∂x}[2xy^3+4x^3y]= 2y^3+12x^2y]$
  - $f_{yy}= \frac{∂}{∂y}[\frac{∂f}{∂y}] = \frac{∂}{∂y}[3x^2y^2+x^4]= 6x^2y$
  - $f_{xy}= \frac{∂}{∂y}[\frac{∂f}{∂x}] = \frac{∂}{∂y}[2xy^3+4x^3y]= 6xy^2 + 4x^3$
  - $f_{yx}= \frac{∂}{∂x}[\frac{∂f}{∂y}] = \frac{∂}{∂x}[3x^2y^2+x^4] = 6xy^2 + 4x^3$
- With successive differentiation, we can obtain the following third order partial derivatives...
  1. $\frac{∂^3f}{∂x^3} = \frac{∂}{∂x}[\frac{∂^2f}{∂x^2}]$
  2. $\frac{∂^3f}{∂y^3} = \frac{∂}{∂y}[\frac{∂^2f}{∂y^2}]$
  3. $\frac{∂^3f}{∂y∂x^2} = \frac{∂}{∂y}[\frac{∂^2f}{∂x^2}]$
  4. $\frac{∂^3f}{∂x∂y^2} = \frac{∂}{∂x}[\frac{∂^2f}{∂y^2}]$
- We can also continue differentiating to achieve higher order partial derivatives. For example, fourth order partial derivatives can take the form $\frac{∂^4f}{∂x^2∂y^2} = \frac{∂}{∂y}[\frac{∂^3f}{∂y∂x^2}]$

## The Chain Rule for Functions of Two Variables 
- If $x=x(t)$ and $y=y(t)$ are differentiable at $t$, and if $z=f(x,y)$ is differentiable at $(x(t), y(t))$, then $z=f(x(t),y(t))$ is differentiable at $t$ and is defined by $\frac{∂z}{∂t} = \frac{∂z}{∂x}⋅\frac{dx}{dt} + \frac{∂z}{∂y}⋅\frac{dy}{dt}$
  - For example, $z=x^2y, x=t^2, y=t^3$. Find $\frac{∂z}{∂t}$
    - $\frac{∂z}{∂t} = \frac{∂}{∂x}[x^2y]\frac{d}{dt}[t^2]+\frac{∂}{∂y}[x^2y]\frac{d}{dt}[t^3] = (2xy)(2t)+(x^2)(3t^2) = (4xyt)+(3x^2t^2)= (4t^2t^3t)+(3(t^2)^2)t^2)= 4t^6 + 3t^6 = 7t^6$
- In special cases where $z=F(x,y)$ and $y$ is a differentiable function of $x$, the chain rule says $\frac{dy}{dx} = - \frac{\frac{∂F}{∂x}}{\frac{∂F}{∂y}}$
  - For example, find $\frac{dy}{dx}$ given $x^3+y^2x$
    - $\frac{dy}{dx} = \frac{\frac{∂}{∂x}[x^3+y^2-3]}{\frac{∂}{∂y}[x^3+y^2-3]} = - \frac{3x^2+y^2}{2yx}$
- Now, consider a case where $x$ and $y$ are each functions of two variables $u$ and $v$ themselves. If $x=x(u,v)$ and $y=y(u,v)$ and they have first order partial derivatives at $(u,v)$ and $z=f(x,y)$ is differentiable at $(x(u,v),y(u,v))$, then $z=f(x(u,v),y(u,v))$ has  a first order partial derivatives at $(u,v)$, defined by the following formulas:
  1. $\frac{∂z}{∂u} = \frac{∂z}{∂x}⋅\frac{∂x}{∂u} +  \frac{∂z}{∂y}⋅\frac{∂y}{∂u}$
  2. $\frac{∂z}{∂v} = \frac{∂z}{∂x}⋅\frac{∂x}{∂v} +  \frac{∂z}{∂y}⋅\frac{∂y}{∂v}$
    - For example, find $\frac{∂z}{∂u}$ and $\frac{∂z}{∂v}$ given $z=3xty^2$, $x=2u+v$ and $y=\frac{u}{v}$
      - $\frac{∂z}{∂u} = \frac{∂}{∂x}[3x+y^2]\frac{∂}{∂u}[2u+v] + \frac{∂}{∂y}[3x+y^2]\frac{∂}{∂u}[\frac{u}{v}] = (3)(2) + (2y)(\frac{1}{v}) = 6+\frac{2y}{v}$
      - $\frac{∂z}{∂v} = \frac{∂}{∂x}[3x+y^2]\frac{∂}{∂v}[2u+v] + \frac{∂}{∂y}[3x+y^2]\frac{∂}{∂v}[\frac{u}{v}] = (3)(1)+(2y)(\frac{u}{1}) = 3+2yu$

## Functions of Three Variables
- A function of $f(x,y,z)$ with three variables has three partial derivatives $f_{x}(x,y,z)$, $f_{y}(x,y,z)$, and $f_{z}(x,y,z)$. If a dependent variables $x=f(x,y,z)$ is used, the partial derivatives are denoted as $\frac{∂w}{∂x}$, $\frac{∂w}{∂y}$, and $\frac{∂w}{∂z}$.
  - For example, find partial derivatives for $f(x,y,z)=x^3y^2z^4+2xy+z$
    - $f_{x} = 3x^2y^2z^4+2y$
    - $f_{y} = 2x^3yz^4+2x$
    - $f_{z} = 4x^3y^2z^3+1$
- If $x=x(t)$, $y=y(t)$, and $z=z(t)$ are differentiable at $t$ and $w=f(x,y,z)$ is differentiable at $(x(t), y(t), z(t))$, then $w=f(x(t),y(t),z(t))$ is differentiable at $t$ and $\frac{dw}{dt} = \frac{∂w}{∂x}⋅\frac{dx}{dt} +  \frac{∂w}{∂y}⋅\frac{dy}{dt} +  \frac{∂w}{∂z}⋅\frac{dz}{dt}$
  - For example, if $w=x^3y^2z$, $x=t^2$, $y=t^3$, and $z=t^4$, find $\frac{dw}{dt}$
    - $\frac{dw}{dt} = \frac{∂}{∂x}[x^3y^2z]\frac{d}{dt}[t^2] + \frac{∂}{∂y}[x^3y^2z]\frac{d}{dt}[t^3] + \frac{∂}{∂z}[x^3y^2z]\frac{d}{dt}[t^4] = (3x^2y^2z)(2t) + (2x^3yz)(3t^2) + (x^3y^2)(4t^3) = (6x^2y^2zt) + (6x^3yzt^2) + (4x^3y^2t^3) = (6t^15) + (6t^15) + (4t^15) = 16t^15$

## Double Integrals
### Double Integrals Over Rectangular Regions
- The following are called iterated or repeated integrals:
  1. $\int^{d}_c [\int^{b}_a f(x,y)dx]dy$
  2. $\int^{d}_c [\int^{b}_a f(x,y)dy]dx$
- Below I'll demonstrate how to evaluate the double integral $\int^{3}_0 [\int^{2}_1 (1+8xy)dy]dx$
  - $\int^{3}_0 [\int^{2}_1 (1+8xy)dy]dx =\int^{3}_0 [1y+\frac{8xy^2}{2}]_1^2 dx = \int^{3}_0 [(2+16x)-(1+4x)] dx = \int^{3}_0 1+12xdx = 1x + \frac{12x^2}{2}]_0^3 = 57$
  - Notably, the double integral $\int^{2}_1 [\int^{3}_0 (1+8xy)dx]dy$ would produce the same results since we are working in a rectangle defined by inequalities a<=x<=b, c<=y<=d, thus $\int \int f(x,y)dA = \int^{d}_c \int^{b}_a f(x,y)dxdy = \int^{b}_a \int^{d}_c f(x,y)dydx$

### Double Integrals Over Non-Rectangular Regions
- Double integrals over non-rectangular regions can fit into one of two categories, type I or type II, each with different rules: **see page 119 in notebook

# 📚 Linear Algebra
## Gauss-Jordian Eliminaation
- To solve a linear system of equations we can perform algebraic operations on the system that do not alter the solution set and that produce successivley simpler systems until it can be ascertained whether the system is consistent (i.e, solveable) and if so what the solutions are.
- Since rows in an augmented matric correspond to equations in the associated system, the three following operations can be done on the rows: (1) multiple the row through a non-zero constant, (2) interchange two rows, (3) add a constant times one row to another. One of the most reliable ways of doing this is through Gaussian elimination.
- Below is a step-by-step procedure to reduce any matrix to row echleon form:
  1. Locate the leftmost column that isn't all zeros
  2. Interchange top row with another row, if needed, to bring the non-zero entry to the top row
  3. Leftmost entry in row 1 is called $a$. Now, multiple $a$ by $\frac{1}{a}$ to reduce it to a leading 1, then multiple all other entries in that row by $\frac{1}{a}$.
  4. Add suitable multiples of top row to the rows below so all entried below the leading 1 become 0's.
  5. Now, cover the top row of the matrix and begin with step 1 again, but applied to the remaining sub-matrix. Keep repeating steps 1-5 until the matrix is in row echeleon form.
  6. Starting with the last non-zero row and working upward, add suitable multiples of each entry to the row above to introduce zeros above the leading 1's.
  - Steps 1-5 encompass Gaussian elimination, wheres the inclusion of step 6 takes it another step further and is Gauss-Jordian Elimination (results in reduced row echleon form instaed of row echelon form). 
- For example, solve the following system of linear equations with Gauss-Jordian Elimination...
   - $x_1 + 3x_2 - 2x_3 + 2x_5 =0$
  - $2x_1 + 6x_2 - 5x_3 -2x_4 + 4x_5 -3x_6 =-1$
  - $5x_3 + 10x_4 + 15x_6 = 5$
  - $2x_1 + 6x_3 + 8x_4 + 4x_5 + 18x_6 = 6$
  - To solve this system of linear equations we can first put the system of linear equatons into augmented matrix form, demonstrated below...
    
$$\begin{pmatrix}     
1&3&-2&0&2&0&0\\
2&6&-5&-2&4&-3&-1 \\
0 & 0 & 5 & 10 & 0 &15 &5 \\
2 & 6 & 0 & 8 & 4 & 18 &6
\end{pmatrix}$$

 - Then, following Gauss-Jordian Elimination we can reduce the matrix above to reduced row echeleon form, resulting in the following matrix...

$$\begin{pmatrix}     
1 & 3 & 0 & 4 & 2 & 0 & 0 \\
0 & 0 & 1 & 2 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 & 0 & 1 & \frac{1}{3} \\
0 & 0 & 0 & 0 & 0 & 0 & 0
\end{pmatrix}$$

  - Converting the matrix above back into a system of linear equations gives us the following...
    1. $x_1 + 3x_2 + 4x_4 + 2x_5 =0$
    2. $x_3 + 2x_4 =0$
    3. $x_6 = \frac{1}{1}$
  - Then, solving for the leading variables gives us...
    1. $x_1 = -3x_2 -4x_4 -2x_5$
    2. $x_3 = -2x_4$
    3. $x6 = \frac{1}{3}$
  - Now we can assign the free variables $x_2, x_4, x_5$ arbitration values $x_2=r, x_4=s, x_5=t$ giving us the final solution...
    - $x_1 = -3r -4s-2t$
    - $x_2 = r$
    - $x_3 = -2s$
    - $x_4 = s$
    - $x_5 = t$
    - $x_6 = \frac{1}{3}$

# 📚 Ordinary Differential Equations:
## Introduction
- Differential equations are equations that relate one or more unknown functions to their derivatives. For example
  1. $\frac{dy}{dx} = 3y$
  2. $\frac{d^2y}{d^2x} - 6\frac{dy}{dx} + 8y =0$
  3. $y'-y = e^{2x}$
  4. $\frac{d^3y}{d^3x} - t\frac{dy}{dx} + (t^2-1)y = c^t$
- Equations 1-3 above show $y=y(x)$ as an unknown function of $x$, whereas equation 4 have $y=y(t)$ as an unknown function of $t$.
- The order of a differential equation is the order of the highest derivative that appears in the equation. Thus, equation 1 and 3 are first order ODEs, equation 2 is a second order ODE, and equation 4 is a third order ODE.
- A function $y=y(x)$ is a solution to an ODE if the equation is satisfied when $y(x)$ and it's derivatives are substituted. For example, $\frac{dy}{dx} -y = e^{2x}$ has the solution $y=e^{2x}$. 
 
## First Order Ordinary Differential Equations:
### First Order Seperable ODEs
- A first order ODE is seperable if it can be written in the form $\frac{dy}{dx}=g(x)h(y)$ or $\frac{dy}{dx}=\frac{g(x)}{h(y)}$. These two types of equations are called the pre-differential form because the $x$ and $y$ variables are not seperate.
- To solve these types of problems we...
  - Step 1: write the equation in differential form by seperating the $x$ and $y$ variables.
    - (a) $\frac{dy}{dx} = g(x)h(y) → \frac{1}{h(y)}dy = g(x)dx$
    - (b) $\frac{dy}{dx}=\frac{g(x)}{h(y)} → h(y)dy = g(x)dx$
  - Step 2: integrate both sides with respect to the variables ($x$ or $y$)...
    - (a) $\int \frac{1}{h(y)}dy = int\ g(x)dx$
    - (b) $\int h(y)dy = int\ g(x)dx$
  - Step 3: solve for $y$ to get the explicit solution (if possible).
  - Step 4 (only for initial value problems): plug in initial condition to solve for $c$, then write the equation with $c$ plugged in.
- Example 1: solve $\frac{dy}{dx} = \frac{x}{y^2}$
  - $\frac{dy}{dx} = \frac{x}{y^2} → y^2dy = xdx → \int y^2dy = \int xdx → \frac{y^3}{3} = \frac{x^2}{2}+c → y^3 = \frac{3x^2}{2}+3c → y = (\frac{3x^2}{2}+3c)^{1/3}$
- Example 2: solve $x(y-1)\frac{dy}{dx} = y$
  - $x(y-1_\frac{dy}{dx} = y → x(y-1)dy = ydx → (y-1)dy = \frac{ydx}{x} → \frac{(y-1)dy}{y} = \frac{dx}{x} → \frac{y-1}{y}dy = \frac{1}{x}dx → \int \frac{y-1}{y}dy = \int \frac{1}{x}dx → y-ln|y| = ln|x|+c$, which using the properties of logarithms simplifies to $y=ln|xy|+c$
- In some cases there are initial conditions and the 1st order ODE is called an initial value problem. In these cases we include step 4, described above, when solving the problem. For example, solve $\frac{dy}{dx} = -4xy^2$ with the condition $y(0)=1$, which means when $x=0, y=1$.
  -  $\frac{dy}{dx} = -4xy^2 → dy= -4xy^2dx → \frac{1}{y^2}dy = -4xdx → \int \frac{1}{y^2}dy = \int -4xdx → -\frac{1}{y} = -2x^2+c → y= \frac{1}{2x^2+c}$. Now, from the initial condition we get $1=\frac{1}{2(0)^2+c} → 1=\frac{1}{c}$, then $c=1$ and $y= \frac{1}{2x^2+1}$

### First Order Linear ODEs
- Not all first order ODEs are seperable. These ODEs are calld linear if they are expressed in the following form: $\frac{dy}{dx} + p(x)y = q(x)$.
  - For example, $\frac{dy}{dx} + x^2y=e^x$ where $p(x)=x^2$ and $q(x)=e^x$
- To solve these types of problems we...
  - Step 1: start with the ODE in $\frac{dy}{dx} + p(x)y = q(x)$ form.
  - Step 2: identify $p(x)$ and $q(x)$. 
  - Step 3: find the integrating factor $µ(x)$, which is calculated as follows: $µ(x) = e^{\int p(x)dx}$
  - Step 4: multiple both sides of the equation by the integrating factor, $µ(x)$. The left side of the equation will simply to the derivative $\frac{d}{dx}[µ(x)y]$, leaving you with the following: $\frac{d}{dx}[µ(x)y] = µ(x)q(x)$
  - Step 5: integrate both sides, resulting in the following: $\int \frac{d}{dx}[µ(x)y] = \int µ(x)q(x) → µ(x)y = \int µ(x)q(x) + c$
  - Step 6: solve for $y$ by dividing both sides by $µ(x)$
- Example: solve $\frac{dy}{dx}-4xy=x$
  - If $frac{dy}{dx} - 4xy=x$, then $p(x)=-4x$ and $q(x)=x$
  - $µ(x) = e^{\int -4xdx} = e^{-2x^2}$
  - $\frac{d}{dx}[e^{-2x^2}y]= e^{-2x^2}x$
  -  $\int \frac{d}{dx}[e^{-2x^2}y]= \int e^{-2x^2}x → e^{-2x^2}y = -\frac{e^{-2x^2}}{4}+c → y= -\frac{1}{4}+ce^2x^2$
 
 ### Exponential Growth and Decay 
 - Exponential growth adn decay are examples of first order differential equations. A quantity has an exponential growth or decay if at each instant in tme it's rate of increase or decrease is proportional to the amount of quantity present.
 - Exponential growth and decay problems are often presented as linear ODES in the form $\frac{dy}{dx}=ky$ with an initial value of $y(0)=y_0$. However, we can re-write the problem in $\frac{dy}{dx}+p(x)y=q(x)$ form as $\frac{dy}{dt} -ky=0$. After solving this problem we get the following formula: $y(t) = y_0 e^{kt}$ where $t=time$, $y_0=starting quantity$, and $k=growth/decay rate$.
- Example problem: the world population in 1975 is 4B people and grows at a rate of 2%/yr. What is the population in 2000?
  - from the problem we get... $y_0=4B$, $k=0.02, t=0$ in 1975, and $t=25$ in 2000.
  - thus, $y(25)=4e^{0.02 * 25} = 6.59B$
- Now, we can also use the following formulas to calcualte the doubling and halving time of the population...
  - $T=\frac{1}{k}ln2$ is the doubling time and $T=-\frac{1}{k}ln2$ is the halving time (ex, radioactive decay).
 
## Second Order Ordinary Differential Equations
### Homogenous Linear Equations

### Non-Homogenous Linear Equations 

## Systems Of First Order Ordinary Differential Equations

## Solving Non-Homogenous Systems Of Ordinary Differential Equations
