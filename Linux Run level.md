had to changer runlevel in all the application server of startos
ssh into all application server of startos 

```bash
sudo su - 

systemctl get-default

systemctl list-units 

systemctl set-default graphical.target

systemctl start graphical.target

systemctl status graphical.target

systemctl get-default

```  
