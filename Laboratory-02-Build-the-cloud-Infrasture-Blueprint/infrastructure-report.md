# Infrastructure Report

## Operating System
- Name: <output of cat /etc/os-release, e.g. Ubuntu 22.04.x LTS>
- Kernel Version: <output of uname -r>

## Compute
- CPU Model: <output of cat /proc/cpuinfo>
- CPU Cores: <output of nproc>
- Total RAM: <output of free -h>

## Storage
- Disk Capacity: <output of df -h, main / partition size>
- Mounted File Systems: <output of findmnt or mount, list key mounts like /, /boot, /tmp>

## Networking
- Hostname: <output of hostname>
- IP Address: <output of ip a / hostname -I>