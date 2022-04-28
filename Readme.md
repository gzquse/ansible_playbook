```
ansible all --key-file ~/.ssh/id_rsa -i inventory -m ping

ansible all -i inventory-a "/bin/echo hello"

ansible all -m ping -u ziqguo --become --become-user ziqguo -i inventory 

ansible-playbook task1.yaml -i inventory 
 
ansible all -m apt -a "name=snapd state=latest" --become -i inventory

ansible all -m apt -a "upgrade=dist" --become -i inventory 

ansible-playbook install_apache.yaml -i inventory

ansible all -i inventory -m gather_facts | grep ansible_distribution
```
