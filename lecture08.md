# Solving Ax = b, rref

     |1 2 2  2|
     |2 4 6  8|
     |3 6 8 10|
         A   x  = b

Make the Augmented matrix by tacking on b vector

     |1 2 2  2 b1|
     |2 4 6  8 b2|
     |3 6 8 10 b3|

Do normal steps of forward elimination and back substitution

     |1 2 2 2 b1|
     |0 0 2 4 b2 - 2b1|
     |0 0 2 4 b3 - b31|


     |1 2 2 2 b1|
     |0 0 2 4 b2 - 2b1|
     |0 0 0 0 b3 - b2 - b1| = 0

Bottom row gives us the condition for solvability

# Solvability, Condition on b

Ax = b is solvable when b is in C(A)
If a combination of rows of A gives a zero row
then the same combination on b should give a zero b(sub i)

To find the complete solution to Ax = b

1.  start by finding one _particular_ soln

Xparticular, Xp
set all free vars to zero, solve for pivots

given x2 = 0, x4 = 0

    x1 + 2x3 = 1
         2x3 = 3, x3 = 3 / 2, so then x1 = -2

    Xp = | -2|
         |  0|
         |3/2|
         |  0|

2. Add nullspace, Xn
3. Complete solution is  x = Xp + Xn

       A Xp = b
     + A Xn = 0
     ----------
     A(Xp + Xn) = b

      Xcomplete, Xc =  | -2|  +  c1 | 2|     +  c2  | 2|
                       |  0|        | 0|            | 0|
                       |3/2|        |-2|            |-2|
                       |  0|        | 1|            | 1|
                               ^------------ Xn ---------^


## Full column rank

Given an m * n matrix of rank r

r <= m and r <= n
- 0 or 1 solution
- no free vars


Full column rank
- r = m
- no free vars
- *can* solve Ax = b for every b
- can always solve


      r = m = n    |  r = n < m     |    r = m < n    |    r < m, r < n
        R = I      |  R = |I|       |       R = [IF]  |     R = |IF| 
        1 soln to  |      |0|       |    infinity     |         |00| 
        Ax = b     |  0 or 1 soln   |      solns      |    0 or inf solns





