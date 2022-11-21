---
id: qfhatiojg542x6a4yprmtz8
title: Debian
desc: ''
updated: 1659219845146
created: 1658540469218
---
# Setup
## Config
### Create Sudo User
1. Add user  

		adduser $username

(set password)

2. Add to sudo group  

		usermod -aG sudo $username

**1-2. Create and add user**

		adduser admin --ingroup sudo

3. Verify groupadd

		getent group sudo

4. Switch to user

		su - $username

### [[computer.docker]]
```
sudo apt-get update
sudo apt-get install \
    ca-certificates \
    curl \
    gnupg \
    lsb-release
sudo mkdir -p /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/debian/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/debian \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin
```
![[computer.docker#add-user--post-install-setup,1:#*]]

### Add Swap
1. see free memory

  sudo swapon -s
  free -m

sudo fallocate -l 2G /swapfile 
sudo chmod 600 /swapfile
sudo mkswap /swapfile 
sudo swapon /swapfile 