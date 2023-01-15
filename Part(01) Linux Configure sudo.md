Provide sudo access to user yousuf on all app servers.
Make sure you have set up password-less sudo for the user

```bash
#repeat this for all 3 application sever in stratos
sudo su - 

id yousuf 

cat /etc/sudoers | grep yousuf 

visudo 

# add the following lines
yousuf ALL=(ALL)   NOPASSWD:ALL

su - yousuf

id yousuf 

cat /etc/sudoers | grep yousuf
```
