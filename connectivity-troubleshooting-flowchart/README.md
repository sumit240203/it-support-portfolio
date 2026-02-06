# Connectivity Troubleshooting Flowchart

Use this to quickly identify whether an issue is **Wi‑Fi**, **internet**, or **DNS**.

```mermaid
flowchart TD
  A[User reports: "No Internet"] --> B{Connected to Wi‑Fi/Ethernet?}
  B -- No --> C[Connect to correct SSID / check cable]
  C --> D[Test again]
  B -- Yes --> E{Can ping 8.8.8.8?}
  E -- No --> F[Local network/ISP issue: reboot device/router, check IP]
  E -- Yes --> G{Can resolve DNS? (ping google.com / nslookup)}
  G -- No --> H[DNS issue: flush DNS, change DNS, check VPN]
  G -- Yes --> I[App-specific issue: browser cache, proxy, firewall, service outage]
```

## Commands
- Windows: `ipconfig /all`, `ping`, `tracert`, `nslookup`
- macOS: `ifconfig`, `ping`, `traceroute`, `nslookup`
