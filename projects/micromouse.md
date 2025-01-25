---
layout: project
type: project
image: img/micromouse/code.png
title: "Multiples of 3 Table Generator"
date: 2024
published: true
labels:
  - C
summary: "This project generates a table showing numbers up to a user-defined maximum and indicates if they’re multiples of 3 in C."
---



This project is designed to create a table that shows whether numbers from 0 up to a user-specified value are multiples of 3. It's a great example of how simple mathematical operations can be combined with user input handling and conditional logic in C programming. The program prompts the user to enter a positive integer and uses a series of functions to check each number in that range to see if it’s a multiple of 3, generating a table that displays the number alongside a “Yes” or “No” indicating whether or not it's divisible by 3.

**Code Explanation:**
The project is structured with three main functions:

**is_multiple3(int multi):** This function checks if the input number is a multiple of 3. If the number is divisible by 3, it returns 1 (true); otherwise, it returns 0 (false). This logic is used to display the correct result in the table.

```
int is_multiple3(int multi)
{
    if(multi % 3 == 0)
    {
        return 1;
    } 
    else 
    {
        return 0;
    }
}
```

**user_interface():** This function handles user input, ensuring that the user enters a positive integer. If the user enters anything invalid (such as a negative number or non-numeric input), the program will prompt them again until a valid input is provided.

```
int user_interface()
{
    int user_interface;
    int store;
    char temp[25];

    printf("Enter maximum number to show: \n");
    store = scanf("%d", &user_interface);

    while(store != 1 || user_interface <=0)
    {
        printf("Error: please enter an (positive) integer");
        fgets(temp, 25, stdin);
        store = scanf("%d", &user_interface);
    }

    return user_interface;
}
```

**print_table(int tab):** This function generates and prints a table where each row contains a number from 0 to the user-defined maximum value. It calls the is_multiple3() function for each number, printing "Yes" if the number is a multiple of 3 and "No" if it is not.

```
void print_table(int tab)
{
    int multiple;

    printf("Number  Multiple of 3? \n");
    printf("%6d %3s\n", 0, "No");

    for(multiple = 1; multiple <= tab; multiple++)
    {
        if (is_multiple3(multiple) == 1)
        {
            printf("%6d %3s\n", multiple, "Yes");
        }
        else
        {
            printf("%6d %3s\n", multiple, "No");
        }
    }
}

```
**Conclusion:**
This simple C project serves as both a useful exercise for understanding conditionals and loops, and a fun way to experiment with user input validation. The project is designed to be user-friendly and robust, ensuring that only valid input is accepted. It can be expanded upon to check for other mathematical conditions or modified to work with larger sets of numbers. Feel free to fork this repository and improve upon it with additional features such as checking for multiples of other numbers or allowing users to define custom divisibility rules.
