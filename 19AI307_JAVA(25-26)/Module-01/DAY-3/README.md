# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
Count Digits in a Number

## AIM:
To count the number of digits in a given integer.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read an integer input from the user.
4. Initialize a counter to zero.
5. Use a loop that runs until the number becomes zero.
6. In each iteration, increment the counter and divide the number by 10.
7.After the loop ends, print the final digit count.





## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
Developed by: SRIKAAVYAA T
RegisterNumber:  21222323214
*/
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int count=0;
        while(n!=0){
            count+=1;
            n=n/10;
        }

        System.out.println("Digit count: " + count);
    }
}
```

## OUTPUT:
<img width="473" height="232" alt="image" src="https://github.com/user-attachments/assets/68ae4fed-836c-42f5-8e87-e812bb2c58be" />



## RESULT:

The program prints the total number of digits in the entered number.
