# Four Fundamental subspaces for matrix A

1. C(A) , the column space of A, in Rm
2. N(A) , the null space of A, in Rn
3. C(Aₜ), the rowspace of A, all combinations of the rows of A aka C(Aₜ), Rn
4. N(Aₜ), nullspace of Aₜ, aka left nullspace of A, Rm


A is m * n

Rn = row space and nullspace
Rm = col space and nullspace of Aₜ

C(A)
Basis = pivot cols
Dimension = rank r

C(Aₜ)
Basis of C(Aₜ) = pivot cols
Dimension of C(Aₜ) = rank r

N(A)
Basis = special solutions, 1 for each free variable, n - r = # of free vars
Dimension = n - r

N(Aₜ)
Dimension of N(Aₜ) = m - r
Basis of N(Aₜ) =


Example:

|1 2 3 1|     |1  2  3 1|    |1 2 3 1|    |1 0 1 1|   
|1 1 2 1| ->  |0 -1 -1 0| -> |0 1 1 0| -> |0 1 1 0| = R
|1 2 3 1|     |0  0  0 0|    |0 0 0 0|    |0 0 0 0|


= | I   F |
  |       |
  |0 0 0 0|
          

What's this rowspace?

C(A) != C(R), have different column spaces, but have the same rowspace   


What a basis for R? (It will be a basis for the original A), 
the first two rows,

Basis is first r rows of R (not of A)

    |1 0 1 1|
    |0 1 1 0|


4th space, N(At)

At y = 0

  =

yt A = 0t

Basis, how to get it:

    rref| Am*n  Im*m | -> |Rm*n Em*m|

    E m*n = what it took to from A to I (all the row reduction stuff)


   so E A = R

       E          A
   |-1  2 0|  |1 2 3 1|   
   | 1 -1 0|  |1 1 2 1|   
   |-1  0 1|  |1 2 3 1|   





