## Module 27 – Network Troubleshooting

### 🧱 Goal
- Diagnose and resolve network problems **systematically**.
- Use a repeatable process to avoid missing steps.

---

## 1. CompTIA Troubleshooting Methodology

1. **Identify the Problem**
   - Gather information (user reports, error messages, logs).
   - Establish what *changed* recently.
   - Duplicate the problem if possible.

2. **Establish a Theory of Probable Cause**
   - Start with the obvious.
   - Consider simplest explanation first (Occam's Razor).

3. **Test the Theory**
   - If confirmed → move to plan.
   - If not confirmed → form a new theory.

4. **Establish a Plan of Action**
   - Minimize impact.
   - Consider change control requirements.

5. **Implement the Solution**
   - Apply the fix in a controlled manner.

6. **Verify Full System Functionality**
   - Test to ensure problem is truly resolved.
   - Implement preventive measures if possible.

7. **Document Findings, Actions, and Outcomes**
   - Update tickets, network diagrams, knowledge base.

---

## 2. Common Network Troubleshooting Tools

- **Ping** – Basic connectivity test (ICMP Echo).
- **Traceroute / tracert** – Path and latency.
- **ipconfig / ifconfig** – IP configuration details.
- **nslookup / dig** – DNS resolution.
- **netstat** – Active connections and listening ports.
- **arp** – View/modify ARP table.
- **tcpdump / Wireshark** – Packet capture & analysis.
- **Nmap** – Port scanning & host discovery.
- **Cable tester / TDR** – Physical layer faults.
- **Loopback plug** – Test NIC without network.

---

## 3. Common Problem Scenarios

- **No connectivity**
  - Check cabling, link lights, NIC status.
- **Intermittent connectivity**
  - Check interference, loose connections, overloaded links.
- **Slow performance**
  - Check bandwidth usage, errors, high latency.
- **IP conflict**
  - Duplicate IPs → release/renew DHCP or reassign.
- **DNS issues**
  - Test with IP address to bypass DNS.
- **Incorrect VLAN assignment**
  - Causes devices to be isolated.

---

## 4. Layer-by-Layer Thinking (OSI Model)

- **Layer 1**: Check cables, connectors, power.
- **Layer 2**: Switch ports, MAC address tables, VLANs.
- **Layer 3**: IP configuration, routing tables.
- **Layer 4–7**: Firewall rules, application settings.

---

## Exam Pointers
✅ Always follow **CompTIA's 7-step process** in order.  
✅ Start troubleshooting at the **lowest OSI layer possible**.  
✅ Use `ping` and `traceroute` to separate local vs remote issues.  
✅ Document everything — they’ll test you on this step.
