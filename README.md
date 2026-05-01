# File Integrity Checker

## Overview
This is a defensive cybersecurity tool written in **Python**. It uses the **SHA-256 hashing algorithm** to verify the integrity of files. This project demonstrates my understanding of the "Integrity" pillar of the CIA Triad (Confidentiality, Integrity, and Availability).

## How It Works
1. **Hashing:** The script reads a file and generates a unique 64-character hexadecimal string (the hash).
2. **Baseline:** A "trusted" hash is saved to a `baseline.txt` file.
3. **Verification:** The script re-calculates the hash of the target file and compares it against the baseline. If even a single character in the file changes, the hash will change, and the tool will trigger an alert.



## Features
- **Binary Reading:** Capable of hashing text files, images, and executables.
- **Chunked Processing:** Efficiently handles large files by reading them in 4KB blocks to prevent memory crashes.
- **Real-time Alerts:** Immediate console notification if a file has been tampered with.

## How to Use
1. Clone this repository to your local machine.
2. Ensure you have **Python 3.x** installed.
3. Run the script:
   ```bash
   python integrity_checker.py
