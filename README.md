Got it. Here's the modified code where the input is taken directly from the user:

```java
import java.util.LinkedList;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        LinkedList<Integer> list = new LinkedList<>();
        Scanner scanner = new Scanner(System.in);

        System.out.println("Enter numbers separated by space:");

        String[] input = scanner.nextLine().split("\\s+");
        for (String numStr : input) {
            int num = Integer.parseInt(numStr);
            list.add(num);
        }

        printLastThree(list);

        scanner.close();
    }

    static void printLastThree(LinkedList<Integer> list) {
        int size = list.size();
        if (size < 3) {
            System.out.println("Not enough elements in the list");
            return;
        }

        System.out.print("Last three elements: ");
        System.out.print(list.get(size - 3) + " ");
        System.out.print(list.get(size - 2) + " ");
        System.out.println(list.get(size - 1));
    }
}
```

In this version, the program prompts the user to enter numbers separated by spaces. It then reads the input, splits it into individual numbers, converts each number to an integer, and adds them to the `LinkedList`. Finally, it prints the last three elements of the list.
