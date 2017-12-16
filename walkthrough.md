Care and feeding of Saier Lab Ubuntu PCs
========================================

Initial setup
-------------

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
