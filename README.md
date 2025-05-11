sudo apt update
-------------
sudo apt install apt-transport-https ca-certificates curl software-properties-common
--------
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
--------
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"
---
apt-cache policy docker-ce
--------
sudo apt install docker-ce
--------
sudo systemctl status docker


network:
  version: 2
  renderer: networkd
  ethernets:
    eno1:
      dhcp4: false
      dhcp6: false
     addresses:
      - 192.168.10.10/24
     routes:
      - to: default
        via: 192.168.10.1
     nameservers:
       addresses: [192.168.10.1]
