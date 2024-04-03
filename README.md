import random

def number_guessing_game():
    # Set the range for the random number
    min_number = 1
    max_number = 100
    target_number = random.randint(min_number, max_number)
    
    print("Welcome to the Number Guessing Game!")
    print(f"I'm thinking of a number between {min_number} and {max_number}. Can you guess it?")
    
    # Initialize variables
    attempts = 0
    guessed_number = None
    
    # Main game loop
    while guessed_number != target_number:
        try:
            guessed_number = int(input("Enter your guess: "))
            attempts += 1
            
            if guessed_number < target_number:
                print("Too low! Try again.")
            elif guessed_number > target_number:
                print("Too high! Try again.")
            else:
                print(f"Congratulations! You've guessed the number {target_number} in {attempts} attempts!")
        
        # Handle non-integer inputs
        except ValueError:
            print("Please enter a valid integer.")

# Call the function to start the game
number_guessing_game(1 to 100)
