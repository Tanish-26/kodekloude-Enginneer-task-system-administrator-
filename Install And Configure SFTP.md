```bash
sudo su - 

# adding a user john and adding the given password to its id 

id john 
useradd john 
or
useradd -d /var/www/data -s /sbin/nologin john 
passwd john ----> <password>

# creating the folder and setting up the required permission to it

mkdir /var/www/data
# if this doesnt work then 
mkdir /var/www
mkdir /var/www/data
chown -R root:root /var/www/data
chmod 755 /var/www/data

now edit the /etc/ssh/sshd_config file using vi 
vi /etc/ssh/sshd_config
-----------------------------
Subsystem sftp internal-sftp
Match User john
ForceCommand internal-sftp
PasswordAuthentication yes
ChrootDirectory /var/www/webdata
PermitTunnel no
AllowAgentForwarding no
AllowTcpForwarding no
X11Forwarding no
-----------------------------

# restart the ssh server and check if it running or not
systemctl restart sshd 
systemctl status sshd

#checking using both ssh and sftp and ssh should be blocked and sftp should be allowed 
#exit on the jump server or open another terminal and checking use the below commands 

ssh john@stapp01

sftp john@stapp01
```
