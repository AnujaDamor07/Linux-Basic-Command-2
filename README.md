# Linux-Basic-Command-2
Man command

The man command in Linux is used to display the manual (or help documentation) for other commands and programs.

Basic Usage:

man [command]

For example:

man ls

This will display the manual for the ls command, which is used to list directory contents.

This would show the manual for the printf function in section 3 (library functions).

Common man Options:
◇ man -k keyword: Search for a keyword across all manual pages.
◇ man -f command: Show a short description of a command (similar to whatis).
◇ man -a command: View all the manual pages for a command (if multiple sections exist).


Info command


File: dir,      Node: Top,      This is the top of the INFO tree.


This is the Info main menu (aka directory node).
A few useful Info commands:


  'q' quits;
  'H' lists all Info commands;
  'h' starts the Info tutorial;
  'mTexinfo RET' visits the Texinfo manual, etc.


* Menu:

Archiving
* Cpio: (cpio).                 Copy-in-copy-out archiver to tape or disk.
* Tar: (tar).                   Making tape (or disk) archives.

Basics
* Bash: (bash).                 The GNU Bourne-Again SHell.
* Common options: (coreutils)Common options.
* Coreutils: (coreutils).       Core GNU (file, text, shell) utilities.
* Date input formats: (coreutils)Date input formats.
* Ed: (ed).                     The GNU line editor
* File permissions: (coreutils)File permissions.
                                Access modes.
* Finding files: (find).        Operating on files matching certain criteria.
* Time: (time).                 GNU time utility.

Compression
-----Info: (dir)Top, 318 lines --Top------------------------------------------------------------------------------------No 'Prev' or 'Up' for this node within this document
Note:- for going out from the command press 'Q"

ls -lh

The ls -lh command is used in Unix-like operating systems (such as Linux or macOS) to list the files and directories in the current working directory in a human-readable format. Here's what each part of the command does:
• ls: Lists the files and directories.
• -l: Displays the listing in long format, showing details like file permissions, owner, group, size, and modification date.
• -h: Makes file sizes "human-readable", which means it will show the sizes in KB, MB, GB, etc., instead of just bytes.


cd commad

cd :- The cd command in Linux (and other Unix-like operating systems) stands for "change directory." It is used to navigate between directories in the filesystem.

Navigate to a directory relative to your current location:
command
cd foldername
• If you're in /home/user and there's a subdirectory docs, cd docs will take you to /home/user/docs.

Go up one directory leval:-
command
cd ..
• The .. represents the parent directory. So, cd .. moves you up one level in the directory structure.

Navigate to the home directory
command
cd
• If you run cd with no arguments, it takes you to your home directory (e.g., /home/username).

Navigate to the previous directory:-
command
cd -
• This command takes you back to the last directory you were in before the current one.

• Navigate to the root directory:
command
cd /
• The / represents the root directory, the top level of the filesystem.

Using ~ for your home directory:
commands
cd ~
• The tilde (~) is shorthand for the current user's home directory.

Some Example

# Start in /home/user
cd Documents       # Move into the "Documents" folder
cd ..              # Go back to /home/user
cd ~               # Move to /home/user (home directory)
cd /var/log        # Go to /var/log (absolute path)
cd /               # Go to the root directory


ls -l command

The ls -l command is used to list files and directories in long format, providing detailed information like file permissions, owner, group, size, and timestamp.

Here's an example output of ls -l:
sql

-rw-r--r-- 1 user group  1234 Nov 30 12:34 file1.txt
drwxr-xr-x 2 user group  4096 Nov 30 12:00 directory1
-rwxr-xr-x 1 user group  5678 Nov 30 11:45 script.sh


Breakdown:
• -rw-r--r--: File permissions
• 1: Number of hard links
• user: File owner
• group: Group ownership
• 1234: File size in bytes
• Nov 30 12:34: Last modification date and time
• file1.txt: File name

ls -l -h command

The ls -l -h command in Linux is used to display a detailed list of files and directories in the current directory, along with human-readable file sizes. Here's a breakdown of the flags:
• -l: This flag stands for "long listing format" and provides detailed information about each file or directory, including permissions, number of links, owner, group, size, and the last modification date.
• -h: This flag stands for "human-readable" and makes the file size easier to understand by displaying it in a more user-friendly format, such as KB, MB, or GB, instead of just raw byte values.


$ ls -l -h
total 28K
drwxr-xr-x 2 user user 4.0K Nov 30 12:34 dir1
-rw-r--r-- 1 user user 1.1M Nov 30 12:35 file1.txt
-rw-r--r-- 1 user user 512K Nov 30 12:36 file2.txt
-rw-r--r-- 1 user user  48K Nov 30 12:37 file3.log



Explanation of the columns in the output:
1. File permissions: drwxr-xr-x (first character indicates whether it's a directory (d) or file (-), followed by read/write/execute permissions for the owner, group, and others).
2. Number of links: The number of hard links to the file/directory.
3. Owner: The user who owns the file.
4. Group: The group associated with the file.
5. File size: The file size in a human-readable format (e.g., 4.0K, 1.1M).
6. Last modification date: The date and time the file was last modified.
7. Filename: The name of the file or directory.
This command is useful for getting a quick overview of file details, especially when you're working with directories that contain many files or when you need to check file sizes in a more understandable format.


ls -l -h -a command


The ls -l -h -a command is used in Unix-based systems (like Linux or macOS) to list files in a directory with detailed information. Here's a breakdown of the options used:
• -l (long format): This option provides a detailed listing of files, showing permissions, number of links, owner, group, size, and timestamp (modification time).
• -h (human-readable): This option displays file sizes in a more human-readable format, such as KB, MB, or GB, rather than in raw byte sizes.
• -a (all): This option includes hidden files and directories (those starting with a dot, like .bashrc or .git).

The output typically looks like this:

drwxr-xr-x  5 user group  4.0K Nov 30 14:23 .
drwxr-xr-x 10 user group  4.0K Nov 29 12:17 ..
-rw-r--r--  1 user group  1.1K Nov 30 14:00 file1.txt
-rw-r--r--  1 user group  2.2M Nov 29 11:56 file2.log
-rw-r--r--  1 user group  1.3K Nov 28 09:32 .hiddenfile


Explanation of the columns:
1. Permissions (e.g., drwxr-xr-x): File type and access permissions.
2. Number of links (e.g., 5): How many hard links point to the file or directory.
3. Owner (e.g., user): The user who owns the file.
4. Group (e.g., group): The group associated with the file.
5. Size (e.g., 4.0K or 2.2M): The size of the file, in a human-readable format.
6. Timestamp (e.g., Nov 30 14:23): Last modification date and time.
7. File/Directory name (e.g., file1.txt): The name of the file or directory.
Hidden files and directories (those starting with a dot) are included in the listing when -a is used.

ls -R command

The ls -R command is used in Unix-based systems (like Linux or macOS) to list all files and directories recursively. This means that it will display the contents of the current directory and all subdirectories.
For example, running ls -R in a directory might produce something like this:

dir1:
file1.txt  file2.txt  subdir1/

dir1/subdir1:
file3.txt  file4.txt

dir2:
file5.txt

dir3:
file6.txt  subdir2/

dir3/subdir2:
file7.txt


ls  -aR  Command
 
 The command ls -aR is used in Unix-like operating systems (like Linux or macOS) to list all files and directories recursively, including hidden files (those starting with a dot .). Here's a breakdown of what the flags mean:
• -a: Lists all files, including hidden files (those that start with a dot).
• -R: Lists directories and their contents recursively, meaning it will display the contents of subdirectories as well.

Example of how ls -aR works:

$ ls -aR
.
..  dir1  file1.txt  .hidden_file
./dir1:
file2.txt  .hidden_file_in_dir

This would list all files and directories in the current directory (.) and its subdirectories, including hidden files.

























