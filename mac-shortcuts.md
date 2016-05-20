# Mac Shortcuts

### Screenshots

Take a screen shot of a specific region; save to file

```
$ screencapture -i capture.png
```

### Terminal Shortcuts

Command | Description
--- | ---
<kbd>CTRL</kbd> + <kbd>E</kbd> | Jump to the end of your terminal text
<kbd>CTRL</kbd> + <kbd>A</kbd> | Jump to the start of your terminal text
<kbd>ALT</kbd> + <kbd>→</kbd> | Jump to the next word character
<kbd>ALT</kbd> + <kbd>←</kbd> | Jump to the previous word character
<kbd>CTRL</kbd> + <kbd>U</kbd> | Clear input before the carat (clear entire line)

### Emoji

Command | Description
--- | ---
<kbd>CTRL</kbd> + <kbd>Cmd</kbd> + <kbd>Space</kbd> | Press within any textfield on OSX to open an emoji popover

### Say

Turn an entire text file into an audio file

```
say -f mynovel.txt -o myaudiobook.aiff
```

### Zip Encryption

Archive a folder with encryption (`-r`: recursively enter folder, `-P`: password protect)

```
zip -r -P mySuperSecretPassword secure_output.zip path/to/folder/
```

### Finding files

#### List files over 100Mb

Use `-x` to avoid traversing through mounted drives

```
sudo find -x / -type f -size +100000k -exec ls -lh {} \; | awk '{ print $9 ": " $5 }'
```

