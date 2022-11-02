install NTP on one of the app server 

using following commands 

```bash
ssh banner@stapp03

sudo su -

yum install ntp -y

vi /etc/ntp.conf  ----> server 1.africa.pool.ntp.org

cat /etc/ntp.conf | grep 1.africa
```
