create a use named javed and set its expiry to 2021-04-15
```bash
sudo su -

useradd javed 

chage -E 2021-04-15 javed

chage -l javed 

chage -l javed | grep expiry
```
