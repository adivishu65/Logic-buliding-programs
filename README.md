#include <stdio.h>
int main () {
int side;
printf("Enter side of squar: ");
scanf("%d", & side);
printf(" area is: "%d", side * side);
return 0;
}
#include <stdio.h>

int main() {
    float radius;
    printf("Enter radius: ");
    scanf("%f", &radius);
    printf("area is: %f", 3.14 * radius * radius);
    return 0;
}

#include <stdio.h>

int main() {
    int n;
    printf("Enter number: ");
    scanf("%d", &n);

    if (n % 2 == 0) {
        printf("The number is divisible by 2.\n");
    } else {
        printf("The number is not divisible by 2.\n");
    }

    return 0;
}
#include <stdio.h>

int main() {
    int n;
    printf("Enter number: ");
    scanf("%d", &n);

    if (n % 2 == 0) {
        printf("Even number\n"); // Added newline for better output formatting
    } else { // Corrected 'Jelbed' to 'else'
        printf("Odd number\n"); // Added newline for better output formatting
    }
    return 0;
}
#include <stdio.h>

int main() { // Corrected: main function signature
    int age;
    printf("Enter age: "); // Corrected: printf string literal
    scanf("%d", &age);

    if (age >= 18) { // Corrected: Logical operator for adult (>=)
        printf("adult\n"); // Added newline for better output formatting
    } else if (age >= 13 && age < 18) { // Corrected: Logical operator for teenager (>=)
        printf("teenager\n"); // Added newline for better output formatting
    } else { // Corrected: else block for child
        printf("child\n"); // Added newline for better output formatting
    }

    return 0;
}
#include <stdio.h> 

int main() { 
    int a, b; 
    printf("Enter two numbers: "); 
    scanf("%d%d", &a, &b); 

    if (a > b) { 
        printf("a = %d, is greater\n", a); 
    } else { 
        printf("b = %d, is greater\n", b); 
    } 
    return 0; 
}
#include <stdio.h>

int main() { // Added { and )
    int day;

    printf("Enter a day: ");
    scanf("%d", &day);

    switch (day) { // Added {
        case 1: // Corrected case
            printf("Monday\n"); // Added \n for new line
            break;
        case 2:
            printf("Tuesday\n");
            break;
        case 3: // Corrected case, added ; after printf
            printf("Wednesday\n");
            break;
        case 4: // Corrected case, added ; after printf
            printf("Thursday\n");
            break;
        case 5:
            printf("Friday\n");
            break;
        case 6: // Corrected case, added ; after printf
            printf("Saturday\n");
            break;
        case 7:
            printf("Sunday\n");
            break;
        default: // Corrected keyword
            printf("Not a day\n");
            break; // Good practice to have break in default too
    } // Added }

    return 0; // Essential for main function
}

#include <stdio.h>

int main() { // main function signature needs parentheses
    int marks;
    printf("Enter marks: "); // String literals need double quotes
    scanf("%d", &marks);

    if (marks > 90) { // Opening curly brace for if block
        printf("FC Grades: A\n"); // Corrected printf and added newline
    } else if (marks > 70) { // Corrected "Print" to "printf"
        printf("FC Grades: B\n"); // Added newline
    } else if (marks >= 40) { // Corrected parentheses
        printf("Grades: C\n"); // Added newline
    } else { // Corrected "&" to "else"
        printf("Grades: Fail\n"); // Corrected "Cu" to "Grades" and added newline
    }

    return 0; // Added return statement for main function
}

#include <stdio.h> // Include the standard input/output library

int main() { // Correct main function declaration
    char ch; // Declare a character variable

    printf("Enter a character: "); // Prompt the user for input
    scanf(" %c", &ch); // Read a single character, with a space before %c to consume leftover newline characters

    // Check if the character is an uppercase letter
    if (ch >= 'A' && ch <= 'Z') { // Correct comparison with character literals
        printf("Uppercase\n"); // Print "Uppercase" and a newline
    } 
    // Otherwise, check if the character is a lowercase letter
    else if (ch >= 'a' && ch <= 'z') { // Correct comparison with character literals
        printf("Lowercase\n"); // Print "Lowercase" and a newline
    } 
    // If neither, it's not an English alphabet
    else {
        printf("Not an English alphabet\n"); // Print "Not an English alphabet" and a newline
    }

    return 0; // Indicate successful execution
}
#include <stdio.h>

int main() { // main function declaration requires parentheses
    int n;
    printf("Enter number: ");
    scanf("%d", &n);

    int sum = 0; // Initialize sum
    // sum = sum; // This line is redundant

    int i; // Declare loop variable 'i' before use
    for (i = 1; i <= n; i++) { // Correct loop syntax
        sum = sum + i; // Add 'i' to sum in each iteration
    }

    printf("Sum is: %d\n", sum); // Correct printf format string and add newline

    return 0;
}

#include <stdio.h>

int main() {
    int n, i; // Declare variables n and i
    printf("Enter a number: "); // Prompt the user for input
    scanf("%d", &n); // Read an integer from the user and store it in n

    for (i = 1; i <= 10; i++) { // Loop from i = 1 to 10
        printf("%d\n", n + i); // Print the sum of n and i, followed by a newline
    }

    return 0; // Indicate successful program execution
}

#include <stdio.h>

int main() {
    int i;
    for (i=5; i<= 50; i++) {
        if (i%2!=0){
            printf("%d\n", i);
            return 0;
        }
    }
    return 0;
}

#include <stdio.h>

int main() {
    int n; // Declare variable 'n' to store the input number
    long long fact = 1; // Declare 'fact' to store the factorial, initialized to 1. Use 'long long' for larger factorials.
    int i; // Declare loop counter 'i'

    printf("Enter number: "); // Prompt the user to enter a number
    scanf("%d", &n); // Read the integer input from the user and store it in 'n'

    // Handle negative input as factorials are not defined for negative numbers
    if (n < 0) {
        printf("Factorial is not defined for negative numbers.\n");
    } 
    // Handle the case of 0! which is 1
    else if (n == 0) {
        printf("Factorial of 0 is: 1\n");
    } 
    // Calculate factorial for positive numbers
    else {
        for (i = 1; i <= n; i++) {
            fact = fact * i; // Multiply 'fact' by the current value of 'i'
        }
        printf("Final factorial is: %lld\n", fact); // Print the calculated factorial. Use %lld for long long.
    }

    return 0; // Indicate successful program execution
}

#include <stdio.h>

// Function prototypes must be declared before main()
void namaste();
void bonjour();

int main() {
    char ch;
    printf("Enter f for French and i for Indian: ");
    // Added a space before %c to consume potential leading whitespace/newline characters
    scanf(" %c", &ch);

    // Use if-else if for correct logic flow
    if (ch == 'i' || ch == 'I') { // Added case-insensitivity
        namaste();
    } else if (ch == 'f' || ch == 'F') {
        bonjour();
    } else {
        printf("Invalid input.\n");
    }

    return 0;
}

// Function definitions must match prototypes exactly (void not Vold/veid)
void namaste() {
    printf("Namaste\n"); // Added newline for formatting
}

void bonjour() {
    printf("Bonjour\n"); // Added newline for formatting
}

#include <stdio.h>

// Function declaration (prototype)
int sum(int a, int b);

int main() {
    int a, b; // Declare variables for the two numbers
    printf("Enter two numbers: "); // Prompt the user for input
    scanf("%d%d", &a, &b); // Read the two integers from the user

    int s = sum(a, b); // Call the sum function and store the result
    printf("Sum is: %d\n", s); // Print the calculated sum

    return 0; // Indicate successful program execution
}

// Function definition
int sum(int a, int b) {
    return a + b; // Return the sum of the two input integers
}

#include <stdio.h>

// Function to print the multiplication table of a given number 'n'
void table(int n) {
    int i; // Loop counter

    // Loop from 1 to 10 to generate the multiplication table
    for (i = 1; i <= 10; i++) {
        // Print the multiplication expression and its result
        printf("%d * %d = %d\n", n, i, n * i); 
    }
}

int main() {
    int n; // Variable to store the user-entered number

    // Prompt the user to enter a number
    printf("Enter a number: "); 
    // Read the integer input from the user
    scanf("%d", &n); 

    // Call the 'table' function to print the multiplication table
    table(n); 

    return 0; // Indicate successful program execution
}

#include <stdio.h>

// Function prototypes (declarations)
float rectarea(float a, float b);
float circle_area(float radius); // Renamed for clarity
float squareArea(float side);

int main() // Corrected main function signature
{
    float a = 5.0;
    float b = 10.0;
    float side = 4.0;
    float radius = 3.0;

    // Corrected printf statements
    printf("Rectangle Area is %f\n", rectarea(a, b));
    printf("Square Area is %f\n", squareArea(side));
    printf("Circle Area is %f\n", circle_area(radius));

    return 0; // Standard end of main function
}

// Function definitions

float squareArea(float side) // Removed extra parenthesis
{
    return side * side;
}

float circle_area(float radius) // Renamed function
{
    return 3.14 * radius * radius; // Added multiplication operators
}

float rectarea(float a, float b)
{
    return a * b;
}

#include <stdio.h> // Include standard input/output library

// Function declaration (prototype)
void printHW(int count);

int main() { // Main function, entry point of the program
    printHW(5); // Call the recursive function with an initial count of 5
    return 0; // Indicate successful program termination
}

// Function definition
void printHW(int count) { // 'int' for the parameter type, curly brace for function body
    if (count == 0) {
        return; // Base case: stop recursion when count reaches 0
    }

    printf("Hello world\n"); // Print "Hello world" followed by a newline
    printHW(count - 1); // Recursive call: decrement count and call the function again
}

#include <stdio.h>

// Function prototype
int sum(int n);

int main() {
    // Correctly call the function and print the result
    printf("Sum is: %d\n", sum(5));
    // main function should return an int value
    return 0; 
}

// Function definition
int sum(int n) {
    if (n == 1) {
        return 1;
    } else {
        // Corrected variable names and calculation
        int sumNm1 = sum(n - 1); 
        int sumN = n + sumNm1; // Should add 'n' to the previous sum
        return sumN;
    }
}

#include <stdio.h> // Include the standard input/output library

// Function prototype for the factorial function
int fact(int n);

int main() { // Main function where program execution begins
    // Print the factorial of 5
    printf("Factorial is: %d\n", fact(5)); 
    return 0; // Indicate successful program termination
}

// Recursive function to calculate the factorial
int fact(int n) { 
    if (n == 0) { // Base case: factorial of 0 is 1
        return 1;
    }
    // Recursive case: n! = n * (n-1)!
    int factNm1 = fact(n - 1); // Calculate factorial of n-1
    int factN = factNm1 * n;   // Multiply by n
    return factN;
}#include <stdio.h>

// Function prototype declaration
float convertTemp(float celcius);

int main() {
    float celsius_temp = 25.0; // Example Celsius temperature
    float fahrenheit_temp = convertTemp(celsius_temp);

    printf("%f Celsius is equal to %f Fahrenheit\n", celsius_temp, fahrenheit_temp);

    return 0;
}

// Function definition
float convertTemp(float celcius) {
    float far = (celcius * (9.0 / 5.0)) + 32;
    return far;
}

#include <stdio.h>

// Function declaration (prototype)
int calcPer(int s, int m, int z);

int main() {
    // Corrected variable types for whole numbers (integers)
    int sub1_score = 95;
    int sub2_score = 90;
    int sub3_score = 85;
    
    // Call the function and print the result
    printf("Percentage is: %d\n", calcPer(sub1_score, sub2_score, sub3_score)); 
    
    return 0;
}

// Function definition
int calcPer(int s, int m, int z) {
    // Calculate total score / number of subjects (integer division)
    return (s + m + z) / 3; 
}

#include <stdio.h>

int main() {
    int n1, n2, temp; // Declare temp for swapping in GCD algorithm

    printf("Enter two numbers: ");
    if (scanf("%d %d", &n1, &n2) != 2) { // Check if scanf successfully read two integers
        printf("Invalid input.\n");
        return 1; // Indicate an error
    }

    // Euclidean algorithm to find GCD
    while (n2 != 0) {
        temp = n2;
        n2 = n1 % n2;
        n1 = temp;
    }

    printf("The GCD is: %d\n", n1);
    return 0; // Indicate successful execution
}

#include <stdio.h>

int main() {
    int year;

    printf("Enter a year: ");
    scanf("%d", &year);

    // Leap year conditions:
    // A year is a leap year if it is divisible by 400,
    // OR if it is divisible by 4 but not by 100.
    if ((year % 400 == 0) || ((year % 4 == 0) && (year % 100 != 0))) {
        printf("%d is a leap year.\n", year);
    } else {
        printf("%d is not a leap year.\n", year);
    }

    return 0;
}

#include <stdio.h>

int main() {
    int n, sum = 0, r; // Corrected variable declaration syntax

    printf("Enter number: "); // Added a colon for better readability
    scanf("%d", &n);

    // Loop to extract digits and sum them
    while (n > 0) { // Corrected syntax for while loop body
        r = n % 10;   // Get the last digit
        sum += r;     // Add the digit to the sum
        n /= 10;      // Remove the last digit from the number (integer division)
    }

    printf("Sum of digits: %d\n", sum); // Corrected printf syntax and moved outside the loop

    return 0;
}

#include <stdio.h>

int main() {
    int n, r, reversed_num = 0; // Initialize reversed_num

    printf("Enter number: ");
    scanf("%d", &n);

    int original_n = n; // Store original for final print

    while (n > 0) {
        r = n % 10; // Get the last digit
        reversed_num = reversed_num * 10 + r; // Build the reversed number
        n = n / 10; // Remove the last digit
    }

    printf("Original number: %d\n", original_n);
    printf("Reversed number: %d\n", reversed_num);

    return 0;
}


#include <stdio.h>
#include <ctype.h> // Include this header for isalpha(), islower(), etc. if needed

int main() {
    char ch; // Declare a variable to store the character

    printf("Enter character: ");
    // Use %c format specifier for reading a single character
    scanf(" %c", &ch); // Added a space before %c to ignore leading whitespace/newlines

    // Convert to lowercase to simplify the check, assuming only alphabets are entered
    char lower_ch = tolower(ch);

    // Check if the character is an alphabet AND if it is a vowel
    if (isalpha(ch)) {
        if (lower_ch == 'a' || lower_ch == 'e' || lower_ch == 'i' || lower_ch == 'o' || lower_ch == 'u') {
            printf("Vowel\n");
        } else {
            printf("Consonant\n");
        }
    } else {
        printf("Not an alphabet\n");
    }

    return 0;
}

#include <stdio.h>

int main() {
    int a, b, c; // Declare integer variables for the three numbers

    printf("Enter three numbers: "); // Prompt the user for input
    scanf("%d%d%d", &a, &b, &c); // Read the three integer values

    // Determine the largest number using if-else if-else statements
    if (a >= b && a >= c) { // Check if 'a' is the largest
        printf("%d is the biggest.\n", a);
    } else if (b >= a && b >= c) { // Check if 'b' is the largest
        printf("%d is the biggest.\n", b);
    } else { // If neither 'a' nor 'b' is the largest, then 'c' must be
        printf("%d is the biggest.\n", c);
    }

    return 0; // Indicate successful program execution
}
