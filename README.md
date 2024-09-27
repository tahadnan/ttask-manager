# TaskManager

TaskManager is a simple Python package for managing tasks. It's designed to be used in command-line interface (CLI) applications, providing basic task management functionality.

## Description

This package was created as part of a learning project to understand Python package development and distribution. While it's not intended to be a comprehensive task management solution, it serves as a practical example of how to structure and package a Python project.

The TaskManager package provides functionality to:
- Add tasks to a to-do list
- Mark tasks as completed
- Remove tasks from the list
- View current tasks and completed tasks

## What's New in 0.2.5 Release:

**Enhanced Save and Load Functionality:** The save_current_state and load_recent_state methods were updated to ensure that the data.json file is saved and loaded from the same directory as the main Python file. This improves the reliability of data storage and retrieval.

## Usage

Here's a quick example of how to use the TaskManager effectively:

```python
from ttask_manager.ttask_manager import TaskManager

# Create a new TaskManager instance
tm = TaskManager()

# Load existing tasks (if any)
tm.load_recent_state()

# Add multiple tasks to the to-do list
tm.add_task("Write README", "Create setup.py", "Push to GitHub", "Test the application")

# View current to-do tasks
print(tm.current_state('to-do'))

# Mark specific tasks as done
tm.task_done("Write README", "Test the application")

# View completed tasks
print(tm.current_state('done'))

# Generate a report of today's tasks
print(tm.report())

# Clear the to-do list after completing tasks
tm.clear_todo_list()

# Reset both lists if needed
tm.reset()
```

This example showcases how to create a TaskManager instance, load existing tasks, manage to-do and completed tasks, generate a daily report, and reset the lists as needed.

## Features

- Add multiple tasks at once
- Remove tasks from the to-do list
- Mark tasks as completed
- View current to-do list and completed tasks
- Clear to-do or completed lists
- Reset both lists

## Development
This project was primarily created as a learning exercise in Python package development. Its simplicity is intentional, and there are no plans for significant feature additions or expansions. However, if you find a bug or have a suggestion for a minor improvement, feel free to open an issue on the GitHub repository.

## Notice

Due to the pressure of my studies, I will be taking a pause from further development on the TaskManager. Thank you for your understanding and support during this time.

## Licensing

The code in this project is licensed under MIT license.

## Author

Taha Yasser Adnan

This project is part of my journey in learning Python package development. While it may not be a groundbreaking package, it represents an important step in understanding the process of creating, packaging, and distributing Python projects.

