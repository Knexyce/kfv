# kfv_bash

**Warning: This script contains code with malicious intent and must be used responsibly. Running this script can cause severe damage to systems, including crashes and data loss.**

## Overview

`kfv_bash` is a Python script that demonstrates the behavior of fork bombs and other resource-exhaustion exploits. It is intended for educational and research purposes only, to understand how such attacks work and how to defend against them.

**Do not run this script on production systems or without explicit consent from the system owner.**

## Features

- Executes multiple forms of fork bombs using Bash, Python, and Perl.
- Attempts to clear the terminal screen to obscure the activity.
- Demonstrates the impact of resource exhaustion on a system.

## Usage

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/kfv_bash.git
   cd kfv_bash
   ```

2. Run the script:
   ```bash
   python kfv_bash.py
   ```

   **Important:** Only run this script in a controlled environment, such as a virtual machine or container, where system resources can be limited and monitored.

## How It Works

- **Screen Clearing**: The `clear_screen` function attempts to clear the terminal using various methods (`cls`, `clear`, `tput clear`, etc.).
- **Fork Bombs**: The `virus` function launches multiple forms of fork bombs:
  - Bash fork bomb: `:(){ :|:& };:`
  - Recursive Python forking: `os.fork()`
  - Perl fork bomb: `perl -e 'fork while fork'`
- **Loop Execution**: The script repeatedly executes these behaviors in a loop.

## Educational Purpose Only

This script is strictly for demonstrating the behavior of malicious scripts in a safe and controlled environment. It should never be used with malicious intent or on systems without prior consent.

## Disclaimer

The authors of this script are not liable for any damages resulting from the misuse of this code. By using this script, you agree to take full responsibility for your actions.

## Resources

- [Understanding Fork Bombs](https://en.wikipedia.org/wiki/Fork_bomb)
- [Ethical Hacking Guidelines](https://www.eccouncil.org/what-is-ethical-hacking/)
