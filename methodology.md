# Lab Methodology

## Purpose

To practise capturing and inspecting network traffic generated in a controlled virtual machine environment.

## Procedure

1. Inspect available interfaces using `ip addr`.
2. Start Wireshark and select `eth0`.
3. Begin packet capture.
4. Generate ICMP traffic using `ping -c 4 1.1.1.1`.
5. Generate DNS traffic using `nslookup example.com`.
6. Generate HTTPS request traffic using `curl -I https://example.com`.
7. Stop the capture and inspect the packet list.
8. Apply the `dns`, `icmp`, and `tcp` display filters.
9. Save screenshots documenting the traffic categories.
10. Review evidence before documenting conclusions.

## Evidence Handling

Screenshots are retained in the project's `screenshots/` directory.

Raw packet captures are excluded from the public repository by default because they may contain internal addresses, domain lookups, and other potentially sensitive metadata.

## Validation

DNS, ICMP, and TCP traffic were confirmed during the lab's evidence verification.

Detailed packet-level findings should be added only after inspecting the relevant packets and recording their actual fields.

## Safety

The exercise focuses on traffic generated from the user's own virtual machine and ordinary diagnostic requests.

Any future packet capture or investigation should be limited to systems and networks for which the user has authorization.
