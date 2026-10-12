# Network Traffic Analysis Lab

## Project Overview

This project demonstrates practical network traffic capture and analysis using Wireshark in a Kali Linux virtual machine.

The lab involved capturing network packets, generating test traffic, applying display filters, and examining DNS, ICMP, and TCP traffic.

The objective was to develop foundational skills in packet inspection, protocol identification, and security-focused documentation.

## Objectives

- Capture traffic on an active network interface.
- Identify DNS, ICMP, and TCP traffic.
- Apply Wireshark display filters.
- Examine packet fields and communication patterns.
- Document observations, limitations, and security relevance.

## Lab Environment

- Operating system: Kali Linux
- Virtualization: VMware Workstation
- Packet analysis tool: Wireshark 4.6.6
- Capture interface: eth0

## Tools and Commands

| Tool or command | Purpose |
|---|---|
| `ip addr` | Inspect network interfaces and IP addresses |
| `ping -c 4 1.1.1.1` | Generate ICMP traffic for connectivity testing |
| `nslookup example.com` | Generate a DNS lookup |
| `curl -I https://example.com` | Generate HTTPS request traffic |
| Wireshark | Capture, filter, and inspect packets |

## Display Filters

| Filter | Purpose |
|---|---|
| `dns` | Display DNS packets |
| `icmp` | Display ICMP packets |
| `tcp` | Display TCP packets |
| `tcp.port == 443` | Display TCP packets using port 443 |

## Evidence

The `screenshots/` directory contains evidence collected during the lab.

- `01-initial-capture.png` — initial packet capture.
- `02-dns-analysis.png` — DNS traffic inspection.
- `03-icmp-analysis.png` — ICMP traffic inspection.
- `04-tcp-analysis.png` — TCP traffic inspection.

DNS, ICMP, and TCP traffic were confirmed during evidence verification.

Exact packet counts, individual DNS results, TCP flag sequences, and connection outcomes have not yet been recorded in the documentation.

## Security Relevance

Network traffic analysis helps security analysts understand communication between hosts, investigate connectivity issues, and examine unusual network behaviour.

DNS inspection can reveal domain lookup activity. ICMP inspection can help assess network reachability. TCP inspection can reveal connection behaviour, including handshakes and termination.

HTTPS encrypts application content, although some connection metadata may remain visible in packet captures.

## Limitations

This was a beginner lab using traffic generated from my own virtual machine.

The observations are limited to the packets captured during the exercise. They do not establish that the network is secure, identify a confirmed security incident, or constitute a comprehensive network assessment.

## Future Improvements

- Record packet counts and representative packet fields.
- Examine TCP handshakes and connection termination.
- Inspect DNS queries and corresponding responses.
- Investigate TLS handshake metadata.
- Practise analysing suspicious traffic in an authorized lab.
- Compare observations against a known-good baseline.

## Author

Oluwaseun Adebayo

Cybersecurity Learning Portfolio — Day 2
