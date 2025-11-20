# Ex.No:3(b) POLYMORPHISM

## QUESTION:
Write a Java program to calculate simple interest using method overloading for different time durations.
You are asked to build a Bank Interest Calculator that uses method overloading to compute simple interest based on:
Standard 1-year duration
User-defined number of years
The program should:
Prompt the user to enter the principal amount and rate of interest
Ask whether the user wants to enter a custom time duration or use the default 1-year duration
Based on the user input, call the appropriate overloaded method to compute and display the interest

## AIM:
To calculate simple interest using method overloading for different time durations in Java.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Start the program and create a class containing two overloaded calculateInterest methods.
4. Read principal amount and rate of interest from the user using Scanner.
5. Ask the user whether they want to enter a custom time duration.
6. Based on the user’s response, call the appropriate overloaded method with or without the time parameter.
7. Display the calculated simple interest and terminate the program.





## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: SRIKAAVYAA T
RegisterNumber:  212223230214
*/
import java.util.Scanner;
class prog {
    void calculateInterest(double principal, double rate) {
        double interest = (principal * rate * 1) / 100;
        System.out.println("Interest for 1 year: ₹" + interest);
    }
    void calculateInterest(double principal, double rate, int time) {
        double interest = (principal * rate * time) / 100;
        System.out.println("Interest for " + time + " years: ₹" + interest);
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        prog bank = new prog();
        double principal = sc.nextDouble();
        double rate = sc.nextDouble();
        sc.nextLine(); 
        String choice = sc.nextLine();
        if (choice.equalsIgnoreCase("yes")) {
            int time = sc.nextInt();
            bank.calculateInterest(principal, rate, time);
        } else {
            bank.calculateInterest(principal, rate);
        }
        sc.close();
    }
}

```



## OUTPUT:

<img width="701" height="261" alt="image" src="https://github.com/user-attachments/assets/9ed62d12-01a4-417e-947f-c0b2f2df36e6" />


## RESULT:
The program successfully calculates simple interest using either the default 1-year duration or a user-defined time period.
