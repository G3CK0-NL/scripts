# QR

Script that can:

- Generate a QR code from its arguments
- Generate a QR code from the clipboard content
- TODO: Scan a QR code and put the text on the clipboard and stdout

## Prerequisites

- You need the packages `qrencode` (for QR encoding) and `xsel` (for clipboard access):
  
  ```shell
  sudo apt install -y qrencode xsel
  ```

- This script is built for Debian-ish systems (Debian, Ubuntu, Kali, ...)

## Installation

Copy the script to your `/usr/local/bin` directory.

Do not forget to `chmod +x /usr/local/bin/qr` if needed.

## Usage

To create a QR code from arguments:

```shell
$ qr This text will end up in the QR code
# QR code will be displayed by the default image viewer.
```

Or create a QR code from the clipboard:

```shell
# Copy some text
$ qr
# QR code will be displayed by the default image viewer.
```
