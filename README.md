# Using reduced GALAH spectra and tables

## Format of the reduced data folders

Usually one would downlaod the reduced data from Datacentral or run a cloud client to synchronise their storage with Datacentral. To get the datadirectly  from Datacentral, you need to log in and then you can download rany GALAH data from
> https://cloud.datacentral.org.au/apps/files/?dir=/GALAH&fileid=1155726

speciffically the latest reductions from 
> https://cloud.datacentral.org.au/apps/files/?dir=/GALAH/obs/reductions/Iraf_6.0&fileid=15489397

Datacentrall is also running an Owncloud service, for which you need the appropriate client:
> https://owncloud.com/

The latest version of reduced data is named 6.0 and the complete products take 2.6 TB of space.

For the purpose of this tutorial, there is a small sample of the data provided in the folder ``sample_data``. It consists of a few spectra from one single night. The folder structure mimics the one on Datacentral.

Explore the folder before we continue with understanding its contents.

## Opening a table

Reduction tables come in .fits, .csv, and .hdf5 formats. Let's look at the fits format table. In the folder ``sample_data`` we have a table called dr6.0.fits. This table would contain an entry for each combined spectrum for all nights. There is also a similar table in the folder ``sample_data/210115/db`` called 210115.fits. It has the same structure as dr6.0.fits, but only entries for the night 210115. In this tutoriasl the two tables are bot truncated to just 6 entries for 6 stars discussed in this tutorial.

Tables are best explored in TOPCAT.

## Opening a spectrum

Combined spectra are found in the folder ``210115/spectra/com``. There are four .fits files for each observed object, their names ending in numbers 1, 2, 3, and 4 for spectra made with the blue, green, red, and IR arms. 

For a quick overview of a .fits file I like to use fitsview. TOPCAT or ds9 will fail to display these files correctly. From hereon we will use python to open the .fits files, extract spectra and some header information.

### Extensions


