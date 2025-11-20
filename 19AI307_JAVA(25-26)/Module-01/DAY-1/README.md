# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:
Lovely is entering a battle arena tournament, but only heroes who meet specific power and skill criteria are allowed inside.
To enter the arena, a hero (Lovely) must satisfy any one of these conditions:
Her power level is above 80 and her rank is above 5
→ (power > 80 && rank > 5)
Or she has a magic orb and her experience is at least 3 years
→ (hasMagicOrb == true && experience >= 3)
Note: If either of the above conditions is satisfied, she is allowed to enter. Otherwise, she is rejected.

## AIM:
To determine whether Lovely can enter the battle arena based on her power, rank, magic orb possession, and experience.

## ALGORITHM :
1.	Read inputs: power, rank, hasMagicOrb, and experience.
2. Check if power > 80 and rank > 5.
3. Check if hasMagicOrb is true and experience ≥ 3.
4. Combine both conditions using OR to determine eligibility.
5. Print whether Lovely can enter the arena based on the final result.

## PROGRAM:
 ```
/*
Program to implement variables and Operators using Java
Developed by: SRIKAAVYAA T
RegisterNumber:  212223230124
*/
import java.util.Scanner;
public class Main {
    public static void main(String args[]) {
        Scanner scan = new Scanner(System.in);

        int power = scan.nextInt();
        int rank = scan.nextInt();
        boolean hasMagicOrb = scan.nextBoolean();
        int experience = scan.nextInt();

        boolean canEnter = (power > 80 && rank > 5) || (hasMagicOrb && experience >= 3);

        System.out.println("Can Enter Arena: " + canEnter);
    }
}
```

## OUTPUT:

<img width="594" height="281" alt="image" src="https://github.com/user-attachments/assets/4cdb6d03-f3db-43a9-bd9d-7e5589bf3645" />


## RESULT:
The program outputs true if Lovely meets the entry conditions; otherwise it outputs false.
