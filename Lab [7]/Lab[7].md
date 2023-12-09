# Lab [7]
## 1. Using the useradd command, add accounts for the following users in your system: user1, user2,
## user3, user4, user5, user6 and user7. Remember to give each user a password.
![Q1](./Pics/1.png)
![Q1](./Pics/1.1.png)
![Q1](./Pics/1.2.png)

## 2. Using the groupadd command, add the following groups to your system.
## Group GID
## sales 10000
## hr 10001
## web 10002
## Why should you set GID in this manner instead of allowing the system to set the GID by default?
### We specify the id because the id is generated from 1000 by default as the users ids so we need 
### to specify higher number than 1000 that won't interfer with group ids.
![Q1](./Pics/2.png)

## 3. Using the usermod command to add user1 and user2 to the sales secondary group, user3 and user4 to the hr secondary group. User5 and user6 to web secondary group. 
## And add user7 to all secondary groups
![Q1](./Pics/3.png)

## 4. Login as each user and use id command to verify that they are in the appropriate groups. How else might you verify this information?
![Q1](./Pics/4.png)
![Q1](./Pics/4.1.png)

## 5. Create a directory called /depts with a sales, hr, and web directory within the /depts directory.
![Q1](./Pics/5.png)

## 6. Using the chgrp command, set the group ownership of each directory to the group with the matching name
![Q1](./Pics/6.png)

## 7. Set the permissions on the /depts directory to 755, and each subdirectory to 770
![Q1](./Pics/7.png)

## 8. Set the set-gid bit on each departmental directory
![Q1](./Pics/8.png)

## 9. Use the su command to switch to the user2 account and attempt the following commands:
- touch /depts/sales/user2.txt
- touch /depts/hr/ user2.txt
- touch /depts/web/ user2.txt
### Which of these commands succeeded and which failed? What is the group ownership of the files that were created?
#### only the first command succeded to create the fila because user2 is member of group sales that is a group added to the directory and has write and execute commands on this directory
![Q1](./Pics/9.png)
![Q1](./Pics/9.1.png)

## 10. Configure sudoers file to allow user3 and user4 to use /bin/mount and /bin/umount commands, while allowing user5 only to use fdisk command.
![Q1](./Pics/10.1.png)

## 11. Login by user3 and try to unmount /boot.
## 12. Login by user4 and remount /boot. Also try to view the partition table using fdisk.
![Q1](./Pics/11,12.png)

## 13. Create a directory with permissions rwxrwx---, grant a second group (sales) r-x permissions
![Q1](./Pics/13.png)

## 14. create a file on that directory and grant read and write to a second group (sales)
![Q1](./Pics/14.png)

## 15. set the the owning group as the owning group of any newly created file in that directory.
![Q1](./Pics/15.png)

## 16. Grand your colleagues a collective directory called /opt/research, where they can store generated research results. 
## Only members of group profs and grads should be able to create new files in the directory, and new file should have the following properties:
- the directory should be owned by root
- new files should be group owned by group grads
- group profs should automatically have read/write access to new files
- group interns should automatically have read only access to new files
- other users should not be able to access the directory and its contents at all.
![Q1](./Pics/16.png)

## 17. Change your default SELinux mode to permissive and reboot.
![Q1](./Pics/17.png)
![Q1](./Pics/17.1.png)

## 18. After reboot, verify the system is in permissive mode.
![Q1](./Pics/18.png)

## 19. Change the default SELinux mode to enforcing.
![Q1](./Pics/19.png)

## 20. Change the current SELinux mode to enforcing.
![Q1](./Pics/20.png)

## 21. Copy /etc/resolv.conf file to root's home directory.
## 22. Observe the SELinux context of the intial /etc/resolv.conf
![Q1](./Pics/21,22.png)

## 23. Move resolv.conf from root's home directory to /etc/resolv.conf
## 24. Observe the SELinux of the newly copied /etc/resolv.conf
## 25. Restore the SELinux context of the newly positioned /etc/resolv.conf
## 26. Observe the SELinux context of the restored /etc/resolv.conf
![Q1](./Pics/23-26.png)

## 27. Configure OpenSSH to allow pulic key-based login credentials
## 28. Create an SSH key-pair
![Q1](./Pics/28.png)

## 29. Configure to login without the need of a password.
![Q1](./Pics/29.png)
![Q1](./Pics/29.1.png)

## 30. Configure SSH to prevent root logins.
![Q1](./Pics/30.png)

## 31. Configure logrotate default setting to compress log files when they are rotated.
![Q1](./Pics/31.png)
