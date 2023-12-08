# Open-stack

![image](https://github.com/rishabh727/Open-stack/assets/143151167/42a8bd4a-77ab-4d68-afd5-d6bc8c5a3e1d)


*OpenStack is an open-source cloud platform that manages distributed compute, network and storage resources, aggregates them into pools, and allows on-demand provisioning of virtual resources through a self-service portal.



# Deploying Openstack by using Devstack


### Update and Upgrade the System:
```
apt update -y && apt upgrade -y
```
### Reboot the system:
```
sudo reboot
```
### Create Stack user:
```
sudo useradd -s /bin/bash -d /opt/stack -m stack
```
```
sudo chmod +x /opt/stack
```
### Assign sudo priveleges:
```
echo "stack ALL=(ALL) NOPASSWD: ALL" | sudo tee /etc/sudoers.d/stack
```
### Switch user:
```
su - stack
```
### Install git and download DevStack:
```
sudo apt install git -y
```
### Clone devstack’s git repository:
```
git clone https://git.openstack.org/openstack-dev/devstack
```
### Create devstack configuration file:
```
cd devstack
```
```
vim local.conf
```
```
:wq
```
```
[[local|localrc]]
# Password for KeyStone, Database, RabbitMQ and Service
ADMIN_PASSWORD=StrongAdminSecret
DATABASE_PASSWORD=$ADMIN_PASSWORD
RABBIT_PASSWORD=$ADMIN_PASSWORD
SERVICE_PASSWORD=$ADMIN_PASSWORD
# Host IP - get your Server/VM IP address from ip addr command
HOST_IP=10.208.0.10
```
### The ADMIN_PASSWORD is the password that you will use to log in to the OpenStack login page. The default username is admin.
### The HOST_IP is your system’s IP address that is obtained by running ifconfig or ip addr commands.
### Install OpenStack:
```
./stack.sh

```
- ***TO REACH YOUR OPENSTACK USER LOGIN DASHBOARD PUT YOUR  PUBLIC IP ON SEARCH ENGINE***

- ***And you will successfully get this interface***
- 
