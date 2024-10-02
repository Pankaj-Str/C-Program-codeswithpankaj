# C-Program-codeswithpankaj


### 1. What are escape operators? Give examples of their usage.
**Explanation**: Escape operators are special character combinations used in strings to represent specific characters that can't be typed directly. Common examples include `\n` (newline), `\t` (tab), `\\` (backslash), etc.

**Code**:
```c
// www.codeswithpankaj.com
#include <stdio.h>

void escape_operators_examples() {
    printf("Escape operators examples:\n");
    printf("Newline character: This is line 1.\nThis is line 2.\n");
    printf("Tab character: Column 1\tColumn 2\n");
    printf("Backslash character: This is a backslash \\.\n");
    printf("Single quote: \'Hello\'\n");
    printf("Double quote: \"Hello\"\n");
}

int main() {
    escape_operators_examples();
    return 0;
}
```

### 2. Write a program to calculate the area and perimeter of a square and a rectangle.
**Code**:
```c
// www.codeswithpankaj.com
#include <stdio.h>

void area_and_perimeter() {
    float side, length, breadth;

    // Square
    printf("Enter the side length of the square: ");
    scanf("%f", &side);
    printf("Area of Square: %.2f\n", side * side);
    printf("Perimeter of Square: %.2f\n", 4 * side);

    // Rectangle
    printf("Enter the length and breadth of the rectangle: ");
    scanf("%f %f", &length, &breadth);
    printf("Area of Rectangle: %.2f\n", length * breadth);
    printf("Perimeter of Rectangle: %.2f\n", 2 * (length + breadth));
}

int main() {
    area_and_perimeter();
    return 0;
}
```

### 3. How would you find the biggest number out of three numbers?
**Code**:
```c
// www.codeswithpankaj.com
#include <stdio.h>

void biggest_of_three() {
    int a, b, c;
    printf("Enter three numbers: ");
    scanf("%d %d %d", &a, &b, &c);

    if (a >= b && a >= c) {
        printf("The biggest number is: %d\n", a);
    } else if (b >= a && b >= c) {
        printf("The biggest number is: %d\n", b);
    } else {
        printf("The biggest number is: %d\n", c);
    }
}

int main() {
    biggest_of_three();
    return 0;
}
```

### 4. Write a program to display multiplication tables.
**Code**:
```c
// www.codeswithpankaj.com
#include <stdio.h>

void multiplication_tables() {
    int num, i;
    printf("Enter a number to display its multiplication table: ");
    scanf("%d", &num);

    for (i = 1; i <= 10; i++) {
        printf("%d x %d = %d\n", num, i, num * i);
    }
}

int main() {
    multiplication_tables();
    return 0;
}
```

### 5. How do you print even numbers up to a certain range?
**Code**:
```c
// www.codeswithpankaj.com
#include <stdio.h>

void even_numbers_range() {
    int range, i;
    printf("Enter the range to print even numbers up to: ");
    scanf("%d", &range);

    printf("Even numbers up to %d:\n", range);
    for (i = 1; i <= range; i++) {
        if (i % 2 == 0) {
            printf("%d ", i);
        }
    }
    printf("\n");
}

int main() {
    even_numbers_range();
    return 0;
}
```

### 6. Write a program to calculate the average of odd numbers below a given range.
**Code**:
```c
// www.codeswithpankaj.com
#include <stdio.h>

void average_of_odd_numbers() {
    int range, i, sum = 0, count = 0;
    float average;

    printf("Enter the range: ");
    scanf("%d", &range);

    for (i = 1; i < range; i++) {
        if (i % 2 != 0) {
            sum += i;
            count++;
        }
    }

    average = (float)sum / count;
    printf("Average of odd numbers below %d: %.2f\n", range, average);
}

int main() {
    average_of_odd_numbers();
    return 0;
}
```

### 7. How can you calculate the net salary of an employee, given basic salary and deductions?
**Code**:
```c
// www.codeswithpankaj.com
#include <stdio.h>

void calculate_net_salary() {
    float basic, deductions, net_salary;

    printf("Enter the basic salary: ");
    scanf("%f", &basic);

    printf("Enter the deductions: ");
    scanf("%f", &deductions);

    net_salary = basic - deductions;
    printf("Net Salary: %.2f\n", net_salary);
}

int main() {
    calculate_net_salary();
    return 0;
}
```

### 8. Write a program to find out if a student passes or fails based on given marks.
**Code**:
```c
// www.codeswithpankaj.com
#include <stdio.h>

void student_pass_fail() {
    int marks;
    printf("Enter student's marks: ");
    scanf("%d", &marks);

    if (marks >= 40) {
        printf("Student Passes\n");
    } else {
        printf("Student Fails\n");
    }
}

int main() {
    student_pass_fail();
    return 0;
}
```

### 9. What is a prime number? Write a program to check if a given number is prime.
**Code**:
```c
// www.codeswithpankaj.com
#include <stdio.h>

void check_prime() {
    int num, i, is_prime = 1;
    printf("Enter a number to check if it's prime: ");
    scanf("%d", &num);

    if (num <= 1) {
        is_prime = 0;
    } else {
        for (i = 2; i <= num / 2; i++) {
            if (num % i == 0) {
                is_prime = 0;
                break;
            }
        }
    }

    if (is_prime) {
        printf("%d is a prime number.\n", num);
    } else {
        printf("%d is not a prime number.\n", num);
    }
}

int main() {
    check_prime();
    return 0;
}
```

### 10. Write a program to check if a number is a perfect number.
**Code**:
```c
// www.codeswithpankaj.com
#include <stdio.h>

void check_perfect_number() {
    int num, i, sum = 0;
    printf("Enter a number to check if it's a perfect number: ");
    scanf("%d", &num);

    for (i = 1; i < num; i++) {
        if (num % i == 0) {
            sum += i;
        }
    }

    if (sum == num) {
        printf("%d is a perfect number.\n", num);
    } else {
        printf("%d is not a perfect number.\n", num);
    }
}

int main() {
    check_perfect_number();
    return 0;
}
```
### 11. How can you determine if a number is an Armstrong number?
**Code**:
```c
// www.codeswithpankaj.com
#include <stdio.h>
#include <math.h>

void check_armstrong() {
    int num, original, remainder, n = 0;
    int result = 0;

    printf("Enter a number to check if it's an Armstrong number: ");
    scanf("%d", &num);

    original = num;

    // Find number of digits in num
    while (original != 0) {
        original /= 10;
        ++n;
    }

    original = num;

    // Compute the sum of the power of individual digits
    while (original != 0) {
        remainder = original % 10;
        result += pow(remainder, n);
        original /= 10;
    }

    if (result == num) {
        printf("%d is an Armstrong number.\n", num);
    } else {
        printf("%d is not an Armstrong number.\n", num);
    }
}

int main() {
    check_armstrong();
    return 0;
}
```

### 12. Write a program to check if a number is a palindrome.
**Code**:
```c
// www.codeswithpankaj.com
#include <stdio.h>

void check_palindrome() {
    int num, reversed = 0, original, remainder;
    printf("Enter a number to check if it's a palindrome: ");
    scanf("%d", &num);

    original = num;

    while (num != 0) {
        remainder = num % 10;
        reversed = reversed * 10 + remainder;
        num /= 10;
    }

    if (original == reversed) {
        printf("%d is a palindrome.\n", original);
    } else {
        printf("%d is not a palindrome.\n", original);
    }
}

int main() {
    check_palindrome();
    return 0;
}
```

### 13. Write a program to determine if a given character is a vowel or not.
**Code**:
```c
// www.codeswithpankaj.com
#include <stdio.h>

void check_vowel() {
    char ch;
    printf("Enter a character: ");
    scanf(" %c", &ch);

    if (ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u' ||
        ch == 'A' || ch == 'E' || ch == 'I' || ch == 'O' || ch == 'U') {
        printf("%c is a vowel.\n", ch);
    } else {
        printf("%c is not a vowel.\n", ch);
    }
}

int main() {
    check_vowel();
    return 0;
}
```

### 14. How can you find the sum of digits of a number?
**Code**:
```c
// www.codeswithpankaj.com
#include <stdio.h>

void sum_of_digits() {
    int num, sum = 0, remainder;
    printf("Enter a number: ");
    scanf("%d", &num);

    while (num != 0) {
        remainder = num % 10;
        sum += remainder;
        num /= 10;
    }

    printf("Sum of digits: %d\n", sum);
}

int main() {
    sum_of_digits();
    return 0;
}
```

### 15. Write a program to create a four-function calculator (addition, subtraction, multiplication, division).
**Code**:
```c
// www.codeswithpankaj.com
#include <stdio.h>

void calculator() {
    char operator;
    double num1, num2, result;

    printf("Enter an operator (+, -, *, /): ");
    scanf(" %c", &operator);
    printf("Enter two operands: ");
    scanf("%lf %lf", &num1, &num2);

    switch (operator) {
        case '+':
            result = num1 + num2;
            printf("Result: %.2lf\n", result);
            break;
        case '-':
            result = num1 - num2;
            printf("Result: %.2lf\n", result);
            break;
        case '*':
            result = num1 * num2;
            printf("Result: %.2lf\n", result);
            break;
        case '/':
            if (num2 != 0)
                result = num1 / num2;
            else {
                printf("Division by zero error!\n");
                return;
            }
            printf("Result: %.2lf\n", result);
            break;
        default:
            printf("Invalid operator.\n");
    }
}

int main() {
    calculator();
    return 0;
}
```

### 16. What are nested for loops? Write a program to demonstrate their usage.
**Explanation**: A nested `for` loop is a loop inside another loop. It's often used to iterate through multidimensional structures like matrices.

**Code**:
```c
// www.codeswithpankaj.com
#include <stdio.h>

void nested_loops() {
    int i, j;
    for (i = 1; i <= 3; i++) {
        for (j = 1; j <= 3; j++) {
            printf("i = %d, j = %d\n", i, j);
        }
    }
}

int main() {
    nested_loops();
    return 0;
}
```

### 17. Write a program to create an asterisk graph based on user input.
**Code**:
```c
// www.codeswithpankaj.com
#include <stdio.h>

void asterisk_graph() {
    int rows, i, j;
    printf("Enter the number of rows: ");
    scanf("%d", &rows);

    for (i = 1; i <= rows; i++) {
        for (j = 1; j <= i; j++) {
            printf("* ");
        }
        printf("\n");
    }
}

int main() {
    asterisk_graph();
    return 0;
}
```

### 18. How do you swap two integers without using a third variable?
**Code**:
```c
// www.codeswithpankaj.com
#include <stdio.h>

void swap_without_third_variable() {
    int a, b;
    printf("Enter two numbers: ");
    scanf("%d %d", &a, &b);

    a = a + b;
    b = a - b;
    a = a - b;

    printf("After swapping: a = %d, b = %d\n", a, b);
}

int main() {
    swap_without_third_variable();
    return 0;
}
```

### 19. Write a program to generate Floyd’s triangle.
**Code**:
```c
// www.codeswithpankaj.com
#include <stdio.h>

void floyds_triangle() {
    int n, i, j, num = 1;
    printf("Enter the number of rows for Floyd's triangle: ");
    scanf("%d", &n);

    for (i = 1; i <= n; i++) {
        for (j = 1; j <= i; j++) {
            printf("%d ", num);
            num++;
        }
        printf("\n");
    }
}

int main() {
    floyds_triangle();
    return 0;
}
```

### 20. How can you generate a Fibonacci series up to a given range?
**Code**:
```c
// www.codeswithpankaj.com
#include <stdio.h>

void fibonacci_series() {
    int n, t1 = 0, t2 = 1, nextTerm = 0;

    printf("Enter the range for Fibonacci series: ");
    scanf("%d", &n);

    printf("Fibonacci Series: %d, %d", t1, t2);
    nextTerm = t1 + t2;

    while (nextTerm <= n) {
        printf(", %d", nextTerm);
        t1 = t2;
        t2 = nextTerm;
        nextTerm = t1 + t2;
    }
    printf("\n");
}

int main() {
    fibonacci_series();
    return 0;
}
```

