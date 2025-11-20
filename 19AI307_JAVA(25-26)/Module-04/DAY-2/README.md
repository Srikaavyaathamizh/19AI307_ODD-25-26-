# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
At an international airport, only one Radar Control Tower exists. This tower is responsible for handling all flight communications regardless of how many flights are coming in. Each incoming flight must contact this tower to register its approach.
To ensure safety and consistency, all flights must communicate with the same instance of the tower. If multiple towers are created, it may lead to inconsistent instructions — a huge risk in aviation.
Your task is to simulate this system using the Singleton pattern.
Key Hint (Hidden in Story):
Only one control tower object should exist.
Every flight contacting it should register its name.
You should log the order of flights that contacted the tower.

## AIM:
To implement the Singleton design pattern in Java to ensure that only one Radar Control Tower instance handles all incoming flight registrations.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class RadarControlTower with a private static instance and a private constructor.
4. Implement getInstance() to return the single shared tower object.
5. Store flight names in a list and define registerFlight() to log each contact.
6. In the main class, read the number of flights and their names.
7. For each flight, get the same tower instance and register the flight through it.





## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: SRIKAAVYAA T
RegisterNumber:  212223230214
*/
import java.util.*;

class RadarControlTower {
    private static RadarControlTower instance;
    private List<String> flights = new ArrayList<>();

    // private constructor — prevents creating multiple instances
    private RadarControlTower() {}

    // getInstance() ensures only one instance exists
    public static RadarControlTower getInstance() {
        if (instance == null) {
            instance = new RadarControlTower();
        }
        return instance;
    }

    // Register flight and print message
    public void registerFlight(String flightName) {
        flights.add(flightName);
        System.out.println(flightName + " registered with Radar Control Tower. Total Flights: " + flights.size());
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = Integer.parseInt(sc.nextLine());

        for (int i = 0; i < n; i++) {
            String flightName = sc.nextLine();

            // Get the single tower instance and register flight
            RadarControlTower tower = RadarControlTower.getInstance();
            tower.registerFlight(flightName);
        }

        sc.close();
    }
}
```




## OUTPUT:
<img width="1273" height="235" alt="image" src="https://github.com/user-attachments/assets/ec5cda6c-e5aa-473a-a64f-f5ada77590b0" />



## RESULT:
The program successfully simulates the Radar Control Tower using the Singleton pattern, ensuring all flights communicate with a single tower instance and registering them in proper order.
