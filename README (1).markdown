# Basic Calculator Program

## Overview
This is a simple Python calculator program that performs basic arithmetic operations (addition, subtraction, multiplication, and division) based on user input.

## Features
- Takes two numbers as input
- Accepts one of four operations: +, -, *, /
- Performs the requested calculation
- Displays the result in a user-friendly format
- Handles division by zero errors
- Validates operation input
- Handles non-numeric input errors

## How to Use
1. Run the program in a Python environment
2. Enter the first number when prompted
3. Enter the second number when prompted
4. Enter the operation you want to perform (+, -, *, /)
5. View the result
6. Choose whether to perform another calculation

## Example Usage
**Addition**:
```
Enter the first number: 10
Enter the second number: 5
Enter the operation (+, -, *, /): +
10.0 + 5.0 = 15.0
Do you want to perform another calculation? (yes/no): no
```

**Division by Zero**:
```
Enter the first number: 10
Enter the second number: 0
Enter the operation (+, -, *, /): /
Error: Division by zero is not allowed!
Do you want to perform another calculation? (yes/no): no
```

**Invalid Operation**:
```
Enter the first number: 10
Enter the second number: 5
Enter the operation (+, -, *, /): %
Invalid operation. Please use +, -, *, or /
Do you want to perform another calculation? (yes/no): no
```

**Non-numeric Input**:
```
Enter the first number: abc
Invalid input. Please enter a valid number.
Enter the first number: 10
```

## Error Handling
- Division by zero displays an error message
- Invalid operations prompt the user to enter a valid one
- Non-numeric inputs prompt the user to enter a valid number

## Requirements
- Python 3.x installed

## Installation
No installation required. Simply download the Python script and run it:
```bash
python calculator.py
```

## Code
```python
# Basic Calculator Program

def get_number(prompt):
    while True:
        try:
            return float(input(prompt))
        except ValueError:
            print("Invalid input. Please enter a valid number.")

def get_operation():
    valid_operations = ['+', '-', '*', '/']
    while True:
        operation = input("Enter the operation (+, -, *, /): ")
        if operation in valid_operations:
            return operation
        print("Invalid operation. Please use +, -, *, or /")

def calculate(num1, num2, operation):
    if operation == '+':
        result = num1 + num2
        print(f"{num1} + {num2} = {result}")
    elif operation == '-':
        result = num1 - num2
        print(f"{num1} - {num2} = {result}")
    elif operation == '*':
        result = num1 * num2
        print(f"{num1} * {num2} = {result}")
    elif operation == '/':
        if num2 != 0:
            result = num1 / num2
            print(f"{num1} / {num2} = {result}")
        else:
            print("Error: Division by zero is not allowed!")

def main():
    while True:
        # Get user input
        num1 = get_number("Enter the first number: ")
        num2 = get_number("Enter the second number: ")
        operation = get_operation()

        # Perform the calculation
        calculate(num1, num2, operation)

        # Ask if the user wants to continue
        again = input("Do you want to perform another calculation? (yes/no): ").lower()
        if again != 'yes':
            print("Thank you for using the calculator!")
            break

if __name__ == "__main__":
    main()
```

## Contributing
Contributions are welcome! Please fork the repository and submit a pull request.

## License
This project is open source and available under the MIT License.