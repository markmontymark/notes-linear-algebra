- Matrix Multiplication (4 ways)
- Inverse of A, AB, At
- Gauss-Jordan find A -1

##  Matrix Multiplication (4 ways)

- always say rows before cols

### first way

Matrix A times Matrix B equals Matrix C

    C(3,4) = take A(row 3) and B(col 4) and compute

    a(3,1) * b(1,4) + a(3,2) * b(2,4) + a(3,3) * b(3,4) + (aj

    = Σ a(3,k) * b(k,4)

a matrix A with size (m,n) times a matrix B with size (n,p), when multiplied gives a matrix C with size (m,p)

### 2nd way, the column way

B and C are just a group of columns, which are the products of the matrix A to each column in B

matrix A multiplied by a column on B gives a column in C

### 3rd way, the row way

A and C are just a group of rows, which are the products of a row in matrix A times B gives a row in matrix C

a row in matrix A multiplied by matrix B gives a row  in C

### 4th way, the col * row way

AB = Sum of(cols of A) times (cols of B)

column of A (m x 1) times a row of B (1 x p) gives a (m,p) matrix

Example:

      |2|              |2 12|
      |3|  x |1 6|  =  |3 18|
      |4|              |4 24|


      |2|              |2|           |7|
      |3|  x |1 6|  =  |3| * |1 6| + |8| \* |0 0|  == same matrix above because of |0 0|
      |4|    |0 0|     |4|           |9|




## Inverse of A, AB, At

A-1 (the inverse of A) times A = Identity Matrix, if A-1 exists.  A-1 doesn't always exist

      What is A-1, if A is |1 3|  means  |1 3| x |a c| = |1 0|
                           |2 7|         |2 7| x |b d|   |0 1|

## Gauss-Jordan find A -1

means solving 2 eqns at once:

      |1 3| times |a| = |1|
      |2 7|       |b|   |0|  
                           
      |1 3| times |c| = |0|
      |2 7|       |d|   |1|

     tack on two I cols  |1 3 1 0|
                         |2 7 0 1|

     and do elimination,
     1st elimination step, take 2

     gives |1          3 1 0|
           |2-(1*2)  7-(3 * 2)  0-(1*2)  1-(0*2)|

     gives |1 3  1 0|
           |0 1 -2 1|


Gauss would say stop, but Jordan says continue and eliminate the 3

so, 
      |1 3-(1*3) 1-(-2*3) 0-(1*3)|
      |0 1            -2        1|

      |1 0  7 -3|
      |0 1 -2  1|
