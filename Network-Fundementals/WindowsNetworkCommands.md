# Network Troubleshooting Commands – Windows  
*(CMD & PowerShell)*

## Purpose
This document outlines a small set of essential Windows network troubleshooting commands commonly used in IT support. These commands are typically the first tools used when diagnosing connectivity, DNS, or service-related issues, and focus on quickly identifying where a problem is occurring before deeper investigation or escalation.

---

## Essential Commands

| Command | What it does | Why you’d use it |
|-------|--------------|------------------|
| `ipconfig` | Shows the device’s IP address | To identify a device’s IP address and confirm whether it has received one from the network |
| `ipconfig /all` | Shows detailed network information including DNS, gateway, and DHCP status | To identify misconfigurations in the device’s network settings |
| `ipconfig /release` | Releases the current DHCP-assigned IP address | To force the device to drop its current IP configuration |
| `ipconfig /renew` | Requests a new IP address from DHCP | To resolve issues where a device has an invalid or missing IP address |
| `ipconfig /flushdns` | Clears the local DNS cache | To resolve issues caused by outdated or incorrect DNS records |
| `ping 8.8.8.8` | Tests connectivity to an external IP address | To confirm basic internet connectivity without relying on DNS |
| `ping google.com` | Tests connectivity using DNS | To determine whether an issue is DNS-related |
| `nslookup google.com` | Queries DNS for a hostname | To verify DNS is resolving correctly |
| `Test-NetConnection -Port 443` | Tests connectivity to a specific port | To check whether a service or firewall is blocking access |
| `netstat -ano` | Shows active connections and listening ports | To confirm whether a service is running and listening on the expected port |

---

## Common Command Flags

| Flag | What it does |
|----|--------------|
| `-a` | Shows all connections or interfaces |
| `-n` | Displays addresses and ports numerically |
| `-v` | Shows verbose or detailed output |
| `-c` | Limits the number of requests sent |
| `-p` | Filters by protocol or specifies a port |
| `-r` | Displays the routing table |
| `-o` | Shows the process ID (PID) |
| `-s` | Shows protocol statistics |
| `-I` | Requests headers only (HTTP tools) |
| `-h` / `--help` | Displays help information |

---

## Notes
These commands are typically used together to:
- Confirm IP configuration
- Test basic connectivity
- Verify DNS resolution
- Identify routing or firewall-related issues
- Confirm whether required services are running
