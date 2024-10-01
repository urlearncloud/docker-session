# Docker installation on Ubuntu ( AWS EC2 :- Ubuntu )

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
sudo usermod -aG docker ${USER}
sudo reboot
sudo systemctl start docker
sudo systemctl enable docker
```

```sh
sudo usermod -aG docker ${USER}
sudo reboot
sudo systemctl start docker
sudo systemctl enable docker
```

```sh
sudo systemctl start docker
sudo systemctl enable docker
```

SUCCESSFULLY  INSTALLED
