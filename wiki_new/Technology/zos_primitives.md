# Zero-OS Primitives

## Compute and Storage 

![](img/internet4__zos_overview_compute_storage.png)

### ZMachine 

ZMachine is ThreeFold native container technology implemented in Zero-OS and is fully compatible with Docker. 

Moreover, to increase security and allow different kernels to be used, ZMachine contains a Virtual Machine (VM) Support.

Learn more about ZMachine [here](internet4:zmachine).

### CoreX

CoreX is an optional tools that allows the users to manager their ZMachine over web remotely 

### ZOS Filesystem 

ZOS Filesystem is a small database which contains metadata about files and directories and file payload are stored on a ThreeFold Grid Hub. Users only needs to download payload when they need it and thus reducing ZMachine boot time, bandwidth and disk overhead. 

Learn more about ZOS Filesystem [here](internet4:zflist).

### ZMount 

ZMount is a partition on a SSD disk and is mounted underneath the ZMachine. It is a fast storage and typically used for databases. 

### ZSTOR Filesystem 

ZSTOR is the filesystem of the ZMachine and used the quantum Safe Storage System inside. 

Learn more about Quantum Safe Storage System [here](quantumsafestorage:qss_description).








