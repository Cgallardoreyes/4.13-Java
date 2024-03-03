# 4.13-Java
import java.util.Scanner;

public class Exercise04_13 {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.print("Enter a letter: ");
        String userInput = input.nextLine();

        // Check if the input is a single character
        if (userInput.length() == 1) {
            char letter = userInput.charAt(0);

            if (Character.isLetter(letter)) {
                char lowercaseLetter = Character.toLowerCase(letter);

                if (lowercaseLetter == 'a' || lowercaseLetter == 'e' || lowercaseLetter == 'i' || 
                    lowercaseLetter == 'o' || lowercaseLetter == 'u') {
                    System.out.println(letter + " is a vowel");
                } else {
                    System.out.println(letter + " is a consonant");
                }
            } else {
                System.out.println("Invalid input. Please enter a letter.");
            }
        } else {
            System.out.println("Invalid input. Please enter a single letter.");
        }

        input.close()
