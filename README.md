# EX-06 - Looping
## AIM:
Write a C program to print even numbers ranging from M to N (including M and N values).

## ALGORITHM:
1.	Declare two integer variables to store the values of M and N.
2.	Use the printf function to prompt the user to enter the values of M and N.
3.	Use the scanf function to read the values of M and N from the user.
4.	Use a loop (for or while) to iterate from M to N.
5.	Inside the loop, check if the current number is even.
6.	If the current number is even, print it.
7.	Continue the loop until you have iterated through all numbers from M to N.

## PROGRAM:

```
#include <stdio.h>

int main() {
    int m, n;

    printf("Enter the starting value (M): ");
    scanf("%d", &m);

    printf("Enter the ending value (N): ");
    scanf("%d", &n);

    printf("Even numbers between %d and %d (inclusive):\n", m, n);

    if (m > n) {
        printf("Starting value should be less than or equal to the ending value.\n");
    } else {
        for (int i = m; i <= n; i++) {
            if (i % 2 == 0) {
                printf("%d ", i);
            }
        }
        printf("\n");
    }

    return 0;
}
```

## OUTPUT:

```
Enter the starting value (M): 10
Enter the ending value (N): 25
Even numbers between 10 and 25 (inclusive):
10 12 14 16 18 20 22 24

```

## RESULT:
Thus the program to print even numbers ranging from M to N (including M and N values) has been executed successfully
 
# EX-07-Nested-loop
## AIM:
Write a C program to print the given triangular pattern using loop.

## ALGORITHM:
1.	Declare a variable to store the number of rows in the triangle.
2.	Use the printf function to prompt the user to enter the number of rows.
3.	Use a loop (for or while) to iterate through each row.
4.	Inside the loop, use another loop to print the desired number of asterisks for each row.
5.	Continue the loop until you have printed the entire triangular pattern.

## PROGRAM:

```
#include <stdio.h>

int main() {
    int rows;

    printf("Enter the number of rows for the triangle: ");
    scanf("%d", &rows);

    for (int i = 1; i <= rows; i++) {
        for (int j = 1; j <= i; j++) {
            printf("*");
        }
        printf("\n");
    }

    return 0;
}
```

## OUTPUT:

```
Enter the number of rows for the triangle: 5
*
**
***
****
*****
```

## RESULT:
Thus the program to print the given triangular pattern using loop has been executed successfully
 
# EX-08-Functions
## AIM:
Write a C program to perform addition and subtraction of two numbers using functions (with argument and without return type).

## ALGORITHM:
1.	Declare two functions, one for addition and one for subtraction. Both functions should take two integer arguments.
2.	Inside the addition & subtraction function, add & subtract the two numbers and print the result.
3.	In the main function, declare two integer variables and read their values from the user.
4.	Call the addition and subtraction functions, passing the two numbers as arguments.

## PROGRAM:

```
#include <stdio.h>

// Function to perform addition
void add(int num1, int num2) {
    int sum = num1 + num2;
    printf("Sum: %d + %d = %d\n", num1, num2, sum);
}

// Function to perform subtraction
void subtract(int num1, int num2) {
    int difference = num1 - num2;
    printf("Difference: %d - %d = %d\n", num1, num2, difference);
}

int main() {
    int a, b;

    printf("Enter two integers: ");
    scanf("%d %d", &a, &b);

    add(a, b);       // Calling the addition function
    subtract(a, b);  // Calling the subtraction function

    return 0;
}
```

## OUTPUT:

```
Enter two integers: 10 5
Sum: 10 + 5 = 15
Difference: 10 - 5 = 5
```

## RESULT:
Thus the program to perform addition and subtraction of two numbers using functions has been executed successfully
 
# EX-09-Use For Loop
## AIM:
Write a c program to find the sum of odd digits using for loop

## ALGORITHM:
1.	Declare variables to store the input number and the sum of odd digits.
2.	Initialize the sum of odd digits to 0.
3.	Use a for loop to iterate through each digit of the input number.
4.	Inside the loop, extract the rightmost digit of the number (using the modulo operator % and division by 10).
5.	If the digit is odd, add it to the sum of odd digits.
6.	Print the sum of odd digits.

## PROGRAM:

```
#include <stdio.h>

int main() {
    int number;
    int sumOfOddDigits = 0;

    printf("Enter an integer: ");
    scanf("%d", &number);

    if (number < 0) {
        number = -number; // Handle negative input
    }

    if (number == 0) {
        printf("Sum of odd digits: 0\n");
        return 0;
    }

    for (; number > 0; number /= 10) {
        int digit = number % 10;
        if (digit % 2 != 0) {
            sumOfOddDigits += digit;
        }
    }

    printf("Sum of odd digits: %d\n", sumOfOddDigits);

    return 0;
}
```

## OUTPUT:

```
Enter an integer: 12345
Sum of odd digits: 9

Enter an integer: 987654321
Sum of odd digits: 25
```

## RESULT:
Thus the program to find the sum of odd digits using for loop has been executed successfully.

# EX – 10 - Factorial of a Number Using a Function
## AIM:
To write a C program that calculates the factorial of a given number using a user-defined function.

## ALGORITHM:
1.	Start
2.	Declare the function fact().
3.	In the main() function, call the fact() function.
4.	In fact() function:
a.	Declare variables i, N, and fact (initialized to 1).
b.	Read an integer N from the user.
c.	Use a for loop from 1 to N:
i.	Multiply fact by i in each iteration.
d.	After the loop, print the factorial value.
5.	End

## PROGRAM:

```
#include <stdio.h>

// Function to calculate the factorial of a number
void fact() {
    int i, n;
    long long factorial = 1; // Use long long to handle larger factorials

    printf("Enter a non-negative integer: ");
    scanf("%d", &n);

    if (n < 0) {
        printf("Factorial is not defined for negative numbers.\n");
    } else {
        for (i = 1; i <= n; i++) {
            factorial *= i;
        }
        printf("Factorial of %d = %lld\n", n, factorial);
    }
}

int main() {
    fact(); // Calling the factorial function
    return 0;
}
```

## OUTPUT:

```
Enter a non-negative integer: 5
Factorial of 5 = 120

Enter a non-negative integer: 0
Factorial of 0 = 1
```

## RESULT:
The program correctly computes the factorial of a given number using a separate function and displays the result.
