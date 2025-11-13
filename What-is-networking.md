# TryHackMe Write-up: What is Networking?

This lab is part of the "Pre-Security" learning path and covers the foundational concepts of networking, including the OSI model, TCP/IP, and MAC vs. IP addressing.

## 1. Key Concepts Learned

* **OSI Model:** A 7-layer conceptual model for how network communication works. I learned to identify which layer a protocol or device belongs to (e.g., Layer 3 = IP Addresses, Layer 2 = MAC Addresses).
* **TCP/IP:** The practical 4-layer model that the internet actually uses.
* **Encapsulation:** The process of "wrapping" data in headers and trailers as it moves down the OSI model.
* **Ping (ICMP):** I used the `ping` command to test connectivity, demonstrating a Layer 3 (Network) protocol in action.
* **TCP vs. UDP:** I learned the difference between a "connection-oriented" (TCP, reliable, phone call) and "connectionless" (UDP, fast, postcard) protocol.

## 2. Lab Verification

I successfully connected my Kali VM to the TryHackMe VPN and verified connectivity to the lab machine.

* **Command:** `ping -c 4 [REDACTED_IP]`
* **Result:** 0% packet loss, confirming my network route and VPN were correctly configured.

## 3. How This Applies to a SOC Analyst Job

Understanding the OSI model is not just theory. It's how an analyst identifies an attack.

* A **port scan** (like Nmap) is a **Layer 4 (Transport)** activity.
* A **DDoS attack** might be a **Layer 3 (Network)** or **Layer 7 (Application)** attack.
* Knowing this helps me quickly filter logs in a SIEM (like Splunk or Wazuh) to find the source of a problem.
