<!-- Problem Statement
Write a program which prompts the user to type an affirmation of your choice (we'll use "I am capable of doing anything I put my mind to.") until they type it correctly. Sometimes, especially in the midst of such uncertain times, we just need to be reminded that we are resilient, capable, and strong; this little Python program may be able to help!

Here's a sample run of the program (user input is in blue):

Please type the following affirmation: I am capable of doing anything I put my mind to. Hmmm That was not the affirmation. Please type the following affirmation: I am capable of doing anything I put my mind to. I am capable of doing anything I put my mind to. That's right! :)

Note that you can call input() with no prompt and it will still wait for a user to type something! -->

# The affirmation to be typed by the user
affirmation = "I am capable of doing anything I put my mind to."

# Continuously prompt the user until they type the affirmation correctly
while True:
    user_input = input("Please type the following affirmation: ")
    
    if user_input == affirmation:
        print("That's right! :)")
        break  # Exit the loop if the affirmation is typed correctly
    else:
        print("Hmmm That was not the affirmation.")
