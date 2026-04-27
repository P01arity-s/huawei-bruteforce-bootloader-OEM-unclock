--------- Features
Adaptive Rate Limiting: Automatically adjusts request timing based on device response to bypass basic anti-brute-force triggers.

Multi-Protocol Support: Modular design for testing HTTP/HTTPS, SSH, or Serial interfaces.

Session Management: Saves progress to allow for pauses and resumes in long-running audits.

Custom Wordlist Integration: Optimized for common Huawei default credential patterns.

🛠 Prerequisites
Before running the script, ensure you have the following installed:

Python 3.9+

Required Libraries:

Bash
pip install requests paramiko colorama
📂 Project Structure
Plaintext
├── src/
│   ├── modules/          # Protocol-specific logic (SSH, Web, etc.)
│   └── utils/            # Logging and wordlist parsers
├── wordlists/            # Target credential lists
├── main.py               # Entry point
└── requirements.txt      # Dependencies
⚙️ Usage
Clone the repository:

Bash
git clone https://github.com/username/huawei-bruteforce.git
cd huawei-bruteforce
Configure your target:
Edit the config.yaml or pass arguments via CLI:

Bash
python main.py --target 192.168.1.1 --protocol web --wordlist wordlists/default_huawei.txt
Execution:
The tool will begin iterating through the wordlist. If a match is found, it will be logged to results.txt.

🛡 Mitigation Recommendations
If you are a device administrator, protect your hardware by:

Disabling unused management interfaces (Telnet/SSH) on the WAN side.

Enabling Account Lockout Policy (e.g., lock for 30 minutes after 3 failed attempts).

Using complex, non-default passwords for all administrative accounts.

📄 License
Distributed under the MIT License. See LICENSE for more information.
