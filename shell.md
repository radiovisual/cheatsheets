# Shell cheatsheet

#### Compress all files in a directory

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

#### Colors in a Bash Shell

```
#!/bin/bash

ESC_SEQ="\x1b["
COL_RESET=$ESC_SEQ"39;49;00m"
COL_RED=$ESC_SEQ"31;01m"
COL_GREEN=$ESC_SEQ"32;01m"
COL_YELLOW=$ESC_SEQ"33;01m"
COL_BLUE=$ESC_SEQ"34;01m"
COL_MAGENTA=$ESC_SEQ"35;01m"
COL_CYAN=$ESC_SEQ"36;01m"

echo -e "$COL_MAGENTA This will be Magenta. $COL_RESET"
```