# Ex5 Count Inversions in an Array
## DATE:10/11/25
## AIM:
To write a Java program  to Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < j

## Algorithm
1. Start the program.
2. Declare an array arr[] and a variable count = 0 to store the number of inversions.
3. Read the array elements from the user.
4.  For each pair of elements (arr[i], arr[j]), check if arr[i] > arr[j] and i < j.
5.   If the above condition is true, increment the inversion count.
6.   Continue until all pairs are checked.
7.   Display the total number of inversions found in the array.
8.   Stop the program.

## Program:
```
/*
Program to Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < j
Developed by: Dilli babu K
Register Number: 212224110015
*/

import java.util.Scanner;

public class CountInversions {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter the size of the array: ");
        int n = sc.nextInt();
        int[] arr = new int[n];

        System.out.println("Enter the elements of the array:");
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        int count = 0;

        // Check all pairs (i, j)
        for (int i = 0; i < n - 1; i++) {
            for (int j = i + 1; j < n; j++) {
                if (arr[i] > arr[j]) {
                    count++;
                }
            }
        }

        System.out.println("\nNumber of inversions: " + count);
        sc.close();
    }
}

```

## Output:

<img width="586" height="300" alt="image" src="https://github.com/user-attachments/assets/765b585c-c040-476b-a822-051fe4b9e10a" />


## Result:
Thus the Java program to to Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < jis implemented successfully.
