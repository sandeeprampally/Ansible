# Ansible
Experimenting ansible to fetch/configure devices including servers, routers,switches,firewalls

#First experiment: local PC + vmware server1(ubuntu) + vmware server(gns)

#command1 - connectivity test
ansible all -m ping -i inventory.ini

#command2 - Get all facts
ansible all -m setup -i inventory.ini



