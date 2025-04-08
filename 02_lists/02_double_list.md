<!-- Problem Statement
Write a program that doubles each element in a list of numbers. For example, if you start with this list:

numbers = [1, 2, 3, 4]

You should end with this list:

numbers = [2, 4, 6, 8] -->

# Function to double each element in the list
def double_elements(numbers):
    for i in range(len(numbers)):
        numbers[i] *= 2  # Multiply each element by 2
    return numbers

# Example usage
numbers = [1, 2, 3, 4]
doubled_numbers = double_elements(numbers)
print("The doubled list is:", doubled_numbers)
