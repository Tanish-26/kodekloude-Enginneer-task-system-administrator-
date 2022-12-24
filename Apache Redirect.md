```bash
sudo su -

# checking on which the server is listening on and redirect info
cat /etc/httpd/conf/httpd.conf | grep Listen
cat /etc/httpd/conf/httpd.conf | grep redirect

# adding the port on which the server has to listen
vi /etc/httpd/conf/httpd.conf
adding the port on which we want the server to listen to 
Listen 3002
cat /etc/httpd/conf/httpd.conf | grep Listen

# adding the redirect config to a new file main.conf and checking the changes made 
vi /etc/httpd/conf.d/main.conf

<VirtualHost *:3002>
ServerName stapp02.stratos.xfusioncorp.com
Redirect 301 / http://www.stapp02.stratos.xfusioncorp.com:3002/
</VirtualHost>

<VirtualHost *:3002>
ServerName www.stapp02.stratos.xfusioncorp.com:3002/blog/
Redirect 302 /blog/ http://www.stapp02.stratos.xfusioncorp.com:3002/news/
</VirtualHost>

cat /etc/httpd/conf.d/main.conf

# starting and checking the status of the server
systemctl restart httpd
systemctl status httpd

# validating the setting changed   
curl http://stapp02.stratos.xfusioncorp.com:3002
curl http://www.stapp02.stratos.xfusioncorp.com:3002/
curl http://www.stapp02.stratos.xfusioncorp.com:3002/news/
curl http://www.stapp02.stratos.xfusioncorp.com:3002/blog
```
