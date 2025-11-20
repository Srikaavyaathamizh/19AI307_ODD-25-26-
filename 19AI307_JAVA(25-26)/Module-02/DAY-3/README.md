# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to create a class called BankAccount with private instance variables accountNumber and balance. Provide public getter and setter methods to access and modify these variables.

## AIM:
To create a BankAccount class with private variables and use getter and setter methods to access and update them.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Define a BankAccount class with private variables accountNumber and balance.
4. Provide public setter methods to assign values to these variables.
5. Provide public getter methods to retrieve the stored values.
6. In main, read the account number and balance from the user.
7. Use getter methods to display the stored account details.





## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: SRIKAAVYAA T
RegisterNumber:  212223230214
*/
import java.util.Scanner;
class BankAccount{
    private String accountNumber;
    private double balance;
    
    public String getAccountNumber(){
        return accountNumber;
    }
    public void setAccountNumber(String ac)
    {
        accountNumber=ac;
    }
    public double getBalance(){
        return balance;
    }
    public void setBalance(double bl)
    {
        balance=bl;
    }
}
public class Main{
    public static void main(String args[])
    {
        Scanner scan=new Scanner(System.in);
        BankAccount ob=new BankAccount();
        ob.setAccountNumber(scan.nextLine());
        ob.setBalance(scan.nextDouble());
        String a=ob.getAccountNumber();
        System.out.println("Account Number: "+a);
        double b=ob.getBalance();
        System.out.println("Balance: "+b);     
        }
}
```

## OUTPUT:

<img width="785" height="185" alt="image" src="https://github.com/user-attachments/assets/4e2bb9f3-36c7-45bf-951a-9bfb71340b85" />


## RESULT:
The program displays the entered account number and balance using getter methods.
