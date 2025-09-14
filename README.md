# Broskies_hubtasks.day2

📌 Task Explanation: To-Do List Application (Console-based)

Objective

The goal of this task was to implement a simple To-Do List Manager in Python. A To-Do list helps users keep track of tasks they need to complete. The application should allow adding, removing, and viewing tasks, and the tasks must be persistent (saved to a file) so they are available even after closing the program.



What We Built

We created a Console-based To-Do List Application (todo.py) with the following features:

1. View Tasks → Displays all the current tasks with numbers.
2. 2. Add Task → Allows the user to input a new task and save it.
3. Remove Task → Lets the user delete a task by selecting its number.
4. Persistent Storage → All tasks are saved in a text file (tasks.txt), so they remain available next time the program is run.
5. User-friendly Menu → Provides a simple menu to navigate the application.

 
Why We Built It

To practice Python fundamentals: lists, file handling, functions, loops, and user input.

To demonstrate how to build a real-world utility app with persistence.

To create something that is simple, practical, and extendable (later we could add deadlines, priorities, or task completion status).

This project reflects the use of software engineering basics — modular design, persistence, and user interaction.



How We Built It

We followed these steps:

1. Data Structure

Used a list to store tasks in memory.

Example: ["Buy groceries", "Complete homework", "Go jogging"].

2. Persistence with Files

Used a text file (tasks.txt) to store tasks permanently.

Functions load_tasks() and save_tasks() handle reading and writing tasks.

Used Python’s built-in open() function for file operations.

3. Core Functionalities

View tasks: Iterates through the list and displays tasks with numbering.

Add task: Takes input from user, appends to list, and saves to file.

Remove task: Deletes a task by index and updates the file.

4. Menu-driven Program

Implemented a loop with choices so users can select operations.

Keeps running until the user chooses to exit.


Sample Program Flow

==== To-Do List Menu ====
1. View Tasks
2. Add Task
3. Remove Task
4. Exit
Choose an option (1-4): 2
Enter a new task: Finish Python homework
Task 'Finish Python homework' added successfully.

==== To-Do List Menu ====
1. View Tasks
2. Add Task
3. Remove Task
4. Exit
Choose an option (1-4): 1

Your To-Do List:
1. Finish Python homework


Outcome

A persistent CLI To-Do List Application.

Demonstrates Python basics (lists, functions, file handling, loops, conditionals).

Can be extended later (add priorities, deadlines, mark tasks as complete, etc.).



📌 Interview Questions & Answers

1. How do you open and write to a file in Python?

You use the built-in open() function with appropriate mode:

# Writing to a file
with open("tasks.txt", "w") as f:
    f.write("Hello World")

"w" → write (overwrites file)

"a" → append (adds new content)

"r" → read


Using with ensures the file is closed automatically.


---

2. What are common file modes?

"r" → Read (default mode). File must exist.

"w" → Write. Creates file if not exists, overwrites if it does.

"a" → Append. Creates file if not exists, adds content at the end.

"r+" → Read and Write. File must exist.

"w+" → Write and Read. Creates/overwrites file.

"a+" → Append and Read. Creates file if not exists.



---

3. What’s the use of strip()?

Removes leading and trailing whitespace (spaces, \n, \t, etc.) from a string.


text = "  hello\n"
print(text.strip())   # "hello"

This is useful when reading lines from a file because they often include a newline character (\n).


---

4. How do lists work in Python?

Lists are ordered, mutable collections of items (can store mixed data types).

Example:


tasks = ["Read book", "Go jogging", "Buy milk"]
tasks.append("Do homework")   # adds to the end
print(tasks[0])               # "Read book"

Lists allow adding, removing, indexing, slicing, and iterating over elements.



---

5. What is the difference between append() and insert()?

append(item) → Adds an element at the end of the list.

insert(index, item) → Adds an element at a specific index.


tasks = ["A", "B"]
tasks.append("C")        # ["A", "B", "C"]
tasks.insert(1, "X")     # ["A", "X", "B", "C"]


---

6. How can you remove elements from a list?

remove(value) → Removes the first occurrence of a specific value.

pop(index) → Removes element at given index (default is last).

del list[index] → Deletes element at index.


tasks = ["A", "B", "C"]
tasks.remove("B")   # ["A", "C"]
tasks.pop(0)        # removes "A" → ["C"]


7. What are context managers (with statement)?

A context manager simplifies resource management (like files).

Using with ensures files are closed automatically, even if errors occur.


with open("tasks.txt", "r") as f:
    data = f.read()
# file is automatically closed


8. How do you loop through a file line by line?

with open("tasks.txt", "r") as f:
    for line in f:
        print(line.strip())

This is memory-efficient because it reads one line at a time instead of the whole file.


9. What is a data structure?

A data structure is a way of organizing and storing data so it can be used efficiently.

Examples in Python:

List (ordered collection)

Tuple (immutable list)

Dictionary (key-value pairs)

Set (unordered unique items)


10. What happens if the file doesn’t exist?

If you open with "r" (read), Python raises a FileNotFoundError.

If you open with "w" or "a", Python creates a new file automatically.


try:
    with open("nofile.txt", "r") as f:
        data = f.read()
except FileNotFoundError:
    print("File not found!")








