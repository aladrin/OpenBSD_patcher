# An automated way to patch OpenBSD from source
### OpenBSD_stager
Install on OpenBSD client. This is a wrapper that connects to a Linux host to create a 3GB ramdisk and serve over NFS. It then mounts this and OpenBSD_patcher command is run. Finally when completed, the stage is unmounted.
### OpenBSD_patcher
Install on OpenBSD client. This pulls the source to the stage and assembles the patching script.
### OpenBSD_ramdisk
Install on a Linux host where you have enough ram for a 3GB ramdisk to serve over NFS. This has only been tested on Ubuntu.
```
usage: To apply and build the patches
       OpenBSD_stager nfshost OpenBSD_patcher -p
       To install the patches
       OpenBSD_stager nfshost OpenBSD_patcher -i
```
