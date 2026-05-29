# zip-password-cracker
A Python script designed to brute-force password-protected ZIP archives using a dictionary attack, built during the Forage AIG Cybersecurity Simulation.

# ZIP Archive Brute-Force Simulator

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
