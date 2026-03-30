🔥 Penetration Testing Toolkit 🔥
COMPANY: CODETECH IT SOLUTIONS

NAME: THEJASWI 

INTERN ID: CT1S6581 

DOMAIN: CYBER SECURITY & ETHICAL HACKING

DURATION: 8 WEEKS

🚀 Overview
Welcome to the Python-based modular penetration testing toolkit—your go-to solution for ethical hacking and security testing. Designed for professionals and cybersecurity enthusiasts, this toolkit provides a robust set of modules for network scanning, brute-force attacks, and vulnerability assessment.
⚡ Key Features
✅ Port Scanner – Discover open ports on a target system effortlessly.
✅ Brute-Force Attack – Automate login attacks using a dictionary-based approach.
✅ Vulnerability Scanner – Detect SQL Injection and Cross-Site Scripting (XSS) vulnerabilities.
✅ Utility Functions – Validate IP addresses and enhance testing accuracy.
🛠️ Installation
Ensure you have Python installed (version 3.x recommended) and install the required dependencies:

pip install -r requirements.txt

🎯 Usage Guide
Easily run penetration tests using command-line arguments:

🔍 1. Port Scanning
Scan for open ports within a specific range:

python main.py scan --start <start_port> --end <end_port>

Example:
python main.py scan 192.168.1.1 --start 20 --end 100

🔑 2. Brute-Force Attack
Test login credentials with a password list:

python main.py brute <password_file>

Example:
python main.py brute http://example.com/login admin passwords.txt

🛡️ 3. Vulnerability Scanning
Scan for SQL Injection and XSS vulnerabilities:

python main.py vuln

Example:
python main.py vuln http://example.com/search query

📂 Project Structure
📦 toolkit/ ├── init.py

├── port_scanner.py

├── brute_forcer.py

├── vulnerability_scanner.py

├── utils.py

📜 main.py

📜 requirements.txt

📂 tests/ ├── test_brute_forcer.py

├── test_port_scanner.py

├── test_utils.py

✅ Running Tests
Run unit tests to ensure functionality:

pytest

🤝 Contributing
We welcome contributions! Fork the repo, create a feature branch, and submit a pull request. Report bugs or suggest features via GitHub Issues.

⚠️ Disclaimer
🚨 This toolkit is for educational and ethical hacking purposes only. Unauthorized or malicious use is strictly prohibited and may lead to legal consequences.

📜 License
This project is open-source and licensed under the MIT License. Feel free to use and modify it for ethical hacking and research purposes.

🔥 Stay ethical, hack responsibly, and secure the digital world! 🔥
OUTPUT:
1. Port Scanner
Command: python main.py scan 127.0.0.1 --start 1 --end 1024

Output: Scanning ports: 100%|████████████████████████████████████████| 1024/1024 [00:10<00:00, 100.00 ports/s] Open ports: [22, 80, 443]

2. Brute Forcer
Command: python main.py brute http://example.com/login admin passwords.txt

Output: Trying password: password123 Trying password: admin123 Login successful: ('admin', 'admin123')

3. Vulnerability Scanner
Command: python main.py vuln http://example.com/search?query=test query

Output: Testing for SQL Injection... SQL Injection vulnerability found!

Testing for XSS... XSS vulnerability found!

4. Error Handling
Example: Invalid IP Address

Command: python main.py scan invalid_ip --start 1 --end 100

Output: Invalid IP address

5. Progress Bar (Port Scanner with tqdm)
Command: python main.py scan 127.0.0.1 --start 1 --end 1024

Output: Scanning ports: 100%|████████████████████████████████████████| 1024/1024 [00:10<00:00, 100.00 ports/s] Open ports: [22, 80, 443]

6. Colored Output
Example: Successful Login

Command: python main.py brute http://example.com/login admin passwords.txt

Output: Trying password: password123 Trying password: admin123 Login successful: ('admin', 'admin123') # This line will be green

Example: Failed Login
Command: python main.py brute http://example.com/login admin wrong_passwords.txt

Output: Trying password: wrong1 Trying password: wrong2 Login failed # This line will be red

7. Reporting
Example: JSON Report

Command: python main.py scan 127.0.0.1 --start 1 --end 1024 --format json

Output: json Copy { "target": "127.0.0.1", "open_ports": [22, 80, 443], "timestamp": "2023-10-15T12:34:56Z" }

8. Unit Tests
Command: python -m pytest tests/

Output: ============================= test session starts ============================= collected 3 items

tests/test_port_scanner.py . [ 33%] tests/test_brute_forcer.py . [ 66%] tests/test_utils.py . [100%]

============================== 3 passed in 0.05s ==============================

9. Interactive Shell Mode
Command: python main.py shell

Output: Welcome to the Penetration Testing Toolkit shell! Type 'help' for a list of commands.

scan 127.0.0.1 --start 1 --end 1024 Scanning ports: 100%|████████████████████████████████████████| 1024/1024 [00:10<00:00, 100.00 ports/s] Open ports: [22, 80, 443]

brute http://example.com/login admin passwords.txt Trying password: password123 Trying password: admin123 Login successful: ('admin', 'admin123')

exit Goodbye!
