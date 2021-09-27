# GMRT Archive Data Processing Utility

This repository contains code for different stages of the data processing pipeline for the NCRA-TIFR GMRT Archive Data Processing Utility. The stages are as follows:
1) filtering valid LTA data files,
2) converting LTA data files to UVFITS data files,
3) precalibrating the UVFITS files,
4) and finally converting the precalibrated UVFITs data files to scientific quality images stored as FITS files

We used the SPAM software for processing the above stages. SPAM (originally developed by Huib Intema) can be downloaded from https://github.com/NCRA-TIFR/gmrt-spam

This data processing pipeline was deployed on a compute cluster built in-house at NCRA.

Compute infrastructure was as follows:

1) Beowolf Cluster architecture
2) A total of 30 compute nodes and 1 master node.
3) Master node acted as the fileserver for the compute stack - AIPS, SPAM, Obit, Parseltongue softwares - which is NFS exported to a set of compute nodes
4) Compute nodes have standard Ubuntu 16.04 server installation plus additional software libraries installed via Tentakel from the master node
5) Ganglia tool was used to monitor cluster status

Pipeline figure:

<img src="https://github.com/architsakhadeo/gadpu/blob/master/images/gadpu.png?raw=true" width="500">
