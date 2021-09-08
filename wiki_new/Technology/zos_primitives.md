# Zero-OS Primitives

Built on top of the ThreeFold Grid, Digital Self uses lightweight and cutting edge Zero-OS primitives to create a fully autonomous and self healing system. 

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

### Zero-DB 

Being built underneath the Blockchain Database (BCDB), the Zero-DB is a key-value store using “always write”, which allows history tracking, rollback features out-of-box, and ensures data consistency and improves performance. It will also be a key component for the Blockchain Database to know if the Digital Self has updated its access right.

With the help of the Zero-DB, BCDB stores immutable data in an append-only fashion, implying that it is used to store metadata locally, such as access right in relation to the Digital Self. 

### ZDisk 

Virtual Disk creates the possibility to create and use virtual disks which can be attached to containers (and virtual machines). 

The technology is designed to be redundant without having to do anything. 

## Network 

![](img/internet4__zos_network_overview.png)

### Z-NET

Z-Net is a decentralized networking platform allowing any compute and storage workload to be connected together on a private (overlay) network and exposed to the existing internet network. It is the foundation of any architecture running on the ThreeFold Grid. 

Learn more about Z-Net [Here](internet4:znet). 

### Planetary Network 

Planetary Network is an overlay network which lives on top of the existing internet or other peer-to-peer network created - A network where everyone is connected to everyone through a end-to-end encryption system without any intermediaries. 

All traffic between two Digital Selves will go over this Planetary Network. 

Learn more about Planetary Network [here](internet4:planetary_network). 

### ZNIC 

ZNIC is the interface of the Planetary Network. It is a peer-to-peer network built on top of the ThreeFold Grid and looks for shortest communication path between two Digital Selves. 

### Web Gateway 

The Web Gateway is the mechanism that connect the private networks to the open Internet in such a way that there is no direct connetion between internet and the secure workloads running in the ZMachine. 

Learn more about Web Gateway [here](internet4:webgw). \












