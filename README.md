# bash-commands

### rsync:

`rsync -a --stats --progress user@remote-location.edu:/map/to/dir /Local/dir/branch`

### vim:

Exit vim:
<kbd>Esc</kbd> , <kbd>:</kbd>, <kbd>q</kbd>

Exit and save changes: 
<kbd>Esc</kbd> <kbd>:</kbd> <kbd>w</kbd><kbd>q</kbd>

### Change r/w/x permissions only to the folders/subfolders in a directory, excluding the files:
`sudo find /path/to/dir -type d -exec chmod 755 {} \;`

### grep:
`grep -r 'stringToSearch' *`.   
Search for string `pattern` in all files/folders in directory:  
`grep -rnw '/path/to/somewhere/' -e 'pattern'`.   
Search the output of some command:   
`ls -halt | grep "pattern"`

### virtualenv: choose python distro

`virtualenv -p /usr/bin/path-to-python-version env_name`


## setup jupyter 
In remote server:  
`jupyter lab --no-browser --port=8001`     
In local computer / laptop:  
`alias jupLAB="ssh -N -f -L localhost:8001:localhost:8001 awick@remote.url && open http://localhost:8001"`  

## tmux 
new session:   
`tmux new -s session-name`  
attach to last session:  
`tmux a`   
list active sessions:   
`tmux ls`. 

## Source .bashrc upon login:
Add the following to `~/.profile`:

```
if [ -s ~/.bashrc ]; then
    source ~/.bashrc;
fi
```


## Colored PS1  
Add to `~/.bashrc`:  
`export PS1="\e[0;34m[\u@\h \W]\$ \e[m"`
