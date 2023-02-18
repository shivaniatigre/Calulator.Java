# Calulator.Java
Calculator.Java repository contains code in Java for developing an application that can perform all the arithmetic calculations in the capacity of a calculator

MAIN.JAVA

        public class Main {
        public static void main(String[] args) {
        // get user input for numbers and/or array
        double[] arr = UserInput.getArrayInput();
        double num1 = UserInput.getNumberInput("Enter first number: ");
        double num2 = UserInput.getNumberInput("Enter second number: ");

        // perform calculations using Calculator methods
        double sum = Calculator.sum(arr);
        double variance = Calculator.variance(arr);
        double stdDeviation = Calculator.standardDeviation(arr);
        double addResult = Calculator.add(num1, num2);
        double subResult = Calculator.subtract(num1, num2);
        double mulResult = Calculator.multiply(num1, num2);
        double divResult = Calculator.divide(num1, num2);

        // display results
        System.out.println("Sum of array: " + sum);
        System.out.println("Variance of array: " + variance);
        System.out.println("Standard deviation of array: " + stdDeviation);
        System.out.println("Addition result: " + addResult);
        System.out.println("Subtraction result: " + subResult);
        System.out.println("Multiplication result: " + mulResult);
        System.out.println("Division result: " + divResult);
    }
    }

USERINPUT.JAVA

    import java.util.Scanner;

    public class UserInput {
    private static Scanner scanner = new Scanner(System.in);

    /**
     * Gets input from user for a single number.
     *
     * @param message the message to display to the user before taking input
     * @return the number entered by the user
     */
    public static double getNumberInput(String message) {
        System.out.print(message);
        return scanner.nextDouble();
    }

    /**
     * Gets input from user for an array of numbers.
     *
     * @return the array of numbers entered by the user
     */
    public static double[] getArrayInput() {
        System.out.print("Enter size of array: ");
        int size = scanner.nextInt();
        double[] arr = new double[size];
        for (int i = 0; i < size; i++) {
            System.out.print("Enter element " + (i+1) + ": ");
            arr[i] = scanner.nextDouble();
        }
        return arr;
    }
    }

CALCULTOR.JAVA

     public class Calculator {
    /**
     * Adds two numbers and returns the result.
     *
     * @param num1 the first number to add
     * @param num2 the second number to add
     * @return the sum of the two numbers
     */
    public static double add(double num1, double num2) {
        return num1 + num2;
    }

    /**
     * Subtracts the second number from the first number and returns the result.
     *
     * @param num1 the number to subtract from
     * @param num2 the number to subtract
     * @return the result of the subtraction
     */
    public static double subtract(double num1, double num2) {
        return num1 - num2;
    }

    /**
     * Multiplies two numbers and returns the result.
     *
     * @param num1 the first number to multiply
     * @param num2 the second number to multiply
     * @return the product of the two numbers
     */
    public static double multiply(double num1, double num2) {
        return num1 * num2
