# Lab 1: Linux Command Line Basics

## Objective
Practice essential Linux commands for navigation and file management.

## Prerequisites
- Access to a Linux terminal (Linux VM or WSL)

## Tasks

### Task 1: Navigation
1. Open your terminal
2. Display your current working directory using `pwd`
3. List all files in your home directory (including hidden files)
4. Create a new directory called `cybersec_lab1`
5. Navigate into the new directory

### Task 2: File Creation and Manipulation
1. Create an empty file named `notes.txt`
2. Add the text "Cybersecurity is important!" to the file using echo
3. Display the contents of the file
4. Copy the file to `notes_backup.txt`
5. Create a directory called `backups` and move `notes_backup.txt` into it

### Task 3: Finding Information
1. Use the `man` command to read about the `grep` command
2. Create a file with multiple lines of text
3. Use `grep` to search for a specific word in that file

## Deliverables
Document each command you used and take screenshots showing the results.

## Commands Reference
```bash
pwd          # Print working directory
ls -la       # List all files with details
mkdir        # Make directory
cd           # Change directory
touch        # Create empty file
echo         # Print text (can redirect to file)
cat          # Display file contents
cp           # Copy files
mv           # Move/rename files
grep         # Search text patterns
man          # Display manual pages
```

## Questions
1. What is the difference between absolute and relative paths?
2. What does the `-la` flag do in the `ls` command?
3. How can you view hidden files in Linux?
