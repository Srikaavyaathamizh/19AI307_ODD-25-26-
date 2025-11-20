# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
You are building customizable robots using the Prototype Pattern. Clone an existing robot template and change its name and feature.

## AIM:
To implement the Prototype Pattern in Java by cloning an existing robot object and displaying both the original and cloned robots.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a Robot class with attributes name and feature.
4. Implement the clone() method to return a new Robot object with the same values (deep copy).
5. Read robot name and feature from the user.
6. Create a prototype robot using the input values.
7. Clone the prototype and display both the original and cloned robot details.





## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: SRIKAAVYAA T
RegisterNumber:  212223230214
*/
import java.util.Scanner;

class Robot implements Cloneable {
    String name, feature;

    Robot(String name, String feature) {
        this.name = name;
        this.feature = feature;
    }

    public Robot clone() {
        return new Robot(name, feature);
    }

    void display(String tag) {
        System.out.println(tag + ": " + name + " - " + feature);
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String name = sc.nextLine();
        String feature = sc.nextLine();

        Robot prototype = new Robot(name, feature);
        Robot cloned = prototype.clone();

        prototype.display("Original Robot");
        cloned.display("Cloned Robot");
    }
}

```

## OUTPUT:

<img width="1170" height="298" alt="image" src="https://github.com/user-attachments/assets/12fcd814-0674-4bb4-ac2e-cd9526b49f07" />


## RESULT:
The program successfully clones the robot using the Prototype Pattern and displays both the original and cloned robot with identical attributes.
The program successfully clones the robot using the Prototype Pattern and displays both the original and cloned robot with identical attributes.
