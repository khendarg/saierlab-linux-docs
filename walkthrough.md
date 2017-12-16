Care and feeding of Saier Lab Ubuntu PCs
========================================

Initial setup
-------------

### Getting ResearchData mounted

1. Install nfs-common: 
```
# apt-get install nfs-common
```

2. Make `/ResearchData`:
```
# mkdir /ResearchData
```

3. Add the following line to `/etc/fstab`:
```fstab
132.239.144.57:/Volumes/LaCie/ResearchData /ResearchData  nfs     rw,intr,exec    0       0
```

4. Restart the machine and 

Copyleft Kevin J. Hendargo 2017. All rights reversed.
