# Ex.No:5(D) THREAD PRIORITY

## QUESTION:

Write a java program for determine the priority and name of the current thread.
## AIM:
To read text input and print only the lines that contain the word "Java".

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read multiple lines from the user until "exit" is entered.
4. Store only those lines that contain the word "Java".
5. When the user types "exit", print all saved lines.
6. Continue reading until input ends or more "Java" lines appear.
7. At EOF, print any remaining lines containing "Java".





## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: SRIKAAVYAA T
RegisterNumber:  212223230214
*/
import java.util.Scanner;

public class ThreadDetails {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Read thread name from user
        String name = sc.nextLine();

        // Get current thread
        Thread t = Thread.currentThread();

        // Set the name
        t.setName(name);

        // Display required output
        System.out.println("Priority of Thread: " + t.getPriority());
        System.out.println("Name of Thread: " + t.getName());
        System.out.println(t);

        sc.close();
    }
}
```


## OUTPUT:

<img width="682" height="192" alt="image" src="https://github.com/user-attachments/assets/941abf0f-44ef-4ef6-8d73-f0402be0e02c" />


## RESULT:
The program successfully filters and prints only the lines that include the word "Java", ignoring all others.

