
# Wireshark Installation Guide for Ubuntu

## Installation Steps

### 1. Update and Upgrade the System
Before installing any software, ensure your system is updated:

```bash
sudo apt update
sudo apt upgrade -y
```

### 2. Install Wireshark
Run the following command to install Wireshark:

```bash
sudo apt install wireshark -y
```

### 3. Configure Non-Root Access (Optional)
During installation, you'll see the prompt:

> **"Should non-superusers be able to capture packets?"**

- Select **Yes** if you want non-root users to capture packets.
- If you selected **No** or skipped this step, reconfigure it later using:

```bash
sudo dpkg-reconfigure wireshark-common
```

Then, add your user to the `wireshark` group:

```bash
sudo usermod -aG wireshark $USER
```

To apply group changes, log out and log back in.

### 4. Verify Installation
Check if Wireshark is successfully installed:

```bash
wireshark --version
```

### 5. Run Wireshark
To launch Wireshark, use either of these methods:
- From the terminal:

```bash
wireshark
```

- Search for **Wireshark** in the application menu.

### Optional: Installing the Latest Version
To install the latest version of Wireshark:

1. Add the official Wireshark PPA:

```bash
sudo add-apt-repository ppa:wireshark-dev/stable
sudo apt update
```

2. Install Wireshark:

```bash
sudo apt install wireshark -y
```

### 6. Uninstall Wireshark (if needed)
If you need to remove Wireshark:

```bash
sudo apt remove wireshark wireshark-common -y
```

