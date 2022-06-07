# Using reduced GALAH spectra and tables

## Format of the reduced data folders

Usually one would downlaod the reduced data from Datacentral or run a cloud client to synchronise their storage with Datacentral. To get the datadirectly  from Datacentral, you need to log in and then you can download rany GALAH data from
> https://cloud.datacentral.org.au/apps/files/?dir=/GALAH&fileid=1155726
speciffically the latest reductions from 
> https://cloud.datacentral.org.au/apps/files/?dir=/GALAH/obs/reductions/Iraf_6.0&fileid=15489397
Datacentrall is also running an Owncloud service, for which you need the appropriate client:
> https://owncloud.com/
The latest version of reduced data is named 6.0 and the complete products take 2.6 TB of space.

For the purpose of this tutorial, there is a small sample of the data provided in the folder sample_data. It consists of a few spectra from one single night. The folder structure mimics the one on Datacentral.



## Opening a table

Reduction tables come in .fits, .csv, and .hdf5 formats. Let's look at the fits format table. In the folder sample_data we have 
