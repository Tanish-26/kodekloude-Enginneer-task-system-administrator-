the DB server of strotus stopped working  troubleshoot  it
 
```bash
# in the db server of stratos 
sudo su -

systemctl status mariadb 

systemctl restart mariadb #try this 

systemctl start mariadb #try this

# in the /var/lib folder a folder named mysql is missing so first create a foler in /var/lib/ 

mkdir /var/lib/mysql

# the process /usr/libexec/mariadb-prepare-db-dir could not be executed and
# failed so we have to do it mannually in order to start the db server
# in order to start the db server run the command 

sudo /usr/libexec/mariadb-prepare-db-dir

# then start the db server using 

systemctl start mariadb 

systemctl status mariadb
```
