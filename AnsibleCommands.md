LIST OF ANSIBLE COMMANDS TO RUN TASKS:


1) ansible-playbook -i <inventory> <playbook.yaml> <options>


2) ansible-playbook -i inventory playbook1.yaml -e file_state=touch

3) ansible-playbook -i inventory playbook1.yaml --tags create-file -e file_state=touch

4) ansible-playbook -i inventory playbook1.yaml --skip-tags create-file --tags delete-file  -e file_state=touch