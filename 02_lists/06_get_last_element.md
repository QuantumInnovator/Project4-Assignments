<!-- Problem Statement
Fill out the function get_last_element(lst) which takes in a list lst as a parameter and prints the last element in the list. The list is guaranteed to be non-empty, but there are no guarantees on its length. -->

# Function to get the last element of the list
def get_last_element(lst):
    print(lst[-1])  # Print the last element

# Main program to prompt user for list input
if __name__ == "__main__":
    n = int(input("Enter the number of elements in the list: "))
    user_list = []
    
    # Loop to get user input for each element in the list
    for _ in range(n):
        element = input("Enter an element: ")
        user_list.append(element)
    
    # Call the function to print the last element
    get_last_element(user_list)
