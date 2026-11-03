# W8IP-To Router 🚀

<div align="center">

![Version](https://img.shields.io/badge/version-2.0-blue.svg)
![Python](https://img.shields.io/badge/python-3.6+-green.svg)
![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20Linux%20%7C%20Termux-lightgrey.svg)
![License](https://img.shields.io/badge/license-MIT-orange.svg)

**Advanced IP Scanner & Router Detection Tool**

*Ultra-fast multi-threaded network scanner with comprehensive device information*

[Features](#features) • [Installation](#installation) • [Usage](#usage) • [Screenshots](#screenshots) • [Credits](#credits)

</div>

---

## 📋 Table of Contents

- [Description](#description)
- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
  - [Windows Installation](#windows-installation)
  - [Linux Installation](#linux-installation)
  - [Termux Installation (Android)](#termux-installation-android)
- [Usage](#usage)
- [Examples](#examples)
- [Output Information](#output-information)
- [Screenshots](#screenshots)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [Credits](#credits)
- [License](#license)

---

## 📖 Description

**W8IP-To Router** is a professional-grade, ultra-fast IP scanner designed to discover and identify devices on your network. Built with multi-threading technology, it can scan entire subnets in seconds while providing comprehensive information about each discovered device.

### What Makes It Special?

- 🚀 **Ultra-Fast Scanning**: Up to 200 concurrent threads for lightning-fast results
- 🎯 **Smart Detection**: Automatically identifies routers, servers, and device types
- 🌐 **Complete Network Info**: Shows WLAN IP, Gateway, and Public IP
- 📊 **Rich Device Details**: MAC address, manufacturer, NetBIOS, OS detection
- 💾 **Auto-Save Results**: Saves detailed reports to timestamped TXT files
- 🎨 **Beautiful UI**: Color-coded terminal output with animations
- 📱 **Cross-Platform**: Works on Windows, Linux, Mac, and Termux (Android)

---

## ✨ Features

### Network Information Display
- ✅ **WLAN (WiFi) IP Address** - Your wireless connection IP
- ✅ **Ethernet IP Address** - Your wired connection IP
- ✅ **Default Gateway/Router IP** - Your router's IP address
- ✅ **Public IP Address** - Your internet-facing IP
- ✅ **Date & Time** - 12-hour format with full date

### Device Scanning & Detection
- ✅ **Ultra-Fast Multi-threaded Scanning** - Scan 254 IPs in ~15-20 seconds
- ✅ **Live Progress Animation** - Real-time scanning progress with spinner
- ✅ **Port Scanning** - Detects open ports 80 and 8080 (HTTP services)
- ✅ **Response Time Measurement** - Shows connection speed in milliseconds

### Device Information Collected
- ✅ **IP Address** - Device network address
- ✅ **Hostname/Device Name** - DNS name resolution
- ✅ **NetBIOS Name** - Windows computer name
- ✅ **MAC Address** - Physical hardware address
- ✅ **Manufacturer** - Device manufacturer from MAC OUI database (100+ vendors)
- ✅ **Device Type** - Auto-detection (Router, Server, VM, NAS, Computer)
- ✅ **User/Computer Name** - Extracted from NetBIOS or hostname
- ✅ **TTL & OS Detection** - Network hops and operating system guess
- ✅ **Open Ports & Services** - Port details with service identification
- ✅ **Access URLs** - Direct clickable web access links

### Special Features
- ✅ **WiFi Router Detection** - Automatically identifies and highlights routers
- ✅ **Auto-Save to TXT** - Detailed reports with timestamps
- ✅ **Color-Coded Output** - Easy-to-read terminal display
- ✅ **Termux Support** - Full Android compatibility
- ✅ **Error Handling** - Graceful handling of timeouts and errors

---

## 📦 Requirements

### Minimum Requirements
- **Python**: 3.6 or higher
- **Operating System**: Windows 7+, Linux, macOS, Termux (Android 7+)
- **Network**: Active network connection
- **Permissions**: Standard user permissions (root/admin not required)

### Python Packages
- All required packages are built-in (no pip install needed!)
  - `socket` - Network communication
  - `threading` - Multi-threaded scanning
  - `subprocess` - System command execution
  - `ipaddress` - IP address manipulation

---

## 🔧 Installation

### Automatic Installation (Recommended)

#### Quick Install (One Command)
```bash
chmod +x install.sh && ./install.sh
```

---

### Windows Installation

#### Method 1: Using Git
```cmd
# Clone repository
git clone https://github.com/w8bdcr-official/W8BDCR-IP-To-Router-Scanner
cd W8BDCR-IP-To-Router-Scanner

# Run the tool
python W8IP-To-Router-Scanner.py
```

#### Method 2: Manual Download
1. Download ZIP from GitHub
2. Extract to your desired location
3. Open Command Prompt in the folder
4. Run: `python W8IP-To-Router-Scanner.py`

#### Python Installation (if not installed)
1. Download Python from [python.org](https://www.python.org/downloads/)
2. Run installer and check "Add Python to PATH"
3. Verify: `python --version`

---

### Linux Installation

#### Method 1: Using Git
```bash
# Clone repository
git clone https://github.com/w8bdcr-official/W8BDCR-IP-To-Router-Scanner
cd W8BDCR-IP-To-Router-Scanner

# Make files executable
chmod +x install.sh W8IP-To-Router-Scanner.py

# Run auto-installer
./install.sh
```

#### Method 2: Manual Setup
```bash
# Install Python (if needed)
sudo apt-get update
sudo apt-get install python3 python3-pip

# Install network tools
sudo apt-get install net-tools iproute2

# Run the tool
python3 W8IP-To-Router-Scanner.py
```

---

### Termux Installation (Android)

#### 🚀 Quick Install (Copy & Paste All Commands)
```bash
# All-in-one installation for Termux
pkg update && pkg upgrade -y && pkg install python git wget curl net-tools iproute2 -y && git clone https://github.com/w8bdcr-official/W8BDCR-IP-To-Router-Scanner && cd W8BDCR-IP-To-Router-Scanner && chmod +x install.sh W8IP-To-Router-Scanner.py && ./install.sh
```
**This single command does everything! Just copy, paste, and wait.**

---

#### 📝 Detailed Step-by-Step Guide

Complete guide for Android devices:

#### Step 1: Install Termux
1. Download **Termux** from [F-Droid](https://f-droid.org/packages/com.termux/)
   - Do NOT use Google Play Store version (outdated)
2. Install and open Termux

#### Step 2: Update Termux
```bash
# Update package lists and upgrade (accept all prompts)
pkg update && pkg upgrade -y
```
*This updates Termux to the latest version*

#### Step 3: Install All Required Packages
```bash
# Install all necessary packages in one command
pkg install python git wget curl net-tools iproute2 -y

# Alternative: Install packages one by one
pkg install python -y
pkg install git -y
pkg install wget -y
pkg install curl -y
pkg install net-tools -y
pkg install iproute2 -y

# Grant storage permission (optional, for saving files)
termux-setup-storage
```

**What each package does:**
- `python` - Programming language to run the tool
- `git` - Version control to download the tool
- `wget` - Download utility (for public IP detection)
- `curl` - Transfer data utility (alternative for public IP)
- `net-tools` - Network utilities (arp command)
- `iproute2` - IP routing utilities (ip command)

#### Step 4: Clone Repository
```bash
# Clone the tool
git clone https://github.com/w8bdcr-official/W8BDCR-IP-To-Router-Scanner

# Navigate to directory
cd W8BDCR-IP-To-Router-Scanner

# Make executable
chmod +x install.sh W8IP-To-Router-Scanner.py
```

#### Step 5: Run Auto-Installer
```bash
./install.sh
```

#### Step 6: Run the Tool
```bash
# Method 1: Direct execution
python W8IP-To-Router-Scanner.py

# Method 2: Using launcher (after install.sh)
w8ip
```

#### Termux Tips
- **Grant permissions**: Termux may need storage permission to save results
- **Keep screen on**: Long scans may need screen to stay active
- **WiFi recommended**: More reliable than mobile data
- **Root not required**: Tool works perfectly without root access

---

## 🚀 Usage

### Basic Usage

1. **Start the tool**
   ```bash
   python3 W8IP-To-Router-Scanner.py
   ```

2. **Enter IP range**
   - Start IP: `192.168.1.1`
   - End IP: `192.168.1.254`

3. **Wait for scan to complete**
   - Watch the live progress animation
   - Results appear as devices are found

4. **Review results**
   - Check terminal output
   - Review saved TXT file

### Command Examples

```bash
# Windows
python W8IP-To-Router-Scanner.py

# Linux/Mac
python3 W8IP-To-Router-Scanner.py

# Termux
python W8IP-To-Router-Scanner.py
# or (after installation)
w8ip
```

### Scanning Tips

- **Small range**: 192.168.1.1 to 192.168.1.10 (fast test)
- **Standard subnet**: 192.168.1.1 to 192.168.1.254 (most home networks)
- **Large network**: 10.0.0.1 to 10.0.0.254 (office networks)
- **Single IP**: Use same IP for start and end

---

## 📊 Output Information

### Terminal Display

The tool displays information in organized sections:

#### 1. Network Information
```
NETWORK INFORMATION
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

LOCAL IP ADDRESSES:
  ╰─➤ WLAN (WiFi):  192.168.1.100
  ╰─➤ Ethernet:     192.168.1.105

ROUTER/GATEWAY:
  ╰─➤ Default Gateway: 192.168.1.1 (Your Router)

PUBLIC IP ADDRESS:
  ╰─➤ Public IP:       203.45.67.89 (Internet IP)
```

#### 2. Scanning Progress
```
[⠹] Scanning IPs... Progress: 127/254 | Found: 3 devices
```

#### 3. Device Information
```
[+] DEVICE FOUND: 192.168.1.1

DEVICE INFORMATION:
  Device Name:       TP-Link_Router
  NetBIOS:           TPLINK-AP
  IP Address:        192.168.1.1
  MAC:                A4:2B:B0:XX:XX:XX
  Manufacturer:      TP-Link
  Type:               Router/Gateway
  User:               TPLINK-AP
  TTL:                64
  OS Guess:          Linux/Unix/Android
  Status:             ● ONLINE

  🔶 WiFi ROUTER DETECTED: TP-Link_Router

OPEN PORTS & SERVICES:
  • Port 80/tcp - HTTP
    Service:         HTTP
    Details:         Web Server (Unencrypted)
    Response Time:   12.45 ms
    Access URL:      http://192.168.1.1
```

#### 4. Scan Summary
```
SCAN COMPLETED - SUMMARY
  Total hosts scanned:      254
  Devices found (online):   5
  Total open ports found:   8
  Scan completed:           2025-10-15 02:31:23 PM
```

### Saved File Output

Results are automatically saved to:
```
W8IP_Scan_Results_YYYYMMDD_HHMMSS.txt
```

Contains:
- Complete scan details
- All device information
- Summary tables
- Router detection results
- Tool credits

---

## 🎯 Examples

### Example 1: Home Network Scan
```bash
python3 W8IP-To-Router-Scanner.py

# Enter when prompted:
Start IP: 192.168.1.1
End IP: 192.168.1.254

# Results in ~15-20 seconds
```

### Example 2: Small Range Test
```bash
python3 W8IP-To-Router-Scanner.py

# Enter when prompted:
Start IP: 192.168.1.1
End IP: 192.168.1.10

# Results in ~2-3 seconds
```

### Example 3: Single Device Check
```bash
python3 W8IP-To-Router-Scanner.py

# Enter when prompted:
Start IP: 192.168.1.1
End IP: 192.168.1.1

# Results in <1 second
```

---

## 🖼️ Screenshots

### Network Information Display
Shows your complete network configuration including WiFi IP, gateway, and public IP.

### Live Scanning Animation
Real-time progress with spinning animation and device counter.

### Device Details
Comprehensive information for each discovered device with color coding.

### Summary Report
Complete scan statistics and device table.

---

## 🔧 Troubleshooting

### Common Issues

#### Issue: Python not found
**Solution:**
```bash
# Windows
Download from python.org

# Linux
sudo apt-get install python3

# Termux
pkg install python
```

#### Issue: Permission denied
**Solution:**
```bash
chmod +x W8IP-To-Router-Scanner.py install.sh
```

#### Issue: No devices found
**Possible causes:**
- Firewall blocking scans
- Wrong IP range
- Devices have ports 80/8080 closed

**Solution:**
- Check firewall settings
- Verify IP range (use `ipconfig` or `ip addr`)
- Some devices don't have web servers

#### Issue: Slow scanning
**Solution:**
- Check network connection
- Reduce IP range for testing
- Close other network-heavy applications

#### Issue: Can't detect WLAN IP (Termux)
**Solution:**
```bash
# Install required tools
pkg install net-tools iproute2

# Verify WiFi connection
ip addr
```

#### Issue: Public IP shows "Not Available"
**Solution:**
- Check internet connection
- Try running again (API might be temporarily down)
- Firewall might block external requests

---

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. **Report Bugs**: Open an issue with details
2. **Suggest Features**: Share your ideas
3. **Submit Pull Requests**: Improvements and fixes
4. **Share**: Star the repo and tell others!

### Development Setup
```bash
git clone https://github.com/w8bdcr-official/W8BDCR-IP-To-Router-Scanner
cd W8BDCR-IP-To-Router-Scanner
# Make changes
# Test thoroughly
# Submit PR
```

---

## 👏 Credits

### Author
**W8BDCR**
- GitHub: [@W8BDCR](https://github.com/w8bdcr-official)

### Special Thanks
- Python community for excellent libraries
- Open-source contributors
- Users providing feedback and suggestions

### Tools & Technologies
- Python 3
- Socket programming
- Multi-threading
- ANSI color codes
- Subprocess management

---

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

```
MIT License

Copyright (c) 2025 W8BDCR

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software.
```

---

## 📞 Support

- **Issues**: [GitHub Issues](https://github.com/w8bdcr-official/W8BDCR-IP-To-Router-Scanner/issues)
- **Discussions**: [GitHub Discussions](https://github.com/w8bdcr-official/W8BDCR-IP-To-Router-Scanner/discussions)

---

## ⭐ Show Your Support

If you find this tool useful, please:
- ⭐ Star this repository
- 🔀 Fork and contribute
- 📢 Share with others
- 🐛 Report bugs
- 💡 Suggest features

---

<div align="center">

**Made with ❤️ by W8BDCR**

*Happy Scanning! 🚀*

</div>


