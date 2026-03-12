# Ansible
Experimenting ansible to fetch/configure devices including servers, routers,switches,firewalls

#First experiment: local PC + vmware server1(ubuntu) + vmware server(gns)
#inventory.ini is
#[local servers]
server1 ansible_host=172.16.73.156 ansible_user=root ansible_password=eve
server2 ansible_host=172.16.73.154 ansible_user=gns3 ansible_password=gns3

#command1 - connectivity test
ansible all -m ping -i inventory.ini

#command2 - Get all facts
ansible all -m setup -i inventory.ini



