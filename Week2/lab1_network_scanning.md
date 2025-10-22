# Lab 1: Network Scanning Basics

## Objective
Learn to use basic network tools to explore and understand network infrastructure.

## Prerequisites
- Linux terminal access
- Basic understanding of IP addresses and networking

## Legal Notice
⚠️ **IMPORTANT**: Only scan networks and systems you own or have explicit permission to scan. Unauthorized scanning is illegal.

## Tasks

### Task 1: Basic Network Information
1. Find your IP address: `ip addr` or `ifconfig`
2. Display your routing table: `ip route` or `route -n`
3. View active network connections: `netstat -tuln`
4. Check your DNS configuration: `cat /etc/resolv.conf`

### Task 2: Using Ping
1. Ping a public server (e.g., `ping -c 4 8.8.8.8`)
2. Ping your default gateway
3. Analyze the output (time, TTL, packet loss)

### Task 3: DNS Queries
1. Use `nslookup` to query a domain name
2. Use `dig` to get detailed DNS information
3. Compare the results from both tools

### Task 4: Traceroute
1. Trace the route to a remote server: `traceroute google.com`
2. Identify the number of hops
3. Note any timeouts or unusual patterns

### Task 5: Port Scanning (Optional - requires nmap)
If nmap is installed, scan your own machine:
```bash
nmap -sV localhost
nmap -p 1-1000 127.0.0.1
```

## Commands Reference
```bash
ip addr              # Show IP addresses
netstat -tuln        # Show listening ports
ping                 # Test connectivity
nslookup             # Query DNS
dig                  # DNS lookup tool
traceroute           # Trace network path
nmap                 # Network scanner (if installed)
```

## Deliverables
1. Document all commands used and their output
2. Create a network diagram of your local network
3. Answer the questions below

## Questions
1. What is the difference between TCP and UDP?
2. What port numbers are considered "well-known ports"?
3. What does TTL (Time To Live) mean in a ping response?
4. Why might a traceroute show asterisks (*) for some hops?
5. What is the purpose of port scanning in security assessments?

## Safety Reminder
Always obtain proper authorization before scanning any network. Use these skills ethically and legally.
