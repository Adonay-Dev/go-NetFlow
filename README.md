# go-CICFlowMeter

  **go-CICFlowMeter** is a high-performance, real-time network flow analyzer written in Go. Inspired by CICFlowMeter, this tool captures live network traffic, constructs flows per the OSI model, and extracts rich flow features for security, performance, and behavioral analysis.

---

## 🚀 Features

- 🧠 **OSI Layer-Based Flow Classification**  
  Flows are categorized by their OSI layer (Application, Transport, Network, etc.).

- 📡 **Real-Time Packet Capture**  
  High-speed live traffic monitoring using `gopacket` (libpcap-based).

- 📊 **Advanced Feature Extraction**  
  Extracts byte/packet counts, durations, TCP flags, inter-arrival times, and more.

- 🔁 **Flow Timeout and Expiration Handling**  
  Dynamically expires and flushes completed flows.

- 🔄 **Modular Export Support**  
  Export to JSON, CSV, Kafka, InfluxDB, or any custom plugin.

- 🔒 **Lightweight & Cross-Platform**  
  Written in Go for easy deployment and scalability.

---

## 📦 OSI Layer Flow Support

| Layer             | Example Protocols | Extracted Features                                |
|-------------------|-------------------|---------------------------------------------------|
| Application Layer | HTTP, DNS, FTP ...    | Method types, response codes, domain names    |
| Transport Layer   | TCP, UDP ...          | Port-based flows, TCP flags, retransmissions  |
| Network Layer     | IP, ICMP ...          | TTL, fragmentation, protocol type             |
| Data Link Layer   | Ethernet ...          | MAC address pairs, EtherType                  |

---

## 🛠️ Installation

### Prerequisites
- Go 1.20 or higher
- libpcap installed (on Linux/macOS)
- Root or capture permissions on your interface

### Clone and Build

```bash
git clone https://github.com/yourusername/go-CICFlowMeter.git
cd go-CICFlowMeter
....