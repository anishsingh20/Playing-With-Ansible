# Playing-With-Ansible
This repository contains code &amp; some basic examples on using Ansible to manage a set of host target machine.


### List of Ansible Modules

[Module Index](https://docs.ansible.com/ansible/2.8/modules/modules_by_category.html)


### Important Ansible commands

LIST OF ANSIBLE COMMANDS TO RUN TASKS:


```ansible
ansible-playbook -i <playbook.yaml>
```

```ansible
ansible-playbook -i inventory playbook1.yaml -e file_state=touch
```
```ansible
ansible-playbook -i inventory playbook1.yaml --tags create-file -e file_state=touch
```

```ansible
ansible-playbook -i inventory playbook1.yaml --skip-tags create-file --tags delete-file -e file_state=touch
```

```ansible
ansible-playbook -i new_inventory playbook_with_variables.yaml -e file_state=touch --start-at-task='Task 3 for bck'
```
Getting host variables: 

```ansible
ansible -m debug -i new_inventory -a "var=hostvars['vm1']['ansible_host']" all ansible -m debug -i new_inventory -a "var=hostvars" all
```
Testing Plays with check mode without impacting the remote machine or changing anything there: 
```ansible
ansible-playbook -i Inventory_files/new_inventory Playbooks/TemplatesDict.yaml --check
```

Create an Ansible Galaxy: 

```ansible
ansible-galaxy init create_user
```
Login to ansible-galaxy: 
```ansible
ansible-galaxy login
```

Import an ansible galaxy online : 

```ansible
ansible-galaxy import <github_user> <github_dir_name>
```


Search roles on Ansible galaxy: 
```ansible
ansible-galaxy search <role_name>
```
Install a role from ansible galaxy to a specific location ./ : 

```ansible
ansible-galaxy install anishsingh20.ansible_galaxy_create_user -p ./
```

encrypting a file in ansible : 
```ansible
ansible-vault encrypt vault
```
Edit our vault file: 
```ansible
ansible-vault edit
```
