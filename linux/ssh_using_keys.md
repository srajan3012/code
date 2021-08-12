## SETUP PASSWORD LESS SSH PUBLIC KEY PRIVATE KEY
### To setup automatic login from machine_A to machine_B:
1. Generate a public and private key pair on machine_A using:
  * `ssh-keygen -t rsa`
2. copy public key generated on machine_A into machine_B
  * `cat ~/id_rsa.pub | ssh machine_B 'cat >> ~/.ssh/authorized_keys'` 
