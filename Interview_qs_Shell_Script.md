
# Top Most Asked Shell Scripting Interview Questions

### 1. List some of the commonly used shell commands ?
```bash
ls: lists the contents of a directory.
pwd: prints the current working directory.
cd: This is used to change directory.
mkdir: This creates a new directory.
rmdir: This removes an empty directory.
mv: This is used to move or rename files and directories.
cp: This copies files and directories.
rm: This removes files or directories.
touch: This creates an empty file.
```
### 2. Write a simple shell script to list all processes 
```bash 
#!/bin/bash

# Use ps command to list all processes
ps -e

exit 0
```
### 3.Write a script to print only errors from a remote log
```bash
#!/bin/bash

curl <URL> | grep ERRORS
```
### 4.Write a shell script to print numbers divided by 3 & 5 and not 15
```bash 
#!/bin/bash

# Loop through numbers from 1 to 100 (adjust as needed)
for num in {1..100}
do
  # Check if divisible by 3 and 5 (but not by 15)
  if [[ $((num % 3)) == 0 ]] && [[ $((num % 5)) == 0 ]] && [[ $num != 15 ]]; then
    echo "$num"
  fi
done
```
### 5.Write a script to print number of "S" in Mississippi
```bash 
#!/bin/bash

word="Mississippi"
s_count=$(echo $word | grep -o  'S' <<< $word | wc -l)

echo "There are $s_count 'S' in '$word'."
```
### 6.How will you debug the shell script?
```bash 
set -x
```
### 7.What is crontab in Linux? Can you provide an example of usage?
Crontab in Linux lets you schedule tasks. It's a file containing commands and their schedules. You edit the crontab using crontab -e and write entries with a specific format. For example, to run a backup script at midnight every day:
```bash
0 0 * * * /path/to/backup_script.sh
```
### 8. How to open a read-only file?
```bash 
cat -r file.txt
```
### 9. What is a difference between soft and hard link?
Soft link (symbolic link) acts like a shortcut to a file, pointing to its location. A hard link creates another reference to the same data block, so deleting one won't affect the other as long as the data is still referenced elsewhere.
### 10. What is a difference between break and continue statements ?
Both break and continue alter loop flow in shell scripts, but target different points:

Break: Exits the entire loop immediately, skipping any remaining iterations.

Continue: Skips the current iteration of the loop and moves on to the next one.
### 11. What are some disadvantages of Shell scripting?
Shell scripting has limitations:

1- Slower execution compared to compiled languages.

2- Less suited for complex tasks due to limited data structures and error handling.

3- Prone to errors as mistakes can have a bigger impact compared to some other programming languages.
### 12. What a different types of loops and when to use?
1- for loop: Iterate a fixed number of times, good for processing lists or arrays. 

```for item in list; do command; done  ``` 

2- while loop: Execute commands as long as a condition is true, useful for repetitive tasks until a certain point. 

``` while condition; do command; done ```

3- until loop: Similar to while, but keeps looping until the condition becomes true, helpful for waiting until something happens. 

``` until condition; do command; done ```

### 13. Is bash dynamic or statically typed and why?
Bash is a dynamically typed language. You don't declare variable types beforehand. The script interprets the type based on the value assigned during execution. This makes it flexible but can lead to errors if you use a variable with an unexpected type.

### 14. Explain about a network troubleshooting utility?
Network troubleshooting utilities are tools that help diagnose and fix issues within computer networks. They can pinpoint problems like connection failures, slow speeds, or malfunctions in network devices.
```traceroute <URL>```

### 15. How will you sort list on names in a file ?
You can sort a list of names in a file using ```sort``` command

```sort -k1 <file.txt> ```

This sorts the file "file.txt" based on the first field (key 1), which assumes names are in the first column 

### 16. How will you manage logs of a system that generate huge log files everyday?

Here are some ways to manage logs of a system generating large files daily:

1- Log Rotation: Use a tool like ```logrotate``` to automatically compress and archive old logs, freeing up disk space and keeping recent entries accessible.

2- Log Aggregation: Send logs to a centralized log management system for easier analysis and filtering, reducing the load on individual machines.

3- Log Level Control: Adjust log levels (e.g., debug vs. error) to only capture essential information, minimizing log volume.

