create a collaborative directory with permission & ownership set to only sysops group

```bash
sudo su -

#create new directory

mkdir -p /sysops/data

ll -lsd /sysops/data/

ls -la /sysops/data/

#change group ownership 

chgrp -R sysops /sysops/data

ll -lsd /sysops/data

#changing group permission

chmod -R 2770 /sysops/data

ll -lsd /sysops/data/

ls -ld /sysops/data/

```
