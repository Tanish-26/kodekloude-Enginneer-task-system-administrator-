had to change and copy some file owned by rose in a folder

```bash
sudo su -

ls -lrt /home/usersdata

ls -lrt /media/

find /home/usersdata/ -type f -user ravi |wc -l

find /home/usersdata/ -type f -user ravi -exec cp --parents {} /ecommerce \;

ls -lrt /media/home/usersdata/
```
