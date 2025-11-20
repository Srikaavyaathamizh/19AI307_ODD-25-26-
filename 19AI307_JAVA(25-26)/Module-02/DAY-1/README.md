# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Define a class Teacher with attributes: name (String), subject (String), and experience (int, years). 


## AIM:
To define a Teacher class and display a teacher’s details including name, subject, and years of experience.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Define a Teacher class with attributes: name, subject, and experience.
4. Read the teacher’s name, subject, and years of experience from the user.
5. Create an object of the Teacher class.
6. Pass the input values to a method that displays the teacher's details.
7.Print the output in the required format using the method.



## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: SRIKAAVYAA T 
RegisterNumber:  2122223230214
*/
import java.util.Scanner;
public class Main{
    public static void main(String args[])
    {
        Scanner scan=new Scanner(System.in);
        Teacher obj=new Teacher();
        String a=scan.nextLine();
        String b=scan.nextLine();
        int c=scan.nextInt();
        obj.method(a,b,c);
    }
}
class Teacher{
    String name;
    String subject;
    int year;  
    public void method(String name,String subject,int year)
    {
        System.out.println("Mr. "+name+" teaches "+subject+" and has "+year+" years experience.");
    }
}
```


## OUTPUT:

<img width="1186" height="228" alt="image" src="https://github.com/user-attachments/assets/b7bc30f4-90cb-4fdf-ad3f-f18ad4ee0e6d" />


## RESULT:
The program prints a formatted message showing the teacher's name, subject taught, and experience
