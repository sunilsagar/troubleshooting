The `case` statement in Bash is a powerful tool for conditional branching based on the value of a variable. It allows you to perform different actions depending on the value of a given variable. Here are some `case` statement snippets in Bash with explanations:

**Example 1: Basic `case` Statement**

```bash
#!/bin/bash

fruit="apple"

case "$fruit" in
  "apple")
    echo "It's an apple."
    ;;
  "banana")
    echo "It's a banana."
    ;;
  "cherry")
    echo "It's a cherry."
    ;;
  *)
    echo "Unknown fruit."
    ;;
esac
```

- This script sets the variable `fruit` to "apple" and uses a `case` statement to check its value.
- Depending on the value of `fruit`, it executes different code blocks within the `case` statement.

**Example 2: Using Patterns in `case`**

```bash
#!/bin/bash

day="Monday"

case "$day" in
  [Mm]*)
    echo "The day starts with 'M'."
    ;;
  [Tt]*)
    echo "The day starts with 'T'."
    ;;
  *)
    echo "It's another day."
    ;;
esac
```

- This script sets the variable `day` to "Monday" and uses patterns in the `case` statement to match the starting letter.
- It checks if the day starts with "M" or "T" and performs different actions based on the pattern.

**Example 3: Handling Multiple Values in a Single `case`**

```bash
#!/bin/bash

fruit="banana"

case "$fruit" in
  "apple" | "banana")
    echo "It's an apple or a banana."
    ;;
  "cherry" | "date")
    echo "It's a cherry or a date."
    ;;
  *)
    echo "Unknown fruit."
    ;;
esac
```

- This script checks the value of the `fruit` variable and performs actions if it matches either "apple" or "banana" or "cherry" or "date."

**Example 4: Using Variables in `case` Patterns**

```bash
#!/bin/bash

number=3

case "$number" in
  1)
    echo "One"
    ;;
  2)
    echo "Two"
    ;;
  3)
    echo "Three"
    ;;
  *)
    echo "Unknown number."
    ;;
esac
```

- This script uses the variable `number` to determine which action to take based on its value within the `case` statement.

**Example 5: Handling User Input**

```bash
#!/bin/bash

echo "Enter a fruit name: "
read fruit

case "$fruit" in
  "apple" | "banana")
    echo "It's a common fruit."
    ;;
  "cherry" | "date")
    echo "It's a less common fruit."
    ;;
  *)
    echo "Unknown fruit."
    ;;
esac
```

- This script reads user input for a fruit name and uses a `case` statement to determine if it's a common or less common fruit.

These examples demonstrate different use cases for the `case` statement in Bash, from basic conditional branching to more complex pattern matching and user input handling.
