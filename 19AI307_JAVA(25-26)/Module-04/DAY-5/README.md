# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Build a simple Air Traffic Control System where multiple Airplane objects request landing through a central mediator.

## AIM:
To implement the Mediator design pattern by creating a central Air Traffic Control system that manages landing requests from multiple airplanes.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create an AirTrafficControl class acting as the mediator that decides whether an airplane can land.
4. Maintain a runway status and handle landing permissions through requestLanding().
5. Create an Airplane class that sends landing requests to the mediator instead of managing landing logic itself.
6. Read airplane names and landing behavior from the user in the main program.
7. For each airplane, request landing through the mediator and display the corresponding output.





## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: SRIKAAVYAA T
RegisterNumber:  21223230214
*/
import java.util.*;

class AirTrafficControl {
    private boolean runwayFree = true;

    public boolean requestLanding(Airplane airplane) {
        if (runwayFree) {
            runwayFree = false;
            System.out.println(airplane.getName() + " granted landing.");
            return true;
        } else {
            System.out.println(airplane.getName() + " denied landing. Runway busy.");
            return false;
        }
    }

    public void releaseRunway() {
        runwayFree = true;
    }
}

class Airplane {
    private String name;
    private AirTrafficControl control;

    public Airplane(String name, AirTrafficControl control) {
        this.name = name;
        this.control = control;
    }

    public String getName() {
        return name;
    }

    public void requestLanding(boolean releaseAfterLanding) {
        boolean allowed = control.requestLanding(this);
        if (allowed) {
            System.out.println(name + " landed successfully.");
            if (releaseAfterLanding) {
                control.releaseRunway();
            }
        }
    }
}

public class AirTrafficSystem {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        AirTrafficControl control = new AirTrafficControl();

        int n = Integer.parseInt(sc.nextLine()); // number of airplanes
        boolean release = sc.nextLine().equalsIgnoreCase("true"); // release after landing?

        List<Airplane> airplanes = new ArrayList<>();
        for (int i = 0; i < n; i++) {
            String name = sc.nextLine();
            airplanes.add(new Airplane(name, control));
        }

        for (Airplane plane : airplanes) {
            plane.requestLanding(release);
        }

        sc.close();
    }
}
```

## OUTPUT:

<img width="980" height="218" alt="image" src="https://github.com/user-attachments/assets/0e752771-b129-42c2-ba68-662777a5a414" />


## RESULT:
The program successfully simulates an Air Traffic Control system where multiple airplanes request landing through a single mediator, ensuring controlled and coordinated landings.
