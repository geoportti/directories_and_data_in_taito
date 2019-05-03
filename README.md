<img src="https://github.com/geoportti/Logos/blob/master/geoportti_logo_300px.png">

# Directories and data in Taito

This article gives the general overview of the different directories in Taito environment. More detailed information can be found [here](https://research.csc.fi/taito-disk-environment).

## User home directory

The files in this directory are kept indefinetily (they will be deleted 90 days after the account is closed). Users can install their own software in their home directory, and instruct the batch job files to find those programs. Not for long-time storage not for large data sets. The default quota is 50 GB and there is a backup of the directory.

The environment variable `HOME` points to the user home directory:
```
echo $HOME # print your home directory path
cd $HOME # go to your home directory
```

## User working directory

The working directory is located on a different filesystem that is much faster than the filesystem where the home directory is located. This directory should be used for copying data sets that are needed in the analyses, and to store the output of the calculations. All the files that are not modified in 90 days are removed. There is no backup.

The environment variable: `WRKDIR`

## Public data

There are many national data sets from different organizations available in Taito. They can be found at
```
/proj/ogiir-csc
```

## Usage and Citing

When used, the following citing should be mentioned: "We made use of geospatial
data/instructions/computing resources provided by the Open Geospatial
Information Infrastructure for Research (oGIIR,
urn:nbn:fi:research-infras-2016072513) funded by the Academy of Finland."
