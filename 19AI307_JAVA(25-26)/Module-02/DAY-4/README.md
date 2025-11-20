# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Create a constructor in a class and call a normal method from it. 

## AIM:
To demonstrate calling a normal method from a constructor in a Java class.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Define a class with instance variables for name and score.
4. Create a constructor that initializes these variables with user-provided values.
5. Define a normal method to print the student’s details and their result status.
6. In the main method, read input values and create an object of the class.
7. Call the normal method to display the student information.





## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: SRIKAAVYAA T
RegisterNumber:  212223230214
*/
import java.util.Scanner;
public class Main{
    public static void main(String args[])
    {
        Scanner scan=new Scanner(System.in);
        String name=scan.nextLine();
        int score=scan.nextInt();
        Demo ob=new Demo(name,score);
        ob.method();
    }
}
class Demo{
    String name;
    int score;
    
    Demo(String n,int s)
    {
        name=n;
        score=s;
    }
    public void method()
    {
        System.out.println("Student Name: "+name);
        System.out.println("Marks Scored: "+score);
        if(score>=40)
        {
            System.out.println("Status: Pass");
        }
        else
        {
            System.out.println("Status: Fail");
        }
    }  
}
```


## OUTPUT:

<img width="546" height="230" alt="image" src="https://github.com/user-attachments/assets/92779fee-8e99-40cf-b99c-b5999e61282e" />


## RESULT:
The program displays the student's name, marks, and pass/fail status using a method invoked after object creation.
