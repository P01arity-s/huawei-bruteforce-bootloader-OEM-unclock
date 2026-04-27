# Huawei Security Research: Brute-Force Framework

A Python-based utility designed for authorized security auditing of Huawei device interfaces. This tool automates credential testing against specific interfaces to identify weak configuration patterns and improve device hardening.

> [!CAUTION]
> **Disclaimer**: This tool is for educational and authorized security testing purposes only. Usage against devices without prior explicit consent is illegal. The author assumes no liability for misuse or damage.

---

## 🥀 Features

* **Adaptive Rate Limiting**: Automatically adjusts request timing based on device response to avoid service denial.
* **Multi-Protocol Support**: Modular design for testing HTTP/HTTPS, SSH, or Serial interfaces.
* **Session Management**: Saves progress to allow for pauses and resumes in long-running audits.
* **Custom Wordlist Integration**: Optimized for common Huawei default credential patterns.

## 🛠 Prerequisites

Before running the script, ensure you have the following installed:

* **Python 3.9+**
* **Required Libraries**:
    ```bash
    pip install requests paramiko colorama
    ```

## 📂 Project Structure

```text
├── src/
│   ├── modules/          # Protocol-specific logic (SSH, Web, etc.)
│   └── utils/            # Logging and wordlist parsers
├── wordlists/            # Target credential lists
├── main.py               # Entry point
└── requirements.txt      # Dependencies
