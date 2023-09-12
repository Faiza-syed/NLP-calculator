import re

def add(x, y):
    return x + y

def subtract(x, y):
    return x - y

def multiply(x, y):
    return x * y

def divide(x, y):
    return x / y

def perform_calculation(num1, num2, operation):
    if operation == 'add':
        return add(num1, num2)
    elif operation == 'subtract':
        return subtract(num1, num2)
    elif operation == 'multiply':
        return multiply(num1, num2)
    elif operation == 'divide':
        return divide(num1, num2)
    else:
        return None

print("Enter a command (e.g., 'Add 5 and 3', 'Multiply 2 by 4'):")
user_input = input("Command: ")

# Extract numbers and operation from user input using regular expressions
numbers = re.findall(r'\d+', user_input)
operation = re.findall(r'[a-zA-Z]+', user_input)

if len(numbers) == 2 and len(operation) == 2:
    num1 = float(numbers[0])
    num2 = float(numbers[1])
    result = perform_calculation(num1, num2, operation[0].lower())

    if result is not None:
        print("Result:", result)
    else:
        print("Invalid command")
else:
    print("Invalid command")
