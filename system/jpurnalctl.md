`journalctl` is a command-line utility used for querying and viewing system logs stored in the systemd journal. It is commonly used on Linux-based operating systems that use systemd as their init system. The systemd journal is a centralized logging system that collects and stores log messages from various components of the system, including services, the kernel, and system processes.

Here are some common `journalctl` commands and their purposes:

1. **View All System Logs:**

   ```bash
   journalctl
   ```

   This command displays all system logs, starting with the most recent entries. It provides a continuous log output, allowing you to scroll through logs as new entries are added.

2. **Filter Logs by Service:**

   ```bash
   journalctl -u service_name
   ```

   This command filters logs to show only entries related to a specific service. Replace `service_name` with the name of the service you want to inspect.

3. **View Logs with Real-time Updates:**

   ```bash
   journalctl -f
   ```

   Use this command to view logs in real-time. It continuously updates the log output as new log entries are recorded.

4. **Filter Logs by Time Range:**

   ```bash
   journalctl --since "yyyy-mm-dd HH:MM:SS" --until "yyyy-mm-dd HH:MM:SS"
   ```

   This command allows you to view logs within a specific time range. Replace the date and time values with the desired start and end times.

5. **View Logs from the Previous Boot:**

   ```bash
   journalctl -b -1
   ```

   Use this command to display logs from the previous system boot. `-1` represents the boot immediately preceding the current one, `-2` represents the boot before that, and so on.

6. **Display Logs in a Pager (Less):**

   ```bash
   journalctl | less
   ```

   This command pipes the journal output to the `less` pager, allowing you to navigate through logs more easily.

7. **View Logs from a Specific File:**

   ```bash
   journalctl -u service_name -b -0 -o cat
   ```

   This command displays logs from a specific service (`service_name`) in the current boot (`-b 0`) and formats them as plain text (`-o cat`).

8. **Clear Old Logs to Free Disk Space:**

   ```bash
   sudo journalctl --vacuum-time=duration
   ```

   This command removes older log entries to free up disk space, where `duration` specifies how far back in time to keep logs. For example, `--vacuum-time=30d` retains logs from the last 30 days.

`journalctl` provides powerful tools for inspecting system logs, diagnosing issues, and monitoring system activity. It is especially useful for troubleshooting problems and tracking system events.
