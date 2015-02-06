- Bases of new vector spaces
- Rank one matrices
- Small world graphs

## Bases of new vector spaces

    M is all 3x3 matrices (we can add them, multiply them by scalars)
    
    S is a subspace of Symmetric 3x3 matrices
    U is subspace of upper triangular 3x3 matrices
    
    
    Basis for M (given M description above)
    
    find the Basis, then Count the number of bases to get the Dimension
    
    One basis
    
    |1 0 0|   |0 1 0|   |0 0 1|       |0 0 0|
    |0 0 0|   |0 0 0|   |0 0 0|       |0 0 0|  there are
    |0 0 0| , |0 0 0| , |0 0 0| , ... |0 0 1|  9 of them 
    
    So, Dimension of M is 9
    
    dimension of S is 6
    
    dimension of U is 6
    
    
    SnU = means S intersection U = symmetric and upper triangular
        = diagonal 3x3 matrices
        = dimension 3
    
    We are not interested in SuU = S union U, because it's not a subspace
    
    S+U = this is combinations of things in S and things in U
        = sum (duh)
        = any element of S + any element of U
        = all 3x3's
    
    dim(S+U) = 9
    
    dim(S) = 6 + dim(U) = 6 
    
        =
    
    dim (SnU) = 3 + dim(S+U) = 9 
    
        = 12


     d²y                special solution:
     --- + y = 0        y = c1 cosx + c2 sinx
     dx²                

     y = cos x, sin x, these are the Basis
    dimension(solution space) = 2


## Rank one matrices

    Example of a matrix w/ rank 1
    
    A = |1 4  5|   |1| * |1 4 5|
        |2 8 10|   |2| 
    
    Basis is the first row, [1 4 5]
    Basis of the column space, r = 1
    dim C(A) = rank = dim C(At)
    
    Rank 1 matrix has
    
         A = UVt 
    
    M = all 5x17 matrices
    
    subset of rank 4 matrices, is a subspace
    subset of rank 1 matrices, not a subspace
    
    
    In R4, v = [v1 v2 v3 v4], 
           S = all v in R4 with 
               v1 + v2 + v3 + v4 = 0
             = nullspace of A = |1 1 1 1|
             rank of A is 1
             dim N(A) = n - r = 3
    
    Basis of S aka "special solutions"
    
         |-1|  |-1|  |-1|
         | 1|  | 0|  | 0|
         | 0|  | 1|  | 0|
         | 0|  | 0|  | 1|
    
    C(A), all multiples of |1 1 1 1|
    C(A) = R1, 
    N(At) = 0


## Small world graphs


   Graph = set of nodes, edges connecting the nodes


