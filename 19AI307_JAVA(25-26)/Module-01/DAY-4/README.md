# Ex.No:1(D) ARRAYS

## QUESTION:
Write a Java program to print all elements in an array that are greater than a given value

 

## AIM:
To print all array elements greater than a given value.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the number of elements and store them in an array.
4. Read the value to compare with array elements.
5. Initialize a flag to track if any element is greater than the given value.
6. Traverse the array and print each element that is greater than the given value.
7. If no such element is found, display an appropriate message.





## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
Developed by: SRIKAAVYAA T
RegisterNumber:  212223230214
*/
import java.util.Scanner;

public class Main {
    public static void main(String args[]) {
        Scanner scan = new Scanner(System.in);

        int n = scan.nextInt();
        int arr[] = new int[n];

        for (int i = 0; i < n; i++) {
            arr[i] = scan.nextInt();
        }

        int value = scan.nextInt();

        boolean found = false;
        for (int i = 0; i < n; i++) {
            if (arr[i] > value) {
                System.out.println(arr[i]);
                found = true;
            }
        }

        if (!found) {
            System.out.println("No elements greater than " + value);
        }
    }
}
```

## OUTPUT:

<img width="673" height="238" alt="image" src="https://github.com/user-attachments/assets/59c1f18e-0448-45e3-bb11-16fb4b8d3d9a" />


## RESULT:
The program displays elements greater than the entered value or prints a message if none exist.
