# 🛡️ Cybersecurity Home Lab with pfSense, Kali Linux, and Ubuntu

## **Overview**

This project demonstrates a realistic **cybersecurity home lab** built with VirtualBox to simulate, analyze, and defend against network attacks. The lab includes a pfSense firewall acting as the security gateway, a Kali Linux attacker machine, and an Ubuntu victim machine, all connected in a segmented network.

The lab models a real-world scenario of perimeter security, simulating a Denial-of-Service (DoS) attack, analyzing it with Wireshark, and mitigating it using firewall rules. This is a highly valuable hands-on environment for anyone interested in network security, blue team operations, or ethical hacking.

---

## **Key Features & Uses**

✅ Simulate a secure network perimeter with pfSense
✅ Learn network segmentation and routing concepts
✅ Practice launching and defending against DoS attacks
✅ Observe live packet captures with Wireshark
✅ Build, test, and validate firewall rules
✅ Safely test security tools without harming a production network
✅ Develop skills relevant to SOC analysts, blue-teamers, or cybersecurity students

---

## **Benefits**

* **Hands-on skills**: Configure, monitor, and defend a network from real attack tools
* **Safe environment**: Contains attacks within an isolated lab
* **Portfolio project**: Shows practical skills to potential employers
* **Repeatable**: Easily reset and rerun scenarios as needed
* **Low cost**: Runs on free software (VirtualBox, pfSense, Kali, Ubuntu)
* **Realistic practice**: Mirrors real SOC and blue-team processes

---

## **Architecture Diagram**

```
[Home LAN (192.168.0.0/24)]
         |
     [pfSense WAN (bridged)]
         |
 [pfSense LAN (LabNet 192.168.1.0/24)]
    |                               |
[Ubuntu Victim]             [Kali Attacker]
```

---

## **Requirements**

✅ **Host System**

* At least 8GB RAM
* 40GB free disk
* Windows/macOS/Linux with administrative privileges
* VirtualBox 7.x or higher

✅ **ISOs to Download**

* pfSense Community Edition (CE) 2.7.x
* Kali Linux (latest)
* Ubuntu 22.04 Desktop

✅ **Network Setup**

* Bridged network for pfSense WAN and Kali
* Internal network (`LabNet`) for pfSense LAN and Ubuntu

✅ **Software**

* Wireshark (on Ubuntu victim)

---

## **How it Works (High Level)**

1. **pfSense** acts as the firewall between the attacker (Kali) and the victim (Ubuntu).
2. **Kali** launches DoS traffic towards the victim.
3. **Ubuntu** uses Wireshark to analyze the attack.
4. **pfSense** is configured with rules to block the attacker’s traffic and logs the blocking events.

This process demonstrates the complete incident response workflow — from detection to mitigation.

---

## **How to Get Started**

👉 See the `setup` for step-by-step detailed instructions.

---

## **License**

This project is open for personal education use under the MIT License.

---
