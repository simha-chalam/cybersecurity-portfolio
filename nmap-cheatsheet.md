---

## 📍 1. Basic Scans

| Command                        | Description                            |
|-------------------------------|----------------------------------------|
| `nmap 192.168.1.1`            | Scan a single IP                       |
| `nmap 192.168.1.1 192.168.1.2`| Scan multiple IPs                      |
| `nmap 192.168.1.1-50`         | Scan a range of IPs                    |
| `nmap 192.168.1.0/24`         | Scan an entire subnet                  |

---

## 🚪 2. Port Scanning

| Command                         | Description                      |
|----------------------------------|----------------------------------|
| `nmap -p 22 192.168.1.1`         | Scan specific port               |
| `nmap -p 1-1000 192.168.1.1`     | Scan a range of ports            |
| `nmap -p- 192.168.1.1`           | Scan all 65535 ports             |

---

## ⚙️ 3. Service and Version Detection

| Command                                 | Description                   |
|----------------------------------------|-------------------------------|
| `nmap -sV 192.168.1.1`                 | Detect service versions       |
| `nmap -sV --version-all 192.168.1.1`   | Aggressive version detection  |

---

## 🖥️ 4. OS Detection

| Command                                | Description                      |
|----------------------------------------|----------------------------------|
| `nmap -O 192.168.1.1`                 | Detect OS                        |
| `nmap -O --osscan-guess 192.168.1.1`  | Guess OS more aggressively       |

---

## 🧠 5. Aggressive Scan

| Command            | Description                                             |
|-------------------|---------------------------------------------------------|
| `nmap -A 192.168.1.1` | Aggressive scan (OS, version, script, traceroute) |

---

## 📜 6. Scripting Engine (NSE)

| Command                                  | Description                      |
|------------------------------------------|----------------------------------|
| `nmap --script vuln 192.168.1.1`        | Run vulnerability scan           |
| `nmap --script default 192.168.1.1`     | Run default scripts              |
| `nmap --script http-enum 192.168.1.1`   | Run specific script              |
| `nmap --script-help default`           | Show help for default scripts    |

---

## 🎭 7. Stealth and Evasion

| Command                                  | Description                       |
|------------------------------------------|-----------------------------------|
| `nmap -sS 192.168.1.1`                  | Stealth (SYN) scan                |
| `nmap -Pn 192.168.1.1`                  | Treat all hosts as online         |
| `nmap -f 192.168.1.1`                   | Fragment packets (evade IDS)      |
| `nmap --data-length 50 192.168.1.1`     | Obfuscate scan with extra padding |

---

## 🕓 8. Timing and Performance

| Command                | Description            |
|------------------------|------------------------|
| `nmap -T0 192.168.1.1` | Slowest (paranoid)     |
| `nmap -T4 192.168.1.1` | Faster (default)       |
| `nmap -T5 192.168.1.1` | Fastest (very noisy)   |

---

## 🔄 9. Output Formats

| Command                               | Description                   |
|----------------------------------------|-------------------------------|
| `nmap -oN output.txt 192.168.1.1`     | Save normal output            |
| `nmap -oX output.xml 192.168.1.1`     | Save XML output               |
| `nmap -oG output.gnmap 192.168.1.1`   | Save grepable output          |
| `nmap -oA scan 192.168.1.1`           | Save in all formats           |

---

## 📂 10. Input & Output from Files

| Command                                     | Description                      |
|---------------------------------------------|----------------------------------|
| `nmap -iL targets.txt`                     | Input targets from file          |
| `nmap -iL hosts.txt -oA results`           | Scan from file and save results  |

---

## 🧪 11. Firewall & IDS Testing

| Command               | Description                        |
|------------------------|------------------------------------|
| `nmap -sA 192.168.1.1` | ACK scan                           |
| `nmap -sN 192.168.1.1` | TCP Null scan                      |
| `nmap -sX 192.168.1.1` | Xmas scan                          |
| `nmap -sF 192.168.1.1` | FIN scan                           |

---

## 🧱 12. Protocol Scans

| Command                       | Description              |
|-------------------------------|--------------------------|
| `nmap -sT 192.168.1.1`        | TCP connect scan         |
| `nmap -sU 192.168.1.1`        | UDP scan                 |
| `nmap -sS -sU 192.168.1.1`    | TCP + UDP scan           |
| `nmap -6 2001:db8::1`         | IPv6 scan                |

---

## 🔧 13. Miscellaneous Options

| Command                          | Description                       |
|----------------------------------|-----------------------------------|
| `nmap --top-ports 20 192.168.1.1`| Scan top 20 most used ports       |
| `nmap --reason 192.168.1.1`      | Show why ports are in a state     |
| `nmap --open 192.168.1.1`        | Show only open ports              |
| `nmap --traceroute 192.168.1.1`  | Perform traceroute                |
| `nmap --iflist`                  | Show available network interfaces |

---
