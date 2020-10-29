create_user
=========

Create a user and a ssh public key on remote hosts, for remote access to the user from remote machines. 

Requirements
------------


# default variables required
# user name
user_name: anishdefault

# Default user state

user_state: present/absent

# SSH key location

ssh_key: /etc/ssh/ssh_host_rsa_key.pub

Role Variables
--------------

NONE

Dependencies
------------

NONE

Example Playbook
----------------

# Create a playbook with below parameters
---
- hosts: vm
  tasks:
     - include_role:
         name: create_user
       vars:
         user_name: anish
         ssh_key: /etc/ssh/ssh_host_rsa_key.pub


License
-------

MIT

Author Information
------------------

Anish Singh Walia(loveeanish@gmail.com)
