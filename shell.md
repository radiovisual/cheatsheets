#Shell cheatsheet

###Compress all files in a directory

Compress all files from folderToCompress directory into a file named compressFileName.tar.gz
Note: works with GNU tar
```
$ tar -zcvf compressFileName.tar.gz folderToCompress
```

Also use the asterik `*` to compress everything in the current directory
Note: works for GNU tar
```
$ tar -zcvf compressFileName.tar.gz *
```

Same command as above, for non-GNU system. In addition to being portable, this solution is useful if you want to pass arguments to gzip (e.g., --test or --best), since afaik even GNU tar doesn't provide a way to send arguments to gzip.
```
$ tar cvf - folderToCompress | gzip > compressFileName
```

To expand the archive:
```
zcat compressFileName | tar xvf -
```
