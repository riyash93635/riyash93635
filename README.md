import random

def guessing_game():
    print("Welcome to the Number Guessing Game!")
    print("I'm thinking of a number between 1 and 100.")
   
    secret_number = random.randint(1, 100)
    max_attempts = 10
    attempts = 0
    
    while attempts < max_attempts:
        try:
            # Get the user's guess
            guess = int(input(f"Attempt {attempts + 1}/{max_attempts}. Take a guess: "))
           
            attempts += 1
        
            if guess < secret_number:
                print("Too low! Try again.")
            elif guess > secret_number:
                print("Too high! Try again.")
            else:
                print(f"Congratulations! You guessed it in {attempts} attempts. The number was {secret_number}.")
                break
        except ValueError:
            print("Please enter a valid number.")
    
    if attempts == max_attempts and guess != secret_number:
        print(f"Sorry, you've used all your attempts. The number was {secret_number}. Better luck next time
guessing_game()

<!---
riyash93635/riyash93635 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
