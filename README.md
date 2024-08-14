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
