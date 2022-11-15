have to install cups in all application server of stratos and make sure that the server is running on boot

repeat the following process for all 3 application server in stratos  
```bash

sudo su -

yum install nscd -y

systemctl start cups

systemctl status cups

systemctl restart cups

systemctl status cups

```
