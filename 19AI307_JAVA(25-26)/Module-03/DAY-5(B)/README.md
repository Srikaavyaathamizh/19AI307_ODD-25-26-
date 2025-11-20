# Ex.No:3(F) WRAPPER CLASS

## QUESTION:
Write a Java program to check if a number is an Armstrong number using Math.pow() and the Integer wrapper class. Take input from the user.

## AIM:
To create an inner class in Java and access its methods through an object of the outer class.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Define an outer class Out with a constructor to initialize the name.
4. Create an inner class In inside Out containing a method that prints a message.
5. In the main program, read the user's name as input.
6. Create an object of the outer class and then create an inner class object using it.
7. Call the inner class method to display the greeting message.





## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by: SRIKAAVYAA T
RegisterNumber:  212223230214
*/
import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = Integer.parseInt(sc.nextLine()); // Using Integer wrapper class
        int originalNum = num;
        int sum = 0;
        int digits = String.valueOf(num).length();  // number of digits
        while (num > 0) {
            int digit = num % 10;
            sum += Math.pow(digit, digits); // Using Math.pow()
            num /= 10;
        }
        if (sum == originalNum) {
            System.out.println(originalNum + " is an Armstrong number.");
        } else {
            System.out.println(originalNum + " is not an Armstrong number.");
        }
    }
}
```


## OUTPUT:

<img width="770" height="242" alt="image" src="https://github.com/user-attachments/assets/0fb56db6-756c-4298-b905-909cf851912d" />


## RESULT:
The program successfully creates an inner class object and displays a message using data from the outer class.
