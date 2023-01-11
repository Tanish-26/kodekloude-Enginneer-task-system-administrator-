```bash
# on all application server do the following
sudo su -

sudo yum install -y iptables-services

systemctl enable iptables

systemctl start iptables

systemctl status iptables

iptables -R INPUT 5 -p tcp --destination-port 8086 -s 172.16.238.14 -j ACCEPT
iptables -A INPUT -p tcp --destination-port 8086 -j DROP service iptables save

service iptables save

rpm -qc iptables-services

sudo /sbin/iptables-save

iptables -L

# on jump-server
curl stapp01:8086

curl stapp02:8086

curl stapp03:8086
```
