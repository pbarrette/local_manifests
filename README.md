# local_manifests

To build the LOS 13.0 version for the Obake device family,
follow the steps below:

## Setup build tree
Create the directory for your build tree, usually '~/android/lineage',
then 'cd' into it and run the following commands:
```Shell session
repo init -u https://github.com/LineageOS/android.git -b cm-13.0
cd .repo
git clone https://github.com/pbarrette/local_manifests
cd local_manifests
git checkout cm-13.0
cd ../..
repo sync
```

This will remove the broken LineageOS official build for obake and
replace it with mine.

It will also download the obake specific binaries from my
'proprietary_vendor_motorola' repo, which is just a trimmed down
fork of those provided by 'TheMuppets'.