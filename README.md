# Useful Commands

## Packages for Debian 9
### htop (interactive system-monitor)
  `sudo apt-get install htop`
### Google Chrome 
```
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
dpkg -i google-chrome-stable_current_amd64.deb
```
### VLC (media player)
  `sudo apt-get install vlc`
### Vim (text editor)
  `sudo apt-get install vim`
  * to use Vim with mouse, edit your `/home/user/.vimrc` file and put this in it:  
  ```
  set ttymouse=xterm2  
  set mouse=a
  set mousemodel=popup  //http://www.vim.org/htmldoc/options.html#%27mousemodel%27 
  ```
### Sublime Text
 https://www.sublimetext.com/3
 
## Postgres
```
sudo apt-get install postgres
sudo apt-get install pgtop 
```  (specific version eg.: postgres-9.3)

### Can be useful:
* login as postgres (psql root user):  
    ```
    sudo su postgres
    psql
    ```
     or 
    `sudo -u postgres psql`
* Change password of a user:  
  `ALTER USER user_name WITH PASSWORD 'new_password';`
* TODO: postgis, create_db, db dump & restore, backup, log files (xlog reset), truncate,  \x, \dt+, list: processes, indexes, functions.
## Debian 
 * Find all file (or directory, given with the type arg.) in the current directory, and executes `chmod 644` (or any given command)  
  `find . -type f -exec chmod 644 {} \;`
 * Deletes all symlinks in folder:  
 `find . -maxdepth 1 -type l -delete`
 * Wipes out your data (be careful! commmit before using this):
 `badblocks -ws` 
 * Test your cpu:
 `for i in 1 2 3 4; do while : ; do : ; done & done &`
### HDD check & repair sectors
```
echo "disk 1 sda" > /path/to/doc && badblocks -ws /dev/sda >> /path/to/doc
```
