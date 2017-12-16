Care and feeding of Saier Lab Ubuntu PCs
========================================

Initial setup
-------------

### Getting ResearchData mounted

1. Install nfs-common: 
```bash
sudo apt-get install nfs-common
```

2. Add the following line to `/etc/fstab`:
```fstab
132.239.144.57:/Volumes/LaCie/ResearchData /ResearchData  nfs     rw,intr,exec    0       0
```


Copyleft Kevin J. Hendargo 2017. All rights reversed.
