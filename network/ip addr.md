IP addr using the `ip` command, along with examples:

**Example 1: Displaying Network Interfaces and IP Addresses**

```bash
#!/bin/bash

echo "Network Interfaces and IP Addresses:"

ip addr show
```

- This script uses the `ip addr show` command to display information about all network interfaces and their associated IP addresses.

**Example 2: Displaying IP Address of a Specific Interface**

```bash
#!/bin/bash

interface="eth0"

echo "IP Address of $interface:"

ip addr show dev "$interface" | awk '/inet / {print $2}'
```

- This script displays the IP address of a specific network interface (`eth0` in this example).
- It uses `ip addr show` with a specific interface and filters the output using `awk` to extract the IP address.

**Example 3: Adding a New IP Address to an Interface**

```bash
#!/bin/bash

interface="eth0"
new_ip="192.168.1.100/24"

echo "Adding IP Address $new_ip to $interface:"

sudo ip addr add "$new_ip" dev "$interface"
```

- This script adds a new IP address (`192.168.1.100/24`) to a network interface (`eth0` in this example) using the `ip addr add` command.
- It requires administrative privileges, so `sudo` is used.

**Example 4: Removing an IP Address from an Interface**

```bash
#!/bin/bash

interface="eth0"
ip_to_remove="192.168.1.100/24"

echo "Removing IP Address $ip_to_remove from $interface:"

sudo ip addr del "$ip_to_remove" dev "$interface"
```

- This script removes an existing IP address (`192.168.1.100/24`) from a network interface (`eth0` in this example) using the `ip addr del` command.
- It requires administrative privileges, so `sudo` is used.
