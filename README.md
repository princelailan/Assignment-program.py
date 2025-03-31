# Assignment-program.py
def process_file(): try: filename = input("Enter the filename to read: ") with open(filename, "r") as infile: content = infile.read()

with open("modified_" + filename, "w") as outfile:
        outfile.write(content[::-1])

    print(f"Modified content saved to modified_{filename}")
except FileNotFoundError:
    print("Error: File not found.")
except PermissionError:
    print("Error: Permission denied.")
except Exception as e:
    print(f"Unexpected error: {e}")

process_file()

