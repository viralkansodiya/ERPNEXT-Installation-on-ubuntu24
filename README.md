### Installation Processs

## Prerequisites
### Install ubuntu 24 on your vertual mechine or host with ubuntu 24

## Update and Upgrade Packages

```
sudo apt-get update -y
```

```
sudo apt-get upgrade -y
```
## Create new user on ubuntu

```
sudo adduser [frappe-user]
usermod -a -G sudo [frappe-user]
su [frappe-user] 
cd /home/[frappe-user]
```


## Install Git on Ubuntu

```
sudo apt-get install git
```
## Install Python and setuptools and dev environment

```
sudo apt-get install python3-dev python3.12-dev python3-setuptools python3-pip
```

## Installation of virtual-environment for python 3.12

```
sudo apt-get install python3.12-venv
```

## Install Software Common Properties 

```
sudo apt-get install software-properties-common

```

## Install MariaDB

```
sudo apt install mariadb-server mariadb-client

```

## Install Redis Server

```
sudo apt-get install redis-server
```

## Install Other Packages Which Helps You to Convert HTML to PDF

```
sudo apt-get install xvfb libfontconfig wkhtmltopdf
sudo apt-get install libmysqlclient-dev
```

## Install and setup MySql Server
 
```
sudo mysql_secure_installation
```

 * Enter your current password for root (enter for none):
   * if you have root pass then input otherwise you can press "Enter" key
 * Switch to unix_socket authentication [Y/N]: Y
 * Change the root password [Y/n]: 
   * 'Y' if you want to change
 * Remove anonymous user [Y/N]: Y
 * Disallow root login remotely? [Y/n]: N
 * Remove test database and access to it? [Y/n]: Y
 * Reload privilege tables now? [Y/n]: Y

## Edit you mysql config file 

```
sudo nano /etc/mysql/my.cnf
```

Copy this below section and past in to your config file

```

[mysqld]
character-set-client-handshake = FALSE
character-set-server = utf8mb4
collation-server = utf8mb4_unicode_ci

[mysql]
default-character-set = utf8mb4

```

## Install Curl

```
sudo apt install curl
```

## Install Node

```
curl https://raw.githubusercontent.com/creationix/nvm/master/install.sh | bash

source ~/.profile

nvm install 18
```

## Install npm

```
sudo apt-get install npm

```

## Install yarn

```
sudo npm install -g yarn

```

## Install frappe-bench

```
sudo pip3 install frappe-bench
```

## Initialize Frappe Bench

```
sudo pip3 install frappe-bench --break-system-packages
```

## Initialize Frappe Bench in a specific version

```
bench init --frappe-branch version-15 frappe-bench
```

```
cd frappe-bench
```

## Apply a permission to user directory

```
chmod -R o+rx /home/[frappe-user]

```

## Create a new site

```
bench new-site [site-name]
```

## Get Erpnext Version-15 and install on your site

```
bench get-app --branch version-15 erpnext
```

```
bench install-app erpnext
```

## Set up your site for production

```
bench --site [site-name] enable-scheduler
```

```
bench --site [site-name] set-maintenance-mode off
```

### Setup virtual environment if not setup

## Setup

```
sudo apt install python3-venv
python3 -m venv env
```

## Active your virtual environment

```
source env/bin/activate
```

## Install ansible (Python Package)

```
sudo /usr/bin/python3 -m pip install ansible --break-system-packages
```

## Install fail2ban

```
sudo apt install fail2ban
```

## Install and setup nginx

```
sudo apt update

sudo apt install nginx
```
## Install and setup supervisor

```
sudo apt update && sudo apt install supervisor
```

## Setup production
```
sudo bench setup production [frappe-user]
```
<hr>

# Get other standard and other apps from your github account

Standard App

```
bench get-app --branch [branch-name or version] [app name]
```

App from git hub account

```
bench get-app --branch [branch-name] [app-name] [github remote link]
```
