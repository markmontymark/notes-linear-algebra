- Graphs and Networks
- Incidence matrices
- Kirchhoff's Laws


## Graphs and Networks

Graph: made up of nodes, edges

    1 ->- 4    n = 4 nodes
    |\|  /     m = 5 edges
   \| \ /|
    2->3

Edges

1. 1 ->- 2
2. 2 ->- 3
3. 1 ->- 3
4. 1 ->- 4
5. 3 ->- 4


    Incidence Matrix

     Node  1  2  3  4 

         |-1  1  0  0|  edge 1 \
    A =  | 0 -1  1  0|  edge 2  - Taken together, these form a loop
         |-1  0  1  0|  edge 3 /
         |-1  0  0  1|  edge 4
         | 0  0 -1  1|  edge 5        

Loops lead to linearly dependent row(s)

Notes:  
- first 3 rows taken together form a loop
- if you add row1 to row2, you get row3, so combination of rows is dependent        


What's N(A)?

The nullspace tells what combinations of rows give us zero.
The main question is are the columns independent or dependent?

Solve Ax = 0 to find the nullspace

      |-1  1  0  0| |x1|    |x2 - x1|    |0|
      | 0 -1  1  0| |x2|    |x3 - x2|    |0|
      |-1  0  1  0| |x3| =  |x3 - x1| =  |0|
      |-1  0  0  1| |x4|    |x4 - x1|    |0|
      | 0  0 -1  1|         |x4 - x3|    |0|


x = x1, x2, x3, x4 =  _potentials_ at the nodes

**** e = Ax *****

The equations above, ie x2-x1=0, give us the potential differences


*y = Ce*

all x's = 0 are in the nullspace

           |0|  |1|                                     |1|
           |0|  |1|                                     |1|
       x = |0|  |1|  are in the null space, so also c * |1| 
           |0|, |1|                                     |1|
           |0|  |1|                                     |1|

dim N(A) is 1

rank is 3

N(At) = At * y = 0

dim of N(At) 

At is  n x m, 4 x 5

      |-1  0 -1 -1  0|  |y1|   |0|
      | 1 -1  0  0  0|  |y2|   |0|
      | 0  1  1  0 -1|  |y3| = |0|
      | 0  0  0  1  1|  |y4|   |0|
                        |y5|

dim N(At) = m - r, 5 - 3 = 2


there is a matrix C, (y's represent currents on the edges)

Ohm's Law says current on an edge is some number * the potential drop

## Kirchoff's Law

 At y = 0, is called Kirchoff's Current Law, KCL


     - y1      - y3 - y4        = 0

This is law saying that in = out, there a net zero change

       y1 - y2                  = 0
            y2 + y3      - y5   = 0
                      y4 + y5   = 0

Basis for N(At), looking for 2 vectors

These are both loops, 
- 1st loop is 1->2 (aka y1), 2->3(y2), 1->3(y3)
- 2nd loop is 1->3 (aka y3), 1->4(y4), 3->4(y5)

      | 1|   | 0|
      | 1|   | 0|
      |-1| , | 1|
      | 0|   |-1|
      | 0|   | 1|

- and a big loop around the whole graph, [1 1 0 -1 1],
  this is NOT in the nullspace because it is DEPENDENT

R(A), the rowspace of A, the number of independent rows is 3

      |-1  0 -1 -1  0|            
      | 1 -1  0  0  0|            
      | 0  1  1  0 -1|            
      | 0  0  0  1  1|            
                            
Pivot columns are 1, 2 and 4, correlates to y1, y2, y4

A graph with *no loops*, like above y1, y2, y4 is called a _Tree_


dim N(At) = m - r

  #loops = #edges - (#nodes - 1)

  #nodes - #edges + #loops = 1

  aka _Euler's formula_

Linear Algebra proves Euler's formula


Basic equation of Applied Math (in equilibrium)

    At C A x = f


