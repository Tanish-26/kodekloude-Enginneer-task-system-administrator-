```bash
# install haproxy install application server of statos 
# and configure the logrotate for monthly and 3 rotation

sudo su -

yum install haproxy -y

ls /etc/LogRotate.d
vi /etc/logrotate.d/haproxy
# in the file put 
monthly # if given daily remove it and put monthly 
rotate 3

systemctl start haproxy 
systemctl status haproxy

# do the above for all 3 app servers
```
