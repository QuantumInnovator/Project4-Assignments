<!-- Problem Statement
10 even 11 odd 12 even 13 odd 14 even 15 odd 16 even 17 odd 18 even 19 odd -->




# Loop through numbers from 10 to 19
for num in range(10, 20):
    # Check if the number is even or odd
    if num % 2 == 0:
        print(f"{num} even", end=" ")
    else:
        print(f"{num} odd", end=" ")
