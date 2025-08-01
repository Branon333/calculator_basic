#Basic Calculator Program 

#This is a simple Python calculator program that performs basic arithmetic operations (addition, subtraction, multiplication, and division) based on user input.

#Features
Takes two numbers as input

Accepts one of four operations: +, -, *, /

Performs the requested calculation

Displays the result in a user-friendly format

Handles division by zero errors

Validates operation input

#How to Use
Run the program in a Python environment

Enter the first number when prompted

Enter the second number when prompted

Enter the operation you want to perform (+, -, *, /)

#View the result

Example Usage
text
Enter the first number: 10
Enter the second number: 5
Enter the operation (+, -, *, /): +
10.0 + 5.0 = 15.0
Error Handling
Division by zero will display an error message

Invalid operations will prompt the user to enter a valid one

#Requirements
Python 3.x installed

#Installation
No installation required. Simply download the Python script and run it:

bash
python calculator.py
Code
python
# Basic Calculator Program

# Get user input
num1 = float(input("Enter the first number: "))
num2 = float(input("Enter the second number: "))
operation = input("Enter the operation (+, -, *, /): ")

# Perform the calculation
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
else:
    print("Invalid operation. Please use +, -, *, or /")

#Contributing
Contributions are welcome! Please fork the repository and submit a pull request.

#License
This project is open source and available under the MIT License.

