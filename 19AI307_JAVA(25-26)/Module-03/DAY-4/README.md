# Ex.No:3(D)    INTERFACE 

## QUESTION:
You are programming bots that analyze weather data. Each bot must implement a common interface and give a prediction.
 Bot Types:
SunBot: Predicts "HOT" if temperature > 30, else "MODERATE".
RainBot: Predicts "COLD" if temperature < 20, else "WARM".

## AIM:
To implement weather-prediction bots using a common interface and polymorphism in Java.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Define a WeatherBot interface with a predict method for temperature-based predictions.
4. Implement SunBot to return "HOT" or "MODERATE" depending on temperature.
5. Implement RainBot to return "COLD" or "WARM" based on the temperature value.
6. Read temperature and bot selection from the user in the main method.
7. Create the chosen bot object, call predict, and display the predicted weather condition.





## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by: SRIKAAVYAA T
RegisterNumber: 212223230214 
*/
import java.util.Scanner;
interface WeatherBot {
    String predict(int temperature);
}
class SunBot implements WeatherBot {
    public String predict(int temperature) {
        if (temperature > 30)
            return "HOT";
        else
            return "MODERATE";
    }
}
class RainBot implements WeatherBot {
    public String predict(int temperature) {
        if (temperature < 20)
            return "COLD";
        else
            return "WARM";
    }
}
public class WeatherPrediction {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int temperature = sc.nextInt();
        int botType = sc.nextInt();

        WeatherBot bot;

        if (botType == 1)
            bot = new SunBot();
        else
            bot = new RainBot();

        System.out.println(bot.predict(temperature));
        sc.close();
    }
}
```


## OUTPUT:

<img width="326" height="143" alt="image" src="https://github.com/user-attachments/assets/e9307cca-b3b4-4a40-a079-ef36ea5621b5" />


## RESULT:

The program successfully predicts weather conditions using either SunBot or RainBot based on user input.
