# Computing the null space (Ax = 0)

# Pivot variables - free variables

# Special solutions - rref(A) = R


## Computing the null space (Ax = 0)
 

    A = |1 2 2  2|
        |2 4 6  8|
        |3 6 8 10|

## Pivot variables - free variables

On to elimination

multiplier of 2 for pivot at (1,1)

   yields

        |1 2 2  2|
        |0 0 2  4|
        |3 6 8 10|

next, multiplier of 3 for pivot at (2,3)

   yields

        |1 2 2 2|
        |0 0 2 4|
        |0 0 2 4|

finally, multiplier of 1 for pivot at (2,3)

   yields the U matrix

        |1 2 2 2|
        |0 0 2 4|
        |0 0 0 0|
         ^ f ^ f     ^ = pivot columns (2 of them), f = free columns (2 of them)

* This is also called Upper Triangular (but not a square matrix so not _really_ triangular
* Also called Echelon form (because it stair-steps down and to the right)

First pivot was 1 from (1,1)
the second pivot was 2 from (2,3)


There are 2 pivots.  This is also called the Rank of the matrix.  Rank 2

Now we want to solve Ux = 0

equations to solve (translating Ux = 0) are 

    x1 + 2x2 + 2x3 + 2x4 = 0
               2x3 + 4x4 = 0


    start with x =  | |  (x2 and x4 are free variables so we can arbitrarily choose values for them)
                    |1|  (here, we've just chosen x2 = 1 and x4 = 0)
                    | |
                    |0|

    plug in x2 and x4 values into equations and get 

                    |-2| 
                    | 1| 
                    | 0|
                    | 0|

because 2x3 + 4(0) = 0, x3 = 0
then, x1 + 2x2 + 2(0) + 2(0) = 0, x1 = -2 

this vector, [-2 1 0 0] is in the nullspace and any multiple of it is in the nullspace

but this isn't the whole nullspace.  
Let's pick new values for free values, this time: 

                | |
                |0|
                | |
                |1|

because 2x3 + 4(1) = 0, x3 = -2
then, x1 + 2(0) + 2(-2) + 2(1) = 0, x1 = 0 

                | 2|
                | 0|
                |-2|
                | 1|

So, full nullspace is 

         |-2|         | 2|
       c | 1|   +   d | 0| 
         | 0|         |-2|
         | 0|         | 1|

## Special solutions - rref(A) = R


rref = Reduced row echelon form
- has zeros above and below the pivots

So, we have U

        |1 2 2 2|
        |0 0 2 4|
        |0 0 0 0|

substract -1, (-1)row2 - row1), yields

        |1 2 0 -2|
        |0 0 2  4|
        |0 0 0  0|

now divide by 2 on 1st pivot yields,

        |1 2 0 -2|
        |0 0 1  2|  = Rref (or just R)
        |0 0 0  0|

Notice that we have identity matrix, |1 0|, in the pivot rows,columns
                                     |0 1|


Rx = 0 is 

        x1 + 2x2    - 2x4 = 0
                 x3 + 2x4 = 0

 
         |1 0|    |2 -2|
         |0 1|    |0  2|
       pivot(I)  free (F)
         cols      cols
    
    
    R = |I F|
        |0 0|
    

Nullspace matrix  (N)
- the columns are the special solutions

We want RN = 0

What N will do the job?

      N = |-F|
          | I|


    |I F| * |-F| = 0
    |0 0|   | I|
  

Rx = 0 is

    |I F| * |x(pivot)|
            |x(free) |

means, x(pivot vars) + F * x(free vars) = 0
       x(p) = -F * x(f)


Another example, starting from At (transpose of A)


    A = |1 2  3|
        |2 4  6|
        |2 6  8|
        |2 8 10|

after first pivot (w/ multiplier 2) yields

    A = |1 2 3| then exchange  |1 2 3| then next pivot is (2,2) |1 2 3|, which gives us our U
        |0 0 0|  row2 and row3 |0 2 2| and use multiplier 2     |0 2 2|
        |0 2 2|                |0 0 0|                          |0 0 0|
        |0 4 4|                |0 4 4|                          |0 0 0|

rank again is 2, because we used to 2 pivots
and 1 free column

equations are ...      ... so we choose 1 for our only free variable,(x3) and plug it in the equations to solve for x1 and x2
  
    x1 + 2x2 + 3x3 = 0       2x2 + 2(1) = 0, so x2 = -1, then
         2x2 + 2x3 = 0       x1 + 2(-1) + 3(0) = 0, so x1 = -1

    So, Ux = 0, is U |-1| = 0
                     |-1|    
                     | 1|    
     


whole null space is c [-1 -1 1]

Now to get R

    |1 2 3| multiplier 1,  |1 0 1|, so this is R
    |0 2 2| subtract row1  |0 1 1| 
    |0 0 0| from row2      |0 0 0|
    |0 0 0|                |0 0 0|



