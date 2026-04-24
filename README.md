# Aquatic Facility Network Simulation (Cisco Packet Tracer)

## Overview

This project simulates a small-business IT network based on my aquatic facility where I work. The goal was to model how common workplace devices (front desk systems, staff laptops, printers, and wireless clients) connect within a network and to practice troubleshooting typical IT support issues.

The network was built in Cisco Packet Tracer and includes both wired and wireless infrastructure, along with a firewall that represents security boundaries between internal systems and the internet.

---

## Objectives

* Design a realistic small-scale business network
* Configure core networking components (firewall, switch, wireless access point)
* Simulate device connectivity across wired and wireless environments
* Practice troubleshooting common IT support issues

---

## Network Topology

The network follows this structure:

Cloud (Internet) → Firewall → Switch → Devices
                                  \
                                  Wireless Access Point → Wireless Devices

### Devices Included:

* 2 Desktop PCs (Front Desk / POS System)
* 3 Staff Laptops (Wireless)
* 1 Network Printer
* 1 Tablet (simulate a wireless display/TV system)
* Wireless Access Point (WRT300N)
* Switch (2960-24TT)
* Firewall (ASA 5505)
* Cloud-PT (Internet simulation)

---

## Network Configuration

### IP Addressing Scheme

| Device                   | IP Address      |
| ------------------------ | --------------- |
| Firewall (Gateway)       | 192.168.1.1     |
| Wireless Access Point    | 192.168.1.3     |
| Desktop PCs              | 192.168.1.10–11 |
| Laptops (DHCP or static) | 192.168.1.20–22 |
| Printer                  | 192.168.1.50    |
| Tablet (Display)         | 192.168.1.60    |

---

### Firewall Configuration

The ASA 5505 firewall is configured with:

* **Inside interface (VLAN 1)** → 192.168.1.1
* **Outside interface (VLAN 2)** → Simulated internet connection
* Default route to external network

This allows internal devices to communicate with external systems while maintaining a logical separation between trusted and untrusted networks.

---

### Wireless Configuration

* SSID: `HARD-Staff`
* Security: WPA2-PSK
* Wireless devices include laptops and a tablet

---

## Troubleshooting Scenarios

This project includes simulated IT support scenarios to reflect real-world issues:

### 1. No Internet Access

* Cause: Incorrect default gateway
* Fix: Configure the correct gateway IP

### 2. Printer Not Reachable

* Cause: Incorrect IP configuration or subnet mismatch
* Fix: Verify IP settings and network connectivity

### 3. Wireless Connection Failure

* Cause: Incorrect SSID or password
* Fix: Reconfigure wireless credentials

### 4. Device Communication Issues

* Cause: Network misconfiguration
* Fix: Verify addressing and connectivity

### 5. Front Desk System Offline

* Cause: Physical disconnection or incorrect configuration
* Fix: Reconnect device and validate network settings

