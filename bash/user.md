The `useradd` command is used to add new user accounts to the system. It allows you to specify various user account attributes, such as the username, user ID (UID), group ID (GID), home directory, shell, and more. Here's a snippet of the `useradd` command along with an example:

**Basic Syntax:**
```bash
useradd [options] username
```

**Common Options:**
- `-c, --comment COMMENT`: Add a comment or description for the user.
- `-d, --home HOME_DIR`: Specify the home directory for the user.
- `-g, --gid GROUP`: Set the initial login group of the user.
- `-G, --groups GROUPS`: Specify additional groups for the user.
- `-s, --shell SHELL`: Set the user's login shell.
- `-u, --uid UID`: Set the user's numerical user ID.

**Example: Creating a New User**

```bash
sudo useradd -m -s /bin/bash johndoe
```

- This command creates a new user named `johndoe` with the following attributes:
  - `-m`: Create the user's home directory if it doesn't exist.
  - `-s /bin/bash`: Set the user's login shell to `/bin/bash`.

**Additional User Management Commands:**

After creating a user, you may also need to set or modify their password, as well as manage user accounts. Here are some additional user management commands:

1. **Setting a Password for the User:**
   ```bash
   sudo passwd johndoe
   ```

   - This command allows you to set or change the password for the user `johndoe`.

2. **Adding User to a Group:**
   ```bash
   sudo usermod -aG groupname johndoe
   ```

   - Use `usermod` to add the user `johndoe` to an existing group (`groupname`).

3. **Modifying User Attributes:**
   ```bash
   sudo usermod -c "John Doe" -s /bin/zsh johndoe
   ```

   - Use `usermod` to modify user attributes like the comment and shell.

4. **Deleting a User:**
   ```bash
   sudo userdel -r johndoe
   ```

   - To delete the user `johndoe`, including their home directory and mail spool, use `userdel` with the `-r` option.

These commands provide a basic overview of how to manage user accounts in Linux. Proper user management is essential for system administration and security.
