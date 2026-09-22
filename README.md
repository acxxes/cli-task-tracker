# CLI Task Tracker
CLI application that takes commands to add, update and delete tasks. Tasks will be saved as a JSON file when executing the JSON command. The JSON file will be saved on the projects root folder.

## Features 
- **Add Task:** Adds a new task with a description, status, creation/update date and an id
- **Update Task:** Edit an existing task's description
- **Delete Task:** Remove a task
- **Mark Task:** Change a task's status to todo, in-progress, or done
- **List Tasks:** View all tasks, or filter by status
- **Export to JSON:** Save the current task list to `tasks.json` in the project root (manual; see command below)

## Tech Stack

- Java 21 
- Gson (JSON serialization)
- Maven

## Prerequisites

- Java 21 (or later)
- No need to install Maven separately — the project includes the Maven Wrapper (`mvnw`)

## Installation 
````bash
git clone https://github.com/acxxes/cli-task-tracker.git
cd cli-task-tracker
````

## Running the Application
````bash
./mvnw compile exec:java

````
or run the `Main` class from your IDE
## Usage
Once running you will see a `>` prompt. Available commands:
````
# Listing all commands
task-cli --help

# Adding a new task
task-cli add "{description}"

# Updating a task
task-cli update {id} "{new description}"

# Deleting a task
task-cli delete {id}

# Marking a task as in progress
task-cli mark-in-progress {id}

# Marking a task as done
task-cli mark-done {id}

# Listing all tasks
task-cli list

# Listing tasks by status
task-cli list todo
task-cli list in-progress
task-cli list done

# Create/Write JSON file
write json

# Exit the application
exit
````
## Credits
Project idea from: https://roadmap.sh/projects/task-tracker

