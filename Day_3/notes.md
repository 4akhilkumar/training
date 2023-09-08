**Day 3: Functions, Modules, and Lists/Tuples (Approx. 30 minutes)**

**Session 1 (Functions - 10 minutes):**

- **Functions**

  **Explanation:**
  - Functions are like reusable tools in programming. They allow you to define a block of code that can be called multiple times with different inputs.
  - Functions help you write clean, modular code, making it easier to understand, debug, and maintain.

  **Syntax of Function Definition:**
  - In Python, you define a function using the `def` keyword, followed by the function name and parentheses containing any parameters.
  - The basic structure of a function is as follows:

    ```python
    def function_name(parameter1, parameter2, ...):
        # Code block to execute when the function is called
        # Optionally, return a value using the "return" statement
    ```

  **Importance of Function Documentation and Naming Conventions:**
  - Functions should have clear and descriptive names that indicate their purpose.
  - Documentation in the form of docstrings is essential to explain what the function does, what parameters it accepts, and what it returns.

  **Daily Life Example:**
  - Think of a recipe as a function. A recipe provides clear instructions (the function's code) on how to cook a dish. You can use the same recipe (function) with different ingredients (parameters) to make various meals.

  **Python Code:**
  ```python
  def greet(name):
      """This function greets the person passed in as a parameter."""
      return f"Hello, {name}!"

  # Calling the function
  message = greet("Alice")
  print(message)  # Output: "Hello, Alice!"
  ```

  - In this code, the `greet` function takes a `name` parameter and returns a greeting message.

**Session 2 (Modules and Libraries - 10 minutes):**

- **Modules and Libraries**

  **Explanation:**
  - In Python, modules are files containing Python code, and libraries are collections of modules.
  - Modules and libraries are used to organize and reuse code, making it more efficient and maintainable.

  **Importing Modules:**
  - You can import built-in modules or external libraries using the `import` statement.
  - Use the `import` statement to make functions, classes, and variables defined in a module accessible in your code.

  **Creating Custom Modules:**
  - You can create your own modules by defining functions, classes, or variables in a separate `.py` file and importing them into your programs.

  **Daily Life Example:**
  - Consider a toolbox where each drawer contains different tools. Each drawer is like a module, and the tools are like functions or variables. You open a specific drawer (import a module) to access the tools you need.

  **Python Code:**
  ```python
  # Import the math module to access mathematical functions
  import math

  # Use a function from the math module
  result = math.sqrt(25)
  print(result)  # Output: 5.0
  ```

  - In this code, we import the `math` module to use the `sqrt` function for calculating the square root.

Certainly, let's provide a more convincing and relatable daily life example for tuples:

**Session 3 (Lists and Tuples - 10 minutes):**

- **Lists and Tuples**

  **Explanation:**
  - Lists and tuples are fundamental data structures in Python used to store collections of items.
  - Lists are mutable, meaning you can change their contents (add, remove, or modify items) after creation.
  - Tuples, on the other hand, are immutable, meaning they cannot be altered once defined. This immutability provides data integrity.

  **Creating Lists and Tuples:**
  - To create a list, you enclose items in square brackets `[...]`.
  - To create a tuple, you enclose items in parentheses `(...)`.
  - Items in both lists and tuples can be of different data types.

  **Accessing Elements:**
  - Elements in lists and tuples are accessed using indexing, starting from 0 for the first element.
  - You can also use negative indexing to access elements from the end.

  **Slicing:**
  - Slicing allows you to extract a portion of a list or tuple by specifying a start and end index.
  - The syntax for slicing is `list[start:end]` or `tuple[start:end]`.
  - Slicing returns a new list or tuple containing the specified elements.

  **Modifying Lists (Mutable):**
  - Lists support various operations like appending, inserting, removing, and extending elements.
  - Common list methods include `append()`, `insert()`, `remove()`, `pop()`, and `extend()`.

  **Daily Life Example:**
  - Consider a shopping list as a tuple. When you create a shopping list for a particular week, it represents a fixed plan, and you don't intend to change it during that week (immutable). In contrast, a grocery list as a list can be modified during your shopping trip as you add or remove items (mutable).

  **Python Code:**
  ```python
  # Creating a list
  grocery_list = ["apples", "bananas", "milk"]

  # Creating a tuple
  weekly_plan = ("Monday: Gym", "Tuesday: Work", "Wednesday: Dinner with friends")

  # Accessing elements
  print(grocery_list[0])  # Output: "apples"

  # Negative indexing
  print(grocery_list[-1])  # Output: "milk"

  # Slicing a list
  sliced_groceries = grocery_list[1:3]  # Output: ["bananas", "milk"]

  # Modifying a list
  grocery_list.append("eggs")
  grocery_list[1] = "oranges"
  grocery_list.remove("milk")

  # Attempting to modify a tuple will result in an error
  # weekly_plan[0] = "Tuesday: Yoga"  # TypeError: 'tuple' object does not support item assignment
  ```

  - In this code, we demonstrate the creation, indexing, slicing, and modification of both lists and tuples. Note that attempting to modify a tuple results in a TypeError due to its immutability.
