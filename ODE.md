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
### Seconding Order ODES: Homogenous Linear Equations
- Second order homogenous linear equations have the form $a(x)y'' + b(x)y' +cy=0$. However, for constant coefficients this simplifies to the following: $ay''+by'+cy=0$ or $a\frac{d^2y}{dx^2}+b\frac{dy}{dx}+cy=0$, which are synonymous equations.
- To solve these types of problems we...
  - Step 1: start with the problem in $ay''+by'+cy=0$ form
  - Step 2: substitute $y''=r^2e^{rx}$, $y'=re^{rx}$, and $y=e^{rx}$ into the equation, resulting in the following transformation: $ay''+by'+cy=0$ → $ar^2e^{rx}+bre^{rx}+ce^{rx}=0$
  - Step 3: factor out $e^{rx}$, resulting in the following: $ar^2e^{rx}+bre^{rx}+ce^{rx}=0$ → $e^{rx}(ar^2+br+c)=0$
  - Step 4: Since $e^{rx}≠0$, we can divide both sides by $e^{rx}$ to get the characteristic equation $ar^2+br+c=0$
    - Note: You can jump straight to to the characteristic equation from step 1
  - Step 5: Solve the characteristic equation by solving the quadratic equation $ar^2+br+c=0$ for $r$.
    - $r= \frac{-b ± \sqrt{b^2-4ac}}{2a}$
  - Step 6: determine the form of the general solution...
    - Option 1: if there are two distinct real roots $r_1$ and $r_2$, the general solution is $y(x)=c_{1}e^{r_{1}x}+c_{2}e^{r_{2}x}$
    - Option 2: if there is a repeated real root $r$, the general solution is $y(x)=(c_{1}+c_{2}x)e^{rx}$
    - Option 3: if there are complex conjugate roots $r=α±βi$, the general solution is $y(x)=e^{αx}(c_{1}cos(βx)+c_{2}sin(βx))$
  - Step 7: Obtain the specific solution if given an initial value to solve for.
- Example 1: solve $1y''-3y'+2y=0$
  - $1y''-3y'+2y=0$ → $1r^2-3r+2=0$ → $r= \frac{-(-3) ± \sqrt{-3^2-4(1)(2)}}{2(1)}$, which gives $r_1 = 2$ and $r_2=1$ → thus, $y=c_{1}e^{2x}+c_{2}e^{1x}$
- Example 2: solve the following differential equation representing a dampened harmonic oscillator in circadian rhytmes: $\frac{d^2p}{dt^2}+\frac{4dp}{dt}+4p=0$
  - $\frac{d^2p}{dt^2}+\frac{4dp}{dt}+4p=0$ → $r= \frac{-4 ± \sqrt{4^2-4(1)(4)}}{2(1)}$, which gives repeated real root $r=-2$ → thus, $(c_{1}+c_{2}x)e^{-2x}$

### Seconding Order ODES: Non-Homogenous Linear Equations 
- Seconod order non-homogenous linear equations have the form $ay''+by'+cy= f(x)$ and can be solved with the following steps:
  - Step 1: first, solve the corresponding homogenous equation $ay''+by'+cy=0$ and determine the general solution, which we'll call $y_{h}$
  - Step 2: next, we find the particular solution, $y_{p}$ using the method of undetermined coefficients. When $f(x)$ is a simple polynomial, exponential, sine, or cosine, this allows us to guess the form of $y_{p}$ based on $f(x)$, then determine the coefficients by substituting $y_{p}$ into the differential equaton...
    - If $f(x)$ is polynomial of form $f(x)=ax^n+bx^{n-1}+...$ then $y_{p}$ is polynomial of degree $n$
    - If $f(x)$ is exponential of form $f(x)=e^{kx}$, guess $y_{p}=Ae^{kx}$ or $Axe^{kx}$
    - If $f(x)$ is sine or cosine, guess $y_p = Asin(kx)+Bcos(kx)$
  - Step 3: first differentiate $y_p$ into $y_{p}'$ and  $y_{p}''$, then sub these in for $y''$ and $y'$m and $y$ in the original equation $ay''+by'+cy=f(x)$
  - Step 4: collect like terms, then equate coefficients of like terms from both sides of the equation to solve for unknown coefficients in $y_p$
  - Step 5: Form solution by summing the general solution $y_h$ and particular solution $y_p$... $y(x)=y_{h}(x)+y_{p}(x)$

Example 1 (polynomial): solve $y''-y'-6y=x^2$ 
  - Step 1: First, we find $y_h$, which is $y_h = c_{1}e^{3x}+c_{2}e^{-2x}$
  - Step 2: Since $f(x)=x^2$ is polynomial of degree 2, we expect $y_p$ to have the form $y_{p}=Ax^2 +Bx+C$
  - Step 3: Now, we differentiate $y_{p}$ to get $y_{p}'=2Ax+B$ and $y_{p}''=2A$, then we sub these into the original equation to get $2A-(2Ax+b)-6(Ax^2+Bx+c)=x^2$, which simplifies to $2A-(2Ax+B)-(6Ax^2-6Bx-6C)=x^2$
  - Step 4: Now we collect like terms to get $-6Ax^2-2Ax-6Bx+2A-B-6C=x^2$, then equate coefficients of like terms from both sides...
    - $x^2$ term: -6Ax^2 =x^2 → $-6A=1$
    - $x$ term: $-2Ax-6Bx = 0$ → $-2A-6B=0$ 
    - Constant term: $2A-B-6C=0$
    - Now, from $-6A=1$ we get $A=-\frac{1}{6}$. Thus, we can solve for the remaining terms...
      - $x$ term: $-2A-6B = 0$ → $-2(-\frac{1}{6})-6B=0$ means $B=\frac{1}{18}$
      - constant: If we sub A and B into $2A-B-6C=0$ we get $C=-\frac{7}{108}$
    - Thus, $y_p = -\frac{1}{6}x^2 + \frac{1}{18}x - \frac{7}{108}$
  - Step 5: $y(x) = c_{1}e^{3x}+c_{2}e^{-2x} -\frac{1}{6}x^2 + \frac{1}{18}x - \frac{7}{108}$

Example 2 (exponential): solve $y''-3y'+2y=e^x$
  - Step 1: $y_h = c_{1}e^{2x}+c_{2}e^{x}$
  - Step 2: since $f(x)=e^x$, we guess that the particular solution has the form $y_p = Ae^x$. However, this solution produces incosistent results where where $0=e^x$ and $x=0$, which is impossible because it implies $0=1$. Thus, we guess again with $y_p = Axe^x$.
  - Step 3-5: If $y_p = Axe^x$, then $y_{p}'=Ae^x + Axe^x$ and $y_{p}'' = 2Ae^x + Axe^x$. Thus, $(2Ae^x + Axe^x)-3(Ae^x+Axe^x)+2(Axe^x)=e^x$, which simplifies to $(-Ae^x)=e^x$, thus $A=-1$ and $y_p = -xe^x$. Finally, we get $y(x)=c_1e^{2x}+c_2e^x-xe^x$

## Systems Of First Order Ordinary Differential Equations
- A system of first order ODEs involves multiple equations, each describing the rate of change of one of the dependent variables with respect to a single independent variable. These systems generally have the form $\frac{dy}{dx}= Axy+b$ where $y$ is an $n$-dimensional vector of dependent variables,  $A$ is a nxn matrix, and $b$ is a $n$-dimensional vector of constants or functions of $x$.
- Additionally, when $b=0$ the system is homogenous and takes the form $\frac{dy}{dx}=Ay$, whereas when $b≠0$, the system is non-homogenous and take the form above. 

### Solving Homogenous Systems of first order ODES
- Step 1: first, write the syste in matrix form $\frac{dy}{dx}=Ay$ where $A$ is an nxn matrix and $y$ is an $n$-dimensional vector of the form $y=[y_1, y_2,.. y_n]$
  - Example in notebook on pg.130
- Step 2: find eigenvalues of $A$. Recall, eigenvalues of nxn matrix $A$ satisfy the equation $det(λI-A)=0$
- Step 3: for each eigenvalue, $λ$, find the correspondng eigenvector by solving $(λI-A)x=0$
- Step 4: form the general solution. If all eigenvalues are distinct, the general solution is $y(x)=c_{1}e^{λ_{1}x}+c_{2}e^{λ_{2}x}+...c_{n}e^{λ_{n}x}$
- Example problem in notebook on pg. 131

### Solving Non-Homogenous Systems of first order ODES
- Step 1: First, solve the corresponding homogenous system $\frac{d}{dx}y_g=Ay_h$
- Step 2: find a particular solution to the non-homogenous system $\frac{d}{dx}=Ay_p+b(x)$. A common method is undetermined coefficients, where $y_p$ is assumed to be a constant vector $[y_1p, y_2p]$ and $\frac{d}{dx}y_p=0$, so the equation becomes $0=Ay_p+b$, then solve for $y_p$ via back substitution.
- Step 3: write the full solution, $y(x)=y_h(x)+y_p(x)$ → $y(x)=c_{1}e^{λ_{1}x}+c_{2}e^{λ_{2}x}+...c_{n}e^{λ_{n}x} + [y_1p, y_2p, ...y_np]$
- Example problem in notebook on pg. 121
