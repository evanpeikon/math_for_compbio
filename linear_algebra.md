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
   
  **Note - I skipped the remainder of this section since GitHub's Latex formatting within Markdown is a bit too clunky. However, important topics you should learn include matrix products as linear combinations, how to find the transpose, trace, and inverse of a matrix, solving linear systems via matrix inversion, how to solve linear systems with common coefficient matrix, rules associated with diagonal and triangular matrices, network analyses, determinants by co-factor expansion, vectors in coordinate space, linear combinations of vectors, vector norms, distance in $r^n$, inner products, dot products as matrix multiplication, orthogonal vectors, linear combinatons, linear independance and dependance, basis for vector space, coordiantes relative to basis, row, column, and null space, rank and nullity, matrix transformations from $R^n$ to $R^m$, dynamical systems and markov chains, eigenvalues and eigenvectors, finding eigenvalues and bases for eigenspaces, and diagnonalization of matrices. 

## Book Recomendation For Linear Algebra 
- Howard Anton's "Elimentary Linear Algebra". I found this book much more useful than Gilbert Strang's texts, which are more commonly recommended. 
