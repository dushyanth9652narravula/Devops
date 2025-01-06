# Basic Commands Of Linux

- There are actually 4 basic commands in linux. Those are :

  **whoami** : `whoami` command is used to find who is the present user login in.

  **pwd** : `pwd` command is used to find the present working directory.

  **ls** : `ls` command is to list all the files and directories present in the current directory.

  **cat** : `cat` command is to read the contents of the file.

  <b>Ex</b>: `Cat <filename>`  or `cat <absolute path of the file>`

  **cd** : `cd <path>` command is used to change the directory .

- If you look at the prompt in shell, then we can see  `[vagrant@vbox ~]$` which indicates `vagrant` is the username, `vbox` is the localhost name and `$` indicates normal User shell and `~` symbol represents that you are in the home directory of vagrant user.

- If you log in to the root user by using the command `sudo -i`, then you can see te prompt like this `[root@vbox ~]#` where `root` indicates root user, `vbox` indicates the localhsot name and `#` indicates the root user shell and `~` symbol represents that you are in the home directory of root.

- Directory structure of the linux is :

  1) **Root Directory** - `/` : This is the top most directory in the hierarcy. It is called as root directory. It contains all other directories and files in the system. 

  2) **Home Directories** : `/home` directory contains all the users present in that operating system except root user. `/home/username` contains all the personal directories of that user. `/root` has all the directories of the root user. If you move to any other directory using `cd` command then to get into home directory you need to use `cd` and hit enter which will take you to home directory of that user

  3) **User Executable** : User executable directories are `/bin`, `/usr/bin`, `/usr/local/bin`. These contains essential executable programs such as `ls`, `cp`,`mv` needed for the system boot and for basic operation.

  4) **System Executables** : System Executable directories are `/sbin`, `/use/sbin`, `/usr/local/sbin`. These directories contains the system administration binaries such as `fsck`, `reboot`.

  5) **Other Mountpoints** : Mountpoints directories are `/mnt`, `/media`. `/mnt` contains the temporary mount points for the devices such as USB drives or external devices. `/media` autmoatically mounts the removable media.

  6) **Configuration** : `/etc` is the configuration directory in the linux. It contains the system-wide configuration files eg. `/etc/passwd`, `/etc/hosts` .

  7) **Temporary Files** : `/tmp` is used for the temporary file storage. These files are often removed when we  reboot.

  8) **Kernals and Bootloader** : `/boot` holds the files needed for the booting of the system. E.g kernal files, GRUB configurations.

  9) **Server Data** : `/var` and `/srv` contains the server data. `/var` contains the information that changes frequently, such as logs (`/var/log`), mail, and temporary files. `/srv` contains the data for system services, like web server files for hosting.

  10) **System Information** : `/proc` and `/sys` contains the system information.

  11) **Shared Libraries** : `/lib`, `/usr/lib`, `/usr/local/lib` are the shared libraries for root and users.

- From the diretory structure of linux, we can understand that every command that we are running is a file, everything is a file in linux. And all that files are text files which made it easy to configure settings of the system with just making few changes in that text file. In other operating systems, we need to go to settings tab and go to some other tabs in that settings tab to change the configurations.

## Some File Commands

- Before going to see the some File command let us know syntax of linux. The syntax of the linux is :

  `command  options arguments`

  **Ex** : `ls -l /home/vagrant` -> It going to display all the files present in vagrant user in the long list format which includes permisions to tat file , when it was created etc. Here command is `ls`, options are `-l` and the arguments are file path `/home/vagrant`

- File commands are :

  1) **mkdir** : `mkdir` command to used to make or create a directory. The syntax is `mkdir <directory name>`.

     **Ex** : `mkdir dev`  -> it create the dev directory in the present directory. If you want to create mutiple directories at a time then you can use this `mkdir ops backupdir`. To create mutiple directories you just need to pass the directory names as arguments.

  2) **touch** : `touch` command to used to create files in te linux. The syntax is `touch <file name>`.

     **Ex** : `touch testfile1.txt` -> It creates the testfile1.txt in the current directory. If you want to create file in any other directory then you need to use absolute path as argument instead of relative path. i.e `touch /home/vagrant/testfile1.txt`. If you want to create multiple files with same name but numbering is different then you need to use the following syntax. `touch testfile{1..10}.txt`

  3) **cp** : `cp` command is used to copy files  to the given directory. The syntax is `cp <path1> <path2>`. 

     **Ex** : `cp testfile1.txt dev` -> It copies testfile1.txt to the dev directory. If you want to copy a directory to another directory then you need to use option `-r`. So syntax is `cp -r dev ops` -> it copies dev directory to ops directory. `cp` command is used to copy contents from one file to another file also.

  4) **mv** : `mv` command is used to move one file or directory to another directory. The syntax is `mv <path1> <path2>`.

     **Ex** : `mv dev backupdir` -> It moves dev directory to backupdir. `mv` command can be used to rename a file or directory. But the file with that new name should not exist in that directory. If that new name exists then it will do move operation instead of rename operation. `mv ops operations` -> It renames ops directory to operations directory.

  5) **rm** : `rm` command is used to remove the files and directories in linux. The syntax is `rm <file or directory name>` .

     **Ex** : `rm testfile1.txt` -> it removes testfile1.txt from the current directory. If you want to remove the entire directory ten you need to use option `-r`. `rm -r dev` which remove entire dev directory. If you want to all the files or directories in the current directory then we need to `*` symbol. `rm -r *` -> removes all the files and directories presnt in the current directory. But beware while using `*` it will remove all the files or directories present in the current directory.

 - **Note** : If you want any help regarding the commnad then we can use `--help` option. For example `cp --help` gives all te documentation of the `cp` command. Here we can observe in linux we use single hypen `-` for single word options and double hypen `--` for multi word options.