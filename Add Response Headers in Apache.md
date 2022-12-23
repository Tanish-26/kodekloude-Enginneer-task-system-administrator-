```bash
sudo su -

yum install -y httpd

vi /etc/httpd/conf/httpd.conf 
# adding the following lines to the file
Listen 3000

Header set X-XSS-Protection "1; mode=block"

Header always append X-Frame-Options SAMEORIGIN

Header set X-Content-Type-Options nosniff

# checking the changes
cat /etc/httpd/conf/httpd.conf | grep Listen
cat /etc/httpd/conf/httpd.conf | grep X 

# starting and checking the status of the server
systemctl start httpd
systemctl status httpd

# adding index.html file 
vi /var/www/html/index.html

# adding this line to the file 
Welcome to the xFusionCorp Industries!

cat /var/www/html/index.html

# checking the the changes 
curl http://stapp02:3000
```
