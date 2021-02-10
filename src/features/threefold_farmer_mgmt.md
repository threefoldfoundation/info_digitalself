![](threefold_mgmt.png)

# ThreeFold Farmer Management System

stores info like

- farms and relation to 3nodes
- pricing
  - of CU/SU/NU
  - can be more than 1
  - can be linked to specific groups of users (customers)
  - can be linked to farms
- blacklist for customers:
  - specify who can use a 3node capacity
  - blacklist for consumers of capacity in relation to [3nodes](3node)
  - can be linked to farms
- reserve 3nodes (are reserved, not usable for capacity, but still count for farming)
- cultivation wallet: where does money come to as paid for users
  - can be linked to farms
- escalation to farmer when issues
  - over chat in DigitalTwin
  - e.g. node down, registration of capacity did not work, unability to do billing,...

executes on

- billing for the farmer
  - asks for payment to the right digital twin of the consumer using the [autopay](autopay) system.
- some basic health check & escalation to [notification system](notification).

## implementation

Accessible by Zero-OS and any other Digital Twin over Rest Interface.

In version 0.9 this will be done as data files which need to be editted, an use remote interface like ftp.

- specified in [dtml](dtml) or json
- accessible on [dtfs](dtfs)
- interface = [dtftp](dtftp)

- ...

> No UI features in 0.9 release, only editable over DTFS.

> assign: lee/maxime

## roadmap

- power management (< end March)
  - make sure that nodes which are reserved are turned on once a day to do the registration of uptime

**timing not known yet**

- rating system for farmers & nodes
- monitoring overview of health of 3nodes
