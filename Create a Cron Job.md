had to create a cron-job in 3 app server in Stratos of Nautilus 

```bash
Add a cron */5 * * * * echo hello > /tmp/cron_text for root user.

sudo yum install -y cronie

sudo systemctl start crond.service

sudo systemctl status crond.service

sudo crontab -e

sudo crontab -u root -l

sudo crontab -l -u root

sudo ls /var/spool/cron

sudo cat /var/spool/cron/root
```
repeated the following for all the servers
