# Cybersecurity Lab Setup

A simple, isolated cybersecurity practice environment using **Kali Linux** in **Oracle VirtualBox**. This repository records the initial lab setup and provides a starting point for security learning, defensive testing, and controlled experiments.

![Kali Linux running in VirtualBox](20261109_192730.jpg)

## Overview

The lab is designed to provide a safe environment for learning and practicing:

- Linux and command-line fundamentals
- Network discovery and traffic analysis
- Vulnerability assessment
- Web application security testing
- Digital forensics and incident-response exercises

Use the lab only on systems and networks that you own or have explicit permission to test.

## Requirements

- A computer capable of running virtualization
- [Oracle VirtualBox](https://www.virtualbox.org/)
- A Kali Linux installer image or prebuilt VirtualBox image from the [official Kali website](https://www.kali.org/get-kali/)
- At least 4 GB of RAM available for the virtual machine
- Sufficient disk space for the VM, tools, snapshots, and lab data

## Setup

1. Install Oracle VirtualBox.
2. Download Kali Linux from the official Kali Linux website.
3. Create or import a Kali Linux virtual machine in VirtualBox.
4. Allocate resources appropriate for your host system.
5. Install Kali Linux or complete the first-run setup for the imported image.
6. Update the system and installed packages:

   ```bash
   sudo apt update && sudo apt full-upgrade -y
   ```

7. Create a VirtualBox snapshot after the base installation is working. Snapshots make it easier to restore a clean lab state.

## Recommended network configuration

Use **NAT** for initial updates and general internet access. For exercises involving multiple intentionally vulnerable machines, use a dedicated **host-only** or **internal network** so that lab traffic remains isolated from your normal network.

Do not expose intentionally vulnerable services directly to the public internet.

## Verify the installation

Run the following commands inside Kali to confirm that the system and network are available:

```bash
cat /etc/os-release
uname -r
ip addr
```

You should see Kali Linux system information, a kernel version, and the VM's network interfaces.

## Suggested next steps

- Take a clean snapshot before installing additional tools.
- Build a separate target VM or use legal training platforms such as [OWASP Juice Shop](https://owasp.org/www-project-juice-shop/) and [Metasploitable](https://docs.rapid7.com/metasploit/metasploitable-2/).
- Keep notes about commands, findings, and remediation steps.
- Reset or revert targets after each exercise.
- Keep Kali and VirtualBox up to date.

## Safety and ethics

This lab is for authorized testing and education. Never scan, exploit, or access systems without permission. Keep vulnerable machines isolated, avoid using real credentials or sensitive data, and follow the laws and policies that apply to you.

## Repository contents

| File | Description |
| --- | --- |
| `README.md` | Lab overview and setup guidance |
| `20261109_192730.jpg` | Screenshot of Kali Linux running in VirtualBox |

## License

No license has been specified for this repository. Add a license before redistributing the content or using it as a shared project.
