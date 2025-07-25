# QUESTION 1
You are configuring a remote out-of-band management network that connects to router and switch serial ports in a private cloud. What product would you need to install to accomplish this task?

✅ Terminal server  
❌ Federations  
❌ Subnet mask  
❌ I don't know  

Why the others are wrong:
- ❌ **Federations** – This refers to identity trust between organizations, not physical network access tools.
- ❌ **Subnet mask** – That’s for IP network segmentation. Doesn’t connect to serial ports or provide management access.
- ❌ **I don't know** – You will soon. It's a **terminal server**—used in out-of-band access to console ports for remote device management.
---
# QUESTION 2
What Windows Server application presents the server’s graphical desktop on a remote user’s screen?

✅ Remote Desktop Services  
❌ SSH  
❌ Subnet mask  
❌ I don't know  

Why the others are wrong:
- ❌ **SSH** – Secure Shell gives terminal (CLI) access, not a graphical desktop on Windows.
- ❌ **Subnet mask** – It's used for network addressing and segmentation. Doesn't provide user access to desktops.
- ❌ **I don't know** – The correct feature is **Remote Desktop Services**, which streams the GUI to remote users.
---
# QUESTION 3
After deploying a new public website, your validation steps ask you to check the domain name to IP address mappings. What Linux and Windows commands can be used for validation?

✅ dig and nslookup  
❌ Ping  
❌ Remote Desktop Services  
❌ I don't know  

Why the others are wrong:
- ❌ **Ping** – Can show if a host is reachable and may resolve a name to IP, but doesn’t query DNS records in depth.
- ❌ **Remote Desktop Services** – Irrelevant to DNS; used for graphical remote access to Windows systems.
- ❌ **I don't know** – You do now. `dig` (Linux) and `nslookup` (Windows & Linux) are DNS query tools that directly resolve names to IPs and inspect DNS records.
---
# QUESTION 4
What intrusion system will monitor but not act on an Internet-based attack?

✅ IDS  
❌ tcpdump  
❌ Remote Desktop Services  
❌ I don't know  

Why the others are wrong:
- ❌ **tcpdump** – It’s a packet capture tool, not an intrusion system. It records traffic but doesn’t alert on threats.
- ❌ **Remote Desktop Services** – Has nothing to do with network security monitoring.
- ❌ **I don't know** – The correct answer is **IDS** (Intrusion Detection System), which **monitors and alerts**, but doesn’t take action like IPS does.
---
# QUESTION 5
Combining several companies’ user directories together for a unified cloud authentication service is called what?

✅ Federations  
❌ SSH  
❌ Authorization  
❌ I don't know  

Why the others are wrong:
- ❌ **SSH** – Secure Shell is a remote login protocol, not an identity integration method.
- ❌ **Authorization** – That’s the process of granting access *after* authentication. Doesn’t unify identities across orgs.
- ❌ **I don't know** – The term you're looking for is **Federations**, which allow identity trust and single sign-on (SSO) across multiple orgs or domains.
---
# QUESTION 6
Sarah made an SSH connection to a remote bastion host. She needs to add an access control list rule to allow the bastion server to access a new subnet. She needs the source IP address of her host. What command can she run on the server to collect this information?

✅ ifconfig  
❌ Authorization  
❌ tcpdump  
❌ I don't know  

Why the others are wrong:
- ❌ **Authorization** – Refers to granting permissions, not retrieving IP configuration.
- ❌ **tcpdump** – Captures live traffic. Overkill here and doesn't directly display IP settings.
- ❌ **I don't know** – The correct tool is **ifconfig**, which displays IP address info for all interfaces. (On modern systems, `ip a` is more common.)
---
# QUESTION 7
To verify network reachability from a NoSQL database server residing in a private subnet on a public cloud to the application tier, what utility can you use as a quick connectivity test?

✅ Ping  
❌ ifconfig  
❌ Federations  
❌ I don't know  

Why the others are wrong:
- ❌ **ifconfig** – Only shows IP address/interface info; doesn’t test connectivity.
- ❌ **Federations** – Involves identity management and trust—not networking.
- ❌ **I don't know** – The right tool here is **Ping**—classic ICMP test to check if a target is reachable across the network.
---
# QUESTION 8
After a user authenticates to a system, what is it called when the user is given certain rights to access services?

✅ Authorization  
❌ Remote Desktop Services  
❌ ifconfig  
❌ I don't know  

Why the others are wrong:
- ❌ **Remote Desktop Services** – This is a Windows GUI access method, not a security concept.
- ❌ **ifconfig** – A network interface command, not related to user permissions.
- ❌ **I don't know** – Now you do. Once you’ve proven who you are (**authentication**), the system decides *what you can do*—that’s **authorization**.
---
# QUESTION 9
A Cloud+ student you are mentoring asks about the mappings between layer 2 MAC addresses and IP addresses. They want to verify that the VM has the correct network mapping information. Which utility would you tell them to use to gather this information?

✅ ARP  
❌ Terminal server  
❌ Remote Desktop Services  
❌ I don't know  

Why the others are wrong:
- ❌ **Terminal server** – Used for remote serial port access, not for checking network mappings.
- ❌ **Remote Desktop Services** – Grants GUI access to remote systems but doesn’t show MAC/IP tables.
- ❌ **I don't know** – The answer is **ARP (Address Resolution Protocol)**—used to view or manage the local mapping of IP addresses to MAC addresses in the ARP table.
---
# QUESTION 10
A remote user is unable to reach a Linux-based web server hosted in the Singapore zone of the cloud provider. The user is located in Austin, Texas. What command can they use to verify the connection path?

✅ traceroute  
❌ Federations  
❌ Terminal server  
❌ I don't know  

Why the others are wrong:
- ❌ **Federations** – Involves cross-domain identity—not network routing or troubleshooting.
- ❌ **Terminal server** – Used for out-of-band management, not connection path analysis.
- ❌ **I don't know** – The right answer is **traceroute**. It maps each network hop from source to destination and helps diagnose where a failure occurs.
---
# QUESTION 11
Scott is troubleshooting a SQL access issue and wants to look at the TCP packets being sent and received from his network adapter card on the Linux database server. What command would he use to collect the traces?

✅ tcpdump  
❌ ARP  
❌ IDS  
❌ I don't know  

Why the others are wrong:
- ❌ **ARP** – Maps IP to MAC addresses, but doesn’t capture or analyze live traffic.
- ❌ **IDS** – Monitors for threats but doesn’t perform manual packet capture or CLI inspection.
- ❌ **I don't know** – The go-to tool is **tcpdump**. It captures live network packets and shows headers, ports, and flags—perfect for tracking SQL issues.
---
# QUESTION 12
What determines whether servers are in the same IP subnet?

✅ Subnet mask  
❌ Ping  
❌ SSH  
❌ I don't know  

Why the others are wrong:
- ❌ **Ping** – Tests reachability but doesn’t tell you about subnet boundaries.
- ❌ **SSH** – It's for secure remote shell access, not related to network segmentation.
- ❌ **I don't know** – The **subnet mask** defines the network and host portions of an IP address. If two IPs share the same network ID portion, they're in the same subnet.
---
# QUESTION 13
Which text-based remote access application is used to access Linux servers securely in a public cloud?

✅ SSH  
❌ ifconfig  
❌ Subnet mask  
❌ I don't know  

Why the others are wrong:
- ❌ **ifconfig** – Used for checking network configuration, not remote access.
- ❌ **Subnet mask** – Defines IP ranges; unrelated to accessing systems.
- ❌ **I don't know** – It’s **SSH (Secure Shell)**. It encrypts remote terminal sessions and is the gold standard for accessing Linux servers in cloud environments.
---
#cloud-plus #flashcard 