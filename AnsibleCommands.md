LIST OF ANSIBLE COMMANDS TO RUN TASKS:


1) ansible-playbook -i <inventory> <playbook.yaml> <options>

2) ansible-playbook -i inventory playbook1.yaml -e file_state=touch

3) ansible-playbook -i inventory playbook1.yaml --tags create-file -e file_state=touch

4) ansible-playbook -i inventory playbook1.yaml --skip-tags create-file --tags delete-file  -e file_state=touch

5) ansible-playbook -i new_inventory playbook_with_variables.yaml -e file_state=touch --start-at-task='Task 3 for bck'

6) Getting host variables: ansible -m debug -i new_inventory -a "var=hostvars['vm1']['ansible_host']" all
ansible -m debug -i new_inventory -a "var=hostvars" all
 

 7) Testing Plays with check mode without impacting the remote machine or changing anything there: ansible-playbook -i Inventory_files/new_inventory Playbooks/TemplatesDict.yaml --check


 8) Create an Ansible Galaxy: ansible-galaxy init create_user

 9) Login to ansible-galaxy: ansible-galaxy login

 10) Import an ansible galaxy online : ansible-galaxy import <github_user> <github_dir_name>

 11) Search roles on Ansible galaxy: ansible-galaxy search <role_name>

 12) Install a role from ansible galaxy to a specific location ./ : ansible-galaxy install anishsingh20.ansible_galaxy_create_user -p ./

 13) encrypting a file in ansible :  ansible-vault encrypt vault

 14) Edit our vault file: ansible-vault edit <name>