# Ansible Provision for lxc

## Preparation
- install lxc-dev
- install using pip for package lxc-python2

## Running
- Build container images

for run all apps provision use like this.

```
sudo ansible-playbook -i hosts.ini buildLXC.yml -vvv
```

if only using selected apps you want provision use this.

```
sudo ansible-playbook -i hosts.ini buildLXC.yml/buildRemoteLXC.yml --extra-vars "app=redis-1" -vvv
sudo ansible-playbook -i hosts.ini buildLXC.yml/buildRemoteLXC.yml --extra-vars "app=trivmedia-1" -vvv
sudo ansible-playbook -i hosts.ini buildLXC.yml/buildRemoteLXC.yml --extra-vars "app=mysql-1" -vvv
sudo ansible-playbook -i hosts.ini buildLXC.yml/buildRemoteLXC.yml --extra-vars "app=elasticsearch-1" -vvv
sudo ansible-playbook -i hosts.ini buildLXC.yml/buildRemoteLXC.yml --extra-vars "app=mongodb-1" -vvv
sudo ansible-playbook -i hosts.ini buildLXC.yml/buildRemoteLXC.yml --extra-vars "app=hadoop-1" -vvv
sudo ansible-playbook -i hosts.ini buildLXC.yml/buildRemoteLXC.yml --extra-vars "app=mailblackhole-1" -vvv
sudo ansible-playbook -i hosts.ini buildLXC.yml/buildRemoteLXC.yml --extra-vars "app=postgresql-1" -vvv
sudo ansible-playbook -i hosts.ini buildLXC.yml/buildRemoteLXC.yml --extra-vars "app=orbit-payment" -vvv
sudo ansible-playbook -i hosts.ini buildLXC.yml/buildRemoteLXC.yml --extra-vars "app=perconaxtradb-cluster-[1..3]" -vvv
```
*note:*
1.  find variable app in group_vars/all
