# Ansible
Experimenting ansible to fetch/configure devices including servers, routers,switches,firewalls

#First experiment: local PC + vmware server1(ubuntu) + vmware server(gns)
#inventory.ini is
#[local servers]
server1 ansible_host=172.16.73.156 ansible_user=root ansible_password=eve
server2 ansible_host=172.16.73.154 ansible_user=gns3 ansible_password=gns3
#command
ansible all -m ping -i inventory.ini
#command output
(base) MacBook$ ansible all -m ping -i inventory.ini
[WARNING]: Host 'server2' is using the discovered Python interpreter at '/usr/bin/python3.9', but future installation of another Python interpreter could cause a different interpreter to be discovered. See https://docs.ansible.com/ansible-core/2.20/reference_appendices/interpreter_discovery.html for more information.
server2 | SUCCESS => {
    "ansible_facts": {
        "discovered_interpreter_python": "/usr/bin/python3.9"
    },
    "changed": false,
    "ping": "pong"
}
[WARNING]: Host 'server1' is using the discovered Python interpreter at '/usr/bin/python3.10', but future installation of another Python interpreter could cause a different interpreter to be discovered. See https://docs.ansible.com/ansible-core/2.20/reference_appendices/interpreter_discovery.html for more information.
server1 | SUCCESS => {
    "ansible_facts": {
        "discovered_interpreter_python": "/usr/bin/python3.10"
    },
    "changed": false,
    "ping": "pong"
}

