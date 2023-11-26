# Lab [5]
## 1. Compress a file by compress, gzip, zip commands and decompress it again. State the differences between compress and gzip commands.
  - compress:
    compress -v filee
    uncompress -v filee
    
  - gzip:
    gzip -v filee
    gunzip -v filee.gz
    
  - zip
    zip -v zfile.zip filee file1 
    unzip zfile.zip
![Q1](./1.1.png)
![Q1](./1.2.png)
![Q1](./1.3.png)
## 2. What is the command used to view the content of a compressed file.
   zcat filee.Z
   unzip -l zfile.zip
![Q2](./2.png)
## 3. Backup /etc directory using tar utility.
    sudo tar -cvf atchive.tar /etc
![Q3](./3.png)
## 4. Starting from your home directory, find all files that were modified in the last two day.
    find ./ -mtime -2
![Q4](./4.png)

## 5. Starting from /etc, find files owned by root user.
   find -user omar
![Q5](./5.png)

## 6. Find all directories in your home directory.
   find / 
   or 
   locate /  
![Q6](./6.png)

## 7. Write a command to search for all files on the system that, its name is “.profile”. 
  locate .profile
![Q7](./7.png)

## 8. Identify the file types of the following: /etc/passwd, /dev/pts/0, /etc, /dev/sda
  file /etc/passwd
  file /dev/pts/0
  file /etc
  file /dev/sda
![Q8](./8.png)

## 9. List the inode numbers of /, /etc, /etc/hosts.
  ls -i /
  ls -i /etc
  ls -i /etc/hosts
![Q9](./9.1.png)
![Q9](./9.2.png)
![Q9](./9.3.png)

## 10. Copy /etc/passwd to your home directory, use the commands diff and cmp, and Edit in the file you copied, and then use these commands again, and check the output.
  ls -s /etc/passwd /boot/passlink
![Q10](./10.1.png)
![Q10](./10.2.png)
![Q10](./10.3.png)
## 11. Create a symbolic link of /etc/passwd in /boot.
  
![Q11](./11.1.png)

## 12. Create a hard link of /etc/passwd in /boot. Could you? Why?
can't create hard link as the directories are in different partitions.
![Q11](./11.2.png)
