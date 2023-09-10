**Example 1: Basic `while` Loop**

```bash
#!/bin/bash

count=1

while [ $count -le 5 ]; do
  echo "Count: $count"
  ((count++))
done
```

- This script initializes a variable `count` to 1.
- The `while` loop runs as long as the condition `[ $count -le 5 ]` is true (i.e., while `count` is less than or equal to 5).
- Inside the loop, it prints the current value of `count` and increments it.

**Example 2: Reading User Input in a `while` Loop**

```bash
#!/bin/bash

echo "Enter 'q' to quit."

while true; do
  read -p "Enter a value: " input
  if [ "$input" == "q" ]; then
    echo "Exiting..."
    break
  else
    echo "You entered: $input"
  fi
done
```

- This script reads user input in a `while` loop.
- It continues to prompt the user for input until they enter "q."
- If "q" is entered, the loop exits using the `break` statement.

**Example 3: Looping Over Lines in a File**

```bash
#!/bin/bash

file="sample.txt"

while IFS= read -r line; do
  echo "Line: $line"
done < "$file"
```

- This script reads and processes each line in a file named `sample.txt`.
- The `while` loop uses the `read` command with input redirection (`<`) to read lines from the file.
- It assigns each line to the `line` variable and then prints it.

**Example 4: Infinite Loop with User Choice**

```bash
#!/bin/bash

while true; do
  echo "Menu:"
  echo "1. Option 1"
  echo "2. Option 2"
  echo "3. Exit"
  
  read -p "Enter your choice: " choice
  
  case "$choice" in
    1)
      echo "You selected Option 1"
      ;;
    2)
      echo "You selected Option 2"
      ;;
    3)
      echo "Exiting..."
      break
      ;;
    *)
      echo "Invalid choice"
      ;;
  esac
done
```

- This script presents a menu to the user and keeps running in an infinite loop.
- The user selects options 1 or 2, and the script responds accordingly.
- Option 3 allows the user to exit the loop and end the script.

These examples illustrate different use cases for `while` loops in Bash, from basic counting to interactive menu systems and file processing.
