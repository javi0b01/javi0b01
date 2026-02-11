# :memo: Notes
## LINUX
### Learn
1. What is it
2. What does it do
3. Why to use it
4. Getting started
5. Concepts
6. Code samples
7. Documentation
### Resources
- [UNIX](https://unix.org/)
- [Unix](https://en.wikipedia.org/wiki/Unix)
- [What is Unix](https://unix.org/what_is_unix.html)
- [GNU](https://www.gnu.org/home.en.html)
- [Linux.org](https://www.linux.org/)
- [What is Linux](https://www.linux.org/threads/what-is-linux.4106/)
- [Download Linux](https://www.linux.org/pages/download/)
- [Linux tutorials](https://www.linux.org/forums/#linux-tutorials.122)
- [die.net](https://www.die.net/)
- [man7.org](https://man7.org/)
- [Command line reference](https://ss64.com/)
- https://distrosea.com/
- https://support.system76.com/
- https://support.system76.com/articles/customize-gnome/
- https://pop-os.github.io/docs/customize-pop/gnome-tweaks-extensions/gnome-extensions.html
- https://github.com/daveprowse/DrawOnYourScreen3
### Terms and concepts
- UNIX OS
- The kernel
- Clone
- Linux OS
- Distros
- Install distro Linux OS
- Desktop environment
* CLI or Command Line Interface
  - Terminal
* Command
  - Option (flag)
- Case sensitive
- File
* Linux file structure
  * Root directory
    - bin, boot, home directory, etc.
   * Paths
    - Absolute path
    - Relative path
  - Levels (parent, child)
- Working with directories
- Working with files
- Working with file content

- sudo (super user do)
- apt (Advenaced Package Tool)
- Snap package manager
### Basic commands
#### Working with directories, files and file content
```
$ cat /etc/lsb-release
$ ps --no-headers -o comm 1
$ man man
$ man sudo
$ uname -m
$ pwd
$ cd
$ ls
$ clear
$ touch
$ mkdir
$ rmdir
$ file
$ rm
$ cp
$ mv
$ head
$ tail
$ cat
$ echo
$ more
$ less
$ chmod
$ diff
$ telnet
$ ln
$ sudo su -
```
#### System information
```
$ cat /etc/os-release
$ uptime
$ free
$ ps
$ df
$ fdisk
$ lsblk
$ top
htop (package)
```
#### Networking
```
$ ifconfig
$ ip
$ netstat --help
net-tools (package)
```
#### Package manager
```
$ man apt
$ sudo apt update
$ apt list --upgradable
$ sudo apt upgrade
$ sudo apt autoremove
$ sudo apt search <package name>
$ sudo apt install <package name>
$ sudo apt remove <package name>
```
Snap
```
$ snap --version
```
Unattended Upgrades
```
$ sudo apt install unattended-upgrades
$ sudo dpkg-reconfigure --priority=low unattended-upgrades
```
update_system.sh script file
```
#!/bin/bash
# This script automates the system update, upgrade, and cleanup process.

echo "Starting system update..."
sudo apt update -y

echo "Listing upgradeable packages..."
sudo apt list --upgradeable -a

echo "Applying upgrades..."
sudo apt upgrade -y

echo "Removing unnecessary packages..."
sudo apt autoremove -y

echo "System update routine finished."
```
#### Text editors
```
$ vi <file name>
$ vim <file name>
$ nano <file name>
$ emacs <file name>
```
#### systemctl commands
Handle apache2
```
$ sudo systemctl stop apache2
$ sudo systemctl restart apache2
$ sudo systemctl disable apache2
$ sudo systemctl enable apache2
```
## Software Developer
Built by [JAVI](https://github.com/javi0b01/) :copyright: 2020 - 2025  
Found a bug or have an idea? [Contact me](https://www.linkedin.com/in/javi0b01/).
