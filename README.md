<div align="center"><img src="assets/bomb.jpg" alt="SMS Bomber" width="180">SMS Bomber

High-Concurrency SMS / OTP Request Testing Tool

A lightweight Python-based tool for testing SMS/OTP request handling, concurrency, rate limiting, endpoint reliability, and defensive controls in authorized environments.

<br>""Python" (https://img.shields.io/badge/Python-3.9%2B-blue?style=for-the-badge&logo=python)" (https://www.python.org/)
""License" (https://img.shields.io/badge/License-MIT-green?style=for-the-badge)" (LICENSE)
""Platform" (https://img.shields.io/badge/Platform-Windows%20%7C%20macOS%20%7C%20Linux-lightgrey?style=for-the-badge)" (#installation)

</div>---

Overview

SMS Bomber is a Python command-line project built around high-concurrency HTTP request testing.

It can be used by developers and security researchers to evaluate how an application or API behaves under repeated SMS/OTP request traffic, including:

- Request concurrency
- Rate limiting
- Retry handling
- HTTP error handling
- Endpoint reliability
- Response timing
- User-Agent variation
- Defensive controls
- Application-side throttling

The project is intentionally lightweight and runs directly from a terminal.

«Important: Only use this software against systems, APIs, phone numbers, and infrastructure that you own or have explicit permission to test.»

---

Features

- High-concurrency request engine
- Configurable request behavior
- Real-time terminal statistics
- HTTP request handling through "requests"
- User-Agent generation through "fake_useragent"
- Terminal banner rendering with "cfonts"
- Cross-platform Python support
- Lightweight dependency footprint
- MIT licensed

---

Supported Platforms

The project can be used anywhere Python is supported.

Platform| Supported
Windows 10 / 11| ✅
macOS| ✅
Linux| ✅
Ubuntu / Debian| ✅
Fedora| ✅
Arch Linux| ✅
WSL| ✅
Other Python-compatible systems| ✅

---

Installation

1. Install Python

Python 3.9 or newer is recommended.

Download Python from the official website:

https://www.python.org/downloads/

Verify your installation:

python --version

If your system uses "python3":

python3 --version

You should see something similar to:

Python 3.11.x

---

Windows

Clone the repository

Open PowerShell or Command Prompt:

git clone https://github.com/outwiles/sms-bomber.git
cd sms-bomber

If Git is not installed, download it from:

https://git-scm.com/download/win

Create a virtual environment

python -m venv .venv

Activate it:

.venv\Scripts\activate

Install dependencies

python -m pip install --upgrade pip
pip install -r requirements.txt

Run

python bomb.py

---

macOS

Open Terminal:

git clone https://github.com/outwiles/sms-bomber.git
cd sms-bomber

Create a virtual environment:

python3 -m venv .venv

Activate it:

source .venv/bin/activate

Install dependencies:

python3 -m pip install --upgrade pip
pip3 install -r requirements.txt

Run:

python3 bomb.py

---

Linux

Clone the repository:

git clone https://github.com/outwiles/sms-bomber.git
cd sms-bomber

Create a virtual environment:

python3 -m venv .venv

Activate it:

source .venv/bin/activate

Install dependencies:

python3 -m pip install --upgrade pip
pip3 install -r requirements.txt

Run:

python3 bomb.py

Debian / Ubuntu

If "venv" is unavailable:

sudo apt update
sudo apt install python3 python3-pip python3-venv git

Then repeat the installation steps above.

---

Dependencies

The project currently uses:

requests
fake_useragent
cfonts

They are included in:

requirements.txt

Install everything automatically with:

pip install -r requirements.txt

---

Project Structure

sms-bomber/
│
├── assets/
│   └── bomb.jpg
│
├── bomb.py
├── requirements.txt
├── LICENSE
└── README.md

"bomb.py"

Main application.

"requirements.txt"

Python dependency list.

"assets/bomb.jpg"

Project branding / logo asset.

"LICENSE"

MIT license for the project.

---

Running the Project

After installation, start the application from the repository directory:

Windows

python bomb.py

macOS / Linux

python3 bomb.py

The application runs in the terminal and provides its interactive interface and runtime statistics.

For authorized testing, configure the application so that requests are directed only toward infrastructure you control or have explicit permission to assess.

---

Virtual Environment

Using a virtual environment is recommended because it keeps the project's Python packages isolated from the rest of your system.

Create one:

python -m venv .venv

Windows:

.venv\Scripts\activate

macOS / Linux:

source .venv/bin/activate

Install dependencies:

pip install -r requirements.txt

When finished:

deactivate

---

Troubleshooting

"python" is not recognized

On Windows, try:

py --version

If that works, use:

py -m pip install -r requirements.txt
py bomb.py

Make sure Python was installed with Add Python to PATH enabled.

---

"pip" is not recognized

Use Python's module form:

python -m pip install -r requirements.txt

or:

python3 -m pip install -r requirements.txt

---

"ModuleNotFoundError"

Install the project dependencies again:

pip install -r requirements.txt

For Python 3 specifically:

python3 -m pip install -r requirements.txt

---

"fake_useragent" problems

Update the package:

pip install --upgrade fake-useragent

Then retry:

python bomb.py

---

Permission errors on Linux/macOS

Using a virtual environment is preferred over installing packages system-wide:

python3 -m venv .venv
source .venv/bin/activate
python3 -m pip install -r requirements.txt

---

Responsible Use

This project can generate repeated requests and should therefore be treated as a security/load-testing utility.

Use it only when you have authorization.

Recommended testing environments include:

- Your own development server
- A local test API
- A staging environment
- A dedicated security-testing endpoint
- Infrastructure where you have written authorization

Do not use the software to overwhelm third-party services, repeatedly trigger OTP delivery to people without their consent, bypass provider protections, or disrupt telecommunications services.

The maintainer is not responsible for misuse of this software.

---

Development

Contributions are welcome for legitimate security-testing and defensive use cases.

Useful contribution areas include:

- Better error handling
- Improved test reporting
- Safer testing modes
- Local mock SMS providers
- Test-environment configuration
- Rate-limit analysis
- Performance measurement
- Documentation
- Cross-platform improvements

Before submitting a pull request:

git pull

Make your changes, test them locally, and submit a pull request with a clear description of the change.

---

Credits

Author

Aashu / outwiles

GitHub:

https://github.com/outwiles

Repository:

https://github.com/outwiles/sms-bomber

The current project banner identifies the author as Aashu / @outwiles.

Libraries

This project uses the following open-source Python packages:

- Requests — HTTP client functionality
- fake-useragent — User-Agent generation
- cfonts — Terminal banner rendering

Their use in this project is reflected in "requirements.txt".

---

License

This project is licensed under the MIT License.

See ""LICENSE"" (LICENSE) for the complete license text.

Copyright © 2026 outwiles

---

Disclaimer

This software is provided for authorized development, testing, research, and educational purposes.

You are responsible for ensuring that your use of this software complies with applicable laws, regulations, service-provider policies, and the authorization granted by the systems or organizations you test.

The author does not endorse unauthorized traffic generation, harassment, service disruption, or abuse of third-party SMS/OTP infrastructure.

---

<div align="center">Built by outwiles

⭐ If this project is useful for legitimate security testing, consider starring the repository.

</div>
