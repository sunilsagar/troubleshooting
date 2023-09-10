The `for` loop in Bash is used for iterating over a sequence of values, such as elements in an array, files in a directory, or a specified range of numbers. Here are some `for` loop snippets in Bash with explanations:

**Example 1: Iterating over an Array**

```bash
#!/bin/bash

fruits=("apple" "banana" "cherry" "date")

for fruit in "${fruits[@]}"; do
  echo "I like $fruit"
done
```
```
I like apple
I like banana
I like cherry
I like date
```

- This script creates an array called `fruits` containing fruit names.
- The `for` loop iterates over each element in the array, and for each element, it prints a message.

**Example 2: Looping through Files in a Directory**

```bash
#!/bin/bash

directory="/path/to/directory"

for file in "$directory"/*; do
  if [ -f "$file" ]; then
    echo "Found file: $file"
  fi
done
```

- This script iterates through files in a specified directory (`/path/to/directory`).
- It checks if each item is a file using the `-f` test, and if so, it prints the file name.

**Example 3: Looping through Numbers**

```bash
#!/bin/bash

for number in {1..5}; do
  echo "Count: $number"
done
```

- This script uses a brace expansion to create a sequence of numbers from 1 to 5.
- The `for` loop iterates over each number in the sequence and prints it.

**Example 4: Looping through Command Output**

```bash
#!/bin/bash

for user in $(cat /etc/passwd | cut -d: -f1); do
  echo "User: $user"
done
```

- This script reads the usernames from the `/etc/passwd` file using `cat` and `cut`.
- The `for` loop iterates over each username and prints it.

**Example 5: Nested `for` Loop**

```bash
#!/bin/bash

for i in {1..3}; do
  echo "Outer Loop: $i"
  for j in {A..C}; do
    echo "  Inner Loop: $j"
  done
done
```

- This script demonstrates a nested `for` loop.
- The outer loop iterates over numbers 1 to 3, and for each iteration, the inner loop iterates over letters A to C.
