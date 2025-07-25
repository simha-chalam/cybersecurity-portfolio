# 🔥 UFW (Uncomplicated Firewall)

**UFW** is a user-friendly command-line interface for managing **iptables**, the firewall used in most Linux systems.

---

## 🛠️ Basic UFW Commands

### ✅ Enable UFW
```bash
sudo ufw enable
```

### ⛔ Disable UFW
```bash
sudo ufw disable
```

### 🔍 Check Status
```bash
sudo ufw status
```

For more details:
```bash
sudo ufw status verbose
```

---

## 🎯 Rules Management

### 📥 Allow Incoming Connections
```bash
sudo ufw allow 22        # Allow SSH
sudo ufw allow 80        # Allow HTTP
sudo ufw allow 443       # Allow HTTPS
```

You can also specify:
```bash
sudo ufw allow from 192.168.1.100 to any port 22
```

### 🚫 Deny Incoming Connections
```bash
sudo ufw deny 23         # Deny Telnet
```

### 📤 Allow Outgoing Connections (if default is deny)
```bash
sudo ufw allow out 53    # Allow DNS lookups
```

---

## 🔧 Port Ranges and Protocols
```bash
sudo ufw allow 1000:2000/tcp
sudo ufw allow 6000:7000/udp
```

---

## 🔐 Application Profiles

Check available profiles:
```bash
sudo ufw app list
```

Allow by profile:
```bash
sudo ufw allow "OpenSSH"
```

---

## ⚙️ Default Policies
```bash
sudo ufw default deny incoming
sudo ufw default allow outgoing
```

---

## 🧽 Delete a Rule
```bash
sudo ufw delete allow 22
```

---

## 🧱 Example: Secure Server Setup
```bash
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw allow ssh
sudo ufw allow http
sudo ufw allow https
sudo ufw enable
```

---

## 📎 Notes
- Always make sure you don’t block yourself out of SSH (especially on remote servers).
- Use `ufw status numbered` to see rules with line numbers.
- Use `sudo ufw delete [number]` to remove a rule by its number.

---

## 📚 References
- [UFW Manual](https://manpages.ubuntu.com/manpages/latest/en/man8/ufw.8.html)
