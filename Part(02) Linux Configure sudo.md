```bash
sudo su -

id jim 

cat /etc/sudoers | grep jim

usermod -aG root jim

visudo
      # add the following lines to the end of the file 
      jim ALL=(ALL) NOPASSWD:ALL
      
cat /etc/sudoers | grep jim      

id jim
```
