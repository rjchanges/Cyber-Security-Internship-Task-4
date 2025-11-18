# Task 4: Firewall Configuration

## Project Overview
This project demonstrates how to configure network traffic rules using Windows Defender Firewall. The objective was to create a specific inbound rule to block traffic on a designated port to enhance system security.

## Tools Used
* **Firewall:** Windows Defender Firewall with Advanced Security
* **Testing Tool:** Windows PowerShell
* **Protocol Blocked:** Telnet (Port 23)

## Configuration Steps
1.  Opened **Windows Defender Firewall with Advanced Security**.
2.  Created a new **Inbound Rule**.
3.  Selected **Port** as the rule type and specified **TCP** port **23**.
4.  Set the action to **Block the connection**.
5.  Applied the rule to Domain, Private, and Public profiles.

## Verification
To verify the rule was active, I used the PowerShell command:
`Test-NetConnection -ComputerName localhost -Port 23`

**Result:**
The test returned `TcpTestSucceeded : False`, confirming that the port is successfully blocked/closed and not accepting connections.

## Conclusion
Blocking unused or insecure ports like Telnet (23) is a fundamental security practice to reduce the attack surface of a system.
