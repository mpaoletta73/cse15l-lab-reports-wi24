# Lab Report 5 - Putting it All Together (Week 9)

## Part 1 – Debugging Scenario

**Student Question**
Hey everyone, I've been working on this Java program that's supposed to calculate the average of a list of numbers. However, whenever I run it, 
I keep getting this weird error message that says "NaN" instead of the average. I think there might be something wrong with my `calculateAverage` function. Here's the code:

`public class AverageCalculator {
    public static void main(String[] args) {
        double[] numbers = {10.5, 20.0, 30.5, 40.0, 50.5};
        double result = calculateAverage(numbers);
        System.out.println("The average is: " + result);
    }
    public static double calculateAverage(double[] numbers) {
        double sum = 0;
        for (int i = 1; i <= numbers.length; i++) {
            sum += numbers[i];
        }
        return sum / numbers.length;
    }
}`

**Response from TA**
TA Response:
Hey there! It looks like you might have an off-by-one error in your calculateAverage function. Remember that array indices start from 0. 
Try changing the loop condition to i < numbers.length instead of i <= numbers.length. Let me know if that helps!

`public class AverageCalculator {
    public static void main(String[] args) {
        double[] numbers = {10.5, 20.0, 30.5, 40.0, 50.5};
        double result = calculateAverage(numbers);
        System.out.println("The average is: " + result);
    }
    public static double calculateAverage(double[] numbers) {
        double sum = 0;
        for (int i = 0; i < numbers.length; i++) {
            sum += numbers[i];
        }
        return sum / numbers.length;
    }
}`

**Terminal Output after Fix:**
`The average is: 30.3`
**Bug Description:**
After investigating, it turns out that the issue was an off-by-one error in the `calculateAverage` function. 
By changing the loop condition to `i < numbers.length`, the function now correctly calculates the average of the array of numbers.

**To Fix the Bug:**
Update the loop condition in calculateAverage to i < numbers.length.

## Part 2 - Reflection
Throughout this lab and the second half of the quarter, I've learned a great deal about the importance of code review and collaboration in software development. 
Specifically, going through the process of reviewing another group's code, finding potential bugs, suggesting improvements, and discussing these findings has been incredibly valuable. 
It not only helps in spotting errors but also enhances understanding of different coding styles, best practices, and the diverse ways to approach problem-solving in programming.
This experience has highlighted the significance of clear communication in the development process, whether it's writing understandable code, 
giving feedback that is constructive and respectful, or documenting issues and solutions effectively. I've also gained insights into various debugging techniques, 
such as systematically testing different scenarios, reading error messages critically, and learning from others' code.
Learning to work with others' code has been a rewarding experience, and I believe these skills will greatly benefit me as I continue to grow as a software developer.


