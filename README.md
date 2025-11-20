# Module 6
# EX 1 You’re creating a health monitoring device which stores several sensor readings in an array. To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.
## DATE: 05/08/25
## AIM:
To write a JAVA program To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.

## Algorithm
1.Start

2.Read the number of elements (e.g., number of heartbeat readings).

3.Store all readings in an array.

4.Call a recursive function findMin(arr, index)

If index == arr.length - 1, return arr[index]

Else return min(arr[index], findMin(arr, index + 1))

5.Print the minimum value returned by the recursive function.

6.End   

## Program:
```
/*
Program To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.
Developed by: MOHAMMAD SHAHIL
RegisterNumber: 212223240044
*/

import java.util.*;

public class Main {
    static int getMin(int[] arr, int i, int n) {
        if (i == n - 1) {
            return arr[i];
        }

    
        int minRest = getMin(arr, i + 1, n);
       
        return Math.min(arr[i], minRest);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr = new int[n];
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }
        System.out.println(getMin(arr, 0, n));
    }
}

```

## Output:
<img width="649" height="254" alt="513661235-6f3bd15f-b306-4db4-a188-983042447943" src="https://github.com/user-attachments/assets/5ed25ab5-69f7-4f51-b1cc-e16321385233" />



## Result:
Thus the JAVA program to find the minimum value (e.g., lowest heartbeat), implement a recursive method has implemented successfully.


# Ex2 Count how many times a number appears in an array recursively.
## DATE:07/08/2025
## AIM:
To write a Java program to Count how many times a number appears in an array recursively.

## Algorithm:

1.Read the size of the array and its elements.

2.Read the target number to be counted.

3.Call the recursive function countOccurrences(arr, n, target).

4.In recursion: if size becomes 0, return 0; otherwise check the last element and add 1 if it matches the target.

5.Display the final count returned by the recursive function.

## Program:
```
/*
Program Count how many times a number appears in an array recursively.
Developed by: MOHAMMAD SHAHIL
RegisterNumber: 212223240044
*/
import java.util.Scanner;

public class CountOccurrences {

    // Recursive function to count occurrences of a target number
    public static int countOccurrences(int[] arr, int n, int target) {
        //write your code here
        if (n == 0) {
            return 0;
        }

        // Check the last element and add 1 if it matches the target
        if (arr[n - 1] == target) {
            return 1 + countOccurrences(arr, n - 1, target);
        } else {
            return countOccurrences(arr, n - 1, target);
        }
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Input: Size of array
        int size = scanner.nextInt();

        if (size <= 0) {
            System.out.println("Invalid array size. Must be positive.");
            return;
        }

        // Input: Array elements
        int[] arr = new int[size];
        for (int i = 0; i < size; i++) {
            arr[i] = scanner.nextInt();
        }

        // Input: Target number to count
        int target = scanner.nextInt();

        // Compute and display result
        int count = countOccurrences(arr, size, target);
        System.out.println("The number " + target + " appears " + count + " time(s) in the array.");

        scanner.close();
    }
}

```

## Output:

<img width="1027" height="611" alt="513663344-6c352262-b618-42ca-895f-669f0cff5116" src="https://github.com/user-attachments/assets/afab4665-5514-4c2e-96e0-baa8c69fa85b" />



## Result:
Thus, the Java program to Count how many times a number appears in an array recursively is implemented successfully.


# EX3 Write a program to count the number of digits in an integer.
## DATE:12/08/2025
## AIM:
To write a Java program to implement Tower of Hanoi

## Algorithm
1.Start the program.  

2.Read an integer from the user.

3.Define a recursive function countDigits() that counts digits by dividing the number by 10 each time. 

4.Base condition: if the number is 0, return 0. 

5.Recursive step: return 1 + countDigits(number / 10).

6.Display the total count of digits. 7.Stop the program.

## Program:
```
/*
Program to to count the number of digits in an integer
Developed by: MOHAMMAD SHAHIL
RegisterNumber: 212223240044
*/

import java.util.Scanner;

public class CountDigits {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
     
        int num = sc.nextInt();
        
        int count = 0;
        int n = Math.abs(num); 
        
        
        if (n == 0) {
            count = 1;
        } else {
            while (n > 0) {
                n = n / 10;  
                count++;
            }
        }
        
        System.out.println("Number of digits: " + count);

        sc.close();
    }
}

```

## Output:

<img width="601" height="242" alt="image" src="https://github.com/user-attachments/assets/132a7a2a-95ea-4d65-a908-0268fc16eb32" />





## Result:
Thus, the Java program to to count the number of digits in an integer is implemented successfully.



# Ex4 You are given a Java program that performs matrix addition. If Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension, what will be the nature (even/odd/mixed) of the resulting matrix?
## DATE:14/08/2025
## AIM:
To write a java function to evaluate weather the given Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension and find the nature of resultant matrrix.

## Algorithm
1.Start the program.

2.Read the dimensions of both matrices (rows and columns). Check whether Matrix A and Matrix B have the same dimensions. If not, display “Matrices are not of same dimension” and stop.

3.Read Matrix A and check each element:
If every element is odd, continue.

4.If any element is even, mark A as invalid and stop further checking.

5.Read Matrix A and check each element:
If every element is odd, continue.

6.If any element is even, mark A as invalid and stop further checking.

7.If both matrices are valid, compute the resultant matrix (e.g., A + B or any operation specified). Determine the nature of the resultant matrix:

8.If all elements are odd, print “Resultant matrix is an Odd Matrix”.

9.If all elements are even, print “Resultant matrix is an Even Matrix”.
Otherwise, print “Resultant matrix is a Mixed Matrix”.

10.Display the Resultant Matrix.

11.Stop the program.  

## Program:
```
/*
Program to ind the nature of resultant matrrix.
Developed by: MOHAMMAD SHAHIL
RegisterNumber: 212223240044
*/
import java.util.Scanner;

public class MatrixAddition {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int rows = sc.nextInt();
        int cols = sc.nextInt();

        int[][] A = new int[rows][cols];
        int[][] B = new int[rows][cols];
        int[][] result = new int[rows][cols];

        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                A[i][j] = sc.nextInt();
            }
        }
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                B[i][j] = sc.nextInt();
            }
        }
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                result[i][j] = A[i][j] + B[i][j];
            }
        }
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                System.out.print(result[i][j] + " ");
            }
            System.out.println();
        }

       
    }
}


```

## Output:

<img width="422" height="624" alt="513775109-34782319-f865-4fe8-a281-f3aed6852160" src="https://github.com/user-attachments/assets/f2acdaf8-1bf9-4fba-af82-b724d681291b" />




## Result:
Thus, the java program to evaluate weather the given Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension and find the nature of resultant matrrix is implemented successfully.



# Ex5 Count Inversions in an Array
## DATE:19/08/2025
## AIM:
To write a Java program  to Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < j

## Algorithm
1.Start the program.

2.Read the number of elements and store them in an array.

3.Use a modified merge sort to count inversions: .Recursively split the array into halves and count inversions in each half. .While merging two sorted halves,

4.count cross inversions when an element from the right half is placed before elements remaining in the left half.

5.Sum inversions from left half, right half, and cross inversions.

6.Display the total inversion count.

7.Stop the program. 

## Program:
```
/*
Program toto Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < j
Developed by: MOHAMMAD SHAHIL
RegisterNumber: 212223240044
*/
import java.util.Scanner;

public class CountInversions {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        int[] arr = new int[n];

        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        long result = mergeSortAndCount(arr, 0, n - 1);
        System.out.println(result);
    }

    private static long mergeSortAndCount(int[] arr, int left, int right) {
        long count = 0;
        if (left < right) {
            int mid = (left + right) / 2;
            count += mergeSortAndCount(arr, left, mid);
            count += mergeSortAndCount(arr, mid + 1, right);
            count += mergeAndCount(arr, left, mid, right);
        }
        return count;
    }

    private static long mergeAndCount(int[] arr, int left, int mid, int right) {
        int[] leftArr = new int[mid - left + 1];
        int[] rightArr = new int[right - mid];

        System.arraycopy(arr, left, leftArr, 0, leftArr.length);
        System.arraycopy(arr, mid + 1, rightArr, 0, rightArr.length);

        int i = 0, j = 0, k = left;
        long swaps = 0;

        while (i < leftArr.length && j < rightArr.length) {
            if (leftArr[i] <= rightArr[j]) {
                arr[k++] = leftArr[i++];
            } else {
                arr[k++] = rightArr[j++];
                swaps += (mid + 1) - (left + i);
            }
        }

        while (i < leftArr.length) {
            arr[k++] = leftArr[i++];
        }
        while (j < rightArr.length) {
            arr[k++] = rightArr[j++];
        }

        return swaps;
    }
}


```

## Output:
<img width="1232" height="337" alt="image" src="https://github.com/user-attachments/assets/1c867a54-301a-46d6-b6a9-c4446e695ec5" />




## Result:
Thus the Java program to to Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < j is implemented successfully.

