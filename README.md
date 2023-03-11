# An automated way to patch OpenBSD from source
### OpenBSD_stager
Install on OpenBSD client. This is a wrapper that connects to a Linux host to create a 3GB ramdisk and serve over NFS. It then mounts this and OpenBSD_patcher command is run. Finally when completed, the stage is unmounted.
### OpenBSD_patcher
Install on OpenBSD client. This pulls the source to the stage and assembles the patching script.
### OpenBSD_ramdisk
Install on a Linux host "nfshost" where you have enough ram for a 3GB ramdisk to serve over NFS. This has only been tested on Ubuntu.
```
usage: Apply all patches
       OpenBSD_stager nfshost OpenBSD_patcher -p
       Build
       OpenBSD_stager nfshost OpenBSD_patcher -b
       Install
       OpenBSD_stager nfshost OpenBSD_patcher -i
       Build xenocara
       OpenBSD_stager nfshost OpenBSD_patcher -x
       Install xenocara
       OpenBSD_stager nfshost OpenBSD_patcher -X
