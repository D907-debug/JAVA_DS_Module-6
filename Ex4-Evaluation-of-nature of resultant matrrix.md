# Ex4 You are given a Java program that performs matrix addition. If Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension, what will be the nature (even/odd/mixed) of the resulting matrix?
## DATE:10/11/25
## AIM:
To write a java function to evaluate weather the given Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension and find the nature of resultant matrrix.

## Algorithm
1. Start the program.
2. Declare two 2D arrays, A and B, of the same size
3. Initialize Matrix A with all odd numbers and Matrix B with all even numbers.
4.  Create another 2D array C to store the sum of corresponding elements of A and B.
5.  For each element position (i, j):

Compute C[i][j] = A[i][j] + B[i][j].

## Program:
```
/*
Program to find the nature of resultant matrix.
Developed by: Dilli babu K
Register Number: 212224110015
*/

import java.util.Scanner;

public class MatrixNature {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter number of rows: ");
        int rows = sc.nextInt();
        System.out.print("Enter number of columns: ");
        int cols = sc.nextInt();

        int[][] A = new int[rows][cols];
        int[][] B = new int[rows][cols];
        int[][] C = new int[rows][cols];

        System.out.println("\nEnter elements of Matrix A (all odd numbers):");
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                A[i][j] = sc.nextInt();
            }
        }

        System.out.println("\nEnter elements of Matrix B (all even numbers):");
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                B[i][j] = sc.nextInt();
            }
        }

        // Matrix Addition
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                C[i][j] = A[i][j] + B[i][j];
            }
        }

        // Display Resultant Matrix
        System.out.println("\nResultant Matrix (A + B):");
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                System.out.print(C[i][j] + " ");
            }
            System.out.println();
        }

        // Determine nature
        boolean allOdd = true;
        boolean allEven = true;

        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                if (C[i][j] % 2 == 0)
                    allOdd = false;
                else
                    allEven = false;
            }
        }

        System.out.print("\nNature of resultant matrix: ");
        if (allOdd)
            System.out.println("Odd");
        else if (allEven)
            System.out.println("Even");
        else
            System.out.println("Mixed");

        sc.close();
    }
}

```

## Output:

<img width="555" height="418" alt="image" src="https://github.com/user-attachments/assets/08c504f2-6be1-47c8-974e-68f7341b1b34" />


## Result:
Thus, the java program to evaluate weather the given Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension and find the nature of resultant matrrix is implemented successfully.
