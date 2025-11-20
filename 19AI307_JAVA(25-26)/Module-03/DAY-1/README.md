# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:
A jewelry store tracks gold rates for different types of customers. The base class is Customer with attributes like customerId, name, and purchaseWeight (in grams). There are two types of customers: RegularCustomer and PremiumCustomer. RegularCustomer gets a fixed discount of 2% on the gold rate per gram. PremiumCustomer gets a 5% discount plus a special cashback. The base gold rate per gram is input at runtime. For each customer, calculate the final price they pay:

## AIM:
To calculate and display the final gold purchase price for different customer types using inheritance and method overriding.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a base Customer class with attributes, a method to compute discounted price, and a display method.
4. Derive two classes: RegularCustomer (2% discount) and PremiumCustomer (5% discount + cashback).
5. Override getDiscountRate() and display() methods in both derived classes.
6. In main(), read customer type and details, create the appropriate object, and call the display() method.
7. Print computed values including discount, final price, and cashback (only for premium customers).





## PROGRAM:
 ```
/*
Program to implement a Inheritance and Aggregation using Java
Developed by: SRIKAAVYAA T
RegisterNumber:  212223230214
*/
import java.util.*;
import java.text.DecimalFormat;
class Customer {
    String customerId, name;
    double purchaseWeight, goldRatePerGram;
    Customer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        this.customerId = customerId;
        this.name = name;
        this.purchaseWeight = purchaseWeight;
        this.goldRatePerGram = goldRatePerGram;
    }
    double getDiscountRate() { return 0; }
    double calculateFinalPrice() {
        double discountAmount = goldRatePerGram * getDiscountRate() / 100.0;
        double effectiveRate = goldRatePerGram - discountAmount;
        return purchaseWeight * effectiveRate;
    }
    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        DecimalFormat dfDisc = new DecimalFormat("0.#");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: General");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + dfDisc.format(getDiscountRate()) + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
    }
}
class RegularCustomer extends Customer {
    RegularCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }
    double getDiscountRate() { return 2; }
    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        DecimalFormat dfDisc = new DecimalFormat("0.#");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: Regular");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + dfDisc.format(getDiscountRate()) + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
    }
}
class PremiumCustomer extends Customer {
    PremiumCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }
    double getDiscountRate() { return 5; }
    double getCashback() { return calculateFinalPrice() * 0.01; }
    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        DecimalFormat dfDisc = new DecimalFormat("0.#");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: Premium");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + dfDisc.format(getDiscountRate()) + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
        System.out.println("Cashback: " + df.format(getCashback()));
    }
}
public class Main {
    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);      
        while (sc.hasNext()) {
            String type = sc.next();
            if (!sc.hasNext()) break;
            String id = sc.next();
            if (!sc.hasNext()) break;
            String name = sc.next();
            if (!sc.hasNextDouble()) break;
            double weight = sc.nextDouble();
            if (!sc.hasNextDouble()) break;
            double rate = sc.nextDouble();

            Customer c;
            if (type.equalsIgnoreCase("Regular"))
                c = new RegularCustomer(id, name, weight, rate);
            else
                c = new PremiumCustomer(id, name, weight, rate);

            c.display();
        }
        sc.close();
    }
}

```

## OUTPUT:
<img width="791" height="233" alt="image" src="https://github.com/user-attachments/assets/c08d40b4-f2b4-4616-8e58-9a3ebc98d676" />



## RESULT:
The program prints customer details, discount applied, final payable amount, and cashback for premium customers.
