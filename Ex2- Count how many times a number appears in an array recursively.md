
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
