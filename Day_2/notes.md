**Day 2: Conditional Statements and Loops (Approx. 30 minutes)**

**Session 1 (10 minutes):**
- **Conditional Statements (if-else)**

  **Explanation:**
  - Conditional statements are essential in programming as they allow your code to make decisions based on specific conditions, similar to how you make decisions in your daily life.
  - They are used to control the flow of your program by executing different code blocks based on whether a condition is true or false.

  **Syntax of if-else Statements:**
  - In Python, conditional statements are defined using the `if`, `elif` (optional), and `else` (optional) keywords.
  - The basic structure of an `if-else` statement is as follows:
  
    ```python
    if condition:
        # Code block to execute if condition is True
    elif another_condition:  # Optional, can have multiple elif blocks
        # Code block to execute if another_condition is True
    else:  # Optional, only one else block
        # Code block to execute if none of the conditions is True
    ```

  **Examples of Simple if-else Statements:**
  - Let's look at a real-life example: deciding whether to go outside based on the weather.

  **Python Code:**
  ```python
  weather = "rainy"

  if weather == "sunny":
      print("It's sunny outside. Let's go for a walk!")
  elif weather == "rainy":
      print("It's rainy. Better stay indoors.")
  else:
      print("The weather is unknown. Use caution.")
  ```

  - In this code, we use an `if-else` statement to decide what to do based on the value of the `weather` variable.

**Session 2 (10 minutes):**
- **Loops (for and while)**

  **Explanation:**
  - Loops are used to automate repetitive tasks or to perform actions multiple times, similar to how you might repeat certain tasks in your daily life.
  - They allow you to efficiently execute a block of code repeatedly, either for a specified number of times or until a certain condition is met.

  **Syntax and Basic Usage of "for" and "while" Loops:**
  - Python provides two primary loop constructs: `for` loops and `while` loops.
  - `for` loops are used when you know the number of iterations in advance, while `while` loops are used when you want to repeat a block of code until a certain condition is met.
  - The basic structure of a `for` loop is as follows:
  
    ```python
    for item in iterable:
        # Code block to execute for each item in the iterable
    ```

  - The basic structure of a `while` loop is as follows:
  
    ```python
    while condition:
        # Code block to execute as long as the condition is True
    ```

  **Explanation of Loop Control Statements:**
  - Python also provides loop control statements like `break` and `continue` to alter the behavior of loops.

  **"break" Statement:**
  - The `break` statement is used to exit a loop prematurely, even if the loop's condition is not met.
  - It is often used when a specific condition is met, and you want to exit the loop immediately.

  **"continue" Statement:**
  - The `continue` statement is used to skip the current iteration of a loop and continue with the next one.
  - It is often used when a certain condition is met within the loop, and you want to skip further processing for that specific iteration.

**Session 3 (10 minutes):**
- **Practice Exercises Combining Conditionals and Loops**

  **Exercise 1: Calculate Factorial**

  **Explanation:**
  - Calculating the factorial of a number involves multiplying it by all positive integers less than or equal to it. You can use a `while` loop for this.

  **Real-Life Example:**
  - Calculating the factorial is like calculating the total number of ways you can arrange a set of objects in a row.

  **Python Code:**
  ```python
  # Input
  n = int(input("Enter a number: "))

  # Initialize variables
  factorial = 1
  i = 1

  # Calculate factorial using a while loop
  while i <= n:
      factorial *= i
      i += 1

  # Output
  print(f"{n}! =", factorial)
  ```

  - In this code, the user enters a number, and we use a `while` loop to calculate its factorial.

  **Exercise 2: Print Odd Numbers**

  **Explanation:**
  - Printing odd numbers within a range can be done using a `for` loop.

  **Real-Life Example:**
  - Think about counting odd numbers on a scoreboard during a sports game.

  **Python Code:**
  ```python
  # Print odd numbers between 1 and 50 using a for loop
  for num in range(1, 51, 2):
      print(num)
  ```

  - In this code, we use a `for` loop to iterate through numbers from 1 to 50, stepping by 2 to ensure only odd numbers are printed.


- **Exercise 3: Guess the Number Game**

  **Explanation:**
  - In this exercise, you'll create a simple "Guess the Number" game where the computer selects a random number, and the player has to guess it. The game will provide hints if the guess is too high or too low.

  **Real-Life Example:**
  - This exercise simulates a common game scenario where you need to make educated guesses based on feedback.

  **Python Code:**
  ```python
  import random

  # Generate a random number between 1 and 100
  secret_number = random.randint(1, 100)

  print("Welcome to the Guess the Number game!")
  print("I'm thinking of a number between 1 and 100.")

  # Initialize variables
  attempts = 0
  max_attempts = 10  # You can adjust the maximum number of attempts
  
  while attempts < max_attempts:
      # Ask the player for their guess
      guess = int(input("Enter your guess: "))
      
      # Increment the number of attempts
      attempts += 1
  
      # Check if the guess is correct
      if guess == secret_number:
          print(f"Congratulations! You guessed the number ({secret_number})   correctly in {attempts} attempts.")
          break
      elif guess < secret_number:
          print("Too low. Try again.")
      else:
          print("Too high. Try again.")
  
  # If the player couldn't guess the number in max_attempts, reveal the   secret number
  if attempts == max_attempts:
      print(f"Sorry, you've reached the maximum number of attempts. The   secret number was {secret_number}.")
  ```
  
  - In this code, the player attempts to guess a randomly generated secret   number within a specified range. The game provides feedback on whether the guess is too high or too low, and the player has a limited number of   attempts to guess the correct number. This exercise combines loops,   conditional statements, and user input handling to create an interactive game.

  - These practice exercises combine conditional statements and loops to solve real-world problems and encourage participants to practice writing code and think logically.

Please note that these examples and exercises adhere to PEP 8 guidelines for code formatting, indentation, and naming conventions.
