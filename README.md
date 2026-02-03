# Android-Forensic-Extraction-Analysis

Project Overview
This project demonstrates a logical forensic extraction of an Android mobile device using the Andriller CE framework on a Kali Linux environment. The goal was to retrieve critical forensic artifacts while maintaining data integrity and troubleshooting environment-specific dependencies.

🛠️ Technical Stack
Operating System: Kali Linux 2026 (via VMware workstation)
Tools: Andriller CE 3.6.3, ADB (Android Debug Bridge)
Language: Python 3.13
Key Libraries: Jinja2 (Legacy support), MarkupSafe, PyCryptodome

🚀 Challenges & Troubleshooting
During the setup, I encountered and resolved several real-world technical hurdles:
Dependency Conflicts: Resolved AttributeError: module 'jinja2' has no attribute 'evalcontextfilter' by downgrading to compatible legacy versions.
Environment Security (PEP 668): Managed Python packages using a Virtual Environment (venv) to comply with Debian/Kali's externally managed environment policies.
Linux Permissions: Fixed Permission Denied errors on extracted forensic folders by modifying directory ownership and permissions via chmod.

📋 Investigation Workflow
Device Preparation: Enabled USB Debugging and handled "Full Backup" prompts on the target Android device.
Data Acquisition: Performed logical extraction including:
Linked Accounts (Google, Social Media)
System Metadata and Device Identification
Application Lists
Report Generation: Decoded raw backup data into a human-readable HTML forensic report.

📊 Results
The extraction successfully generated a detailed report containing:
Account Forensics: Identified 10+ synced accounts including Gmail, Telegram, and Microsoft.
Device Info: Captured Serial ID, Wi-Fi MAC, and accurate device timestamps.
Storage Analysis: Decoded shared storage structures for further file system analysis.

![](/assets/Extraction.png)
![](/assets/Completed.png)
![](/assets/Report.png)
⚠️ Disclaimer
This project was performed for educational purposes on a personal device with full consent. No unauthorized data was accessed
