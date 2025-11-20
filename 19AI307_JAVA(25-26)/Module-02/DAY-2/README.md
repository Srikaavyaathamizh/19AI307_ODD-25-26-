# Ex.No:2(B) METHODS

## QUESTION:
Write a method void modifyValue(int num) that tries to modify the passed value(add passed value with 10) and print "Inside method: "+num . 
Show in main() that the original value does not change.
After calling modifyValue(int num) method in main , print the "Outside method: "+num

## AIM:
To demonstrate that Java uses pass-by-value, so modifying a method parameter does not change the original variable.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read an integer value from the user.
4. Call the modifyValue(int num) method with the entered value.
5. Inside the method, add 10 to the passed value and print it.
6. Return to the main method after the method call.
7. Print the original value again in main to show it is unchanged.





## PROGRAM:
 ```
/*
Program to implement a Methods using Java
Developed by: SRIKAAVYAA T
RegisterNumber:  212223230214
*/
import java.util.Scanner;
class Method{
    void modifyValue(int num)
    {
        num=num+10;
        System.out.println("Inside method: "+num);
    }    
}
public class Main{
    public static void main(String args[])
    {
        Scanner scan=new Scanner(System.in);
        int num=scan.nextInt();        
        Method ob=new Method();
        ob.modifyValue(num);        
        System.out.println("Outside method: "+num);        
    }
}
```

## OUTPUT:

<img width="506" height="162" alt="image" src="https://github.com/user-attachments/assets/60744a31-eba7-47e4-9d1a-5012b57588db" />


## RESULT:
The program shows different values inside and outside the method, proving the original value remains unchanged.
