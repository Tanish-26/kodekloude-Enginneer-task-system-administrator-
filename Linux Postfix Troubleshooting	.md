the mail server is down check what is the issue and relsove it 
```bash
sudo su - 

systemctl start postfix 
systemctl status postfix 

cat /etc/postfix/main.cf |grep inet_interface

vi /etc/postfix/main.cf # ---> inet_insterfaces=localhost just comment it out using #inet_insterfaces=localhost

#check once again 
cat /etc/postfix/main.cf |grep inet_interface 

systemctl start postfix 
systemctl status postfix 

#and to check the postfix service is running or not use telnet 
```
