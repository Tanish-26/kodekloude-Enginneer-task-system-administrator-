```bash
sudo su - 

# installing the apache tomcat server 
yum install tomcat -y

# configure the server and the required settings
cat /usr/share/tomcat/conf/server.xml | port
vi /usr/share/tomcat/conf/server.xml
change the connector port and the executer port to the required port

#copying file to the required location
# open a new terminal and copy the file from jump sever to app server
scp /tmp/ROOT.war tony@stapp01:/tmp
# on the app server 1  
cp /tmp/ROOT.war /usr/share/tomcat/webapps
ll /usr/share/tomcat/webapps

#starting and checking the server status
systemctl status tomcat
systemctl start tomcat
systemctl status tomcat

# testing the server and the changes made 
curl -i localhost:6300/ROOT

```
