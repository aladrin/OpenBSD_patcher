# An automated way to patch OpenBSD from source
### OpenBSD_stager
Install on OpenBSD client. This is a wrapper.
### OpenBSD_patcher
Install on OpenBSD client. This pulls the source and assembles the patching script.
### OpenBSD_ramdisk
Install on a Linux host where you have enough ram for a 2.5GB ramdisk to serve over NFS.
```
usage: OpenBSD_stager nfshost OpenBSD_patcher -u
```
