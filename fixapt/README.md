# Fix APT

Tries to fix your local apt.

This script:

- Kills hanging apt instances
- Removes remaining apt locks while apt is already terminated
- Fix packages
  - Broken during installation
  - Corrupted files managed by apt
  - Deleted files managed by apt
- Cleans up apt environment (removes unused stuff lying around)

## Prerequisites

- This script is built for Debian-ish systems (Debian, Ubuntu, Kali, ...)
- This script will automatically install the `debsums` package during run

## Installation

Copy the script to your `/usr/local/bin` directory.

Do not forget to `chmod +x /usr/local/bin/fixapt` if needed.

## Usage

> WARNING: It is unsafe to just run some script from the internet with `sudo`: make sure you uderstand its contents!

Start fixing apt:

```shell
$ sudo fixapt
```
