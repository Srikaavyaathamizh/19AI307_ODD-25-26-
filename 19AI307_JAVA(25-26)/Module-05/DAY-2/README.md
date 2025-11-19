# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:
Write a Java program to serialize a collection of objects (like ArrayList<Student>) into a file.


## AIM:
To Write a Java program to serialize a collection of objects (like ArrayList<Student>) into a file.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a Student class that implements Serializable.
4.	Serialize the ArrayList of students to a file using ObjectOutputStream.
5.	Deserialize the file back to an ArrayList using ObjectInputStream.
6.	Display all deserialized student objects.

## PROGRAM:
 ```
/*
Program to implement a Serialization and Deserialization using Java
Developed by: 
RegisterNumber:  
*/
```

## SOURCE CODE:

```
import java.io.*;
import java.util.*;

class Student implements Serializable {
    private static final long serialVersionUID = 1L;
    int id;
    String name;
    double marks;

    public Student(int id, String name, double marks) {
        this.id = id;
        this.name = name;
        this.marks = marks;
    }

    @Override
    public String toString() {
        return "Student{id=" + id + ", name='" + name + "', marks=" + marks + "}";
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = Integer.parseInt(sc.nextLine().trim());

        ArrayList<Student> students = new ArrayList<>();

        for (int i = 0; i < n; i++) {
            int id = Integer.parseInt(sc.nextLine().trim());
            String name = sc.nextLine().trim();
            double marks = Double.parseDouble(sc.nextLine().trim());
            students.add(new Student(id, name, marks));
        }

        sc.close();

        String filename = "students.dat";

        try (ObjectOutputStream oos = new ObjectOutputStream(new FileOutputStream(filename))) {
            oos.writeObject(students);
            System.out.println("Students serialized successfully into: " + filename);
        } catch (IOException e) {
            e.printStackTrace();
        }

        ArrayList<Student> loaded = null;
        try (ObjectInputStream ois = new ObjectInputStream(new FileInputStream(filename))) {
            @SuppressWarnings("unchecked")
            ArrayList<Student> temp = (ArrayList<Student>) ois.readObject();
            loaded = temp;

            System.out.println("Students deserialized successfully from: " + filename);
            System.out.println(); // important: empty line

            System.out.println("Deserialized Students:");
            for (Student s : loaded) {
                System.out.println(s);
            }

        } catch (IOException | ClassNotFoundException e) {
            e.printStackTrace();
        }
    }
}
```





## OUTPUT:
<img width="1188" height="813" alt="image" src="https://github.com/user-attachments/assets/6b65e683-5c1a-4695-90c1-0f97020a0534" />



## RESULT:
Thus the above Java program to serialize a collection of objects (like ArrayList<Student>) into a file is executed successfully.


