Care and feeding of Saier Lab Ubuntu PCs
========================================

Initial setup
-------------

### Getting ResearchData mounted

1. Install nfs-common: 
```bash
# apt-get install nfs-common
```

1. Make `/ResearchData`:
```bash
# mkdir /ResearchData
```

1. Add the following line to `/etc/fstab`:
```fstab
132.239.144.57:/Volumes/LaCie/ResearchData /ResearchData  nfs     rw,intr,exec    0       0
```

1. Restart the machine and 

Copyleft Kevin J. Hendargo 2017. All rights reversed.
