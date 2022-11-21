replace some word in backup server of nautilus stratos
```bash

sudo su -

cd /root 

cat nautilus.xml | grep About 

sudo sed -i 's#About#Maritime#g' nautilus.xml

cat nautilus.xml | grep About

cat nautilus.xml | grep Maritime
```
