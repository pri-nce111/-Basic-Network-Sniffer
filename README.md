# Basic-Network-Sniffer
Build a network sniffer in Python that captures and  analyzes network traffic. This project will help you  understand how data flows on a network and how  network packets are structured


# 📡 Network Sniffer & Analyzer

This project is a Python-based network sniffer and analyzer tool using `Scapy`, `Pandas`, and `Matplotlib`. It captures real-time network packets, extracts useful information, performs statistical analysis, and visualizes the data in various charts.

---

## 🔧 Features

- Capture live network packets (TCP, UDP, HTTP, DNS, ICMP)
- Extract detailed packet information
- Perform traffic statistics (protocol, IPs, ports, sizes)
- Visualize traffic patterns (pie charts, bar charts, histograms)
- Export data to CSV and generate JSON summary reports
- Optional simulated traffic mode for demonstration/testing

---

## 📦 Requirements

- Python 3.6+
- Root/admin privileges (for real packet capture)
- Install required packages:

```bash
pip install scapy pandas matplotlib seaborn
⚠️ On some systems, Scapy may require additional permissions or tools (like tcpdump or libpcap).

🚀 Usage
Run the Sniffer
bash
Copy
Edit
python your_script_name.py
The script will:

Capture 30 packets or timeout after 20 seconds

Display the first 10 packets

Generate analysis summary

Create CSV and JSON report files

Simulate Network Traffic (No root access)
If you are running in an environment like Google Colab or do not have permission to sniff packets:

Uncomment the run_simulation() line at the bottom of the script.

Run the script to analyze synthetic data.

📊 Output Files
network_traffic_analysis.csv — Captured packet data

network_analysis_report.json — Summary report with key findings

Visualizations — Plotted inline using matplotlib

🧪 Example Statistics
Protocol distribution (TCP, UDP, HTTP, DNS)

Top 10 source IPs

Top 10 destination ports

Packet size stats: mean, min, max, total

🛠️ Customization
Modify start_sniffing(packet_count=30, timeout=20) to adjust capture settings

Add more protocol layers in extract_packet_info() to extend functionality

Enhance visualizations using Seaborn or Plotly

📌 Notes
Designed for educational and diagnostic purposes

Live packet capture works best on a local machine with admin/root privileges

Use responsibly and ensure compliance with local laws and network policies
