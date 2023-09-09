**Day 4: Dictionaries, Sets and File Handling (Approx. 20 minutes each)**

**Session 1 (Dictionaries - 20 minutes):**

- **Dictionaries**

  **Explanation (5 minutes):**
  - Dictionaries are versatile data structures that store data as key-value pairs. They are unordered and mutable, allowing for efficient data organization.
  - Key-value pairs are similar to real-world dictionaries, where words (keys) have corresponding definitions (values).

    - **In python we already have list and tuple then why dictionary?**  
        - In Python, dictionaries serve a distinct and valuable role compared to lists and tuples. While lists and tuples are both used for storing collections of data, dictionaries provide a different way to organize and access data. Here are some key reasons why dictionaries are essential:

        1. **Key-Value Mapping:**  
        Dictionaries are primarily used for creating key-value mappings. Each item in a dictionary consists of a key and its associated value. This key-value relationship makes dictionaries especially useful when you need to look up values based on specific keys.

        2. **Fast Lookups:**  
        Dictionaries provide fast lookups because they use a hash table data structure internally. This means that you can quickly retrieve a value associated with a key, even if the dictionary contains a large number of items. Lists and tuples, on the other hand, require iterating through elements to find a specific value, which can be slower for large collections.

        3. **Unordered:**  
        Dictionaries are unordered collections, which means that the order of items is not guaranteed. This is different from lists and tuples, which maintain a specific order. Dictionaries are designed for efficient key-based retrieval rather than maintaining order.

        4. **Flexibility:**  
        Dictionaries can store a wide range of data types as both keys and values. This flexibility allows you to create data structures that are more complex and versatile than lists or tuples, which typically store homogeneous data.

        5. **Labeling Data:**  
        Dictionaries are often used to label or tag data. They provide a way to associate descriptive keys with values, making it easier to understand the meaning of each data point in a collection.

        6. **Data Transformation:**  
        Dictionaries are instrumental when transforming or restructuring data. They allow you to map data from one form to another efficiently. For example, you can convert data from a list of pairs into a dictionary for easier access and manipulation.

        7. **Avoiding Index-Based Access:**  
        While lists and tuples rely on index-based access (e.g., `my_list[2]`), dictionaries allow you to access values using meaningful keys (e.g., `my_dict['age']`). This can lead to more readable and self-explanatory code.

        8. **Data Retrieval by Attribute:**  
        Dictionaries are commonly used in object-oriented programming to represent objects with attributes. Each attribute is stored as a key, and its value can be retrieved by name, similar to accessing object attributes.

        In summary, dictionaries are a crucial data structure in Python because they offer a way to organize and access data based on meaningful keys. While lists and tuples are valuable for ordered collections of data, dictionaries excel in scenarios where fast and meaningful data retrieval is required. Each data structure has its own purpose and use cases, and choosing the right one depends on your specific programming needs.

  **Creating Dictionaries (5 minutes):**
  - Dictionaries can be created using:
    - Curly braces: `{key1: value1, key2: value2, ...}`
    - The `dict()` constructor: `dict(key1=value1, key2=value2, ...)`
    - Initializing an empty dictionary: `my_dict = {}`

  **Accessing Elements (5 minutes):**
  - To access values, use square brackets with the key: `my_dict[key]`.
    - Use the `get()` method for safe access; it returns a default value if the key doesn't exist.

  **Modifying Dictionaries (5 minutes):**
  - Dictionaries are mutable, allowing for adding, updating, or removing key-value pairs:
    - Adding: `my_dict[new_key] = new_value`
    - Updating: `my_dict[existing_key] = new_value`
    - Removing: `del my_dict[key_to_remove]`

  **Python Code (10 minutes):**
  ```python
  # Creating dictionaries
  contact = {"John": "john@email.com", "Alice": "alice@email.com", "Bob": "bob@email.com"}
  empty_dict = {}

  # Accessing values
  email = contact["Alice"]  # Output: "alice@email.com"

  # Safely accessing values with get()
  phone = contact.get("Charlie", "Not found")  # Output: "Not found"

  # Modifying dictionaries
  contact["Eve"] = "eve@email.com"
  del contact["Bob"]

  # Using dictionary comprehension
  numbers = [1, 2, 3, 4, 5]
  squares = {x: x**2 for x in numbers}  # Output: {1: 1, 2: 4, 3: 9, 4: 16, 5: 25}
  ```

  - This code illustrates creating, accessing, and modifying dictionaries, including safe access with `get()` and the use of dictionary comprehensions.

  - What is a dictionary comprehension?  
    Dictionary comprehensions are a concise and Pythonic way to create dictionaries. They allow you to generate dictionaries in a single line of code by specifying the key-value pairs using a loop and an expression. Dictionary comprehensions have a similar syntax to list comprehensions, but instead of creating lists, they create dictionaries.

    The basic syntax of a dictionary comprehension is as follows:

    ```python
    {key_expression: value_expression for element in iterable}
    ```

    Here's how dictionary comprehensions work:

    1. You specify a `key_expression` and a `value_expression` that define how the keys and values of the dictionary should be generated for each element in the `iterable`.

    2. The `iterable` is usually a list, tuple, or any iterable data structure that you want to loop through.

    3. The loop iterates over each element in the `iterable`, and for each element, the `key_expression` and `value_expression` are evaluated to generate a key-value pair in the resulting dictionary.

    4. The key-value pairs are added to the dictionary.

    Here's a simple example that demonstrates the use of a dictionary comprehension to create a dictionary of squares:

    ```python
    numbers = [1, 2, 3, 4, 5]
    squares = {x: x**2 for x in numbers}
    ```

    In this example, the `numbers` list is iterated, and for each number `x`, the dictionary comprehension generates a key-value pair where the key is the number itself, and the value is its square. After the comprehension is executed, the `squares` dictionary will contain `{1: 1, 2: 4, 3: 9, 4: 16, 5: 25}`.

    Dictionary comprehensions are a powerful and concise way to create dictionaries from existing data or perform transformations on data while constructing dictionaries. They can make your code more readable and efficient when dealing with data that can be structured as key-value pairs.

    - What is the difference between dictionary comprehensions and the normal way of creating dictionaries?
        Dictionary comprehensions and the normal way of creating dictionaries in Python both serve the purpose of constructing dictionaries, but they differ in terms of readability, conciseness, and ease of use. Let's compare both methods:

        **1. Dictionary Comprehensions:**

        **Pros:**

        - Concise: Dictionary comprehensions allow you to create dictionaries in a single line of code, making them concise and easy to read.
        
        - Expressive: They are expressive and allow you to specify how keys and values should be generated from an iterable.

        - Pythonic: They follow the Pythonic philosophy of "readability counts," as they often make your code more readable and elegant.

        **Cons:**

        - Limited Use: Dictionary comprehensions are best suited for cases where you can generate key-value pairs based on a straightforward expression.

        **Example:**
        
        ```python
        numbers = [1, 2, 3, 4, 5]
        squares = {x: x**2 for x in numbers}
        ```

        **2. Normal Way of Creating Dictionaries:**

        **Pros:**

        - Versatility: The normal way allows for more complex logic when constructing dictionaries. You can use loops and conditional statements for more intricate key-value assignments.

        - Readability: In some cases, using traditional loops can be more readable, especially when the logic for generating key-value pairs is complex.

        **Cons:**

        - Verbosity: It can be more verbose and require more lines of code compared to dictionary comprehensions.

        - Readability Trade-off: Complex dictionary construction logic can make code harder to read and maintain.

        **Example:**

        ```python
        numbers = [1, 2, 3, 4, 5]
        squares = {}
        for x in numbers:
            squares[x] = x**2
        ```

        **Which to Choose:**

        - Use dictionary comprehensions when you have a simple and straightforward mapping of keys to values, as they are concise and enhance code readability.

        - Use the normal way of creating dictionaries when you need more complex logic, conditionals, or need to work with data structures that require iterative processing before constructing the dictionary.

        In practice, the choice between dictionary comprehensions and the traditional approach depends on the specific requirements and complexity of your task. Both methods have their place in Python programming and can be used as needed to achieve your goals while maintaining code clarity and maintainability.

- **Sets**  
    Sets are a fundamental data structure in Python that represent a collection of unique and unordered elements. In a set, each element can only appear once, ensuring that there are no duplicate values. Sets are denoted by curly braces `{}` or by using the `set()` constructor. Here's a detailed explanation of sets, along with examples in both daily life and coding:

    **1. Basics of Sets:**

    - **Definition:** A set is an unordered collection of unique elements.

    - **Syntax:** Sets are defined using curly braces `{}` or by using the `set()` constructor.

    **Example:**

    ```python
    fruits = {"apple", "banana", "cherry"}
    ```

    **Daily Life Analogy:**

    Think of a set as a bag of unique items. For example, a bag of unique keys to various rooms in a building. Each key appears only once in the bag, and you can quickly check if a key belongs to the set.

    **2. Creating Sets:**

    - You can create a set by enclosing elements in curly braces `{}` or by using the `set()` constructor.

    **Examples:**

    ```python
    # Using curly braces
    colors = {"red", "green", "blue"}

    # Using the set() constructor
    shapes = set(["circle", "square", "triangle"])
    ```

    **3. Set Operations:**

    - Sets support various operations such as union, intersection, difference, and symmetric difference, which allow you to perform operations on sets similar to how you would with mathematical sets.

    **Examples:**

    ```python
    # Union
    set1 = {1, 2, 3}
    set2 = {3, 4, 5}
    union_set = set1 | set2  # or set1.union(set2)

    # Intersection
    intersection_set = set1 & set2  # or set1.intersection(set2)

    # Difference
    difference_set = set1 - set2  # or set1.difference(set2)

    # Symmetric Difference
    symmetric_difference_set = set1 ^ set2  # or set1.symmetric_difference(set2)
    ```

    **Daily Life Analogy:**

    Consider two shopping carts with items. Union represents all items in both carts, intersection represents items common to both carts, difference represents items only in one cart, and symmetric difference represents items in either cart but not in both.

    **4. Adding and Removing Elements:**

    - You can add elements to a set using the `add()` method and remove elements using the `remove()` or `discard()` method.

    **Examples:**

    ```python
    my_set = {1, 2, 3}

    # Adding an element
    my_set.add(4)

    # Removing an element
    my_set.remove(2)  # Raises an error if the element doesn't exist

    # Removing an element safely
    my_set.discard(5)  # No error even if the element doesn't exist
    ```

    **5. Set Comprehensions:**

    - Similar to list comprehensions, you can create sets using set comprehensions, which allow you to generate sets with a concise and readable syntax.

    **Example:**

    ```python
    squares = {x**2 for x in range(1, 6)}
    ```

    **Daily Life Analogy:**

    Think of set comprehensions as a way to create a unique collection of items based on a rule. For example, collecting unique coins from different countries based on their value.

    **6. Common Use Cases:**

    - Sets are often used for tasks that require uniqueness checking, membership testing, and set operations.

    **Examples:**

    - Removing duplicates from a list:

    ```python
    numbers = [1, 2, 2, 3, 4, 4, 5]
    unique_numbers = list(set(numbers))
    ```

    - Checking if a user's input contains unique values.

    **In Summary:**

    Sets are a valuable data structure when you need to work with collections of unique and unordered elements. They offer fast membership testing and support set operations for comparing and combining sets. In daily life, sets can be likened to collections of distinct items, such as unique coins, keys, or even a unique list of ingredients for recipes. In coding, sets simplify tasks involving uniqueness and set operations.

**Session 2 (File Handling - 20 minutes):**

- **File Handling**

  **Explanation (5 minutes):**
  - File handling is essential for reading and writing data to and from files in Python.
  - Proper file closure and exception handling are crucial for data integrity and error handling.

  **Reading from Files (5 minutes):**
  - Open files with modes like 'r' (read) and read data using methods like `read()`, `readline()`, or by iterating over lines with a `for` loop.

  **Writing to Files (5 minutes):**
  - Open files in write mode ('w') or append mode ('a') and use methods like `write()` or `writelines()` for writing.
  - Pay attention to data formatting for better readability.

  **Using "with" Statement (5 minutes):**
  - The "with" statement ensures proper file handling by automatically closing files when the block is exited.
  - It can also be used for other custom contexts.

  **Error Handling (5 minutes):**
  - Use `try` and `except` blocks for error handling when working with files.
  - Handle exceptions such as `FileNotFoundError` and `PermissionError` gracefully.

  **Python Code (10 minutes):**
  ```python
  # Reading from a file line by line
  with open("sample.txt", "r") as file:
      for line in file:
          print(line, end="")

  # Writing to a file with formatting
  with open("output.txt", "w") as file:
      file.write("Line 1: This is a sample line.\n")
      file.write("Line 2: Another line here.\n")

  # Appending to a file
  with open("output.txt", "a") as file:
      file.write("Line 3: Appended line.\n")

  # Error handling example
  try:
      with open("nonexistent.txt", "r") as file:
          content = file.read()
  except FileNotFoundError:
      print("File not found.")
  except PermissionError:
      print("Permission denied.")
  ```

  - This code demonstrates reading from and writing to files, proper file closure using the "with" statement, and error handling when working with files.

**Session 3 (Practical Exercises and Examples - 20 minutes):**

- **Exercise 1: Contact Book (7 minutes)**

    **Question:**
    Create a contact book program using a dictionary to store contacts as key-value pairs. Implement a menu-driven interface allowing users to:
    - Add new contacts with names as keys and contact information as values.
    - View existing contacts by iterating through the dictionary.
    - Delete contacts by providing a name (key) to remove.
    - Save the contact dictionary to a file (e.g., JSON) for persistence between sessions.

    **Code Solution:**
    ```python
    # Initialize an empty contact dictionary
    contacts = {}

    while True:
        print("\nContact Book Menu:")
        print("1. Add Contact")
        print("2. View Contacts")
        print("3. Delete Contact")
        print("4. Exit")
        
        choice = input("Enter your choice (1/2/3/4): ")

        if choice == "1":
            # Add a new contact
            name = input("Enter the name: ")
            email = input("Enter the email: ")
            contacts[name] = email
            print(f"Contact {name} added.")

        elif choice == "2":
            # View all contacts
            if not contacts:
                print("Contact book is empty.")
            else:
                print("\nContacts:")
                for name, email in contacts.items():
                    print(f"{name}: {email}")

        elif choice == "3":
            # Delete a contact
            name = input("Enter the name to delete: ")
            if name in contacts:
                del contacts[name]
                print(f"Contact {name} deleted.")
            else:
                print(f"Contact {name} not found.")

        elif choice == "4":
            # Exit the program
            break

        else:
            print("Invalid choice. Please enter a valid option.")

    # Save the contact dictionary to a file (e.g., JSON) for persistence
    import json

    with open("contacts.json", "w") as file:
        json.dump(contacts, file)

    print("Contact book saved.")
    ```

- **Exercise 2: Word Frequency Counter (7 minutes)**

    **Question:**
    Create a program to read a text file and count the frequency of each word. Implement data preprocessing steps such as removing punctuation and converting text to lowercase. Create a dictionary to store word frequencies as key-value pairs. Finally, display the most frequent words and their frequencies.

    **Code Solution:**
    ```python
    import string

    # Read the text file
    with open("text.txt", "r") as file:
        text = file.read().lower()  # Convert text to lowercase

    # Remove punctuation and split into words
    translator = str.maketrans('', '', string.punctuation)
    words = text.translate(translator).split()

    # Create a dictionary to store word frequencies
    word_freq = {}

    for word in words:
        if word in word_freq:
            word_freq[word] += 1
        else:
            word_freq[word] = 1

    # Find the most frequent words
    sorted_freq = sorted(word_freq.items(), key=lambda x: x[1], reverse=True)

    # Display the top 10 most frequent words
    print("\nTop 10 Most Frequent Words:")
    for word, freq in sorted_freq[:10]:
        print(f"{word}: {freq} times")
    ```

- **Exercise 3: Temperature Log (6 minutes)**

    **Question:**
    Create a program that logs temperature data to a file for record-keeping. Design a user-friendly interface that allows users to:
    - Add new temperature records with a timestamp.
    - View historical temperature data, including timestamps.
    Utilize a file format suitable for storing time-series data (e.g., CSV) for easy retrieval and analysis.

    **Code Solution:**
    ```python
    import csv
    import datetime

    # Create a function to add a temperature record
    def add_temperature_record():
        timestamp = datetime.datetime.now().strftime("%Y-%m-%d %H:%M:%S")
        temperature = float(input("Enter temperature (°C): "))
        
        with open("temperature_log.csv", mode="a", newline="") as file:
            writer = csv.writer(file)
            writer.writerow([timestamp, temperature])
        
        print(f"Temperature recorded at {timestamp}.")

    # Create a function to view temperature history
    def view_temperature_history():
        with open("temperature_log.csv", mode="r") as file:
            reader = csv.reader(file)
            print("\nTemperature History:")
            for row in reader:
                timestamp, temperature = row
                print(f"{timestamp}: {temperature} °C")

    while True:
        print("\nTemperature Log Menu:")
        print("1. Record Temperature")
        print("2. View Temperature History")
        print("3. Exit")
        
        choice = input("Enter your choice (1/2/3): ")

        if choice == "1":
            add_temperature_record()

        elif choice == "2":
            view_temperature_history()

        elif choice == "3":
            break

        else:
            print("Invalid choice. Please enter a valid option.")
    ```
