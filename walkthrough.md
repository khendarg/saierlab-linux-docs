Care and feeding of Saier Lab Ubuntu PCs
========================================

Initial setup
-------------

### Installing Ubuntu

It is highly recommended that you consult the [official tutorial](https://tutorials.ubuntu.com/tutorial/tutorial-install-ubuntu-desktop) or [documentation](https://help.ubuntu.com/community/Installation), as this guide is not likely to be updated anywhere near as frequently.

1. Download the latest x86\_64 ISO

2. Make sure the checksum matches

3. Write to a flash drive (replace FLASHDRIVE with the appropriate drive identifier):
```
# dd if=ubuntu_iso.iso of=/dev/FLASHDRIVE bs=8K
```

4. Sync thrice by actually typing sync thrice:
```
$ sync
$ sync
$ sync
```

5. Remove the flash drive and insert it in the target machine

6. Turn the machine on and enter BIOS

7. Set the priority for flash drives higher than for any bootable hard drives

8. For computers bought after 2012, disable UEFI SecureBoot

9. Save and restart

10. Install Ubuntu


### Setting up crucial directories

1. Make `/usr/local/BlastDB`:
```
# mkdir /usr/local/BlastDB
```

### Mount ResearchData

1. Install nfs-common: 
```
# apt-get install nfs-common
```

2. Make `/ResearchData`:
```
# mkdir /ResearchData
```

3. Add the following line to `/etc/fstab`:
```
# echo "SERVERIP:/Volumes/LaCie/ResearchData /ResearchData  nfs     rw,intr,exec    0       0" >> /etc/fstab
```

4. Restart the machine and check that `/ResearchData` exists and contains the appropriate files:
```
# ls /ResearchData
<list of files>
```

### Install software

1. Install the available bioinformatics packages:
```
sudo apt-get install clustalx clustalo ncbi-blast+ python-biopython python3-biopython fastaq pymol jmol jmol-applet emboss libccp4c0 libccp4-dev
```

Copyleft Kevin J. Hendargo 2017. All rights reversed.
