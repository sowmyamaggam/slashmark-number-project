# slashmark-number-project
# Number Guessing Game


import random


print("=== NUMBER GUESSING GAME ===")


secret_number = random.randint(1, 100)
attempts = 0


while True:
    guess = input("Enter your guess (1-100): ")


    # Check if input is a number
    if not guess.isdigit():
        print("Please enter a valid number!")
        continue


    guess = int(guess)
    attempts += 1


    if guess < secret_number:
        print("Too low! Try again.")


    elif guess > secret_number:
        print("Too high! Try again.")


    else:
        print("Congratulations! You guessed the number.")
        print("Total attempts:", attempts)
        break
