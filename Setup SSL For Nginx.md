```bash
sudo su -

# checking the given ssl cert and key which is stored in /tmp

ls /tmp 

# installing package manager epel-release and usnig it to install nginx  

yum install epel-release -y 

yum install nginx -y

# editing the configuration file for nginx 
vi /etc/nginx/nginx.conf
 
adding server_name ip of the system
and uncommenting the tls setting and (404 501)
adding location of key and cert 
/etc/pki/CA/certs/ cert here
/etc/pki/CA/services/ key here 

# copying the cert and key to the required location and checking

cp /tmp/nautilus.cert /etc/pki/CA/certs
cp /tmp/nautilus.cert /etc/pki/CA/services

ll /etc/pki/CA/certs/
ll /etc/pki/CA/services/

# deleting the old index.txt and creating a new one with (Welcome!)

cat /etc/nginx/nginx.conf | grep root

ls -lsd /usr/share/nginx/html/index.html

rm /usr/share/nginx/html/index.html

vi /usr/share/nginx/html/index.html  --> Welcome!

cat /usr/share/nginx/html/index.html

# starting nginx service and checking its status and cheching the server using curl request 

systemctl start nginx

systemctl status nginx

curl -Ik https://stapp03  

# if its a 200 ok then exit the app server and on the jump server using the following command to test it 

curl -Ik https://stapp03
```
