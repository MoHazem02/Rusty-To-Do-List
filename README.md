# Rusty-To-Do-List

Rusty-To-Do-List is a command-line to-do tracker written in Rust. It allows users to record tasks into a text file, display them as a list in the terminal, and mark them as complete.
![image](https://github.com/MoHazem02/Rusty-To-Do-List/assets/66066832/8096f093-1e0a-4a1f-a0b2-2df2259892c9)

## Features

The program interface supports three main actions:

1. **Add New Tasks**: Users can add new tasks to their to-do list.
2. **Remove Completed Tasks**: Completed tasks can be removed from the list.
3. **Print All Current Tasks**: Users can view all the tasks currently in the list.

## Data Storage

To persist to-do items, the program utilizes a text file. Tasks are stored in a file format like JSON to encode the information. The program handles saving data to storage and retrieving it from storage seamlessly.

## Dependencies

The following dependencies are used in this project:

- `anyhow = "1.0.83"`: For flexible error handling.
- `structopt = "0.3.26"`: For parsing command-line arguments.
- `serde_json = "1.0"`: For JSON serialization and deserialization.
- `home = "0.5.9"`: For determining the user's home directory.
- `chrono = { version = "0.4", features = ["serde"] }`: For handling date and time, with serde support for serialization.
- `serde = { version = "1.0", features = ["derive"] }`: For JSON serialization and deserialization.

## Usage

To use the Rusty-To-Do-List, follow these steps:

1. Clone the repository to your local machine.
2. Navigate to the project directory.
3. Build the project using Cargo.
4. Run the executable file with appropriate command-line arguments to add, remove, or print tasks.

Example:
```bash
cargo run -- -j test-journal.json add "Buy groceries"
cargo run -- -j test-journal.json add "Finish Embedded Course"
cargo run -- -j test-journal.json done 1
cargo run -- -j test-journal.json list
```

