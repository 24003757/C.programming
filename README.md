# C.programming
# Name: VINOLIA ALAINA. R
# Reg No. 212224240184

## 1.Write a C program to find the maximum of three numbers without using logical operators.
```
#include <stdio.h>

int main() {
    int a, b, c, max;

    printf("Enter three numbers: ");
    scanf("%d %d %d", &a, &b, &c);

    max = a;

    if (b > max)
        max = b;

    if (c > max)
        max = c;

    printf("Maximum = %d", max);

    return 0;
}
```
# OUTPUT:
<img width="1919" height="1145" alt="image" src="https://github.com/user-attachments/assets/9d49df6c-fd0f-415e-8e00-3a42a7004c66" />


## 2.Write a C program to check whether the given year is leap year or not by adding century leap year or non-century leap year in the output (Eg: 2000 is a century leap year, 2024 is a non-century leap year)
```
#include <stdio.h>

int main() {
    int year;

    printf("Enter year: ");
    scanf("%d", &year);

    if (year % 400 == 0) {
        printf("%d is a Century Leap Year", year);
    }
    else if (year % 100 == 0) {
        printf("%d is a Century Non-Leap Year", year);
    }
    else if (year % 4 == 0) {
        printf("%d is a Non-Century Leap Year", year);
    }
    else {
        printf("%d is Not a Leap Year", year);
    }

    return 0;
}
```

# OUTPUT:
<img width="1919" height="1151" alt="image" src="https://github.com/user-attachments/assets/ac21d4f7-f4de-487f-89e2-0a5adf3c3d2d" />


## 3.Write a C program to find whether the entered character is alphabet / digit / special character. If the entered character is an alphabet then say it is vowel or consonant without using built in functions
```
#include <stdio.h>

int main() {
    char ch;

    printf("Enter a character: ");
    scanf(" %c", &ch);

    if ((ch >= 'a' && ch <= 'z') || (ch >= 'A' && ch <= 'Z')) {

        printf("Alphabet\n");

        if (ch=='a'||ch=='e'||ch=='i'||ch=='o'||ch=='u'||
            ch=='A'||ch=='E'||ch=='I'||ch=='O'||ch=='U') {
            printf("Vowel");
        } else {
            printf("Consonant");
        }

    }
    else if (ch >= '0' && ch <= '9') {
        printf("Digit");
    }
    else {
        printf("Special Character");
    }

    return 0;
}

```
# OUTPUT:
<img width="1919" height="1144" alt="image" src="https://github.com/user-attachments/assets/bc7ca11c-3e5c-4bb9-8cd7-17df360eda78" />


## 4.Write a C program for simple ATM simulation with operations Check Balance, Deposit, Withdraw, Exit using switch and update balance accordingly.
```

#include <stdio.h>

int main() {
    int choice;
    float balance = 1000, amount;

    do {
        printf("\n1. Check Balance\n2. Deposit\n3. Withdraw\n4. Exit\n");
        printf("Enter choice: ");
        scanf("%d", &choice);

        switch (choice) {
            case 1:
                printf("Balance = %.2f\n", balance);
                break;

            case 2:
                printf("Enter amount to deposit: ");
                scanf("%f", &amount);
                balance += amount;
                printf("Updated Balance = %.2f\n", balance);
                break;

            case 3:
                printf("Enter amount to withdraw: ");
                scanf("%f", &amount);
                if (amount <= balance) {
                    balance -= amount;
                    printf("Updated Balance = %.2f\n", balance);
                } else {
                    printf("Insufficient Balance\n");
                }
                break;

            case 4:
                printf("Thank you!\n");
                break;

            default:
                printf("Invalid choice\n");
        }

    } while (choice != 4);

    return 0;
}
```
# OUTPUT:
<img width="1914" height="1143" alt="image" src="https://github.com/user-attachments/assets/6bb3f730-cf24-44bf-a4b1-fe8cb2da8f4d" />


## 5.Write a C program for menu driven calculator using switch statement.
```
#include <stdio.h>

int main() {
    int choice;
    float a, b;

    printf("Enter two numbers: ");
    scanf("%f %f", &a, &b);

    printf("\n1.Add\n2.Subtract\n3.Multiply\n4.Divide\n");
    printf("Enter choice: ");
    scanf("%d", &choice);

    switch (choice) {
        case 1:
            printf("Result = %.2f", a + b);
            break;

        case 2:
            printf("Result = %.2f", a - b);
            break;

        case 3:
            printf("Result = %.2f", a * b);
            break;

        case 4:
            if (b != 0)
                printf("Result = %.2f", a / b);
            else
                printf("Division by zero error");
            break;

        default:
            printf("Invalid choice");
    }

    return 0;
}
```
# OUTPUT:
<img width="1916" height="1144" alt="image" src="https://github.com/user-attachments/assets/59499d87-e8a9-48d2-a250-9adbd536db59" />

