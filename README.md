# zfs-replicator

*Automatic replication between ZFS volumes on separate hosts*

## Requirements
* zfs

## Installation

```
### Clone project
git clone https://github.com/navargas/zfs-replicator.git
cd zfs-replicator/

### Create ./nodes.list file
### (see configuration section below)

### Install on nodes
./replicator install
```


## Configuration
```
username@ip_address1 alias1
username@ip_address2 alias2
...
```

## Usage
To create a new replicated volume run
```
./replicator create volume_name alias_of_master
```
The volumes will be mounted at /var/replicator/data/**volume_name**.

Changes will flow from the master to the other nodes on a set interval.
