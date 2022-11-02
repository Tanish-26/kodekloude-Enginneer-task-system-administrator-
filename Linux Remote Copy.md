Linux Remote copy
Using rcp(Remote Copy Protocol) or scp(Secure Copy Protocol ) to copy a file from a thor(the jump server to stapp01(app server1))

used the following commands

```bash
ls -lrt /tmp

sudo cat /tmp/nautilus.txt.gpg

sudo scp -r /tmp/nautilus.txt.gpg steve@172.16.238.11:/tmp

ssh steve@stapp02

sshpass -p '******' ssh -o StrictHostKeyChecking=no steve@172.16.238.11

ls -l /tmp

sudo mv /tmp/nautilus.txt.gpg /home/opt

ls -l /home/opt/

sudo cat /home/opt/nautilus.txt.gpg
```
