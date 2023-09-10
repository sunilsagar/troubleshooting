
`dnf` (Dandified YUM) is a modern package manager used in Red Hat-based Linux distributions, including Red Hat Enterprise Linux (RHEL), CentOS, and Fedora. It is the successor to the traditional `yum` package manager and offers several improvements and features. Here's an overview of `dnf` and its key features:

**Key Features of `dnf`**:

1. **Dependency Resolution**: `dnf` features robust dependency resolution, making it easier to install packages with all their required dependencies.

2. **Parallel Downloads**: `dnf` can download multiple packages simultaneously, which speeds up the installation process.

3. **Transaction History**: `dnf` keeps a transaction history, allowing you to review and undo package operations.

4. **Plugin System**: `dnf` supports plugins that extend its functionality, such as additional repositories or package management tools.

5. **Modules Support**: `dnf` introduces the concept of modules, which allows you to install and manage software stacks with different versions and profiles.

6. **Improved Performance**: `dnf` is generally faster than its predecessor, `yum`, due to its use of libsolv for dependency solving.

**Basic `dnf` Commands**:

1. **Installing Packages**:

   ```bash
   sudo dnf install package_name
   ```

   To install a package and its dependencies, use the `install` command followed by the package name.

2. **Updating Packages**:

   ```bash
   sudo dnf update
   ```

   This updates all installed packages to their latest versions.

3. **Searching for Packages**:

   ```bash
   dnf search search_term
   ```

   Use this command to search for packages based on a keyword.

4. **Listing Installed Packages**:

   ```bash
   dnf list installed
   ```

   Lists all installed packages.

5. **Removing Packages**:

   ```bash
   sudo dnf remove package_name
   ```

   Removes the specified package from your system.

6. **Listing Available Repositories**:

   ```bash
   dnf repolist
   ```

   Lists available repositories and their status.

7. **Transaction History**:

   ```bash
   dnf history list
   ```

   Lists recent package transactions.

8. **Undoing a Transaction**:

   ```bash
   sudo dnf history undo transaction_id
   ```

   Reverts a package operation based on its transaction ID.

9. **Installing Groups of Packages**:

   ```bash
   sudo dnf groupinstall group_name
   ```

   Installs a group of related packages.

Remember to replace `package_name`, `search_term`, and `group_name` with the actual names you're working with. Administrative privileges (usually `sudo`) may be required for some `dnf` commands.


10. **List Existing Repositories:**

   Before adding a new repository, it's a good practice to check the existing repositories. You can list them using the following command:

   ```bash
   dnf repolist
   ```

11. **Add a New Repository:**

   Use the `dnf config-manager` command to add a new repository. You'll typically need to provide the URL or repository ID for the repository you want to add. Here's the general syntax:

   ```bash
   sudo dnf config-manager --add-repo repository_url_or_id
   ```

   - `repository_url_or_id`: Replace this with the URL or repository ID of the repository you want to add. You can often find the repository URL on the project's website or documentation.

   For example, to add the EPEL (Extra Packages for Enterprise Linux) repository, you can use the following command:

   ```bash
   sudo dnf config-manager --add-repo=https://download.fedoraproject.org/pub/epel/epel-release-latest-8.noarch.rpm
   ```

   This command adds the EPEL repository to your system.

12. **List the Added Repository:**

   After adding the repository, you can list it to verify that it has been successfully added:

   ```bash
   dnf repolist
   ```

   The added repository should now appear in the list.

13. **Refresh the Repository Cache:**

   To ensure that the repository metadata is up to date, refresh the repository cache:

   ```bash
   sudo dnf makecache
   ```

   This step is important because it makes the packages from the new repository available for installation.

14. **Install or Update Packages:**

   With the repository added, you can use `dnf` to install or update packages from that repository.

Keep in mind that administrative privileges (usually provided by `sudo`) may be required for some `dnf` commands.


15. **Install the EPEL Repository Package:**

   EPEL provides a package called `epel-release` that you can install to add the EPEL repository configuration to your system. Use the following `dnf` command with administrative privileges to install it:

   ```bash
   sudo dnf install epel-release
   ```

   This command will download and install the `epel-release` package, which includes the repository configuration.

16. **Confirm the Repository Addition:**

   After the installation is complete, you can verify that the EPEL repository has been added to your system by listing the enabled repositories:

   ```bash
   dnf repolist
   ```

   You should see the EPEL repository listed in the output.

17. **Update the Repository Cache:**

   To ensure that the repository metadata is up to date, run the following command to update the `dnf` repository cache:

   ```bash
   sudo dnf makecache
   ```

   This step ensures that you can immediately use packages from the EPEL repository.
