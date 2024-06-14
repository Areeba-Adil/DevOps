
# Basic Linux Commands with Example

This cheat sheet equips you with essential Linux commands, from easy stuff to more complex tricks.



## 1. File and Directory Commands
## ls

List files and directories

```bash
  ls
```
-l to see detailed information about permissions, ownership, size, and modification date.

```bash
  ls -l
```
-a to reveal hidden files (files starting with a dot)

```bash
  ls -a
```
-h to display file sizes in a more user-friendly format (e.g., KB, MB, GB).

```bash
  ls -lh
```


## cd
Changes the current directory to the specified path.

```bash
  cd /path/to/directory
```


## pwd

Displays the current working directory.
```bash
  pwd
```

## mkdir
Creates a new directory named “directory_name”.
```bash
  mkdir <directory_name>
```
## rm
Use this command with caution! It permanently deletes files and directories.
```bash
  rm <file.txt>
```
Deletes the directory “directory_name” and its contents.

-r Remove directories recursively.
```bash
  rm -r <directory_name>
```
Forcefully deletes the file “file.txt” without confirmation.

-f Force removal without confirmation.
```bash
  rm -f <file.txt>
```
## cp
Copies the file “file.txt” to the specified destination.

```bash
  cp <file.txt> <destination> 
```
Copies the directory “directory” and its contents to the specified destination.

-r  Copy directories recursively.
```bash
  cp -r <directory> <destination>  
```
## mv
Renames the file “file.txt” to “new_name.txt”.
```bash
  mv <file.txt> <new_name.txt> 
```
Moves the file “file.txt” to the specified directory.
```bash
  mv <file.txt> <directory>
```
## touch
Create an empty file or update file timestamps.
```bash
  touch <file.txt>
```
## cat
View the contents of a file.
```bash
  cat <file.txt>
```
## head
 Display the first few lines of a file.
```bash
  head <file.txt>
```
Displays the first 5 lines of the file “file.txt”.

-n specify the number of lines to display.
```bash
  head -n 5 <file.txt>
```
## tail
Display the last few lines of a file.
```bash
  tail <file.txt>
```
Displays the last 5 lines of the file “file.txt”.

-n specify the number of lines to display.
```bash
  tail -n 5 <file.txt>
```
## ln
Creates a symbolic link named “link_name” pointing to “source_file”.

-s create symbolic (soft) links.
```bash
  ln -s <source_file> <link_name>
```
## find
Searches for all files with the extension “.txt” in the specified directory.

-name Search by filename.

-type Search by file type.
```bash
  find /path/to/search -name “*.txt” 
```
## 2. File Permission Commands
## chmod
Change file permissions.

u: User/owner permissions.

g: Group permissions.

o: Other permissions.

+: Add permissions.

–: Remove permissions.

=: Set permissions explicitly.

Grants read, write, and execute permissions to the owner of the file.
```bash
chmod u+rwx <file.txt> 
```
## chown
Change file ownership.
```bash
chown user <file.txt> 
```
## chgrp
Change group ownership.
```bash
chgrp group <file.txt>
```
## umask
Sets the default file permissions to read and write for the owner, and read-only for group and others.
```bash
umask 002
```
## 3. File Compression and Archiving Commands
## tar
Creates a compressed tar archive named “archive.tar.gz” containing the files in the “files/” directory.

-c: Create a new archive.

-x: Extract files from an archive.

-f: Specify the archive file name.

-v: Verbose mode.

-z: Compress the archive with gzip.

-j: Compress the archive with bzip2.
```bash
tar -czvf archive.tar.gz files/ 
```
## gzip
Compresses the file “file.txt” and renames it as “file.txt.gz”.

-d: Decompress files.
```bash
gzip <file.txt> 
```
## zip
Creates a zip archive named “archive.zip” containing “file1.txt” and “file2.txt”.

-r recursively include directories.

```bash
zip archive.zip <file1.txt> <file2.txt> 
```
## 4. Process Management Commands
## ps

Shows all running processes with detailed information.
```bash
ps aux
```

## top
Displays a dynamic view of system processes and their resource usage.

```bash
top
```
## kill

Terminates the process with the specified process ID.

-9 Forcefully kill a process.
```bash
kill PID
```
## pkill
Terminates all processes with the specified name.

```bash
pkill <process_name>
```
## pgrep
Lists all processes with the specified name.

```bash
pgrep <process_name> 
```
## grep
Used to search for specific patterns or regular expressions in text files or streams and display matching lines.

-i: Ignore case distinctions while searching.
```bash
grep -i “hello” <file.txt>
```
-v: Invert the match, displaying non-matching lines.
```bash
grep -v “error” <file.txt>
```
-r or -R: Recursively search directories for matching patterns.
```bash
grep -r “pattern” directory/
```
-l: Print only the names of files containing matches.
```bash
grep -l “keyword” <file.txt>
```
-n: Display line numbers alongside matching lines.
```bash
grep -n “pattern” <file.txt>
```
-w: Match whole words only, rather than partial matches.
```bash
grep -w "pattern" <file.txt>
```
-c: Count the number of matching lines instead of 
displaying them.
```bash
grep -c "pattern" <file.txt>
```
-e: Specify multiple patterns to search for.
```bash
grep -e "pattern1" -e "pattern2" <file.txt>
```
-A: Display lines after the matching line.
```bash
grep -A number "pattern" <file.txt>
```
-B: Display lines before the matching line.
```bash
grep -B number "pattern" <file.txt>
```
-C: Display lines both before and after the matching line.
```bash
grep -C number "pattern" <file.txt>
```
## 5. System Information Commands
## whoami
Display current username.
```bash
whoami
```
## df
Displays disk space usage in a human-readable format.
```bash
df -h
```
## du
Provides the total size of the specified directory.

-h Human-readable sizes.

-s Display total size only.

```bash
du -sh directory/ 
```
## free
Displays memory usage in a human-readable format.

```bash
free -h
```
## 6. Networking Commands
## iconfig
Display network interface information.
```bash
iconfig
```
## wget
Download files from the web.
```bash
wget <URL>
```
## curl
Transfer data to or from a server.
```bash
curl <URL>
```