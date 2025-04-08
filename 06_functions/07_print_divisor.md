<!-- Problem Statement
Write the helper function print_divisors(num), which takes in a number and prints all of its divisors (all the numbers from 1 to num inclusive that num can be cleanly divided by (there is no remainder to the division). Don't forget to call your function in main()!

Here's a sample run (user input is in blue):

Enter a number: 12 Here are the divisors of 12 1 2 3 4 6 12 -->

# Helper function to print divisors
def print_divisors(num):
    print(f"Here are the divisors of {num}")
    for i in range(1, num + 1):
        if num % i == 0:  # Check if 'i' is a divisor of 'num'
            print(i, end=" ")

# Main function to get user input and call the helper function
def main():
    # Ask user to enter a number
    number = int(input("Enter a number: "))
    
    # Call the helper function to print divisors
    print_divisors(number)

# Run the main function
if __name__ == "__main__":
    main()
