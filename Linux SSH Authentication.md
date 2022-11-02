Linux SSH Authentication 
configure the thor jump server to login with password into all 3 app server 

```bash
whoami

ssh-keygen -t rsa

ssh-copy-id tony@stapp01

ssh-copy-id steve@stapp02

ssh-copy-id banner@stapp03

ssh tony@stapp01

whoami

ssh steve@stapp02

whoami

ssh banner@stapp03

whoami
```
