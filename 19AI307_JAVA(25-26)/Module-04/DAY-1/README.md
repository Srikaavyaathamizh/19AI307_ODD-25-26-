# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
You wrote a program that stores some input strings into a String array and prints each string in uppercase.
However, you're getting a NullPointerException.
What should you check in your array before calling .toUpperCase() on a element?

## AIM:
To find the most likely sequence of hidden states (Sunny/Rainy) from a given observation sequence (happy/sad) using the Hidden Markov Model.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Define the transition matrix for moving between hidden states.
4. Define the emission matrix for observation probabilities.
5. Set the initial state probabilities.
6. Apply Forward algorithm to compute probabilities for each observation.
7. Apply Viterbi algorithm to predict the most likely hidden state sequence.
8. Display the predicted hidden states.





## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: SRIKAAVYAA T
RegisterNumber:  212223230214
*/
import java.util.Scanner;
public class UppercaseStrings {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String input = sc.nextLine();
        if (input.equalsIgnoreCase("null")) {
            System.out.println("Null element");
        } else {
            System.out.println(input.toUpperCase());
        }
        sc.close();
    }
}
```

## OUTPUT:
![Uploading image.png…]()



## RESULT:
The sequence of hidden states corresponding to the given observations was successfully computed using the Hidden Markov Model.
