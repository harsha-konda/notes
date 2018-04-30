## 1 – What Is The Shell?
- the shell is program that takes keyboard commands and passes them to the os.
- `$` sign indicates guest priviliges
- `#` sign indicates super user priviliges

### basic commands  
```
$ date
Sat Apr 28 01:53:13 PDT 2018
```

```
# calender
$ cal
```

```
# free space disk
$ df
```

```
# display free memomry 
$ free
```

## 2 - Navigation
```
# display current working directory
$ pwd
```

```
# change working directory
$ cd  
```
### relative path
- `.` current working directory
- `..` parent working directory
- `-` previous working directory
- `~` home working directory

## 3 - Exploring the System

### ls
```
# list contents of directory
$ ls 
-a	list all files including hidden files 
-l 	list in long format
-t 	sort the result by file's modification time
--reverse	reverse the order of the sort
-A -a option except for current directory and parent directory
-d see the contents of the directory rather than the directory itself
-F option classifies the contents
-h human readable format rather than bytes
```
- **ls -l** 

```
total 21
drwxrwxr-x+ 61 root  admin  1952 Apr 27 03:58 Applications
drwxr-xr-x+ 64 root  wheel  2048 Feb 16 04:51 Library
drwxr-xr-x@  2 root  wheel    64 Oct  2  2017 Network
drwxr-xr-x@  4 root  wheel   128 Jan 18 23:34 System
26 18:58 home
```
|field|meaning|
| -----|-----| 
|-rw-r--r--| first charcter indicates type of file(*-* **regular file** , **d** **directory**); each subsequet three character are access rights for the *file's owner*,members of the **file's group*, for **everyone** else |
| 1 | indicates the number of hard links for the file |
| root | username of the file owner|
| root | the name of the group which owns the file |
| %n | the size of the file|

### file
- file names in linux are not required to reflect the notion of file's contents.
- ```file filename``` - when invoked this will print a brief description of the files contents.
- Unix os has the notion that **everything is file**

### less
- a program designed to view big log files, that contain human readable text.

| Command | Action |
|---------|--------|
|pageup or b|scroll up one page|
|space|scroll down one page|
|up arrow| scroll up one line|
|down arrow| scroll down one line|
| G | move to the end of text file |
| g | move to the beginning of text file | 
| /character | for searching the occurence of characters |
| h | diplay help |
| q | quit|

### linux file system
| Directory | Comments |
| ----------| ---------|
| /bin | binaries for the system to boot |
| /boot | contains the linux kernel, initial ram disk image, boot loader |
| /dev | this contains the device nodes, maintains the list of all devices  |
| /etc | contains system wide configuration files, contains shell scripts that start at boottime |
| /home | each user is given a home directory where a user can write his her files |
| /lib | contains shared files used by the core system |
| /media | will contain mount point of removable devices |
| /mnt | contains mount points of removable devices that have been mounted manually |
| /opt | used to install optional software |
| /root | home directory of root account | 
| /sbin | contains system binaries for performing vital tasks |
| /tmp | inteded for temporary transient storage, usually emptied on reboots |
| /usr | contains all the programs and support files used by users | 
| /usr/bin | contains installed executable programs and support files used by regular users | 
| /usr/lib | shared libraries for the programs in /usr/bin | 
| /usr/local | prgrams not included with distribution but are intended for system wide use are installed here | 
| /usr/sbin | contains system administrative programs | 
| /usr/share | contains all shared data used by programs in */usr/bin*|
| /var | the part of the tree where variable data is stored | 
| /var/log | contains log files | 
  
