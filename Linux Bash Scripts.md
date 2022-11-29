given a set of instruction to create a bash script to automate some tasks

```bash
sudo su - 

# creating the bash script
cd /scripts

vi ecommerce_backup.sh

-------
cd /var/www/html/
zip -r xfusioncorp_ecommerce.zip ecommerce
cp xfusioncorp_ecommerce.zip /backup/
cd /backup/
scp xfusioncorp_ecommerce.zip clint@172.16.238.16:~/
ssh clint@172.16.238.16 << EOF
    cp /home/clint/xfusioncorp_ecommerce.zip /backup/
EOF
-------

# allowing user to connect without password
ssh-keygen

ssh-copy-id clint@stbkp01

ssh clint@stbkp01

# adding user to the root group
usermod -aG root tony 

# changing file permission to make the bash script executable and checking 
chmod +x ecommerce_backup.sh

ls -la

# executing the file 
sh ecommerce_backup.sh

#checking for the ecommerce_backup.sh file in the app server  
ls /backup 

# checking for the ecommerce_backup.sh file in the backup server

ssh clint@stpbkp01 

ls /backup
```
