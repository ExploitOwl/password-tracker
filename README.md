Loki Don't Trust You Dude — Password Vault
Overview
Loki Don't Trust You Dude is a secure password vault application written in Python. It uses strong encryption (Fernet symmetric encryption) to protect your saved credentials behind a master password. The program features a simple graphical user interface (GUI) built with Tkinter for easy password management.

Features
Encrypts password entries locally using a master password

Stores passwords securely in an encrypted file (loki_secret_stash.enc)

GUI for adding, viewing, and saving passwords

Protects your data with a salt-based key derivation function

Fun easter egg: If the wrong master password is entered, a spinning skull image appears!

Installation Requirements
Python 3.7 or higher

cryptography package (pip install cryptography)

tkinter (usually included with Python)

Setup
Clone this repository:

bash
Copy
Edit
git clone https://github.com/yourusername/loki-password-vault.git
cd loki-password-vault
Install the required packages:

bash
Copy
Edit
pip install cryptography
Run the vault app:

bash
Copy
Edit
python loki_dont_trust_you_dude.py
Usage
On launch, enter your master password to unlock the vault.

If you enter the wrong master password, the app shows a spinning skull as a fun warning.

Add new entries by specifying the site, username, password, and security tier.

Password entries are saved encrypted and can only be accessed with the correct master password.

File Structure
File	Description
loki_dont_trust_you_dude.py	Main Python script running the vault GUI and encryption logic
loki_secret_stash.enc	Encrypted vault file storing your password data
vault_salt.bin	Salt used for key derivation to ensure encryption security
skull.png	Image used in the GUI (including the skull easter egg)

Security Notes
Your master password is never stored in plain text; it’s used to derive the encryption key.

Salt ensures that even if the master password is weak, encryption remains strong against common attacks.

Keep your salt file and encrypted vault safe and backed up.

Future Improvements
Add password generator tool for creating strong passwords

Implement backup and restore features

Enhance GUI usability and aesthetics

Support for exporting and importing encrypted vault data

About
This project is part of my self-guided learning in cybersecurity and Python programming. It reflects the real-world challenges of building secure applications beyond classroom theory.

