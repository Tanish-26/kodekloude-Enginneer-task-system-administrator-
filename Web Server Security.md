On Nautilus App Server 3 it was identified that the Apache web server is exposing the version number. Ensure this server has the appropriate settings to hide the
version number of the Apache web server.
There is a website hosted under /var/www/html/ecommarce on App Server It was detected that the directory /media lists all of its contents while browsing the URL.
Disable the directory browser listing in Apache config.
Also make sure to restart the Apache service after making the changes.
```bash
sudo su -

#checking for the following in the config file 
cat /etc/httpd/conf/httpd.conf |grep ServerTokens

cat /etc/httpd/conf/httpd.conf |grep ServerSignature

cat /etc/httpd/conf/httpd.conf |grep Indexes

#lets add the following to the https.conf file
vi /etc/httpd/conf/httpd.conf 
\\\
# remove Indexes from the following line 
Options Indexes FollowSymLinks ---> Options FollowSymLinks
# and the following line in last line 
ServerTokens Prod
ServerSignature Off

# again check if the changes are made 
cat /etc/httpd/conf/httpd.conf |grep ServerTokens

cat /etc/httpd/conf/httpd.conf |grep ServerSignature

cat /etc/httpd/conf/httpd.conf |grep Indexes

# start the server and check its status 
systemctl start httpd
systemctl status httpd
```
