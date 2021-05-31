
# Twin Architecture High Level

```mermaid

graph TB

    TwinFront[Twin Front = Nodejs] ---> TwinBack[Twin1 Backend = vlang]
    TwinBack --> redis[Redis]
    TwinBack --> secure_message_bus[Secure Message Bus]
    TwinBack --> QSFS[Quantum Safe Filesystem]
    QSFS --> QSFS_Daemon[QSFS Filesystem Daemon]
    QSFS --> QSFS_Monitor[QSFS Monitor]
    QSFS --> ZDB_LOCAL
    QSFS_Daemon --> ZDB1
    QSFS_Daemon --> ZDB2
    QSFS_Daemon --> ZDB3
    QSFS_Daemon --> ZDB...



```

- quantum safe filesystem used to store all data
- all data as json's in nicely structured directories
    - for now indexing in redis (for lookups)
    - walk over FS -> poor man index in redis
- the SMB realizes communication between twins
- data can never be lost

> TODO: complete the QSFS part

## 2 twins talk to each other


```mermaid

graph TB

    TwinFront1[Twin1 Front] ---> TwinBack1[Twin1 Backend]
    TwinFront2[Twin2 Front] ---> TwinBack2[Twin2 Backend]
    TwinBack1 --> redis1[Redis]
    TwinBack2 --> redis2[Redis]
    TwinBack1 --> secure_message_bus1[Secure Message Bus 1]
    TwinBack2 --- secure_message_bus2[Secure Message Bus 2]
    secure_message_bus1 --- secure_message_bus2[Secure Message Bus 2]




```