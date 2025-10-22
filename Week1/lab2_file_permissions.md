# Lab 2: Linux File Permissions

## Objective
Understand and practice modifying Linux file permissions.

## Prerequisites
Completed Lab 1  
Basic understanding of Linux commands

## Background
Linux uses a permission system to control access to files and directories. Permissions are set for three categories:

Owner (u): The user who owns the file  
Group (g): Users in the file's group  
Others (o): All other users  

Each category can have three types of permissions:

Read (r): 4  
Write (w): 2  
Execute (x): 1

## Tasks
### Task 1: Examining Permissions
Create a file called secret.txt  
Use ls -l secret.txt to view its permissions  
Document the permission string (e.g., -rw-r--r--)  
Explain what each part means  

### Task 2: Modifying Permissions with Symbolic Mode
Remove write permission for group: chmod g-w secret.txt  
Add execute permission for owner: chmod u+x secret.txt  
Set read-only for everyone: chmod a-wx,a+r secret.txt  
Verify changes with ls -l  

### Task 3: Modifying Permissions with Numeric Mode
Set permissions to rwxr-xr-x (755): chmod 755 secret.txt  
Set permissions to rw------- (600): chmod 600 secret.txt  
Set permissions to rw-r--r-- (644): chmod 644 secret.txt  

### Task 4: Understanding Impact
Create a script file called test_script.sh  
Try to execute it without execute permission  
Add execute permission and run it successfully  
Document the difference  

## Sample Script
Create test_script.sh with this content:

```bash
#!/bin/bash
echo "Hello from the cybersecurity club!"
echo "Current date: $(date)"
