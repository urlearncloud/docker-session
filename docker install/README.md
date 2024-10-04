# Docker installation on Ubuntu ( AWS EC2 :- Ubuntu )👨‍💻

## 1. Create a Ubuntu ec2 instance

AMi = ubuntu-22  --->  keypair = ubunu-key.pem/.ppk   --->  instance types = t2.micro

Security group ------> SSH,HTTP,HTTPS (anywhere)

## 2. Connect your instance & then run below commands

```sh
sudo apt update
sudo apt install docker.io -y
sudo systemctl start docker
sudo systemctl enable docker
docker --version
```

```sh
sudo usermod -aG docker ${USER}
sudo reboot
```

```sh
sudo systemctl start docker
sudo systemctl enable docker
```

SUCCESSFULLY  INSTALLED



# Docker installation on Linux ( AWS EC2 :- Linux )👨‍💻


## 1. Create a Linux ec2 instance

AMi = Linux-2  --->  keypair = linux-key.pem/.ppk   --->  instance types = t2.micro

Security group ------> SSH,HTTP,HTTPS (anywhere)

## 2. Connect your instance & then run below commands

```sh
sudo yum update -y
sudo amazon-linux-extras install docker -y   <------------( for linux-2 version only ) // sudo yum install docker -y  <--------------(for linux only)
sudo service docker start
docker --version
```

```sh
sudo usermod -aG docker $USER
sudo reboot
sudo service docker start
```

```sh
sudo service docker start
```
