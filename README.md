# TaskManager

TaskManager is a simple Python package for managing tasks. It's designed to be used in command-line interface (CLI) applications, providing basic task management functionality.

## Description

This package was created as part of a learning project to understand Python package development and distribution. It has evolved into a more robust solution for task management, incorporating features that allow users to easily add, remove, and track tasks along with their priorities.

The TaskManager package provides functionality to:
- Add tasks to a to-do list with customizable priority levels
- Mark tasks as completed
- Remove tasks from the list
- View current tasks and completed tasks
- Generate detailed reports of tasks
- Support for both string and integer priority types

# WHAT'S NEW IN 1.0.0:

In version **1.0.0**, the `TaskManager` class introduces several significant improvements and new features over version **0.2.7**:

- **Task Storage**: Tasks are now stored in **dictionaries** with associated **priority levels**, allowing for more flexible task management.
- **Priority Management**: Users can assign priorities to tasks (e.g., 'high', 'medium', or 'low') using either **string** or **integer** priority types.
- **Task Addition**: The `add_task()` method has been enhanced to accept both **simple string tasks** and **(task, priority) tuples**, giving users more control over task creation.
- **Improved Reporting**: Users can now generate reports filtered by **'to-do'**, **'done'**, or **all tasks**, making the reporting process more customizable.
- **Formatted Task Lists**: Task lists are now displayed with improved formatting, including task numbers and their respective priorities.
- **Enhanced Task Management**: The methods for removing tasks and marking them as done have been refined for better performance and ease of use.
- **State Handling**: Saving and loading the task manager's state via JSON files remains a core feature, but it's now more robust and integrated with the new priority system.

These changes make the `TaskManager` class more powerful and versatile, providing a better user experience and greater flexibility in managing tasks.

## Usage

Here's a quick example of how to use the TaskManager effectively:

```python
from ttask_manager.ttask_manager import TaskManager

# Create a new TaskManager instance
tm = TaskManager()

# Load existing tasks (if any)
tm.load_recent_state()

# Add multiple tasks to the to-do list
tm.add_task(("Write README","medium"), "Create setup.py", ("Push to GitHub","high"), "Test the application")

# View current to-do tasks
tm.current_state('to-do')

# Mark specific tasks as done
tm.task_done("Write README", "Test the application")

# View completed tasks
tm.current_state('done')

# Generate a report of today's tasks
tm.report()

# Clear the to-do list after completing tasks
tm.clear('todo')

# Reset both lists if needed
tm.reset()
```

This example showcases how to create a TaskManager instance, load existing tasks, manage to-do and completed tasks, generate a daily report, and reset the lists as needed.

## Features
- Add multiple tasks at once with customizable priorities
- Remove tasks from the to-do list
- Mark tasks as completed
- View current to-do list and completed tasks with formatting
- Generate customizable reports of tasks (by 'to-do', 'done', or 'all')
- Clear specific lists or reset both lists

## Development
This project was primarily created as a learning exercise in Python package development. Its simplicity is intentional, and there are no plans for significant feature additions or expansions. However, if you find a bug or have a suggestion for a minor improvement, feel free to open an issue on the GitHub repository.

## Notice

Due to the pressure of my studies, I will be taking a pause from further development on the TaskManager. Thank you for your understanding and support during this time.

## Licensing

The code in this project is licensed under MIT license.

## Author

Taha Yasser Adnan

This project is part of my journey in learning Python package development. While it may not be a groundbreaking package, it represents an important step in understanding the process of creating, packaging, and distributing Python projects.

