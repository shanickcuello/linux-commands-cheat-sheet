# linux-commands-cheat-sheet

## The cheat-sheet
This cheat sheet is based on the book "Linux Basics for Hackers" by OccupyTheWeb.
![image](https://github.com/shanickcuello/linux-commands-cheat-sheet/assets/44624042/ee196b6a-8392-4c5a-82aa-aa04bc5b7c61)

Please note that this cheat sheet is not intended to replace the book in any way. It serves simply as a reminder of the most commonly used commands. It does not provide exhaustive details of each command. For more in-depth information, I recommend using the `man` command or `--help` option to learn about each command.
The book provides detailed explanations of each command with examples, which I strongly recommend exploring. You can find it on Amazon and their website:
[Amazon Link](https://www.amazon.com/-/es/OccupyTheWeb/dp/1593278551)
[Website Link](https://www.hackers-arise.com/welcome)


### Basic Commands

| Command | Description | Example Usage |
|---------|-------------|---------------|
| `pwd`   | Prints the current working directory. | `pwd` |
| `whoami`| Displays the current username. | `whoami` |
| `cd`    | Changes the current directory. | `cd /path/to/directory` |
| `ls`    | Lists directory contents. | `ls -la` |
| `--help`| Displays help information for a command. | `ls --help` |
| `man`   | Shows the manual for a command. | `man ls` |
| `locate`| Finds files by name. | `locate filename` |
| `find`  | Searches for files in a directory hierarchy. | `find /path -name filename` |
| `which` | Shows the path of a command. | `which ls` |
| `ps`    | Displays information about running processes. | `ps aux` |
| `cat`   | Concatenates and displays file contents. | `cat file.txt` |
| `mkdir` | Creates a new directory. | `mkdir new_directory` |
| `rm`    | Removes files or directories. | `rm file.txt` `rm -rf directory_name` |
| `rmdir` | Removes empty directories. | `rmdir empty_directory` |
| `mv`    | Moves or renames files or directories. | `mv oldname.txt newname.txt` |
| `touch` | Changes file timestamps or creates an empty file. | `touch newfile.txt` |

### Text Manipulation

| Command | Description | Example Usage |
|---------|-------------|---------------|
| `cat`   | Concatenates and displays file contents. | `cat file.txt` |
| `head`  | Outputs the first part of files. | `head -n 10 file.txt` |
| `tail`  | Outputs the last part of files. | `tail -n 10 file.txt` |
| `nl`    | Numbers lines of files. | `nl file.txt` |
| `sed`   | Stream editor for filtering and transforming text. | `sed 's/old/new/g' file.txt` |
| `more`  | View file contents one screen at a time. | `more file.txt` |
| `less`  | Similar to `more`, but with backward movement. | `less file.txt` |

### System Management Commands

| Command   | Description | Example Usage |
|-----------|-------------|---------------|
| `ps`      | Displays information about running processes. | `ps` |
| `ps aux`  | Displays detailed information about all running processes. | `ps aux` |
| `nice`    | Runs a command with modified scheduling priority. | `nice -n 10 command` |
| `kill`    | Sends a signal to terminate a process. | `kill 1234` |
| `killall` | Kills processes by name. | `killall firefox` |
| `fg`      | Brings a background job to the foreground. | `fg %1` |
| `at`      | Schedules commands to run at a later time. | `echo "command" \| at 10:00` |
| `chown`   | Changes file ownership. | `chown user:group file.txt` |
| `chmod`   | Changes file permissions. | `chmod 755 file.txt` |

### Add or Install Software Commands

| Command   | Description | Example Usage |
|-----------|-------------|---------------|
| `apt`     | Package handling utility for Debian-based systems. | `apt update` |
| `apt-get` | APT package handling utility. | `apt-get install package_name` |

### Network Commands

| Command                | Description | Example Usage |
|------------------------|-------------|---------------|
| `ifconfig`             | Configures network interfaces. | `ifconfig eth0` |
| `iwconfig`             | Configures wireless network interfaces. | `iwconfig wlan0` |
| `dhclient`             | Dynamic Host Configuration Protocol Client. | `dhclient eth0` |
| `dig`                  | DNS lookup utility. | `dig example.com` |
| `iwlist wlan0 scan`    | Scans for available wireless networks. | `iwlist wlan0 scan` |
| `nmcli dev wifi`       | Lists available Wi-Fi networks. | `nmcli dev wifi` |
| `nmcli dev wifi connect some-network password somePassword` | Connects to a Wi-Fi network using `nmcli`. | `nmcli dev wifi connect MyWiFi password MyPassword` |
| `airmon-ng`            | WLAN monitor mode enabling tool. | `airmon-ng start wlan0` |
| `airmon-ng start wlan0`| Puts interface `wlan0` into monitor mode. | `airmon-ng start wlan0` |
| `airodump-ng wlan0`    | Captures raw 802.11 frames. | `airodump-ng wlan0` |
| `aireplay-ng`          | Packet injection tool for 802.11 networks. | `aireplay-ng -0 5 -a 00:11:22:33:44:55 wlan0` |
| `aircrack-ng`          | 802.11 WEP and WPA-PSK keys cracking program. | `aircrack-ng -w wordlist.txt captured.cap` |
| `hcitool`              | Configures Bluetooth connections. | `hcitool scan` |

[802.11](https://en.wikipedia.org/wiki/IEEE_802.11)

### User Environment Variable Management Commands

| Command                       | Description | Example Usage |
|-------------------------------|-------------|---------------|
| `env`                         | Displays the current environment variables. | `env` |
| `set \| more`                  | Displays all shell variables and functions, paginated. | `set \| more` |
| `HISTSIZE`                    | Sets the number of commands to remember in the command history. | `HISTSIZE=1000` |
| `echo $HISTSIZE`              | Displays the current value of the HISTSIZE variable. | `echo $HISTSIZE` |
| `export`                      | Sets environment variables or marks shell variables for export. | `export VAR=value` |
| `export HISTSIZE`             | Exports the HISTSIZE variable to the environment. | `export HISTSIZE=1000` |
| `echo $PATH`                  | Displays the current value of the PATH variable. | `echo $PATH` |
| `someNewVariable="Some value"`| Sets a new shell variable. | `someNewVariable="Some value"` |
| `echo $someNewVariable`       | Displays the value of `someNewVariable`. | `echo $someNewVariable` |
| `unset someNewVariable`       | Removes `someNewVariable` from the shell environment. | `unset someNewVariable` |

### Compressing and Decompressing Commands

| Command         | Description | Example Usage |
|-----------------|-------------|---------------|
| `tar`           | Creates an archive from a list of files. | `tar cvf archive.tar file1 file2` |
| `tar -rvf`      | Appends files to an existing archive. | `tar -rvf archive.tar newfile` |
| `tar -xvf`      | Extracts files from an archive. | `tar -xvf archive.tar` |
| `tar -xf`       | Extracts files from an archive without verbose output. | `tar -xf archive.tar` |
| `gzip`          | Compresses files using gzip. | `gzip file.txt` |
| `bzip2`         | Compresses files using bzip2. | `bzip2 file.txt` |
| `compress`      | Compresses files using the compress program. | `compress file.txt` |
| `uncompress`    | Decompresses files compressed by the compress program. | `uncompress file.txt.Z` |

### Mounting and Unmounting Commands

| Command    | Description | Example Usage |
|------------|-------------|---------------|
| `mount`    | Mounts a filesystem. | `mount /dev/sdb1 /mnt` |
| `umount`   | Unmounts a filesystem. | `umount /mnt` |
| `fsck`     | Checks and repairs a filesystem. | `fsck /dev/sdb1` |
| `df`       | Reports file system disk space usage. | `df -h` |

### Service and Database Commands

| Command              | Description | Example Usage |
|----------------------|-------------|---------------|
| `service`            | Controls system services. | `service apache2 start` |
| `show databases`     | Lists all databases in a DBMS. | `show databases` (MySQL) |
| `use mysql`          | Switches to the MySQL system database. | `use mysql` |
| `use somedatabase`   | Switches to a specific database in DBMS. | `use somedatabase` (MySQL) |
| `show tables`        | Lists tables in the current database. | `show tables` (MySQL) |
| `describe sometable` | Shows the structure of a table. | `describe sometable` (MySQL) |
| `su postgres`        | Switches user to `postgres` (switch user). | `su postgres` |
| `db_status`           | Checks the status of a database (generic). | `db_status` |

### Network Tracing and Proxy Commands

| Command                                     | Description | Example Usage |
|---------------------------------------------|-------------|---------------|
| `traceroute www.shanick.dev`                | Traces the route packets take to a network host. | `traceroute www.shanick.dev` |
| `proxychains`                               | Forces any TCP connection made by any given application through a proxy. | `proxychains command` |
| `proxychains nmap`       | Uses `nmap` with `proxychains` to scan a host through a proxy. | `proxychains nmap -sV -T5 10.19.15.2` |
| `cat /etc/proxychains.conf`         | Displays the content of `/etc/proxychains.conf` using `cat`. | `cat /etc/proxychains.conf` |
| `proxychains firefox www.shanick.dev`       | Opens Firefox and forces it to use a proxy specified in `proxychains.conf`. | `proxychains firefox www.shanick.dev` |

### System Information and Kernel Commands

| Command                           | Description | Example Usage |
|-----------------------------------|-------------|---------------|
| `uname -a`                        | Displays system information including kernel version. | `uname -a` |
| `cat /proc/version`               | Displays Linux kernel version information. | `cat /proc/version` |
| `sysctl -a \| less`               | Displays kernel parameters and their values interactively. | `sysctl -a \| less` |
| `lsmod`                           | Lists loaded kernel modules. | `lsmod` |
| `modprobe -a <module name>`       | Loads specified kernel module(s). | `modprobe -a usb-storage` |
| `modprobe -r <module to delete>`  | Unloads specified kernel module. | `modprobe -r usb-storage` |
| `dmesg`                           | Displays kernel ring buffer messages. | `dmesg` |

### Scheduling Tasks and Service Management

| Command          | Description | Example Usage |
|------------------|-------------|---------------|
| `crontab -e`     | Edits the user's crontab file to schedule tasks. | `crontab -e` |
| `update-rc.d`    | Updates the System V init links for service control scripts. | `update-rc.d apache2 defaults` |
| `rrconf`         | Manages configuration for RunRev scripts. | `rrconf list` |

- 0 8 * * 1 /path/to/command
- 0 indicates the minute (in this case, 0).
- 8 indicates the hour (in this case, 8 AM).
- \* \* indicates that the task will run any day of the month and any month.
- 1 indicates that the task will run every Monday (Monday is day 1 of the week in cron).
- /path/to/command is the path to the command that will be executed.

---
Pull requests are welcome for adding or removing commands, as well as for modifying or correcting errors.
