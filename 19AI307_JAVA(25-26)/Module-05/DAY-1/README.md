# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
Write a program to read user input from the keyboard using InputStreamReader 

## AIM:
To write a program to read user input from the keyboard using InputStreamReader 

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create main class and method
4.	Set up input reader
5.	Use BufferedReader to read input from console.
6.	Print output using System.out.println().
7.	Wrap in try-catch to handle IOException.

## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by: SRIKAAVYAA T
RegisterNumber:  212223230214
*/
```

## SOURCE CODE:

```
import java.io.*;

public class Main {
    public static void main(String[] args) {
        System.out.print(""); 
        try {
            InputStreamReader isr = new InputStreamReader(System.in);
            BufferedReader br = new BufferedReader(isr);

            
            String name = br.readLine();

            
            System.out.println("Hello, " + name + "!");
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}
```


## OUTPUT:
<img width="857" height="235" alt="image" src="https://github.com/user-attachments/assets/e64ae583-62cb-4714-bc2a-e9ae5aa9ecde" />



## RESULT:
Thus the program to read user input from the keyboard using InputStreamReader has been executed successfully.
