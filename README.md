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
