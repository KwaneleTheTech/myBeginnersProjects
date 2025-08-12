import java.util.Scanner;

public class MyCalculator {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        // Prompt user for the first number
        System.out.println("Enter the first number:");
        double num1 = input.nextDouble();

        // Prompt user for the operator
        System.out.println("Enter the operator (+, -, *, /):");
        char operator = input.next().charAt(0);

        // Prompt user for the second number
        System.out.println("Enter the second number:");
        double num2 = input.nextDouble();

        double result;

        // Perform the calculation based on the operator
        switch (operator) {
            case '+':
                result = num1 + num2;
                System.out.println(num1 + " + " + num2 + " = " + result);
                break;

            case '-':
                result = num1 - num2;
                System.out.println(num1 + " - " + num2 + " = " + result);
                break;

            case '*':
                result = num1 * num2;
                System.out.println(num1 + " * " + num2 + " = " + result);
                break;

            case '/':
                if (num2 == 0) {
                    System.out.println("Error: Division by zero is not allowed.");
                } else {
                    result = num1 / num2;
                    System.out.println(num1 + " / " + num2 + " = " + result);
                }
                break;

            default:
                System.out.println("Error: Invalid operator.");
        }

        input.close(); // Close the scanner to prevent resource leaks
    }
}
