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
