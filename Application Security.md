```bash
sudo su -

#checking the iptables 
ls -l /etc/sysconfig/iptables	
cat /etc/sysconfig/iptables 

# checking the sockets or the ports on which the services are running 
ss -tlnp |grep http #apache
ss -tlnp |grep nginx #nginx

# adding the new rules in the iptables 
iptables -A INPUT -p tcp --dport 8085 -m conntrack --ctstate NEW,ESTABLISHED -j ACCEPT

iptables -A INPUT -p tcp --dport 8091 -m conntrack --ctstate NEW -j REJECT

# saving, restarting and checiking the status of iptables service
service iptables save

systemctl start iptables && systemctl status iptables

# checking the iptables if the rules are set right!!
iptables -L

iptables -nvL

# On the jump server checking if the rules set are working 
telnet stbkp01 8091

telnet stbkp01 8085
```
