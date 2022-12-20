```bash 

sudo su -

# checking the file
sudo ls -l /var/www/html/media

sudo ls -l /media

# copying the file to /media folder 
sudo find /var/www/html/media -name '*.css' -exec cp --parents \{\} /media \;

```
