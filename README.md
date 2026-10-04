import java.util.Scanner;

public class ArrayProblems {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        // Array size
        System.out.print("Enter array size: ");
        int n = sc.nextInt();

        // Array creation
        int[] arr = new int[n];

        // Array elements input
        System.out.println("Enter array elements:");
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        // Problem 1: Sum of array elements
        int sum = 0;

        for (int i = 0; i < n; i++) {
            sum += arr[i];
        }

        System.out.println("Sum of elements = " + sum);

        // Problem 2: Largest element
        int largest = arr[0];

        for (int i = 1; i < n; i++) {
            if (arr[i] > largest) {
                largest = arr[i];
            }
        }

        System.out.println("Largest element = " + largest);

        // Problem 3: Reverse the array
        System.out.print("Reversed array: ");

        for (int i = n - 1; i >= 0; i--) {
            System.out.print(arr[i] + " ");
        }

        sc.close();
    }
}
