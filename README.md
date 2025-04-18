# Local Network Security Scanner 🔒

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)
[![Nmap](https://img.shields.io/badge/Nmap-7.92-green)](https://nmap.org/)

## 📋 Overview

A comprehensive network security scanning toolkit designed for local network assessment and vulnerability detection. This project leverages advanced network scanning techniques using Nmap to identify connected devices, analyze open ports, and evaluate potential security risks in IoT environments.

## 🎯 Key Features

- **Network Device Discovery**: Automated detection and identification of all active devices
- **Port Scanning & Analysis**: Comprehensive port scanning with service detection
- **IoT Device Assessment**: Specialized scanning profiles for IoT devices
- **Security Risk Evaluation**: Automated vulnerability assessment reporting
- **Network Mapping**: Visual representation of network topology

## 🛠️ Technical Stack

- **Primary Tool**: Nmap 7.92+
- **Operating System**: Kali Linux (Debian-based)
- **Additional Tools**:
  - Python 3.8+ for automation scripts
  - Network analysis libraries
  - Visualization tools

## 📊 Methodology

### 1. Network Reconnaissance
```bash
# Network interface identification
ifconfig

# Network device discovery
sudo nmap -sn 192.168.1.0/24 -oX scan_results.xml
```

### 2. Port Scanning
```bash
# Comprehensive port scan
sudo nmap -sS -sV -p- 192.168.1.1 --version-intensity 5

# Service detection
sudo nmap -sV --version-all 192.168.1.1
```

### 3. Vulnerability Assessment
- Port security analysis
- Service version verification
- Known vulnerability matching
- Security misconfiguration detection

## 📈 Sample Results

```json
{
    "devices": {
        "router": {
            "manufacturer": "Huawei",
            "ip": "192.168.1.1",
            "open_ports": [
                {"port": 53, "service": "domain", "state": "open"},
                {"port": 80, "service": "http", "state": "open"}
            ]
        },
        "iot_devices": [
            {
                "manufacturer": "GE Lighting",
                "ip": "192.168.1.52",
                "type": "Smart Light"
            },
            {
                "manufacturer": "Amazon Technologies",
                "ip": "192.168.1.54",
                "type": "Smart Home Device"
            }
        ]
    }
}
```

## 🔍 Security Analysis

### Key Findings
1. **Open Services**: Identification of potentially vulnerable network services
2. **IoT Vulnerabilities**: Assessment of IoT device security configurations
3. **Network Exposure**: Analysis of external network exposure points

### Recommendations
- Regular security audits
- Firmware updates management
- IoT device isolation strategies
- Network segmentation implementation

## 🚀 Getting Started

1. Clone the repository:
```bash
git clone https://github.com/mat1520/local-network-security-scanner.git
cd local-network-security-scanner
```

2. Install dependencies:
```bash
# Ensure Nmap is installed
sudo apt-get update
sudo apt-get install nmap
```

3. Run the initial scan:
```bash
sudo ./scan.sh
```

## 📝 Documentation

Detailed documentation is available in the [Wiki](https://github.com/mat1520/local-network-security-scanner/wiki).

## 🔐 Security Considerations

This tool should be used responsibly and only on networks you own or have explicit permission to test. Unauthorized network scanning may be illegal in your jurisdiction.

## 📚 References

- [Nmap Official Documentation](https://nmap.org/docs.html)
- [Kali Linux Documentation](https://www.kali.org/docs/)
- [Network Security Best Practices](https://www.cisecurity.org/controls/cis-controls-list)

## 🤝 Contributing

Contributions are welcome! Please read our [Contributing Guidelines](CONTRIBUTING.md) before submitting pull requests.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---
⭐ If you find this project useful, please consider giving it a star!
