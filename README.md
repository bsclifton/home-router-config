## home-router-config

This is a configuration that I had used on my home router from 2017 until 2020. In 2020, I decomissioned my custom router in favor of Ubiquity hardware.

Also see https://github.com/bsclifton/home-config (may be out of date)

### Preface

Configuration is installed on top of [Ubuntu 16.04](http://releases.ubuntu.com/16.04/) (Xenial Xerus).

[This article](http://arstechnica.com/gadgets/2016/04/the-ars-guide-to-building-a-linux-router-from-scratch/) was the inspiration for creating and configuring my own home router.

### Installing

1. Purchase or build a PC which has two NICs. For my build, I went with:

 - <a target="_blank" href="https://www.amazon.com/gp/product/B01EZGYSGG/ref=as_li_tl?ie=UTF8&camp=1789&creative=9325&creativeASIN=B01EZGYSGG&linkCode=as2&tag=bria07-20&linkId=fed057ee21cea6ef87f1daf5870a1f26">ASUS H110T/CSM H110 Thin Mini-ITX CSM Motherboard (Dual gigabit NICs)</a>
 - <a target="_blank" href="https://www.amazon.com/gp/product/B015VPX2EO/ref=as_li_tl?ie=UTF8&camp=1789&creative=9325&creativeASIN=B015VPX2EO&linkCode=as2&tag=bria07-20&linkId=aa659fb1d3f528e99c3253a081f7783c">Intel 3.70 GHz Core i3-6100 3M Cache Processor</a>
 - <a target="_blank" href="https://www.amazon.com/gp/product/B015YPB8ME/ref=as_li_tl?ie=UTF8&camp=1789&creative=9325&creativeASIN=B015YPB8ME&linkCode=as2&tag=bria07-20&linkId=601afba52ae94577aa9291aa866d06f7">Crucial 32GB Kit (16GBx2) DDR4 2133 MT/s (PC4-17000) SODIMM 260-Pin Memory</a>
 - <a target="_blank" href="https://www.amazon.com/gp/product/B00KLTPUU0/ref=as_li_tl?ie=UTF8&camp=1789&creative=9325&creativeASIN=B00KLTPUU0&linkCode=as2&tag=bria07-20&linkId=cdcacb9780667a869d0ea28ed1c17a92">Transcend 128GB SATA III 6Gb/s MTS400 42 mm M.2 SSD Solid State Drive</a>

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

