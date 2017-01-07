## home-router-config

Build configuration used for my home router (please note this is still a work in progress).

Configuration is installed on top of [Ubuntu 16.04](http://releases.ubuntu.com/16.04/) (Xenial Xerus).

[This article](http://arstechnica.com/gadgets/2016/04/the-ars-guide-to-building-a-linux-router-from-scratch/) was the inspiration for creating and configuring my own home router.

### Installing

1. Purchase or build a PC which has two NICs. For my build, I went with:
 - ASUS H110T/CSM H110 Thin Mini-ITX CSM Motherboard (Dual gigabit NICs)
 - Intel 3.70 GHz Core i3-6100 3M Cache Processor
 - Crucial 32GB Kit (16GBx2) DDR4 2133 MT/s (PC4-17000) SODIMM 260-Pin Memory
 - Transcend 128GB SATA III 6Gb/s MTS400 42 mm M.2 SSD Solid State Drive

2. [Download and install](http://releases.ubuntu.com/16.04/) the latest release for Ubuntu 16.04.
Choosing the server package is preferred to avoid installing any desktop components (such as Unity).

3. Run the following to get started:

```sh
sudo apt install -y vim git isc-dhcp-server unzip openvpn && sudo apt remove -y vim-tiny nano
sudo apt update && sudo apt upgrade -y
git clone git@github.com:bsclifton/home-router-config.git
cd home-router-config/
#TODO: ...
cp -rp ./etc /etc/
```

### About this configuration

- This config uses iptables for NAT and filtering.
- sshd_config is updated to remove root login and to disallow login w/ password.

