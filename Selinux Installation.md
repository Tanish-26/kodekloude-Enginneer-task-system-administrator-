installing selinux and change few config

```bash

# app server 3

sudo su -

# installing selinux along with its dependencies
yum install selinux* -y 

cat /etc/selinux/config 

# In the file where SELINUX=enforcing change it to SELINUX=disbaled

vi /etc/selinuc/config  ------------------>         SELINUX=enforcing --> SELINUX=disbaled

cat /etc/selinux/config | grep SELINUX

# to check the status
getenforce 

```
