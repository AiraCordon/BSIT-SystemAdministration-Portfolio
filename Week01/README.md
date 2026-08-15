# Week 1 – Building My Professional Environment

## Student Information
* **Name:** Dimples Aira Cordon
* **Course:** BS Information Technology
* **Section:** 4D
* **Date:** August 15, 2026

# Objectives
* Set up a complete local development and system administration environment.
* Establish professional digital profiles for collaboration and career development.
* Identify and troubleshoot common software installation issues independently.

---

# Software Installed
* **Visual Studio Code / IDE:** Code editor for scripting and documentation.
* **Git:** Version control system for tracking code changes.
* **VirtualBox / VMware:** Virtualization software to run virtual machines.
* **Linux OS (e.g., Ubuntu Server/Desktop):** Target operating system for system administration tasks.
* **Terminal Emulator / PuTTY:** Tools for command-line access and SSH connections.

---

# Professional Accounts
* **GitHub:** https://github.com/AiraCordon
* **LinkedIn:** https://www.linkedin.com/in/cordon-dimples-aira-m-4234443a9/

---

# Challenges Encountered

1. **Virtualization Disabled in BIOS (VT-x/AMD-V)**
   * **Problem:** VirtualBox failed to launch a 64-bit Linux virtual machine, returning a hardware virtualization error.
   * **Solution:** Restarted the host computer, entered the BIOS/UEFI settings menu, enabled Intel VT-x / AMD-V virtualization technology, saved the settings, and rebooted into the host OS.

2. **Git Path Configuration in Windows Terminal**
   * **Problem:** Running `git` commands in the default Windows Command Prompt resulted in a `'git' is not recognized` error.
   * **Solution:** Reinstalled Git and ensured the option *"Add Git to PATH"* was selected during installation, or manually added `C:\Program Files\Git\cmd` to the system environment variables.

3. **SSH Key Authentication Failure on GitHub**
   * **Problem:** Permission was denied when attempting to push code or connect to GitHub via the terminal using SSH.
   * **Solution:** Generated a new SSH key pair using `ssh-keygen -t ed25519`, added the public key (`.pub`) to GitHub Account Settings under *SSH and GPG keys*, and tested the connection via `ssh -T git@github.com`.

---

# Reflection
Setting up a dedicated professional environment during this first week provided a foundational understanding of the tools essential for modern system administration. Installing virtualization software, configuring a command-line environment, and establishing version control accounts revealed how critical proper setup is to ensuring workflow stability and security. Beyond simply downloading tools, configuring software requires understanding system requirements, environment variables, and authentication mechanisms.

These tools directly support my growth as a future System Administrator by mirroring standard industry practices. Virtualization allows me to test server configurations, manage operating systems, and simulate network setups safely within an isolated environment without risking host system failure. Tools like Git and GitHub instill the discipline of version control and configuration management, which are critical for tracking changes to infrastructure scripts and collaborating effectively with administrative teams. Establishing these habits early ensures I build reliable, scalable, and well-documented systems throughout my professional career.

---

# References
* **Git Official Documentation:** https://git-scm.com/doc
* **Oracle VM VirtualBox User Manual:** https://www.virtualbox.org/manual/
* **Ubuntu Server Documentation:** https://ubuntu.com/server/docs
* **GitHub Docs:** https://docs.github.com/
