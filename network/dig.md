The `dig` command is a powerful tool for querying DNS (Domain Name System) servers to retrieve information about domain names, IP addresses, and DNS records. Here's a snippet of the `dig` command along with an example:

**Basic Syntax:**
```bash
dig [options] [domain]
```

**Common Options:**
- `@server`: Specify the DNS server to query (optional).
- `+short`: Display concise output (only the answer).
- `+trace`: Perform a trace of the DNS query.
- `+recurse`: Enable recursive query mode.
- `+noquestion`: Display the answer without the question section.

**Example: Querying DNS for an A Record**

```bash
dig +short example.com
```

- This command queries the DNS server for the A (address) record of the domain `example.com`.
- The `+short` option is used to display only the IP address associated with the domain.

**Example: Querying DNS for an MX Record**

```bash
dig +short -t MX example.com
```

- This command queries the DNS server for the MX (mail exchange) record of the domain `example.com`.
- The `-t MX` option specifies the record type to query.

**Example: Querying DNS with a Specific DNS Server**

```bash
dig @8.8.8.8 +short example.com
```

- This command queries the DNS server at IP address `8.8.8.8` for the A record of the domain `example.com`.
- The `@` symbol followed by the DNS server's IP address specifies the server to use for the query.

**Example: Performing a DNS Trace**

```bash
dig +trace example.com
```

- This command performs a DNS trace for the domain `example.com`, showing the complete path of DNS servers involved in resolving the domain.

**Example: Recursive DNS Query**

```bash
dig +recurse example.com
```

- This command requests a recursive DNS query for the domain `example.com`. The DNS server will recursively resolve the domain, starting from the root servers if necessary.

**Example: Displaying DNS Query Results without Question**

```bash
dig +noquestion example.com
```

- This command queries the DNS server for the A record of the domain `example.com`, but it displays the answer section only, excluding the question section.

These examples illustrate various use cases of the `dig` command for querying DNS information. It is a valuable tool for network administrators and developers to troubleshoot DNS-related issues and gather DNS records for domain names.
