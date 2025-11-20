# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Define class Game with: Static variable maxScore = 500 Print max score via 3 different object references. Change via one object into 800, and print the output of previous maxScore and changed maxScore. 

## AIM:
To demonstrate calling a normal method from a constructor in a Java class.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Define a class with instance variables for name and score.
4. Create a constructor that initializes these variables with user-provided values.
5. Define a normal method to print the student’s details and their result status.
6. In the main method, read input values and create an object of the class.
6. Call the normal method to display the student information.





## PROGRAM:
 ```
/*
Program to implement a Access Modifiers using Java
Developed by: SRIKAAVYAA T
RegisterNumber:  212223230214
*/
class Game{
    static int maxScore=500;
    
    Game(){
        
    }
    
    Game(int m)
    {
        maxScore=m;
    }
}
public class Main{
    public static void main(String args[]){
        Game ob=new Game();
        System.out.println(ob.maxScore);
        Game ob1=new Game();
        System.out.println(ob1.maxScore); 
        Game ob2=new Game();
        System.out.println(ob2.maxScore);
        Game ob3=new Game(800);
        System.out.println(ob3.maxScore);
        Game ob4=new Game(800);
        System.out.println(ob4.maxScore); 
        Game ob5=new Game(800);
        System.out.println(ob5.maxScore);
        
    }
}
```


## OUTPUT:
<img width="266" height="264" alt="image" src="https://github.com/user-attachments/assets/2f7541ed-b00d-40a5-80ed-88d1cfd42bcf" />



## RESULT:
The program displays the student's name, marks, and pass/fail status using a method invoked after object creation.
