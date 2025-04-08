<!-- Problem Statement
Fill out the function get_first_element(lst) which takes in a list lst as a parameter and prints the first element in the list. The list is guaranteed to be non-empty. We've written some code for you which prompts the user to input the list one element at a time. -->


# Function to get the first element of the list
def get_first_element(lst):
    print(lst[0])  # Print the first element

# Main program to prompt user for list input
if __name__ == "__main__":
    n = int(input("Enter the number of elements in the list: "))
    user_list = []
    
    # Loop to get user input for each element in the list
    for _ in range(n):
        element = input("Enter an element: ")
        user_list.append(element)
    
    # Call the function to print the first element
    get_first_element(user_list)
