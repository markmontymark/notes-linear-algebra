# Inverse of AB, Aₜ

# Product of elimination matrics

# A = LU (no row exchanges)

    A * A⁻¹ = I = A⁻¹ * A
    
    AB * B⁻¹ A⁻¹ = I
    
    (A⁻¹)ₜ * Aₜ = I

so

    (Aₜ)⁻¹ = (A⁻¹)ₜ

## Inverse of AB, Aₜ

## Product of elimination matrics

       E₍₂₁₎        A   =    U
      |1  0|      |2 1|    |2 1|
      |-4 1|      |8 7|    |0 3|
    
       A    =    L        U
      |2 1|    |1 0|    |2 1|
      |8 7|    |4 1|    |0 3|
    
Where L is E₍₂₁₎⁻¹, or the inverse of the elimination matrix

U stands for Upper triangular(elimination matrix) and 
L stands for Lower triangular(elminiation matrix)

## A = LU (no row exchanges)

For A is a 3x3 matrix

    E(3,2) E(3,1) E(2,1) A = U
  
     or 

    A = E(2,1)⁻¹ E(3,1)⁻¹ E(3,2)⁻¹  U
    
       so
    
    L = E(2,1)⁻¹ E(3,1)⁻¹ E(3,2)⁻¹ 


Example:

    E(3,2)    E(2,1)    
    |1  0 0| | 1 0 0|     | 1  0 0|
    |0  1 0| |-1 1 0|  =  |-2  1 0|
    |0 -5 1| | 0 0 1|     |10 -5 1|
    
    A = LU

If no row exchanges,
multipliers (from forward eliminiations)
go directly into L

## Transposes and permutations

    P⁻¹ = Pₜ

