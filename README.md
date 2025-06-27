# 📡 WiFi Password Extractor (Linux & Windows)

This Python script retrieves saved WiFi network names and their passwords from a Linux or Windows system.  
It is designed to help you **recover forgotten WiFi passwords** on your own computer. It automatically detects the operating system and runs the appropriate commands to extract WiFi credentials.

---

## ⚠️ Disclaimer

⚠️ **WARNING**: This script accesses sensitive system configuration files or commands and **requires elevated privileges** (`sudo` on Linux or Administrator on Windows).  
Use **only on systems you own** or have **explicit permission** to access. Misuse may violate privacy laws or computer security laws.

---

## 🧩 Features

- ✅ Automatically detects the OS (`Linux` or `Windows`)
- 🐧 **Linux Mode**:
  - Lists all saved WiFi profiles from `/etc/NetworkManager/system-connections`
  - Extracts the password (`psk`) from the `.nmconnection` file
  - Displays the WiFi name and corresponding password
- 🪟 **Windows Mode**:
  - Uses `netsh wlan show profiles` to list stored WiFi profiles
  - Extracts passwords using `netsh wlan show profile <SSID> key=clear`
- 🖥️ Displays credentials in a clean, tabular format

---

## 💻 How to Execute the Script

### 📝 Step 1: Save the Script

Save the Python script in a file named `wifiPasswords.py`.

---

### 🐧 On Linux

#### ✅ Requirements:
- Python 3 installed
- Admin/root access (`sudo`)

#### ▶️ Run the script:

```bash
sudo python3 wifiPasswords.py
