#!/usr/bin/env bash

# variables - modify them to suite your enviorment

# Storage name
name='storagename'
# Storage access key
key='key'
# Container name
container='public'

# The actual script

#
foldersinit="$(ls -d */)"
filesfirst="$(ls -p $foldersinit | grep -v /)"
folderssecod="$(ls -d $foldersinit*/)"
filessecond="$(ls -p $folderssecod | grep -v /)"


for fn in $filesfirst; do
fileuploadfirst=$(find * -name $fn | head -n 1)
azure storage blob upload -vf $fileuploadfirst -b $fileuploadfirst --container $container -a $name -k $key
# echo $fileuploadfirst
done

for fntwo in $filessecond; do
fileuploadsecond=$(find * -name $fntwo | head -n 1)
# echo $fileuploadsecond
azure storage blob upload -vf $fileuploadsecond -b $fileuploadsecond --container $container -a $name -k $key
done


