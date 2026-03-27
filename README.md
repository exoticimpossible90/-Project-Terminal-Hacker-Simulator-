# -Project-Terminal-Hacker-Simulator-
🚀 Fitur Animasi teks ala hacker Progress loading Fake akses server Random success / fail Warna terminal (biar keliatan pro)

🧠 Kodenya (Python)
import time
import random
import sys
import os

# warna terminal
GREEN = "\033[92m"
RED = "\033[91m"
YELLOW = "\033[93m"
CYAN = "\033[96m"
RESET = "\033[0m"

def typing(text, delay=0.03):
    for char in text:
        sys.stdout.write(char)
        sys.stdout.flush()
        time.sleep(delay)
    print()

def loading_bar():
    for i in range(0, 101, 5):
        sys.stdout.write(f"\r{CYAN}Loading: {i}%{RESET}")
        sys.stdout.flush()
        time.sleep(0.1)
    print("\n")

def fake_hack():
    targets = ["NASA Server", "Bank Database", "Government Files", "Private Network"]
    target = random.choice(targets)

    typing(f"{GREEN}[+] Target Locked: {target}{RESET}")
    time.sleep(1)

    typing(f"{YELLOW}[*] Bypassing security...{RESET}")
    loading_bar()

    typing(f"{YELLOW}[*] Injecting payload...{RESET}")
    loading_bar()

    typing(f"{YELLOW}[*] Cracking password...{RESET}")
    loading_bar()

    result = random.choice(["SUCCESS", "FAILED"])

    if result == "SUCCESS":
        typing(f"{GREEN}[✔] Access Granted!{RESET}")
    else:
        typing(f"{RED}[✖] Access Denied! Firewall detected.{RESET}")

def banner():
    print(f"""{CYAN}
██╗  ██╗ █████╗  ██████╗██╗  ██╗███████╗██████╗ 
██║  ██║██╔══██╗██╔════╝██║ ██╔╝██╔════╝██╔══██╗
███████║███████║██║     █████╔╝ █████╗  ██████╔╝
██╔══██║██╔══██║██║     ██╔═██╗ ██╔══╝  ██╔══██╗
██║  ██║██║  ██║╚██████╗██║  ██╗███████╗██║  ██║
╚═╝  ╚═╝╚═╝  ╚═╝ ╚═════╝╚═╝  ╚═╝╚══════╝╚═╝  ╚═╝
{RESET}""")

def main():
    os.system("cls" if os.name == "nt" else "clear")
    banner()
    typing(f"{CYAN}Initializing hacking system...{RESET}")
    time.sleep(1)

    while True:
        fake_hack()
        print()
        choice = input("Run again? (y/n): ").lower()
        if choice != "y":
            typing(f"{CYAN}Exiting system...{RESET}")
            break

if __name__ == "__main__":
    main()

📦 Cara pakai
Simpan sebagai hacker_simulator.py
Jalankan: python hacker_simulator.py
    
