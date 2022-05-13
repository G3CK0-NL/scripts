# DefaultGW

Displays and sets the default gateway.

## Prerequisites

- This script is built for Debian-ish systems (Debian, Ubuntu, Kali, ...)

## Installation

Copy the script to your `/usr/local/bin` directory.

Do not forget to `chmod +x /usr/local/bin/defaultgw` if needed.

## Usage

TLDR:

```shell
# To show current default gateways
$ ./defaultgw

# To set the default gateway to 10.0.0.1
$ sudo ./defaultgw 10.0.0.1

# To set the default gateway to enp2s0
$ sudo ./defaultgw enp2s0
```

### Show current

See the current default gateway:

```shell
$ ./defaultgw 
Available connections:
lo               UNKNOWN        127.0.0.1/8
enp1s0           UP             192.168.0.14/24
enp2s0           UP             10.0.0.3/24
wlp1s0           DOWN           

Current default gateway(s):
default via 192.168.0.1 dev enp1s0

Use one of the following commands to change the default gateway:
    ./defaultgw <IP>
    ./defaultgw <ETH DEV>
```

### Change by IP

Change the default gateway to a different router IP:

> WARNING: It is unsafe to just run some script from the internet with `sudo`: make sure you uderstand its contents!

```shell
$ sudo ./defaultgw 10.0.0.1
Available connections:
lo               UNKNOWN        127.0.0.1/8
enp1s0           UP             192.168.0.14/24
enp2s0           UP             10.0.0.3/24
wlp1s0           DOWN           

Current default gateway(s):
default via 192.168.0.1 dev enp1s0

Deleting all current default routes...
Setting default gateway to "10.0.0.1"...
Flushing cache...

New default gateway(s):
default via 10.0.0.1 dev enp2s0 
```

### Change by device

Change the default gateway to a different ethernet device.

> NOTE: This is done by using the DNS server defined for the given interface. This works if ROUTER == DNS. YMMV...

> WARNING: It is unsafe to just run some script from the internet with `sudo`: make sure you uderstand its contents!

```shell
$ sudo ./defaultgw enp2s0
Available connections:
lo               UNKNOWN        127.0.0.1/8
enp1s0           UP             192.168.0.14/24
enp2s0           UP             10.0.0.3/24
wlp1s0           DOWN           

Current default gateway(s):
default via 192.168.0.1 dev enp1s0

Deleting all current default routes...
Determining router IP on eth device "enp2s0" (this is set to the DNS server IP - hackhack)...
Setting default gateway to "10.0.0.1"...
Flushing cache...

New default gateway(s):
default via 10.0.0.1 dev enp2s0 
```
