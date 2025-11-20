# Ex.No:3(E) INNER CLASS

## QUESTION:
Write a Java program to create an inner class and access it from the outer class.

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
Program to implement a InnerClass using Java
Developed by: SRIKAAVYAA T
RegisterNumber:  212223230214
*/
import java.util.Scanner;
class Out{
    String name;    
    Out(String n)
    {
        name=n;
    }
    class In{
        void method()
        {
            System.out.println("Hello, "+name+"! This message is from the Inner Class.");
            
        }        
    }
}
public class Main{
    public static void main(String args[])
    {
        Scanner scan=new  Scanner(System.in);
        String name=scan.nextLine();
        Out ob=new Out(name);
        Out.In ob1=ob.new In();
        ob1.method();
    }
}
```


## OUTPUT:

<img width="1123" height="237" alt="image" src="https://github.com/user-attachments/assets/2ee33f2e-03fb-4928-8092-e4c45a91bf70" />


## RESULT:
The program successfully creates an inner class object and displays a message using data from the outer class.
