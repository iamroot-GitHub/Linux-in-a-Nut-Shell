# Linux in a Nut $hell
## Table of Contents
1.  [Shortcuts](https://github.com/iamroot-GitHub/Linux-in-a-Nut-Shell/blob/main/README.md#shortcuts)
2.  [Basic Linux Commands](https://github.com/iamroot-GitHub/Linux-in-a-Nut-Shell/blob/main/README.md#basic-linux-commands)
3.  [Commands Related to Administering Users and Groups](https://github.com/iamroot-GitHub/Linux-in-a-Nut-Shell/blob/main/README.md#commands-related-to-administering-users-and-groups)
4.  [Permissions Configuration Commands](https://github.com/iamroot-GitHub/Linux-in-a-Nut-Shell/blob/main/README.md#permissions-configuration-commands)
5.  [File Management Commands](https://github.com/iamroot-GitHub/Linux-in-a-Nut-Shell/blob/main/README.md#file-management-commands)
6.  [Commands for Authoring Text Files](https://github.com/iamroot-GitHub/Linux-in-a-Nut-Shell/blob/main/README.md#commands-for-authoring-text-files)
7.  [Software Management Commands](https://github.com/iamroot-GitHub/Linux-in-a-Nut-Shell/blob/main/README.md#software-management-commands)
8.  [Commands for Managing Devices, Processes, Memory and the Kernal](https://github.com/iamroot-GitHub/Linux-in-a-Nut-Shell/blob/main/README.md#commands-for-managing-devices-processes-memory-and-the-kernal)
9.  [Service Management Commands](https://github.com/iamroot-GitHub/Linux-in-a-Nut-Shell#service-management-commands)
10. [Network Setting Configuration Commands](https://github.com/iamroot-GitHub/Linux-in-a-Nut-Shell#network-setting-configuration-commands)
11. [Network Security Configuration Commands](https://github.com/iamroot-GitHub/Linux-in-a-Nut-Shell#network-security-configuration-commands)
12. [Security Management Commands](https://github.com/iamroot-GitHub/Linux-in-a-Nut-Shell#security-management-commands)
13. [Script Implementation Commands](https://github.com/iamroot-GitHub/Linux-in-a-Nut-Shell#script-implementation-commands)
14. [IaC Commands](https://github.com/iamroot-GitHub/Linux-in-a-Nut-Shell#iac-commands)
15. [Commands for Managing Containers](https://github.com/iamroot-GitHub/Linux-in-a-Nut-Shell#commands-for-managing-containers)
16. [Linux Installation Commands](https://github.com/iamroot-GitHub/Linux-in-a-Nut-Shell#linux-installation-commands)
### Shortcuts
|Shortcut|Action                                                                                   |
|--------|-----------------------------------------------------------------------------------------|
|Tab     |Autocomplete or show all possilbe results.                                               |
|Ctrl + A|Move the cursor to the beginning of the line.                                            |
|Ctrl + C|Stop (terminate) a running program immediately.                                          |
|Ctrl + D|Log out of current terminal (close SSH connection or terminal application).              | 
|Ctrl + E|Move the cursor to the end of the line.                                                  | 
|Ctrl + K|Erase everything from the current cursor position to the end of the line.                | 
|Ctrl + L|Clear the terminal screen.                                                               |
|Ctrl + N|Displays the next command. Use this shortcut in conjunction with Ctrl + P.               | 
|Ctrl + P|View the previous command. Press repeatedly to keep on going back in the command history.| 
|Ctrl + R|Perform a search in command history.                                                     | 
|Ctrl + U|Erase everything from the current cursor position to the beginning of the line.          | 
|Ctrl + W|Erase the word preceding the cursor position.                                            | 
|Ctrl + Y|Paste the erased text of the Ctrl + K, Ctrl + U, and Ctrl + W shortcuts.                 | 
|Ctrl + Z|Suspend a running program and give you control of the shell.                             |
### Basic Linux Commands
|Command|Syntax     |Purpose                                                             |
|-------|-----------|--------------------------------------------------------------------|
|ls     |ls [option]|Lists the contents of the current directory.                        |
|cat    |cat        |Display the contents of a text file on the screen.                  |
|       |[file-name]|                                                                    |
|cd     |cd /etc    |Change from one directory to another.                               |
|pwd    |pwd        |Displays the present working directory.                             |
|whoami |whoami     |Displays the username of the current user.                          |
|touch  |touch      |Create a new empty file or update the timestamp on an existing file.|
|       |[file-name]|                                                                    |
|man    |man        |Display manual, or help, pages for a specific command.              |
|       |[command]  |                                                                    |
|whatis |whatis     |Procvides a brief description of the specified command.             |
|       |[command]  |                                                                    |
### Commands Related to Administering Users and Groups
|Command |Syntax            |Purpose                                           |
|--------|------------------|--------------------------------------------------|
|passwd  |passwd [user-name]|Manage user passwords.                            |
|chage   |chage -options    |Manage password settings.                         |
|w       |w                 |Display current users on the system.              |
|who     |who               |Display current users on the system.              |
|useradd |useradd           |Add a user.                                       |
|        |-options          |                                                  |
|        |argument          |                                                  |
|usermod |usermod           |Modify a user.                                    |
|        |-options          |                                                  |
|        |argument          |                                                  |
|userdel |userdel           |Delete a user.                                    |
|        |[user-name]       |                                                  |
|id      |id [user-name]    |Gather and display account information.           |
|groupadd|groupadd          |Create a new group.                               |
|        |[group-name]      |                                                  |
|groupmod|groupmod          |Modify an existing group.                         |
|        |-options          |                                                  |
|        |argument          |                                                  |
|groupdel|groupdel          |Remove an existing group.                         |
|        |[group-name]      |                                                  |
|su      |su - [user-name]  |Switch user to the specified user or account name.|
|sudo    |sudo -options     |Exercise delegated privileges.                    |
|        |[command]         |                                                  |
|pkexec  |pkexec program    |Allows an authorized user to execute an action.   |
|        |argument          |                                                  |
### Permissions Configuration Commands
|Command|Syntax                          |Purpose                                                               |
|-------|--------------------------------|----------------------------------------------------------------------|
|umask  |unmask {number}                 |Alter the default permissions on newly created files and directories. |
|chmod  |chmod [options]                 |Modify the permissions of a file or directory.                        |
|       |{mode} {file/directory          |                                                                      |
|       |name}                           |                                                                      |
|chown  |Varies based on desired outcome:|Change the owner, the group, or both for a file or directory.         |
|       |Change the owner but not the    |                                                                      |
|       |group: chown {newowner}         |                                                                      |
|       |{filename}                      |                                                                      |
|       |Change both the owner           |                                                                      |
|       |and the group: chown            |                                                                      |
|       |{newowner}:{newgroup}           |                                                                      |
|       |{filename}                      |                                                                      |
|       |Change the group but            |                                                                      |
|       |not the owner: chown            |                                                                      |
|       |:{newgroup} {filename}          |                                                                      |
|chgrp  |chgrp {group name}              |Change the group ownership of a file or directory.                    |
|       |{file/directory name}           |                                                                      |
|lsattr |lsattr [options]                |Lists attributes of a file or a directory.                            |
|       |{file/directory names}          |                                                                      |
|chattr |chattr [-R]                     |Change attributes of a file or a directory.                           |
|       |[-v {version}]                  |                                                                      |
|       |[+- {attributes}]               |                                                                      |
|       |{file/directory                 |                                                                      |
|       |names}                          |                                                                      |
|getfacl|getfacl {filename}              |Retrieve the ACLs of files and directories.                           |
|setfacl|setfacl [-bR]                   |Change the permissions associated with the ACL of a file or directory.|
|       |[-mx {acl_spec}]                |                                                                      |
|       |{file/directory                 |                                                                      |
|       |names}                          |                                                                      |
### File Management Commands
|Command|Syntax               |Purpose                                                                                                                                         |
|-------|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
|stat   |stat {file-name}     |Display the metadata in a relatively user-friendly structure.                                                                                   |
|file   |file {file-name}     |Display file information based on the file type.                                                                                                |
|ln     |ln [options]         |Create links, either hard or symbolic.                                                                                                          |
|       |{target-name}        |                                                                                                                                                |
|       |{link-name}          |                                                                                                                                                |
|cd     |cd {path}            |Move your present working directory to another directory.                                                                                       |
|tree   |tree {directory-     |Display the filesystem in a hierarchical structure, perhaps making it easier to understand a directory's location relative to other directories.|
|       |name}                |                                                                                                                                                |
|mkdir  |mkdir {new-          |Create directories along the specified path.                                                                                                    |
|       |directory-name}      |                                                                                                                                                |
|cp     |cp {source-file}     |Copy a file into a new location while retaining the source file in its original location.                                                       |
|       |{new-file}           |                                                                                                                                                |
|mv     |mv {source-          |Place the file elsewhere in the filesystem.                                                                                                     |
|       |location}            |                                                                                                                                                |
|       |{destination-        |                                                                                                                                                |
|       |location}            |                                                                                                                                                |
|mv     |mv {original-        |The rename command in Bash.                                                                                                                     |
|       |filename}            |                                                                                                                                                |
|       |{new-filename}       |                                                                                                                                                |
|rmdir  |rm dir               |Remove (delete) a directory with no files in it.                                                                                                |
|       |{directory-          |                                                                                                                                                |
|       |name}                |                                                                                                                                                |
|rm     |rm [options]         |Remove (delete) a file or non-empty directory.                                                                                                  |
|       |{file-name}          |                                                                                                                                                |
|head   |head {file-name}     |Displays the first 10 lines of a file.                                                                                                          |
|tail   |tail {file-name}     |Displays the last 10 lines of a file.                                                                                                           |
|grep   |grep {character-     |Search for strings of characters within a data stream. Grep is case-sensitive unless the -i option is used.                                     |
|       |string}              |                                                                                                                                                |
|xargs  |command              |Read from standard input and executes a command for each argument provided.                                                                     |
|       |[options]            |                                                                                                                                                |
|       |[arguments] |        |                                                                                                                                                |
|       |xargs [options]      |                                                                                                                                                |
|       |{command}            |                                                                                                                                                |
### Commands for Authoring Text Files
### Software Management Commands
### Commands for Managing Devices, Processes, Memory and the Kernal
### Service Management Commands
### Network Setting Configuration Commands
### Network Security Configuration Commands
### Security Management Commands
### Script Implementation Commands
### IaC Commands
|Command|Syntax                   |Purpose                 |
|-------|-------------------------|------------------------|
|git    |git [options]{subcommand}|Manage Git repositories.|
### Commands for Managing Containers
### Linux Installation Commands
|Command       |Syntax                                     |Purpose                                                              |
|------------- |-------------------------------------------|---------------------------------------------------------------------|

