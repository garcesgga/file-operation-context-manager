Context managers in Python provide a clean way to set up and tear down resources automatically, ensuring safe and efficient code execution.

# File operation context manager
This project demonstrates how to create and use a custom context manager in Python to handle file operations safely, printing messages when starting and ending the process.

## Project Files
- `file_operation_context_manager.py`: contains the Python code with a custom context manager and usage example.
- `dados.txt`: simple database example used as input file, containing sample records (e.g., address, name, age, salary).


## Example

```python
from contextlib import contextmanager

@contextmanager
def file_operation(path: str):
    print("Starting operation...")
    file = open(path, "r", encoding="utf-8")
    try:
        yield file
    finally:
        file.close()
        print("Ending operation...")

# Usage:
with file_operation("data.txt") as f:
    for line in f:
        print(line.strip())
