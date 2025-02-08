# Divisibility by 4 Program

## Problem Description

Write a complete, compilable C program that checks whether an integer entered by the user is divisible by 4. The program should handle three different cases based on the input:

1. **Negative Numbers:** The program does not accept negative numbers and will display an error message.
2. **Numbers Between 0 and 100 (Inclusive):** The program checks if the number is divisible by 4 and displays the quotient. If not divisible, it also displays the remainder.
3. **Numbers Greater Than 100:** The program calculates and displays the square root of the number with two decimal precision.

## Input Requirements

- An **integer** entered by the user.

## Output Requirements

- For negative numbers: A message indicating that negative numbers are not accepted.
- For numbers between 0 and 100:
  - A message stating whether the number is divisible by 4.
  - The **quotient** when divided by 4.
  - If not divisible, the **remainder** as well.
- For numbers greater than 100: The **square root** of the number displayed with **2-digit precision**.

## Function Requirements

The program should be modularized with the following functions:

1. **`int getInput()`**  
   - Prompts the user to enter an integer.
   - Scans the number and returns it.

2. **`int isNegative(int n)`**  
   - Returns **1** if the given number is negative, **0** otherwise.

3. **`int isInRange(int n)`**  
   - Checks if the number is between **0 and 100** (inclusive).
   - Returns **1** if true, **0** otherwise.

4. **`int isGreaterThan100(int n)`**  
   - Checks if the number is **greater than 100**.
   - Returns **1** if true, **0** otherwise.

## Function Call Order in `main`

To test the program, the functions should be called in the following order within the `main` function:

1. **Call `getInput()`** to receive the number from the user.
2. **Call `isNegative()`** to check if the number is negative.
   - If negative, print the error message.
3. If the number is not negative:
   - **Call `isInRange()`** to check if the number is between 0 and 100.
     - If true, check divisibility by 4 and print the quotient (and remainder if applicable).
   - If false, **call `isGreaterThan100()`** to handle numbers greater than 100.
     - If true, calculate and print the square root.

## Usage of `math.h`

- The program uses the **`math.h`** library to calculate the square root of numbers greater than 100 using the `sqrt` function.

## Compilation Instructions

When compiling the program, you need to link the math library using the **`-lm`** flag. 

### Example Compilation Command:
```
gcc program.c -lm
```
- `program.c` is your C source file.
- `-lm` links the math library required for functions like `sqrt`.

## Sample Input and Output

### Sample Run 1 (Negative Number)
```
Please enter an integer to see whether it is divisible by 4: -15
The program doesn't accept negative numbers
```

### Sample Run 2 (Divisible by 4)
```
Please enter an integer to see whether it is divisible by 4: 24
The number (24) is divisbile by 4
Quotient: 6
```

### Sample Run 3 (Greater Than 100)
```
Please enter an integer to see whether it is divisible by 4: 121
The entered number is greater than 100 and the square root of it is 11.00
```

### Sample Run 4 (Not Divisible by 4)
```
Please enter an integer to see whether it is divisible by 4: 77
The number (77) is not divisbile by 4
Quotient: 19
Remainder: 1
```

## Notes

- Use appropriate headers, the `main` function, and correct C syntax.
- Use `printf` with formatting specifiers to control decimal precision.

