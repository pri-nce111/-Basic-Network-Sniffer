# Basic-Network-Sniffer
Build a network sniffer in Python that captures and  analyzes network traffic. This project will help you  understand how data flows on a network and how  network packets are structured

Network Sniffer 🔍
A comprehensive real-time network packet capture and analysis tool designed for educational purposes, network diagnostics, and security analysis. Compatible with both local environments and Google Colab.
✨ Features
Core Functionality

Real-time packet capture using raw sockets
Protocol analysis for TCP, UDP, ICMP, and other protocols
Detailed packet parsing including Ethernet, IP, TCP, and UDP headers
Live statistics showing protocol distribution, top IPs, and port usage
Cross-platform compatibility (Linux, Windows, macOS)

Advanced Capabilities

Alternative monitoring mode for restricted environments
Flexible capture options with packet limits and timeouts
Comprehensive statistics with real-time updates
Service identification for common ports
MAC address tracking and Ethernet frame analysis

🚀 Quick Start
Local Installation

Clone or download the script
Install dependencies (optional for enhanced features):
bashpip install psutil

Run with appropriate privileges:
bash# Linux/macOS (requires sudo for raw sockets)
sudo python3 network_sniffer.py

# Windows (run as Administrator)
python network_sniffer.py


Google Colab Usage
Simply upload the script to Google Colab and run:
python# The script automatically detects Colab environment
exec(open('network_sniffer.py').read())
📋 Usage Options
When you run the script, you'll see these options:

Start packet capture - Full raw socket packet capture (requires root/admin)
Start alternative network monitor - System-level network monitoring
Capture with packet limit - Stop after capturing N packets
Capture with timeout - Stop after specified time duration

🔧 Technical Details
Raw Socket Mode

Captures packets at the Ethernet layer
Parses headers for detailed analysis
Requires elevated privileges (root/administrator)
Provides complete packet visibility

Alternative Monitor Mode

Uses system APIs via psutil
Monitors active connections and traffic
Works in restricted environments
No special privileges required

📊 Output Information
Packet Details

Timestamp with millisecond precision
Protocol information (TCP, UDP, ICMP, etc.)
IP addresses (source and destination)
Port numbers for TCP/UDP traffic
MAC addresses for Ethernet frames
Packet size and header details

Statistics Dashboard

Protocol distribution with percentages
Top source IP addresses
Most active destination ports
Capture duration and packet rate
Service identification for common ports

🛡️ Security & Privacy
Important Notes

This tool is designed for educational and diagnostic purposes
Only capture traffic on networks you own or have permission to monitor
Raw socket access requires elevated privileges for security reasons
Be aware of local laws and regulations regarding network monitoring

Best Practices

Use in controlled environments for learning
Respect privacy and legal boundaries
Monitor your own network traffic only
Use alternative mode in shared/restricted environments

🔧 System Requirements
Minimum Requirements

Python 3.6 or higher
Network interface access
For full functionality: root/administrator privileges

Optional Dependencies

psutil - Enhanced system monitoring capabilities
google.colab - Automatic Colab environment detection

Platform Support

✅ Linux - Full functionality with raw sockets
✅ Windows - Full functionality with raw sockets
✅ macOS - Full functionality with raw sockets
✅ Google Colab - Alternative monitoring mode
✅ Other Unix-like systems - Generally supported

🐛 Troubleshooting
Common Issues
"Permission denied" error:

Run with sudo on Linux/macOS
Run as Administrator on Windows
Use alternative monitor mode (option 2)

"Module not found" error:

Install psutil: pip install psutil
The script will attempt auto-installation

No packets captured:

Check network activity on your system
Verify network interface is active
Try alternative monitoring mode

Google Colab specific:

Raw sockets are not available in Colab
Script automatically uses alternative monitoring
Some features may be limited

📚 Educational Use Cases
Network Security Learning

Understand packet structure and protocols
Learn about network communication patterns
Analyze traffic flows and identify services
Practice network forensics techniques

Network Troubleshooting

Identify network bottlenecks
Monitor connection states
Analyze protocol distribution
Debug connectivity issues

System Administration

Monitor network usage patterns
Identify active services and ports
Track network performance metrics
Audit network connections

🔍 Example Output
📦 Packet #15 | 14:30:25.123
Size: 74 bytes | Protocol: TCP
🌐 IP: 192.168.1.100 → 172.217.164.110
   TTL: 64 | Version: 4 | Length: 60
🔌 TCP: Port 54321 → 443
   Seq: 1234567890 | Ack: 9876543210
🔗 MAC: aa:bb:cc:dd:ee:ff → 12:34:56:78:90:ab

📊 CAPTURE STATISTICS
Duration: 30.5s | Packets: 150 | Rate: 4.9 pps

🔗 Protocol Distribution:
   TCP: 120 (80.0%)
   UDP: 25 (16.7%)
   ICMP: 5 (3.3%)

🌐 Top Source IPs:
   192.168.1.100: 95 (63.3%)
   10.0.0.1: 30 (20.0%)
🤝 Contributing
This project welcomes contributions! Areas for improvement:

Additional protocol parsers
Enhanced statistics and visualization
Performance optimizations
Extended platform support
Documentation improvements

⚖️ Legal Disclaimer
This tool is provided for educational and legitimate network administration purposes only. Users are responsible for ensuring compliance with applicable laws and regulations. Only use this tool on networks you own or have explicit permission to monitor.
📖 Learning Resources
Recommended Reading

Computer Networks by Andrew Tanenbaum
TCP/IP Illustrated by W. Richard Stevens
Wireshark documentation for packet analysis
RFC documents for protocol specifications

Related Tools

Wireshark - GUI packet analyzer
tcpdump - Command-line packet capture
nmap - Network discovery and security auditing
netstat - Network connection monitoring

🏷️ Version History

v1.0 - Initial release with core packet capture functionality
Support for TCP, UDP, ICMP protocol analysis
Alternative monitoring mode for restricted environments
Cross-platform compatibility and Google Colab support
