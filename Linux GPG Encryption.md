```bash
ssh natasha@ststor01

sudo su -

cd /home/

ll

gpg --import public_key.asc

gpg --import private_key.asc

gpg --list-keys

gpg --list-secret-keys

gpg --encrypt -r kodekloud@kodekloud.com --armor < encrypt_me.txt -o encrypted_me.asc

gpg --decrypt decrypt_me.asc > decrypted_me.txt

cat encrypt_me.txt

cat encrypted_me.asc

cat decrypted_me.txt

cat decrypt_me.asc
```
