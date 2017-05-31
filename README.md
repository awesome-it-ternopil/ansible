# Setup of develop_pc
Uncoment all roles you want to add in developer_pc.yml

Check version of sofware in ansible/group_vars

Check virtualbox extension pack after install virtualbox (automate)

For running role on remote host you must setup user or add extra-vars in command

Prepare user:
```
adduser user
usermod -a -G sudo user
visudo
user ALL=(ALL) NOPASSWD:ALL
```
For start role
```
ansible-playbook -i remote developer_pc.yml --extra-vars "ansible_ssh_user= ansible_ssh_pass="
```
