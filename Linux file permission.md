there was one app server and a file which automatically load on system bootup but its permission was not set to executable
file was in /tmp/xfusioncrop.sh
changed file permisson as following

```bash
cd /tmp/xfusioncrop.sh
ls -la 
sudo chmod 666 xfusioncrop.sh 
sudo chmod +x xfusioncrop.sh 
```

