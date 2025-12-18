# Network Troubleshooting Commands – macOS & Linux  
*(Terminal)*

## Purpose
This document outlines a small set of essential network troubleshooting commands used on macOS and Linux systems. These commands are commonly used during IT support to diagnose connectivity, DNS, routing, and service-related issues.

---

## Essential Commands

| Command | What it does | Why you’d use it |
|-------|--------------|------------------|
| `ifconfig` | Displays network interfaces and IP addresses | To confirm the device has an IP address (macOS) |
| `ip a` | Displays network interfaces and IP addresses | To confirm the device has an IP address (Linux) |
| `ip route` | Shows the routing table | To confirm the default gateway is set correctly |
| `ping 8.8.8.8` | Tests connectivity to an external IP address | To confirm basic network connectivity without DNS |
| `ping google.com` | Tests connectivity using DNS | To determine whether an issue is DNS-related |
| `traceroute google.com` | Displays the network path to a destination | To identify where traffic is being blocked or delayed |
| `dig google.com` | Queries DNS records for a hostname | To verify DNS resolution and record accuracy |
| `nslookup google.com` | Performs a basic DNS lookup | To quickly confirm DNS resolution |
| `nc -vz host 443` | Tests connectivity to a specific port | To check whether a service or firewall is blocking access |
| `netstat -an` | Shows active connections and listening ports | To confirm whether a service is listening |
| `ss -tulpn` | Shows listening ports and associated processes | To identify which service owns a port (Linux) |
| `curl -I https://example.com` | Retrieves HTTP response headers | To confirm a web service is reachable |

---

## Common Command Flags

| Flag | What it does |
|----|--------------|
| `-a` | Shows all interfaces or connections |
| `-n` | Displays addresses numerically |
| `-v` | Shows verbose output |
| `-c` | Limits the number of requests sent |
| `-p` | Filters by protocol or specifies a port |
| `-I` | Requests headers only (HTTP tools) |
| `-h` / `--help` | Displays help information |

---

## Notes
These commands are typically used to confirm IP configuration, test connectivity, verify DNS resolution, and confirm whether services are reachable on macOS and Linux systems.
