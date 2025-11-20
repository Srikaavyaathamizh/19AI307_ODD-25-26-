# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:
A library charges a fine for every book returned late. For first 5 days the fine is 50 paise, for 6-10 days fine is one rupee and above 10 days fine is 5 rupees. If you return the book after 30 days your membership will be cancelled - Print ("Your Membership would be Cancelled.")
Write a program to accept the number of days the member is late to return the book and display the fine or the appropriate message

## AIM:
To calculate the library fine based on the number of late days and display the fine or membership cancellation message.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the number of late days from the user.
4. If days ≤ 5, compute fine as 0.50 per day.
5. Else if days ≤ 10, compute fine as 1 rupee per day.
6. Else if days ≤ 30, compute fine as 5 rupees per day.
7. If days > 30, print membership cancellation message along with the fine.

## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
Developed by: SRIKAAVYAA T
RegisterNumber:  212223230214
*/
import java.util.Scanner;
public class Main{
    public static void main(String args[])
    {
        Scanner scan=new Scanner(System.in);
        int days=scan.nextInt();
        double fine=0.0;        
        if(days<5)
        {
            fine=days*0.50;
        }
        else if(days<=10)
        {
            fine=days*1.00;
        }
        else if(days<=30)
        {
            fine=days*5.00;
        }
        else
        {
            fine=days*5.00;
        }
       System.out.printf("Fine Amount Pay to Rs :%.2f\n",fine);
       if(days>30){
           System.out.println("Your Membership would be Cancelled.");
           
       }
    }
}
```

## OUTPUT:

<img width="875" height="206" alt="image" src="https://github.com/user-attachments/assets/58acc9eb-8b07-4c95-9cf3-7036b7fe5749" />


## RESULT:
The program outputs the fine amount, and if days exceed 30, it displays that the membership is cancelled.

