# linux-commands-cheat-sheet

### Table 1: Basic Commands

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
| `rm`    | Removes files or directories. | `rm file.txt` |
| `rmdir` | Removes empty directories. | `rmdir empty_directory` |
| `mv`    | Moves or renames files or directories. | `mv oldname.txt newname.txt` |
| `touch` | Changes file timestamps or creates an empty file. | `touch newfile.txt` |

### Table 2: Text Manipulation

| Command | Description | Example Usage |
|---------|-------------|---------------|
| `cat`   | Concatenates and displays file contents. | `cat file.txt` |
| `head`  | Outputs the first part of files. | `head -n 10 file.txt` |
| `tail`  | Outputs the last part of files. | `tail -n 10 file.txt` |
| `nl`    | Numbers lines of files. | `nl file.txt` |
| `sed`   | Stream editor for filtering and transforming text. | `sed 's/old/new/g' file.txt` |
| `more`  | View file contents one screen at a time. | `more file.txt` |
| `less`  | Similar to `more`, but with backward movement. | `less file.txt` |

### Table 3: Network and System Management Commands

| Command   | Description | Example Usage |
|-----------|-------------|---------------|
| `ifconfig`| Configures network interfaces. | `ifconfig eth0` |
| `iwconfig`| Configures wireless network interfaces. | `iwconfig wlan0` |
| `dhclient`| Dynamic Host Configuration Protocol Client. | `dhclient eth0` |
| `dig`     | DNS lookup utility. | `dig example.com` |
| `apt`     | Package handling utility for Debian-based systems. | `apt update` |
| `apt-get` | APT package handling utility. | `apt-get install package_name` |
| `ps`      | Displays information about running processes. | `ps aux` |
| `ps aux`  | Displays detailed information about all running processes. | `ps aux` |
| `nice`    | Runs a command with modified scheduling priority. | `nice -n 10 command` |
| `kill`    | Sends a signal to terminate a process. | `kill 1234` |
| `killall` | Kills processes by name. | `killall firefox` |
| `fg`      | Brings a background job to the foreground. | `fg %1` |
| `at`      | Schedules commands to run at a later time. | `echo "command" | at 10:00` |
