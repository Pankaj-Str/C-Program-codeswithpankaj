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

