import java.util.Random;
import java.util.Scanner;

public class NumberGuessingGame {
    public static void main(String[] args) {

        Random random = new Random();
        Scanner sc = new Scanner(System.in);

        int number = random.nextInt(100) + 1;
        int guess;
        int attempts = 0;

        System.out.println("=== Number Guessing Game ===");
        System.out.println("Guess a number between 1 and 100");

        do {
            System.out.print("Enter your guess: ");
            guess = sc.nextInt();
            attempts++;

            if (guess > number) {
                System.out.println("Too High!");
            } else if (guess < number) {
                System.out.println("Too Low!");
            } else {
                System.out.println("Congratulations! You guessed it.");
                System.out.println("Attempts: " + attempts);
            }

        } while (guess != number);

        sc.close();
    }
}