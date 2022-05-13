# Serve

Serves the current directory via http.

## Prerequisites

- You need `python3` for this (or `python2`, if you are retro)
- This script is built for Debian-ish systems (Debian, Ubuntu, Kali, ...)

## Installation

Copy the script to your `/usr/local/bin` directory.

Do not forget to `chmod +x /usr/local/bin/serve` if needed.

## Usage

TLDR:

```shell
# Go to the directory you want to serve
$ cd ~/Documents

# Start serving
~/Documents$ serve
```

### Port 80

To serve a directory on port 80:

```shell
$ sudo serve
Serving the following:
image.png  textfile.txt  somethingelse.dat
Serving on the following addresses:
 - 192.168.0.14                        http://192.168.0.14:80/
 - 10.0.0.3                            http://10.0.0.3:80/
Serving on port 80...
Serving HTTP on 0.0.0.0 port 80 (http://0.0.0.0:80/) ...
```

### Different port

To serve a directory on a different port:

```shell
$ sudo serve 8080
Serving the following:
image.png  textfile.txt  somethingelse.dat
Serving on the following addresses:
 - 192.168.0.14                        http://192.168.0.14:8080/
 - 10.0.0.3                            http://10.0.0.3:8080/
Serving on port 8080...
Serving HTTP on 0.0.0.0 port 8080 (http://0.0.0.0:8080/) ...
```

> Reminder: using privileged portnumbers (< 1024) will probably require superpowers (eg `sudo`).
