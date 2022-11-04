here we had to install banner on all the application server of stratos 
and the database server of startos 

```bash
#enable SCP on the Jump Server.

sudo su -

sudo yum install -y openssh-clients

#copy the nautilus_banner template 

sudo scp -r /home/thor/nautilus_banner tony@172.16.238.10:/tmp

sudo scp -r /home/thor/nautilus_banner steve@172.16.238.11:/tmp

sudo scp -r /home/thor/nautilus_banner banner@172.16.238.12:/tmp

sshpass peter@172.16.239.10

sudo yum install -y openssh-clients

sudo scp -r /home/thor/nautilus_banner peter@172.16.239.10:/tmp

#Step 5- checking and copying files to right directory and displaying it for all the app server and DB servers 

ssh tony@172.16.238.10

ssh steve@172.16.238.11

ssh banner@172.16.238.12

ssh peter@172.16.239.10

cd /tmp

ls -lrt

sudo mv /tmp/nautilus_banner /etc/motd

ls -l /etc/motd

cat /etc/motd
```
