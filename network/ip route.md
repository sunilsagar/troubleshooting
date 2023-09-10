The `ip route` command is a powerful tool in Linux for configuring and displaying the routing table on a system. It allows you to view and manage the routes that network packets take to reach their destination. Here's a detailed explanation of the `ip route` command with examples:

**Basic Syntax:**
```bash
ip route [options] [command]
```

**Common Options:**
- `show`: Display the routing table.
- `add`: Add a new route.
- `del`: Delete an existing route.
- `default`: Operate on the default route.
- `via`: Specify the gateway (next-hop) for the route.
- `dev`: Specify the network interface for the route.
- `table`: Specify the routing table to use (e.g., `main`, `local`, `default`).

**Examples:**

**1. Displaying the Routing Table:**
```bash
ip route show
```
- This command displays the routing table, showing all routes and their details.

**2. Adding a New Route:**
```bash
sudo ip route add 192.168.2.0/24 via 192.168.1.1 dev eth0
```
- This command adds a route to the `192.168.2.0/24` network via the gateway `192.168.1.1` using the `eth0` network interface.

**3. Deleting a Route:**
```bash
sudo ip route del 192.168.2.0/24 via 192.168.1.1 dev eth0
```
- This command deletes the previously added route.

**4. Adding a Default Route:**
```bash
sudo ip route add default via 192.168.1.1
```
- This command adds a default route, directing all traffic to go through the gateway `192.168.1.1`.

**5. Deleting the Default Route:**
```bash
sudo ip route del default via 192.168.1.1
```
- This command deletes the default route.

**6. Specifying Multiple Routing Tables:**
```bash
ip route show table main
ip route show table local
```
- These commands display routes from the main and local routing tables, respectively. The `table` option allows you to view routes in different tables.

**7. Adding a Host-Specific Route:**
```bash
sudo ip route add 10.0.0.5/32 via 192.168.1.2
```
- This command adds a route to a specific host (`10.0.0.5`) via the gateway `192.168.1.2`.

**8. Displaying Routes with Specific Filters:**
```bash
ip route show 192.168.0.0/16
```
- This command displays routes only for the `192.168.0.0/16` network.

**9. Deleting All Routes to a Specific Network:**
```bash
sudo ip route del 192.168.0.0/16
```
- This command deletes all routes to the `192.168.0.0/16` network.

**10. Displaying Routes for a Specific Network Interface:**
```bash
ip route show dev eth0
```
- This command displays routes associated with the `eth0` network interface.

The `ip route` command is essential for managing and troubleshooting network routing on Linux systems. It allows you to view and manipulate routing tables, ensuring that network traffic reaches its intended destination.
