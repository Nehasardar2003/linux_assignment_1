# Linux Commands Quick Reference

This README provides a handy reference for essential Linux commands, covering file and directory management, file permissions, searching, archiving, and system monitoring.

---

## 1. File and Directory Management

### Copying Files
cp file.txt backup/ # Copy file.txt to backup directory
cp -r dir1 dir2 # Copy directory recursively

### Removing Files and Directories
rm file.txt # Remove a file
rm -r directory_name # Remove directory recursively

### Moving/Renaming Files and Directories
mv oldname.txt newname.txt # Rename a file
mv file.txt /path/to/dir # Move file to directory

### Create an Empty File
touch newfile.txt # Create an empty file

### Show Current Working Directory
pwd

### List Directory Contents
ls # List files
ls -l # Long format listing
ls -a # Include hidden files

---

## 2. File Permissions & Ownership

### Change Permissions
chmod 700 script.sh # Owner: read, write, execute only
chmod ug+rw file.txt # Add read and write to user and group

### Change Ownership
sudo chown user:group file.txt

---

## 3. Viewing File Contents

### View Entire File
cat file.txt

### View Head and Tail
head -n 10 file.txt # First 10 lines
tail -n 10 file.txt # Last 10 lines
tail -f file.txt # Follow file changes live

### Page-by-Page Viewing
less file.txt
more file.txt

---

## 4. Searching and Text Processing

### Search Text with `grep`
grep 'pattern' file.txt
grep -r 'pattern' dir/ # Recursive search

### Extract Columns with `awk`
awk '{print $2}' file.txt # Print second column

### Find and Replace with `sed`
sed 's/old/new/g' file.txt # Replace all occurrences

### Extract with `cut`
cut -d, -f1 file.csv # Extract first CSV column
cut -c10-25 file.txt # Extract chars 10 to 25

---

## 5. Archiving and Compression

### Creating and Extracting Archives
tar -czvf archive.tar.gz dir/ # Create compressed tarball
tar -xzvf archive.tar.gz # Extract archive

### Zip and Unzip Files
zip -r archive.zip folder/
unzip archive.zip
unzip -l archive.zip # List contents without extracting

---

## 6. System Monitoring and Process Management

### List Processes
ps -ef # All running processes
top # Real-time process monitoring
htop # Interactive process viewer

### Kill a Process
kill <pid> # Send SIGTERM
kill -9 <pid> # Force kill with SIGKILL

---

## 7. Disk Usage and File Sizes

### Show Sizes in Human Readable Format
ls -lh # List with sizes in KB, MB, etc.
du -sh dir/ # Disk usage summary for directory
df -h # Disk space usage of all mounted filesystems

---

## 8. File and Directory Creation

### Make Nested Directories
mkdir -p parent/child/grandchild

### Create Symbolic and Hard Links
ln file1.txt hardlink.txt # Hard link
ln -s file2.txt softlink.txt # Symbolic link

---

## 9. Miscellaneous Handy Commands

### Show Command History
history # Show all commands history
history 10 # Show last 10 commands

### Display Current Date and Calendar
date
cal

### Change System Date and Time (requires sudo)
sudo date -s "2025-01-15 14:30:00"

### Find Files Modified Recently
find /path -type f -mtime -1 # Files modified in last 24 hours
find /home -type f -size +100M # Files larger than 100 MB

### Count Word Occurrences in a File
grep -o 'word' file.txt | wc -l

### Monitor Real-Time Log Updates
tail -f application.log

---

For help on any command, use:
man command_name

This quick reference should assist with daily Linux command line tasks and operations.

---

*Prepared based on Linux commands practice and common usage examples.*

