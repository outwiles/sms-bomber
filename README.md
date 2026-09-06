<div align="center">

<img src="assets/logo.png" alt="CurlToCode" width="520">

# CurlToCode

### Universal cURL-to-Code Converter

Convert cURL commands into clean, ready-to-use code across **32 languages and request formats**.

[![Python](https://img.shields.io/badge/Python-3.9%2B-blue?style=for-the-badge&logo=python)](https://www.python.org/)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)
[![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20Linux%20%7C%20macOS%20%7C%20Android-lightgrey?style=for-the-badge)](#installation)

</div>

---

## Overview

**CurlToCode** is a lightweight command-line cURL-to-code converter. Paste a cURL command, select a target, and CurlToCode generates an equivalent request in the selected language or format.

It parses common request components including:

- HTTP method
- URL
- Query parameters
- Headers
- Cookies
- Authentication headers
- Form data
- Request bodies

Everything is processed locally. CurlToCode does not require a hosted conversion service.

## Features

- Interactive terminal interface
- 32 output targets
- cURL command parsing
- HTTP method and URL extraction
- Header handling
- Cookie handling
- Authentication handling
- Form-data and request-body support
- Local processing
- Lightweight Python implementation
- Cross-platform design
- Works with Windows, Linux, macOS, Termux and Android Python environments

## Supported Output Targets

| # | Target |
|---:|---|
| 1 | Python Requests |
| 2 | Python `http.client` |
| 3 | Python Requests |
| 4 | Go `net/http` |
| 5 | Ruby Net::HTTP |
| 6 | PHP Guzzle |
| 7 | PHP cURL |
| 8 | C# HttpClient |
| 9 | Java HttpClient |
| 10 | Node.js `http` |
| 11 | JavaScript Axios |
| 12 | JavaScript Fetch |
| 13 | TypeScript Fetch |
| 14 | Python aiohttp |
| 15 | Elixir Req |
| 16 | JavaScript jQuery |
| 17 | Java OkHttp |
| 18 | C# RestSharp |
| 19 | C++ libcurl |
| 20 | C libcurl |
| 21 | Rust reqwest |
| 22 | Kotlin OkHttp |
| 23 | Swift URLSession |
| 24 | Dart http |
| 25 | R httr2 |
| 26 | Lua LuaSocket |
| 27 | Perl HTTP::Tiny |
| 28 | PowerShell |
| 29 | Wget |
| 30 | Bash curl |
| 31 | Raw HTTP |
| 32 | JSON |

## Requirements

- Python 3.9 or newer
- pip
- Git is recommended for cloning
- A terminal for the full interactive experience

## Installation

### Windows

```powershell
git clone https://github.com/outwiles/CurltoCode.git
cd CurltoCode
py -m pip install -r requirements.txt
py main.py
```

If `py` is unavailable:

```powershell
python -m pip install -r requirements.txt
python main.py
```

### Linux

```bash
git clone https://github.com/outwiles/CurltoCode.git
cd CurltoCode
python3 -m pip install -r requirements.txt
python3 main.py
```

### macOS

```bash
git clone https://github.com/outwiles/CurltoCode.git
cd CurltoCode
python3 -m pip install -r requirements.txt
python3 main.py
```

### Termux

```bash
pkg update
pkg install python git
git clone https://github.com/outwiles/CurltoCode.git
cd CurltoCode
python -m pip install -r requirements.txt
python main.py
```

### Android / PyDroid

Install Python through your Android Python environment, then copy or clone the project.

```bash
python -m pip install -r requirements.txt
python main.py
```

The converter logic is standard Python. Terminal-specific visual effects can vary depending on the Android terminal environment.

## Usage

Start CurlToCode:

```bash
python main.py
```

On macOS or Linux:

```bash
python3 main.py
```

Choose the desired output target and provide a cURL command.

Example:

```bash
curl 'https://example.com/api' -H 'Accept: application/json' -H 'Authorization: Bearer TOKEN' -d 'name=Aashu'
```

CurlToCode parses the request and generates the corresponding code for the selected target.

## How It Works

1. The cURL command is parsed into its individual components.
2. The request data is normalized into an internal structure.
3. The selected generator converts that structure into the requested language or format.
4. The generated result is displayed locally in the terminal.

No remote conversion server is required.

## Project Structure

```text
CurlToCode/
├── assets/
│   └── logo.png
├── curl_to_code/
│   ├── __init__.py
│   ├── core.py
│   └── generators.py
├── main.py
├── requirements.txt
├── README.md
└── LICENSE
```

## Dependencies

Dependencies are listed in `requirements.txt`.

```bash
python -m pip install -r requirements.txt
```

On macOS/Linux:

```bash
python3 -m pip install -r requirements.txt
```

## Troubleshooting

### `ModuleNotFoundError`

```bash
python -m pip install -r requirements.txt
```

### Python is not recognized on Windows

```powershell
py --version
py -m pip install -r requirements.txt
py main.py
```

### `cfonts` is missing

```bash
python -m pip install -r requirements.txt
```

### Terminal styling looks different

Terminal rendering depends on the terminal emulator and operating system. ANSI styling and cfonts output may appear slightly different between terminals while the converter itself remains usable.

## Security and Privacy

CurlToCode processes the supplied cURL command locally.

Be careful when sharing cURL commands or generated code containing:

- API keys
- Bearer tokens
- Session cookies
- Passwords
- Private URLs
- Other credentials

Remove or replace sensitive values before publishing commands or generated output.

## License

CurlToCode is released under the **MIT License**.

See [`LICENSE`](LICENSE) for the complete license text.

## Credits

### Author

**Aashu**

GitHub: [@outwiles](https://github.com/outwiles)

Repository: [CurlToCode](https://github.com/outwiles/CurltoCode)

---

<div align="center">

**CurlToCode — Turn cURL into code.**

</div>
