# bash-commands

### rsync:

`rsync -a --stats --progress user@remote-location.edu:/map/to/dir /Local/dir/branch`

### vim:

Exit vim:
<kbd>Esc</kbd> , <kbd>:</kbd>, <kbd>q</kbd>

### Change r/w/x permissions only to the folders/subfolders in a directory, excluding the files:
`sudo find /path/to/dir -type d -exec chmod 755 {} \;`
