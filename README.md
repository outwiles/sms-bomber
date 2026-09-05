#📱 SMS/OTP Bomber

<div align="center">
  <img src="sms-bomber/assets/bomb.png" alt="SMS Bomber Logo" width="200"/>
  <br>
  <p><strong>A lightweight, multi‑threaded SMS & voice OTP bomber with real‑time logging and intelligent rate‑limiting.</strong></p>
  <p>
    <img src="https://img.shields.io/badge/Python-3.6%2B-blue.svg" alt="Python 3.6+">
    <img src="https://img.shields.io/badge/License-MIT-green.svg" alt="MIT License">
    <img src="https://img.shields.io/badge/Platform-Linux%20%7C%20macOS%20%7C%20Windows%20%7C%20Android-blueviolet" alt="Platforms">
  </p>
</div>

---

📌 Disclaimer

This tool is intended for authorised security testing and educational purposes only.
The author is not responsible for any misuse. Always obtain proper permission before testing any service.
Use at your own risk.

---

✨ Features

· ⚡ 500 concurrent threads (adjustable)
· 🔄 Random User‑Agent rotation to avoid detection
· 🛡️ Automatic cooldown on rate‑limits (429) and HTTP errors (4xx)
· 📊 Real‑time logs – timestamp, URL, status code
· 📈 Live stats – sent/failed/rate‑limited counters
· 🛠️ Fully customisable – easily add/remove endpoints
· 🖥️ Cross‑platform – Termux, Linux, macOS, Windows

---

📦 Requirements

· Python 3.6 or higher
· Internet connection

---

🔧 Installation

📱 Termux (Android)

```bash
pkg update && pkg upgrade
pkg install python git
git clone https://github.com/outwiles/sms-bomber.git
cd sms-bomber
pip install -r requirements.txt
```

🐧 Linux (Debian/Ubuntu)

```bash
sudo apt update
sudo apt install python3 python3-pip git
git clone https://github.com/outwiles/sms-bomber.git
cd sms-bomber
pip3 install -r requirements.txt
```

🍎 macOS

```bash
brew install python3 git
git clone https://github.com/outwiles/sms-bomber.git
cd sms-bomber
pip3 install -r requirements.txt
```

🪟 Windows

1. Install Python 3 from python.org – check “Add Python to PATH”
2. Open Command Prompt (as Administrator) and run:

```cmd
git clone https://github.com/outwiles/sms-bomber.git
cd sms-bomber
pip install -r requirements.txt
```

---

⚙️ Configuration

Open the script and locate the Aashu11 = [] list.
Add your own endpoints in the following format:

```python
Aashu11 = [
    {
        "url": "https://example.com/api/otp",
        "method": "POST",
        "headers": {"Content-Type": "application/json"},
        "json": {"phone": "REPLACE_WITH_TARGET", "country": "IN"}
    },
    {
        "url": "https://api.example.com/v1/otp/send",
        "method": "POST",
        "headers": {"Host": "api.example.com"},
        "data": "mobile=REPLACE_WITH_TARGET&action=send"
    },
    # ... add as many as you want
]
```

· REPLACE_WITH_TARGET is automatically replaced by the phone number you enter.
· Supported methods: POST, PUT, GET.
· Use json for JSON payloads or data for URL‑encoded form data.

---

🚀 Usage

Run the script:

```bash
python bomber.py
```

Then enter the 10‑digit phone number when prompted.

Pass number as argument (skips prompt)

```bash
python bomber.py 9336761059
```

Logging

Every request is printed with a timestamp, URL, and status code:

```
[14:32:15] https://api.example.com/otp -> 200 ✅ OK
[14:32:16] https://api.example.com/otp -> 429 ⏳ RATE
[14:32:17] https://api.example.com/otp -> 404 ❌ FAIL
```

Stats are displayed every 0.5 seconds:

```
[14:32:18] Stats: Sent 142 | Failed 23 | Rate 5
```

---

🛠️ Customisation

Variable Description Default
THREAD_COUNT Number of concurrent workers 500
STATS_REFRESH Stats update interval (seconds) 0.5
Cooldown 429 Wait time after rate‑limit 120s
Cooldown 4xx Wait time after client errors 60s

---

📁 Project Structure

```
sms-bomber/
├── bomber.py              # Main script
├── requirements.txt       # Python dependencies
├── README.md              # This file
└── bomb/
    └── assets/
        └── bomb.png       # Logo
```

---

📄 License

This project is licensed under the MIT License – see the LICENSE file for details.

---

🙏 Credits

· Author: @outwiles
· Logo: Included in bomb/assets/

---

⭐ Support

If you find this tool useful, please star the repository and share it responsibly!

---

Happy testing! 🔥
