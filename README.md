# Common-commands

#### Python environments
```bash
python -m venv .venv
source .venv/bin/activate
```
#### Setup ssh
```bash
pip install openssh-wrapper
or apt install  openssh-server
or sudo yum –y install openssh-server openssh-clients

# Systemctl enable ssh
service ssh start
service ssh status
```

#### ssh-keygen
```bash
source ~/.bashrc
sudo vim /etc/ssh/sshd_config

# Use this setup
# PubkeyAuthentication yes
# PermitRootLogin yes

service ssh restart
```

#### Setup public key
```bash
# id_rsa.pub -> .ssh/authorized_keys
cat ~/.ssh/id_rsa.pub | ssh username@xx.xx.xx.xx 'cat >> .ssh/authorized_keys'
```
