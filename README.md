# An automated way to patch OpenBSD from source
### OpenBSD_stager
Install on OpenBSD client. This is a wrapper that connects to a Linux host to create a 2.5GB ramdisk and serve over NFS. It then mounts this and OpenBSD_patcher command is run. Finally when completed, the stage is unmounted.
### OpenBSD_patcher
Install on OpenBSD client. This pulls the source to the stage and assembles the patching script. If run interactively, you then have the choice to edit and execute the patching.
### OpenBSD_ramdisk
Install on a Linux host where you have enough ram for a 2.5GB ramdisk to serve over NFS. This has only been tested on Ubuntu.
```
usage: OpenBSD_stager nfshost OpenBSD_patcher -u
```
