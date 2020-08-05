# Password
Java code where if the correct password is not chosen after a given number of attempts it denies access.

    import java.util.Scanner;

    public class Password {
      public static void main(String[] args) {
        final String SECRET_PASSWORD = "computer";
        final int MAX_GUESSES = 3;
        String passwordGuess;
        int guesses = 0;
        Scanner input = new Scanner(System.in);

        System.out.println("Enter the password: ");
        passwordGuess = input.next();
        guesses++;

        while (!passwordGuess.equals(SECRET_PASSWORD) && guesses < MAX_GUESSES) {
          System.out.println("Incorrect try again: ");
          passwordGuess = input.next();
          guesses++;
        }
        if (guesses == MAX_GUESSES) {
          System.out.println("Access denied.");
        } else if (passwordGuess.equals(SECRET_PASSWORD)) {
          System.out.println("Welcome!");
        }
      }
    }
