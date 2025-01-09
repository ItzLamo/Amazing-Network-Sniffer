# Amazing Network Sniffer

## Description
A Python-based network sniffer with a user-friendly GUI built using **Tkinter**. This tool captures and displays network packets, providing detailed information about the captured data.

## Features
- **Start/Stop Packet Capture:** Easily control the sniffing process.
- **Packet Filtering:** Filter captured packets by protocol (TCP, UDP, ICMP, or all protocols).
- **Live Statistics:** View the total number of packets captured.
- **Detailed View:** Inspect packet details in JSON format.
- **Save Captures:** Export captured packets to a JSON file.
- **Scrollable Packet List:** View captured packets in a table with columns for time, source, destination, protocol, and length.

## Requirements
- **Python 3.7+**
- Libraries: 
  - `tkinter`
  - `scapy`
  - `queue`
  - `json`
  - `threading`
  - `datetime`

Install required libraries with:
```bash
pip install scapy
```

## How to Use
1. Run the program as an administrator (required for network sniffing).
2. Click **Start Capture** to begin sniffing network packets.
3. Use the **Filters** dropdown to filter packets by protocol.
4. Click a packet in the list to view its details in the **Packet Details** section.
5. Click **Stop Capture** to stop sniffing.
6. Save the captured data to a file by clicking **Save Capture**.

## Output
Captured packets are saved in JSON format when exported. Example output:
```json
[
    {
        "time": "2025-01-09 14:00:00",
        "source": "192.168.1.2",
        "destination": "192.168.1.3",
        "protocol": "TCP",
        "length": 60,
        "details": {
            "sport": 80,
            "dport": 45000,
            "flags": "S"
        }
    }
]
```
