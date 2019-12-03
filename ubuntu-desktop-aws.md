```
sudo apt-get update && sudo apt-get upgrade
export DEBIAN_FRONTEND=noninteractive
sudo apt install -y cinnamon-desktop-environment
sudo apt-get install xrdp

sudo sed -i.bak '/fi/a #xrdp multiple users configuration \n cinnamon2d-session \n' /etc/xrdp/startwm.sh

echo cinnamon2d-session > ~/.xsession
echo cinnamon2d-session > ~/.Xclients 


sudo service xrdp restart

sudo ufw allow 3389/tcp
sudo /etc/init.d/xrdp restart

sudo vim /etc/ssh/sshd_config
Find the line PasswordAuthentication no and change it to PasswordAuthentication yes

sudo -i
passwd ubuntu

sudo useradd -m charles
sudo passwd charles
sudo usermod -aG admin charles
sudo usermod -aG sudo charles

In RDP session

sudo snap install snap-store
```

https://docs.docker.com/install/linux/docker-ce/ubuntu/#install-docker-engine---community-1
