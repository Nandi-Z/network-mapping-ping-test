# network-mapping-ping-test
# Network Mapping & Ping Test Report

## 1. Network Overview

This report documents the mapping of my home network using ipconfig and ping tests.

---

## 2. Network Configuration (ipconfig Output)

Wireless LAN Adapter Wi-Fi:

- IPv4 Address: 172.20.6.184
- Subnet Mask: 255.255.254.0
- Default Gateway (Router): 172.20.6.1

Smartphone:
- IPv4 Address: 172.20.7.142

---

## 3. Network Diagram

```
                [ Internet ]
          <img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/1b8600e3-8b83-4b26-b161-b409b6679365" />
<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/1b8600e3-8b83-4b26-b161-b409b6679365" />
           |
               172.20.6.1
               [ Router ]
                    |
        ---------------------------
        |                         |
172.20.6.184               172.20.7.142
   (My PC)                   (Smartphone)
```

---

## 4. Ping Test Results

### Ping Router (172.20.6.1)

```
Reply from 172.20.6.1: bytes=32 time=2ms TTL=64
Reply from 172.20.6.1: bytes=32 time=1ms TTL=64
```

### Ping Smartphone (172.20.7.142)

```
Reply from 172.20.7.142: bytes=32 time=3ms TTL=128
```

### Ping External Website (google.com)

```
Reply from 142.250.xxx.xxx: bytes=32 time=25ms TTL=115
```

---

## 5. Summary

The local network is functioning correctly. 
All internal devices responded to ping requests with low latency.
Internet connectivity is active and stable.
