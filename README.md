# Week 1 — Cybersecurity Lab Setup

## Overview

This repository documents the setup of a basic cybersecurity lab using Windows, VMware Workstation, and Kali Linux. The goal of Week 1 was to prepare the virtual machine, confirm network connectivity, install/check essential tools, and configure a shared folder for lab files.

## Lab Environment

- **Host operating system:** Windows
- **Virtualization software:** VMware Workstation 26.0.0
- **Virtual machine:** Kali Linux
- **Network mode:** NAT
- **Kali network interface:** `eth0`
- **Kali IP address:** `10.0.0.2/24`
- **Default gateway:** `10.0.0.1`

## Tools

The following tools were checked in Kali Linux:

- **Nmap** — network discovery and security auditing
- **Git** — version control
- **Python 3** — scripting and automation

Version information can be seen in the `05-installed-tools.png` screenshot.

## Network Configuration

Kali Linux uses VMware NAT networking. The configured Kali address is `10.0.0.2/24`, with the default gateway `10.0.0.1`.

Internet and DNS connectivity were checked with:

```bash
ping -c 4 google.com
```

See `02-ip-address.png`, `03-default-gateway.png`, and `04-internet-dns.png` for evidence.

## Shared Folder

A VMware shared folder named `LabShare` is used to exchange files between Windows and Kali Linux.

- **Windows folder:** `E:\Documents\Virtual Machines\LabShare`
- **Kali mount point:** `/mnt/hgfs/LabShare`

The folder was checked from Kali Linux with:

```bash
ls -l /mnt/hgfs/LabShare
```

See `06-shared-folder.png` for evidence.

## VMware Snapshot

An existing VMware snapshot was checked so the virtual machine can be returned to a known state if needed. The snapshot name is not specified here; refer to `07-snapshot.png` for the snapshot shown in VMware Workstation.

## Evidence and Screenshots

Place the screenshots in the `Week1-Screenshots/` folder:

| File | Evidence |
|---|---|
| `01-kali-vm.png` | Kali Linux running in VMware Workstation |
| `02-ip-address.png` | Kali IP address (`ip addr show eth0`) |
| `03-default-gateway.png` | Default route (`ip route`) |
| `04-internet-dns.png` | Internet/DNS connectivity test |
| `05-installed-tools.png` | Nmap, Git, and Python versions |
| `06-shared-folder.png` | Shared folder contents in Kali |
| `07-snapshot.png` | Existing VMware snapshot |
| `08-vmware-network.png` | VMware virtual network settings |
| `09-week1-documentation.png` | Optional screenshot of the completed documentation folder |

## Conclusion

The Week 1 lab environment was set up with Kali Linux running in VMware Workstation. Network connectivity, core tools, and the Windows–Kali shared folder were checked. Screenshots are included as evidence of the setup.

## Safety and Scope

Use this lab only on systems and networks you own or have explicit permission to test. Do not include passwords, private keys, tokens, personal documents, or other sensitive information in this repository.
