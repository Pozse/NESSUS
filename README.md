# Nessus Vulnerability Management + Windows 10 Pro

## Introduction
Nessus Vulnerability Scanner, developed by Tenable Inc., is a widely used tool for identifying and managing vulnerabilities in computer systems and networks. It scans systems for security issues, misconfigurations, and compliance violations across various platforms, including operating systems, network devices, databases, and applications. Nessus uses an extensive library of regularly updated plugins to detect new vulnerabilities, performs both remote and agent-based scans, and offers detailed reports with actionable insights for remediation. Key features include vulnerability detection, compliance audits, malware detection, policy enforcement, and user-friendly interfaces. While it provides comprehensive coverage and regular updates, Nessus can produce false positives and may be resource-intensive for large networks. Despite requiring some expertise for effective use, Nessus is essential for cybersecurity professionals to identify and address security weaknesses before they are exploited.

## Table of Contents
- [Introduction](#introduction)
- [Installation](#installation)
- [Usage](#usage)
- [Features](#features)
- [Dependencies](#dependencies)
- [Configuration](#configuration)
- [Documentation](#documentation)
- [Examples](#examples)
- [Troubleshooting](#troubleshooting)
- [Contributors](#contributors)
- [License](#license)

## Installation

### Required Software
1. [Tenable Nessus](https://www.tenable.com/products/nessus)
   - Registration and key are required but free.
2. [Oracle VirtualBox](https://www.virtualbox.org/)
3. Windows 10 ISO
   - Download the image creation tool, run it, and use the settings to create a Windows 10 Pro ISO.

### Setting up Virtual Machine
1. Open VirtualBox and click on ‘New’.
2. Name your machine and select the Windows 10 image you created as the ISO image.
3. On the ‘Unattended Guest OS Install’ page, create a username and password. No product key is required.
4. Modify the settings if necessary (e.g., 8GB RAM, 50GB storage).
5. Click ‘Next’ and then ‘Finish’.
6. Right-click on your new VM and click ‘Settings’.
7. Go to Network and switch “Attached to: NAT” to “Bridged Adapter”.
8. Start up your new VM and install Windows 10 Pro. If asked for a product key, select “I do not have a product key”.
9. When the option comes up, select “For personal use” and then select “Offline account”.
10. Create your username and password.
11. After starting up, open the RUN (Win + R) and type `firewall.cpl`.
12. Turn off both Private and Public firewall settings. (This is for the purpose of this exercise; not recommended in real scenarios).

### Installing Nessus Essentials
1. Follow the link and register an account. You will receive a ‘key’ and an installer.
2. Install Nessus and note the local URL provided to access the app.
3. Ensure you select Nessus Essentials during installation.

## Usage

### Scanning your VM
1. Open Nessus and click ‘New Scan’ in the top right corner, then select ‘Basic Network Scan’.
2. In your VM, open Command Prompt and type `ipconfig`. Enter your IPv4 address into Nessus under ‘Targets’.
3. Select ‘Discovery’ on the left pane and change it to custom.
4. Select ‘Host Discovery’ and turn off ‘ping the remote host’.
5. Click ‘Save’.
6. Under your Scans, select the play button on the right to launch.
7. The initial scan takes about a minute, showing real-time results. Click through to read about each vulnerability and its remediation.

### Detailed Scan
1. Return to the main screen, click the box next to your scan, select "More" in the top right, then click "Configure."
2. Click the "Credentials" tab beside "Settings" to perform a credentialed scan.
3. On the left pane, select ‘Windows’ and ‘password’ as the authentication method. Enter your username and password.
4. Click ‘Save’ and re-run your scan.

## Features
- Vulnerability detection
- Compliance audits
- Malware detection
- Policy enforcement
- User-friendly interfaces

## Dependencies
- Nessus Vulnerability Scanner
- Oracle VirtualBox
- Windows 10 Pro ISO

## Configuration
- Bridged network adapter setup for the virtual machine
- Firewall disabled on the virtual machine for scanning purposes

## Documentation
- [Nessus Documentation](https://docs.tenable.com/nessus)

## Examples
- Basic and detailed vulnerability scans as described in the Usage section

## Troubleshooting
- Ensure the VM is properly set up and network settings are correctly configured.
- Make sure firewall settings are adjusted for the scan.

## Contributors
- Pozse
