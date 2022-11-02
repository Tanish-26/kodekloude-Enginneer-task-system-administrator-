DNS Troubleshooting of app server 1

changed setting's of resolv.conf so the command will be as following

```bash
ssh tony@172.16.238.10 
cd /etc/
cat resolv.conf
sudo vi resolv.conf
         changed setting from 127.0.0.11 to ---> nameserver 8.8.8.8 
                                                 nameserver 8.8.4.4
cat resolv.conf                                                       
```
