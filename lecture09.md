- Linear independence
- Spanning a space
- BASIS and dimensions

## Linear independence

A is m * n and m < n
- there are nonzero solutions to Ax = 0
- reason: >= 1 free variables

Independence

Vectors x1, x2, x3, ... xn are independent if no combination gives the zero vector (** except the zero combination)

r = n
- they are independent if nullspace of A is only the zero vector N(A) = 0
- no free vars

r < n
- they are dependent if Ac = 0 for some non-zero c,
- has free vars

## Spanning a space

Vectors v1, v2, ..., vl span a space means the space consists of all combinations of those vectors

## BASIS and dimensions

A basis for a space is a sequence of vectors that has 2 properties
- they are independent
- they span the space


Example:


    Space is R3

    One basis is (a list of vectors)
    ^^^
        [1 0 0], [0 1 0], [0 0 1]

they are independent (they are the x,y,z axes, so duh)

Another basis,

      |1| |2| |3|
      |1| |2| |4|
      |2| |5| |8|  


How do we know we have a basis?  put vectors in matrix, forward elimination,
make sure we have no free variables (all columns have a pivot)

Rn n vectors give a basis if the n * n matrix with these cases is invertible

Given a space
- Every basis for the space has the same # of vectors
- this # is the Dimension of the space



Example:

Space is C(A),   N(A)

    |1 2 3 1|    |-1|
    |1 1 2 1|    |-1|
    |1 2 3 1|    | 1|
                 | 0|

They span the space but are not independent
Rank is 2 because two pivots (cols 1,2 are dependent on col3)

    2 = rank(A) = # of pivot columns
      - so 2 is the Dimension of the column space, of C(A)

dim C(A) = r, dimension of column space of A is the rank


another vector in the null space

       |-1|
       | 0|  this is the other special solution
       | 0|
       | 1|

null space tells you what columns in the matrix are independent

the basis of the null space is then

      |-1|  |-1|
      |-1|  | 0|
      | 1|, | 0|
      | 0|  | 1|


dim N(A) = # of free vars

         = n - r

