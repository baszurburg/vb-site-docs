#Linux

## Locations

### Website sourcefiles
The source files for the websites are located in **/var/www/** e.g. */var/www/example.com/public_html*

### Apache2

Apache dir: **/etc/apache2/**

### Mongodb

* datafiles: **/var/lib/Mongodb**
* logfiles: **/var/log/mongodb**
* configuration: **/etc/mongod.conf**
* database: **/data/db**

## Commands

### Frequenlty used

* running processes: `ps aux | grep 'query'`


### Apt-Get

* Update repository: `sudo apt-get update`
* Install a package: `sudo apt-get install [package name]`
* Remove a package: `sudo apt-get remove [package name]`
* Upgrade packages: `sudo apt-get upgrade`
* help: `apt-get help`

[Hey! Get from this](https://www.maketecheasier.com/8-ways-to-maintain-a-clean-lean-ubuntu-machine/)

### Version

* OS: `uname -v`
* version: `lsb_release -a`
* architecture: `uname -m`
* processor: `cat /proc/cpuinfo`

### SSH keys

To create your public and private SSH keys on the command-line:

* `mkdir ~/.ssh`
* `chmod 700 ~/.ssh`
* `ssh-keygen -t rsa`

You will be prompted for a location to save the keys, and a passphrase for the keys. This passphrase will protect your private key while it's stored on the hard drive:

* Enter file in which to save the key (/home/b/.ssh/id_rsa):
* Enter passphrase (empty for no passphrase):
* Enter same passphrase again:

Your public key is now available as .ssh/id_rsa.pub in your home folder.