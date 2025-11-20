# Ex.No:3(C) ABSTRACTION

## QUESTION:
A group of researchers receives mysterious numerical sequences believed to be sent by intelligent alien life. To decode them, scientists have built intelligent SignalAgents that follow abstract processing rules. Each agent listens to the numbers differently.
Your task is to create a system where a base abstract class SignalAgent declares:
java
Copy
Edit
abstract int decodeSignal(int[] signal);
Two intelligent agents extend this class:
PrimeAgent
MirrorAgent
🧩 Agent Behaviors (Described Indirectly):
🔍 PrimeAgent
This agent believes the signal's meaning lies in rarity. It scans the signal, only considers prime numbers, and returns the sum of them.
MirrorAgent
This one trusts symmetry. It compares elements from both ends inward. If all such pairs are perfectly symmetric (same from left and right), it considers the message balanced, otherwise broken.

## AIM:
To decode numerical signals using abstract classes and polymorphism through PrimeAgent and MirrorAgent.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Define an abstract class SignalAgent with an abstract method decodeSignal.
4. Implement PrimeAgent to identify prime numbers in the signal and return their sum.
5. Implement MirrorAgent to check symmetry of the signal from both ends.
6. In the main program, read the signal values and the user’s choice of agent.
7. Create the chosen agent object, call decodeSignal, and display the corresponding output.





## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by: SRIKAAVYAA T
RegisterNumber:  212223230214
*/
import java.util.*;
abstract class SignalAgent {
    abstract int decodeSignal(int[] signal);
}
class PrimeAgent extends SignalAgent {
    private boolean isPrime(int num) {
        if (num < 2) return false;
        for (int i = 2; i <= Math.sqrt(num); i++) {
            if (num % i == 0)
                return false;
        }
        return true;
    }
    @Override
    public int decodeSignal(int[] signal) {
        int sum = 0;
        for (int n : signal) {
            if (isPrime(n))
                sum += n;
        }
        return sum;
    }
}
class MirrorAgent extends SignalAgent {
    @Override
    public int decodeSignal(int[] signal) {
        int left = 0, right = signal.length - 1;
        while (left < right) {
            if (signal[left] != signal[right])
                return 0;  // not balanced
            left++;
            right--;
        }
        return 1;  // balanced
    }
}
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] signal = new int[n];
        for (int i = 0; i < n; i++) {
            signal[i] = sc.nextInt();
        }
        int type = sc.nextInt();

        SignalAgent agent;
        if (type == 1)
            agent = new PrimeAgent();
        else
            agent = new MirrorAgent();

        int result = agent.decodeSignal(signal);

        if (type == 1)
            System.out.println(result);
        else
            System.out.println(result == 1 ? "BALANCED" : "BROKEN");
    }
}
```


## OUTPUT:
<img width="410" height="287" alt="image" src="https://github.com/user-attachments/assets/3aba01cf-247a-4df7-a1be-d20c7d3bcb36" />



## RESULT:
The program successfully processes signals using the selected agent and outputs either the sum of primes or whether the signal is BALANCED or BROKEN.
