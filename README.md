
# 📡 Home Network Mapping & Ping Test

## 📌 Project Overview
This project maps my home network and verifies connectivity using `ipconfig` and `ping` commands.  
The objective is to identify connected devices, record IP configuration details, and confirm both local (LAN) and Internet connectivity.

---

## 🌐 Network Diagram

```mermaid
graph TD
    Internet["🌍 Internet"]:::internet
    Router["📡 Router<br>172.20.6.1"]:::router
    PC["💻 Windows PC<br>172.20.6.184"]:::pc
    Phone["📱 Samsung A03<br>172.20.7.142"]:::phone

    Internet --> Router
    Router --> PC
    Router --> Phone

    classDef internet fill:#4CAF50,color:#ffffff,stroke:#2E7D32,stroke-width:2px;
    classDef router fill:#2196F3,color:#ffffff,stroke:#0D47A1,stroke-width:2px;
    classDef pc fill:#FF9800,color:#ffffff,stroke:#E65100,stroke-width:2px;
    classDef phone fill:#9C27B0,color:#ffffff,stroke:#4A148C,stroke-width:2px;
```

### Network Explanation
- Both the Windows PC and Samsung A03 connect to the router via Wi-Fi.
- The router (172.20.6.1) acts as the default gateway.
- The router connects the local network to the Internet.
- All devices are within the 172.20.x.x private IP range.

---

## 🖥 Device IP Configuration

| Device        | IP Address      | Subnet Mask     | Default Gateway |
|---------------|-----------------|----------------|-----------------|
| Windows PC    | 172.20.6.184    | 255.255.254.0  | 172.20.6.1      |
| Samsung A03   | 172.20.7.142    | 255.255.254.0  | 172.20.6.1      |
| Router        | 172.20.6.1      | —              | —               |

---

## 🧾 IP Configuration Screenshot

### Windows `ipconfig` Output

![IP Configuration](ipconfig.png)

---

## 📡 Ping Test Results

### 1️⃣ Ping Router (LAN Connectivity)

Command used:
```
ping 172.20.6.1
```

Result:
- Replies received successfully
- 0% packet loss
- Confirms communication with the local router

Screenshot:

![Ping Router and Phone](ping router&phone.png)

---

### 2️⃣ Ping Internet (External Connectivity)

Command used:
```
ping google.com
```

Result:
- Replies received successfully
- 0% packet loss
- Confirms active Internet connection

Screenshot:

![Ping Internet](ping internet.png)

---

## ✅ Network Analysis Summary

The Windows PC (172.20.6.184) and Samsung A03 (172.20.7.142) are successfully connected to the router (172.20.6.1).  
Ping tests confirm:

- Successful LAN communication
- Successful Internet connectivity
- No packet loss observed
- Stable and functional network configuration

The home network is operating correctly and all devices are properly connected.

---

## 📂 Repository Contents

```
network-mapping-ping-test/
│
├── README.md
├── ipconfig.png
├── ping internet.png
└── ping router&phone.png
```
