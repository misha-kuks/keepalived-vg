This project deploy 3 VMs on ubuntu server 20.04. Two nodes with nginx and keepalived and one with mysql server.
To start deploy:
1. vagrant up
2. ansible-playbook site.yml

Stateless servers:
web1 192.168.56.50
web2 192.168.56.51

Statefull:
db1 192.168.56.200

Keepalived ip 192.168.56.10

Add line "demosite.local 192.168.56.10" in you hosts file.

When deploy finished, you can open this link http://demosite.local/wp-admin/install.php


Warning: 
Site ru.worpress.org can block downloads package. You can download this package manualy and copy to web servers.