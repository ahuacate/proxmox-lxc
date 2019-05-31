# Proxmox-LXC
LXC Container Builds
## LXC Installs
### 1. PiHole LXC Container - CentOS7
Deploy an LXC container using the CentOS7 proxmox lxc template image:

| Option | Node 1 Value |
| :---  | :---: |
| `CT ID` |100|
| `Hostname` |pihole|
| `Unprivileged container` | ☑ |
| `Template` |centos-7-default_****_amd|
| `Storage` |typhoon-share-01|
| `Disk Size` |8 GiB|
| `CPU Cores` |2|
| `Memory (MiB)` |1024|
| `Swap (MiB)` |512|
| `IPv4/CIDR` |192.168.1.254/24|
| `Gateway` |192.168.1.5|

Using the proxmox LXC `pihole` instance web interface cli install pihole:
`curl -sSL https://install.pi-hole.net | bash`

### 2. OpenVPN Gateway LXC - CentOS7
Deploy an LXC container using the CentOS7 proxmox lxc template image:

| Option | Node 1 Value |
| :---  | :---: |
| `CT ID` |253|
| `Hostname` |vpn-gateway|
| `Unprivileged container` | ☐  (must be be privileged)|
| `Template` |centos-7-default_****_amd|
| `Storage` |typhoon-share-01|
| `Disk Size` |8 GiB|
| `CPU Cores` |1|
| `Memory (MiB)` |2048|
| `Swap (MiB)` |512|
| `IPv4/CIDR` |192.168.1.253/24|
| `Gateway` |192.168.1.5|

Using the proxmox LXC `vpn-gateway` instance web interface cli install openvpn and configure.