# Vector spaces and subspaces

# Column space of A: Solving Ax = b

# Nullspace of A

## Vector spaces and subspaces

Vector space requirements

- v + w and cv are in the space (add any two vectors, v and w, or multiple a vector v by any constant c)
- all combinations of cv + dw are in the space (dw is any multiple d times vector w)
- all subspaces must go through origin: [0 .. 0]


## Column space of A: Solving Ax = b


        |1 1 2|
    A = |2 1 3| = all linear combos of cols
        |3 1 4|
        |4 1 5|

- Vectors are in R4
- Column space of A is a subspace of R4 (because A is a 4x3 matrix)

Which b's allow this system to be solved?

     |1 1 2|        |   |
     |2 1 3| |x1| = | b |
     |3 1 4| |x2|   |   |
     |4 1 5| |x3|   |   |

Can solve Ax = b exactly when b is in C(A), when b is
in a column space of A



## Nullspace of A

- all solutions where 
    
          |x1|
      x = |x2| to the eqn Ax = 0
          |x3|

     |1 1 2|        | 0 |
     |2 1 3| |x1| = | 0 |
     |3 1 4| |x2|   | 0 |
     |4 1 5| |x3|   | 0 |

     or 


     |1 1 2|     | 0 |
     |2 1 3| x = | 0 |
     |3 1 4|     | 0 |
     |4 1 5|     | 0 |


    N(A) contains |0| also | 1| , all are | c| or     | 1| 
                  |0|      | 1|           | c|    c * | 1| a line in R3
                  |0|      |-1|           |-c|        |-1|
    


