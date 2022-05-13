# FixVMware

Tries to fix signing problems with the `vmmon` and `vmnet` VMWare kernel modules when secure boot is enabled.

## Prerequisites

- You need VMWare Workstation installed on your system.
- This script is built for Debian-ish systems (Debian, Ubuntu, Kali, ...)

## Installation

Copy the script to your `/usr/local/bin` directory.

Do not forget to `chmod +x /usr/local/bin/fixvmware` if needed.

## Usage

> WARNING: It is unsafe to just run some script from the internet with `sudo`: make sure you uderstand its contents!

Start fixing VMWare:

```shell
$ sudo fixvmware
```
