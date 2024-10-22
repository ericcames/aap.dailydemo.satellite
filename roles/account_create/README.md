linux_account_create
=========
```
This role will create user accounts
```
Requirements
------------
```
Root access on the machines in the inventory
Vault Credential in Ansible Automation Platform
Vaulted file in the format of files/user_list_example.yml
```
Role Variables
--------------
```
account_create_user_list_vault: ames_user_list_vault.yml
```
Dependencies
------------

Example Playbook
----------------
```
---
- name: Linux account creation
  hosts: satellite

  roles:

    - role: linux_account_create
```
License
-------

https://opensource.org/license/mit
