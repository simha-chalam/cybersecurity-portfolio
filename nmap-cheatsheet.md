# 🕵️‍♂️ Nmap Commands Cheat Sheet

> **Nmap (Network Mapper)** is a free and powerful tool for network discovery and security auditing.  
> ⚠️ Use only on systems you have permission to scan.

---

## 📍 1. Basic Scans
nmap 192.168.1.1                  # Simple scan of one IP
nmap 192.168.1.1 192.168.1.2      # Scan multiple IPs
nmap 192.168.1.1-50               # Scan IP range
nmap 192.168.1.0/24               # Scan an entire subnet
🚪 2. Port Scanning
nmap -p 22 192.168.1.1            # Scan specific port
nmap -p 1-1000 192.168.1.1        # Scan ports 1 to 1000
nmap -p- 192.168.1.1              # Scan all 65535 ports
⚙️ 3. Service and Version Detection
nmap -sV 192.168.1.1              # Detect service versions
nmap -sV --version-all 192.168.1.1 # Aggressive version detection
🖥️ 4. Operating System Detection
nmap -O 192.168.1.1               # Detect operating system
nmap -O --osscan-guess 192.168.1.1 # Guess OS more aggressively
🧠 5. Aggressive Scan
nmap -A 192.168.1.1
# Combines -O, -sV, script scanning, and traceroute
📜 6. Nmap Scripting Engine (NSE)
nmap --script vuln 192.168.1.1          # Run vulnerability scan
nmap --script default 192.168.1.1       # Run default scripts
nmap --script http-enum 192.168.1.1     # Run specific script
🎭 7. Stealth and Evasion
nmap -sS 192.168.1.1                     # TCP SYN (stealth) scan
nmap -Pn 192.168.1.1                     # Skip host discovery (treat all hosts as online)
nmap -f 192.168.1.1                      # Fragment packets (IDS evasion)
nmap --data-length 50 192.168.1.1        # Obfuscate scan with random padding
🕓 8. Speed and Timing
nmap -T0 192.168.1.1    # Slowest (paranoid)
nmap -T4 192.168.1.1    # Faster (recommended for normal use)
nmap -T5 192.168.1.1    # Fastest (can be noisy)
🔄 9. Output Formats
nmap -oN output.txt 192.168.1.1        # Normal output
nmap -oX output.xml 192.168.1.1        # XML output
nmap -oG output.gnmap 192.168.1.1      # Grepable output
nmap -oA fullscan 192.168.1.1          # Save in all formats (adds .nmap, .xml, .gnmap)
📂 10. Save & Read Targets from File
nmap -iL targets.txt                   # Input file with target IPs
nmap -iL hosts.txt -oA scan_results    # Save scan of multiple targets
🧪 11. Firewall and IDS Testing
nmap -sA 192.168.1.1           # ACK scan to check firewall rules
nmap -sN 192.168.1.1           # TCP Null scan (no flags)
nmap -sX 192.168.1.1           # Xmas scan (FIN, PSH, URG flags set)
nmap -sF 192.168.1.1           # FIN scan
🧱 12. Scan Specific Protocols
nmap -sT 192.168.1.1           # TCP connect scan
nmap -sU 192.168.1.1           # UDP scan
nmap -sS -sU 192.168.1.1       # TCP and UDP combo scan
nmap -6 2001:db8::1            # IPv6 scan
🔧 13. Other Useful Flags
nmap --top-ports 20 192.168.1.1        # Scan top 20 common ports
nmap --reason 192.168.1.1              # Show reason why a port is in a specific state
nmap --open 192.168.1.1                # Show only open ports
nmap --traceroute 192.168.1.1          # Perform traceroute
