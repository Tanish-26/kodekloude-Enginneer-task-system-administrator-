disable root login in all application server of stratos

```bash
#do this all all 3 application server
sudo su -

cat /etc/ssh/sshd | grep PermitRootLogin

vi /etc/ssh/sshd

cat /etc/ssh/sshd | grep PermitRootLogin

systemctl restart sshd

sysytemctl status sshd

cat /etc/ssh/sshd
```
