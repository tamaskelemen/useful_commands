# Useful Commands

## Packages for Debian 9
### htop (interactive system-monitor)
  `sudo apt-get install htop`
### Google Chrome 
`wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb`  
 `dpkg -i google-chrome-stable_current_amd64.deb `
### VLC (media player)
  `sudo apt-get install vlc`
### Vim (text editor)
  `sudo apt-get install vim`
  * to use Vim with mouse, edit your `/home/user/.vimrc` file and put this in it:  
  `set ttymouse=xterm2`  
  `set mouse=a`  
  `set mousemodel=popup`  //http://www.vim.org/htmldoc/options.html#%27mousemodel%27 
### Sublime Text
 https://www.sublimetext.com/3
 
## Postgres
`sudo apt-get install postgres`  (specific version eg.: postgres-9.3)

### Can be useful:
* login as postgres (psql root user):  
    `sudo su postgres`  
    `psql`
     or 
    `sudo -u postgres psql`
* Change password of a user:  
  `ALTER USER user_name WITH PASSWORD 'new_password';`
* TODO: postgis, create_db, db dump & restore, backup, log files, \x, \dt+, list: processes, indexes, functions.
## Debian 
 * Find all file (or directory, given with the type arg.) in the current directory, and executes `chmod 644` (or any given command)  
  `find . -type f -exec chmod 644 {} \;`
 * Deletes all symlinks in folder:  
 `find . -maxdepth 1 -type l -delete`
