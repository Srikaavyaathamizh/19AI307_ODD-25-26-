# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:
Use ScheduledExecutorService to delay execution of tasks and print their message.

## AIM:
To use ScheduledExecutorService to schedule delayed execution of multiple tasks that print messages.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the number of tasks from the user.
4. Create a ScheduledExecutorService with a thread pool matching the task count.
5. For each task, read the message and delay time.
6. Schedule each task using scheduler.schedule() with the given delay.
7. Shut down the scheduler and wait until all scheduled tasks finish execution.





## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
Developed by: SRIKAAVYAA T
RegisterNumber:  212223230214
*/
import java.util.Scanner;
import java.util.concurrent.*;

class MessageTask implements Runnable {
    private String message;

    public MessageTask(String message) {
        this.message = message;
    }

    @Override
    public void run() {
        System.out.println(message);
    }
}

public class ScheduledTasksExample {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        // Read number of tasks
        int n = Integer.parseInt(sc.nextLine().trim());

        // Create scheduler
        ScheduledExecutorService scheduler = Executors.newScheduledThreadPool(n);

        // Schedule each task
        for (int i = 0; i < n; i++) {
            String line = sc.nextLine().trim();
            String[] parts = line.split(" ");

            String msg = parts[0];
            int delay = Integer.parseInt(parts[1]);

            scheduler.schedule(new MessageTask(msg), delay, TimeUnit.SECONDS);
        }

        // Shutdown scheduler after all tasks are submitted
        scheduler.shutdown();

        try {
            // Wait until all tasks are completed
            scheduler.awaitTermination(10, TimeUnit.SECONDS);
        } catch (InterruptedException e) {
            e.printStackTrace();
        }

    }
}
```


## OUTPUT:



## RESULT:
The program successfully schedules and prints each message after its specified delay using ScheduledExecutorService.
