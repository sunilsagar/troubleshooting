`systemctl` is a command-line utility used for managing systemd services and units in Linux-based operating systems that use systemd as their init system. Systemd is a system and service manager that replaces traditional init systems like SysV init.

Here are some common `systemctl` commands and their purposes:

1. **Start a Service:**

   ```bash
   sudo systemctl start service_name
   ```

   This command starts a specified service. Replace `service_name` with the name of the service you want to start.

2. **Stop a Service:**

   ```bash
   sudo systemctl stop service_name
   ```

   This command stops a specified service.

3. **Restart a Service:**

   ```bash
   sudo systemctl restart service_name
   ```

   This command stops and then starts a specified service, effectively restarting it.

4. **Enable a Service to Start on Boot:**

   ```bash
   sudo systemctl enable service_name
   ```

   This command configures a service to start automatically when the system boots.

5. **Disable a Service from Starting on Boot:**

   ```bash
   sudo systemctl disable service_name
   ```

   This command prevents a service from starting automatically on boot.

6. **Check the Status of a Service:**

   ```bash
   systemctl status service_name
   ```

   This command provides detailed information about the status of a service, including whether it is running or not. It also displays recent log entries related to the service.

7. **List All Active Units:**

   ```bash
   systemctl list-units --type=service
   ```

   This command lists all active systemd units of the service type. It displays a summary of all running services.

8. **View a Service's Configuration:**

   ```bash
   systemctl cat service_name
   ```

   This command displays the unit file (configuration) for a service. You can view the service's configuration to understand how it's configured.

9. **Reload Systemd Configuration:**

   ```bash
   sudo systemctl daemon-reload
   ```

   Use this command after making changes to systemd unit files to reload the systemd configuration.

10. **View the Dependency Tree of a Service:**

    ```bash
    systemctl list-dependencies service_name
    ```

    This command displays the dependencies of a service in a tree-like format, showing which services it depends on and which services depend on it.

`systemctl` is a fundamental tool for managing services and system initialization in modern Linux distributions that use systemd. It simplifies the process of starting, stopping, and managing services and allows you to check the status of services and their logs.
