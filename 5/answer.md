The steps carried out were:

1. Created a user group ``` filetransfer```
2. Added encrypted user in filetransfer user group 
3. change the ownership of its home directory to root user 
4. create files in its home directory from root user and allow access  to Encrypted 

5. Edited the sshd_config for sftp:
 - Changed the subsyste to ```internal_sftp```
 - Added the newly created filetransfer group 
 
 ```
 Match Group filetransfer
 ChrootDicetory %h
 X11Forwardig no 
 AllowTcpForwarding no
 ForceCommand internal-sftp
 ```
