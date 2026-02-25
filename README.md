# Environment Setup Guide

This document describes how to download and install Quartus 25.1.1 and the required ARM GCC toolchain.

---

## Download

### 1. Quartus

Download the installer file from following link:

- https://www.altera.com/downloads/fpga-development-tools/quartus-prime-pro-edition-design-software-version-25-1-1-linux

Download patch file for Quartus 25.1.1:

- `quartus-25.1.1-1.03-linux.run`

### 2. GCC ARM Toolchain

Download the GCC toolchain from the following link:

- https://www.dropbox.com/scl/fi/dtlzq2qgbaiu7in9k3oy5/gcc-arm-11.2-2022.02-x86_64-aarch64-none-linux-gnu.tar.xz?rlkey=f1tznivjb64p1bvmdauzs5x9b&st=h4biecg6&dl=0

---

## Installation

### 1. Install Quartus

1. Make the installer and patch executable:

```bash
chmod +x qinst-linux-25.1.1-125.run
```

```bash
chmod +x quartus-25.1.1-1.03-linux.run
```

2. Run the installer:

```bash
./qinst-linux-25.1.1-125.run
```

3. Create the installation directory:

```bash
mkdir -p /opt/pkg/altera_pro/25.1.1
```

4. During installation, set the destination path to:

```
/opt/pkg/altera_pro/25.1.1
```
5. Run the patch:

```bash
./quartus-25.1.1-1.03-linux.run
```

---

### 2. Install GCC ARM Toolchain

1. Decompress the `.xz` file:

```bash
xz -d gcc-arm-11.2-2022.02-x86_64-aarch64-none-linux-gnu.tar.xz
```

2. Create the toolchain directory:

```bash
mkdir -p /opt/pkg/gcc-arm-toolchain
```

3. Navigate to the toolchain directory:

```bash
cd /opt/pkg/gcc-arm-toolchain
```

4. Extract the tar file:

```bash
tar xvf <path-to>/gcc-arm-11.2-2022.02-x86_64-aarch64-none-linux-gnu.tar
```

---

## Notes

- You may need `sudo` privileges to install under `/opt`.
- Replace `<path-to>` with the actual directory where the tar file is located.
- Ensure enough disk space is available before installation.
