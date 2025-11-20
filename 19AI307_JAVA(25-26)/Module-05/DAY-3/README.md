# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:
Read a file and print only the lines containing the word "Java".

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
Program to implement a File Handling using Java
Developed by: SRIKAAVYAA T
RegisterNumber:  212223230214
*/
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        List<String> javaLines = new ArrayList<>();

        while (sc.hasNextLine()) {
            String line = sc.nextLine().trim();

            if (line.equalsIgnoreCase("exit")) {
                printJavaLines(javaLines);
                javaLines.clear();
            } else {
                if (line.contains("Java")) {
                    javaLines.add(line);
                }
            }
        }

        // If EOF reached and there are still lines not printed
        if (!javaLines.isEmpty()) {
            printJavaLines(javaLines);
        }

        sc.close();
    }

    private static void printJavaLines(List<String> lines) {
        System.out.println("Lines containing the word 'Java':");
        for (String s : lines) {
            System.out.println(s);
        }
    }
}
```

## OUTPUT:

<img width="971" height="302" alt="image" src="https://github.com/user-attachments/assets/acedf185-7725-4ea9-a002-b6cb3060b085" />


## RESULT:
The program successfully filters and prints only the lines that include the word "Java", ignoring all others.
