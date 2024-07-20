# Raptoreum Smartnode Installer

[![Codacy Badge](https://app.codacy.com/project/badge/Grade/d42502024326445786fef8ac13f3ad4b)](https://app.codacy.com/gh/lorne-rtm/smartnode-installer/dashboard?utm_source=gh&utm_medium=referral&utm_content=&utm_campaign=Badge_grade)

![License](https://img.shields.io/github/license/lorne-rtm/smartnode-installer)

*Fairly, kinda, somewhat easy Smartnode installer.*

This script takes care of Smartnode VPS setup, it needs to be run as root and only has been tested on Ubuntu 22. It should work fine on Ubuntu 20 as well.

This script is provided as is and I do not guarantee it will work for you, you use it at your own risk. If you find a bug or something broken, let me know and I will do my best to get it fixed. Here is what this script does:

- Creates a regular user (mcsmarty) and disables SSH for that user
- Updates and upgrades the OS (no dist upgrade)
- Create 4GB SWAP if needed
- Get latest release binaries and check checksums. If no match script exits.
- Creates raptoreum.conf
- Bootstrap option. If bootstrap is chosen it compares checksum with <https://checksums.raptoreum.com/checksums/bootstrap-checksums.txt/> if mismatch, script exits.
- Creates a few command aliases, saves a bit of typing.
- When synchronizing blockchain local height and explorer height are compared. Progress to next step only when local and explorer height are within 2 of each other.
- Asks for BLS.
- Checks smartnode status and if "Ready" script completes, if any other status script exits with a note.

# Script Demo

https://youtu.be/9UMpJOuXU90
