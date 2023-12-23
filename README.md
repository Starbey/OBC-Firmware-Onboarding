<<<<<<< HEAD
# OBC Firmware Onboarding Challenge

Welcome to Orbital's OBC Firmware Onboarding Challenge! Please visit [this Notion doc](https://www.notion.so/uworbital/Firmware-Onboarding-Challenge-Updated-24340dfccb0547a5a7246ce6d7207c28) for the challenge instructions. Remember to follow our style guide which is written below.

## Style Guide

### Comments

#### Single Line Comments

Variable and function names should be descriptive enough to understand even without comments. Comments are needed to describe any complicated logic. You may use `//` or `/* */` for single line comments.

#### Function Comments

Function comments should exist in the .h file. For static functions, they should exist in the .c file. Function comments should follow the format shown below:
```c
/**
 * @brief Adds two numbers together
 *
 * @param num1 - The first number to add.
 * @param num2 - The second number to add.
 * @return Returns the sum of the two numbers.
 */
uint8_t addNumbers(uint8_t num1, uint8_t num2);
```

#### File Header Comments

- File comments are not required

#### Header Guard

We use `#pragma once` instead of include guards.

### ****Naming and typing conventions****

-   `variableNames` in camelCase
-   `functionNames()` in camelCase
-   `#define MACRO_NAME` in CAPITAL_SNAKE_CASE
-   `file_names` in snake_case
-   `type_defs` in snake_case with _t suffix
    -   Ex:
        ```c
        typedef struct {
          int a;
          int b;
        } struct_name_t
        ```
-   Import statements should be grouped in the following order:
    1.  Local imports (e.g. `#include "cc1120_driver.h`)
    2.  External library imports (e.g. `#include <os_semphr.h>`)
    3.  Standard library imports (e.g. `#include <stdint.h>`)

### ****General Rules****
Some of these rules don't apply in certain cases. Use your better judgement. To learn more about these rules, research NASA's Power of 10.

1. Avoid complex flow constructs, such as [goto](https://en.wikipedia.org/wiki/Goto) and [recursion](https://en.wikipedia.org/wiki/Recursion_(computer_science)).
2. All loops must have fixed bounds. This prevents runaway code.
3. Avoid [heap memory allocation](https://en.wikipedia.org/wiki/Memory_management#DYNAMIC).
4. Use an average of two [runtime assertions](https://en.wikipedia.org/wiki/Assertion_(software_development)#Assertions_for_run-time_checking) per function.
5. Restrict the scope of data to the smallest possible.
6. Check the return value of all non-void functions, or cast to void to indicate the return value is useless.
7. Limit pointer use to a single [dereference](https://en.wikipedia.org/wiki/Dereference_operator), and do not use [function pointers](https://en.wikipedia.org/wiki/Function_pointer).
8. Compile with all possible warnings active; all warnings should then be addressed before release of the software.
9. Use the preprocessor sparingly
10. Restrict functions to a single printed page
=======
# C Programming Challenge - Level 1

This mini-challenge is intended to test your knowledge of C programming. There are 13 C programming questions that can be found in the `challenge.c` file. Your solution to this challenge will be verified automatically on a standard Linux machine once you make a pull request.

To test your solutions locally, you can use the provided Dockerfile to build a Docker image that will run the tests for you.

If you do not have Docker installed on your machine, you can follow the instructions <a href="https://www.notion.so/uworbital/How-To-Docker">here</a>.
 
To build the Docker image, run:
```
docker build -t fw-onboarding-level1 .
```

You can then run the container with:
```
docker run -it --rm -v $(pwd):/app fw-onboarding-level1 /bin/bash
```

This will open a bash shell inside the container. From there, you can begin working on the challenge. You can stay in the container as long as you want, and you can exit the container by typing `exit`.
In order to test your solutions, you'll need to compile the challenge.c file. You can do this by running the following commands in the bash shell:
```
make clean
make all
./build/challenge
```
This will use the provided Makefile to compile the `challenge.c` file and run the resulting executable.

If you've answered all the questions correctly, you'll pass all the test cases. There should be zero build errors/warnings.

>>>>>>> 6df21af9cecf5bf3c546234122cd02763c1cc341
