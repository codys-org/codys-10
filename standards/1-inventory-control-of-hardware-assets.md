# Standard 1: Inventory & Control of Hardware Assets

> **Actively manage (inventory, track, and correct) all hardware devices on the network so that only authorized devices are given access, and unauthorized and unmanaged devices are found and prevented from gaining access.**

---

## Objective

Ensure that every hardware device connected to the organization’s network is known, authorized, and monitored. Prevent unauthorized devices from gaining access and maintain an accurate, up-to-date inventory.

---

## Why It Matters

Unknown or unmanaged hardware represents a significant blind spot in security. Attackers often exploit rogue devices (e.g., personal laptops, IoT devices, or malicious implants) to bypass perimeter controls and establish persistence.

---

## Key Requirements

| # | Requirement |
|---|-----------|
| 1.1 | Maintain a complete, accurate, and current inventory of all hardware assets. |
| 1.2 | Deploy automated asset discovery tools at least weekly. |
| 1.3 | Ensure only authorized devices can connect to the network (e.g., via 802.1X, NAC). |
| 1.4 | Detect and alert on unauthorized devices within 24 hours of connection. |
| 1.5 | Remove or isolate unauthorized devices immediately upon detection. |
| 1.6 | Assign ownership and classification (e.g., critical, sensitive) to each asset. |
| 1.7 | Review and validate the hardware inventory quarterly. |

---

## Implementation Guidance

### Tools & Technologies
- **Network Access Control (NAC)**: Cisco ISE, Aruba ClearPass, ForeScout
- **Asset Discovery**: Tanium, Axonius, Lansweeper, Qualys
- **Endpoint Management**: Microsoft Intune, Jamf, SCCM

### Best Practices
1. Use DHCP logging + DNS + active scanning for comprehensive discovery.
2. Tag devices by role (e.g., server, workstation, IoT, guest).
3. Integrate inventory with CMDB or ITAM systems.
4. Automate onboarding/offboarding workflows.

---

## Verification & Testing

| Test | Method |
|------|--------|
| Verify inventory accuracy | Compare automated scan vs. manual audit |
| Detect rogue device | Connect unauthorized laptop; confirm alert/isolation |
| Review access logs | Confirm only authorized MACs/IPs are active |

---

## Maturity Levels

| Level | Description |
|-------|-------------|
| **1** | Manual spreadsheet tracking |
| **2** | Automated weekly scans |
| **3** | Real-time detection + NAC enforcement |
| **4** | Full integration with CMDB + automated remediation |
| **5** | Predictive analytics + zero-trust hardware access |

---

## References

- [CIS Control 1](https://www.cisecurity.org/controls/inventory-and-control-of-hardware-assets)
- NIST SP 800-53: CM-8
- ISO/IEC 27001: A.8.1.1

---

*Part of the [Defensible 10 Standards](https://www.defensible10.org)*