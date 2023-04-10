```bash
sudo su -

# installing and starting the service
yum install -y postgresql-server postgresql-contrib
postgresql-setup initdb
systemctl enable postgresql && systemctl start postgresql && systemctl status postgresql

# configure the database 
sudo -u postgres psql
CREATE USER kodekloud_top WITH ENCRYPTED PASSWORD''; 
CREATE DATABASE kodekloud_db6 ;
GRANT ALL PRIVILEGES ON DATABASE kodekloud_db6 TO kodekloud_top ;
exit

# implimenting changes in config file of the db
vi /var/lib/pgsql/data/postgresql.conf
# uncomment this line
listen_addresses = 'localhost' # what IP address(es)to listen on

vi /var/lib/pgsql/data/pg_hba.conf

host all all 127.0.0.1/32 md5
local all all md5

# restarting and testing the service
sudo systemctl restart postgresql

psql -U kodekloud_rin  -d kodekloud_db9 -h 127.0.0.1 -W
```
