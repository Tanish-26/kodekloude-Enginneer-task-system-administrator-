```bash
sudo su -

ll /packages/downloaded_rpms/

# creating a yum repo
cd /etc/yum.repos.d/

cat > epel_local.repo

# |-------------------------------------------------|
# |      [epel_local]                               |
# |                                                 |
# |      name=epel_local                            |
# |                                                 |  
# |      baseurl=file:///packages/downloaded_rpms/  | 
# |                                                 |
# |      gpgcheck=0                                 | 
# |                                                 |   
# |      enabled=1                                  |
# |-------------------------------------------------|

# cleaing up and updating repos and listing new repo
sudo yum clean all 

sudo yum update 

sudo yum repolist 

# enabling and using new repo that was created and installing wget using that repo
sudo yum install -y --enablerepo="epel_local" wget
```
