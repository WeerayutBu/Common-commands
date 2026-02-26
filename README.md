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
#### AWS
```bash
# ssh using **ec2-user
ssh -i "aws.pem" ec2-user@xxx.compute-1.amazonaws.com

sudo yum install -y python3
python3 --version
python3 -c "import sys; print(sys.executable)"

# environment moduls
sudo dnf install -y python3 python3-pip python3-virtualenv
python3 -m venv --help
python3 -m venv /tmp/testenv
```
