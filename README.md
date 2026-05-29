![Python](https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python)
![Cybersecurity](https://img.shields.io/badge/Focus-Cybersecurity-red?style=for-the-badge)
![Platform](https://img.shields.io/badge/Simulation-Forage%20%7C%20AIG-darkgreen?style=for-the-badge)
# zip-password-cracker
A Python script designed to brute-force password-protected ZIP archives using a dictionary attack, built during the Forage AIG Cybersecurity Simulation.

> [!WARNING]
> **Educational Disclaimer:** This tool is developed strictly for educational and professional development purposes. Running brute-force attacks against networks or files without explicit prior authorization is illegal. This project was developed within a controlled simulation environment. It is intended to showcase vulnerabilities associated with weak file passwords and highlight the necessity of strong, complex encryption keys.

## ZIP Archive Brute-Force Simulator
This project is a functional Python command-line tool designed to perform a dictionary-based brute-force attack on password-protected ZIP files. I developed this script as part of the **Forage AIG Cybersecurity Job Simulation** to understand how automated scripts crack weak file encryption.

##  Features
- **Dictionary Attack Logic:** Iterates systematically through a pre-defined password list (`rockyou.txt`).
- **Error Handling:** Uses robust `try/except` blocks to handle incorrect password exceptions natively through the Python `zipfile` library without crashing.
- **Efficient Termination:** Automatically stops and exits immediately upon finding the correct key to save computational resources.

##  How It Works
The script utilizes a helper function to attempt file extraction:
- If `extractall()` succeeds, it returns `True`, prints the discovered password, and breaks the loop.
- If it throws a `RuntimeError` (wrong password), it gracefully catches the error, returns `False`, and moves to the next line in the text file.

##  Prerequisites & Setup
To run this project locally, ensure you have Python 3.x installed.

1. Clone this repository:
   ```bash
   git clone [https://github.com/thunder0308/zip-password-cracker.git](https://github.com/thunder0308/zip-password-cracker.git))
2. Place your target encrypted ZIP file (enc.zip) and your password dictionary list (rockyou.txt) into the same directory as the script.
   (You can get rockyou.txt file from the internet)
3. Run the script:
   ```bash
   python bruteforce.py

##  Future Enhancements
- [ ] **Multi-threading:** Upgrade the script to test multiple passwords simultaneously to increase cracking speed.
- [ ] **Argument Parsing:** Implement the `argparse` library so users can pass the ZIP file and wordlist paths directly via the command line (e.g., `python bruteforce.py -z enc.zip -w list.txt`).
- [ ] **Progress Bar:** Add a visual terminal progress bar using `tqdm` to show extraction speed and ETA.
