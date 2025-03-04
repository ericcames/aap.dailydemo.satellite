vm
=========
```
This role will create or delete a vm
```
Requirements
------------
```
Amazon Web Console Account
Amazon Web Services Credential in Ansible Automation Platform
```
Role Variables
--------------
```
vm_name: Satellite
vm_vpc_name: satellite-dailydemo
vm_environment_tag: "Satellite"
vm_user_name: eric.ames
vm_subnet_name: "{{ vm_vpc_name }}_Subnet"
vm_image: ami-0f94618cb3c90e1f5
vm_count: 1
vm_region: us-west-1
vm_assign_public_ip: true
vm_alwaysup: false
vm_instance_type: m5.2xlarge
vm_ec2_security_group_name: "{{ vm_vpc_name }}_SECGRP"
vm_ec2_ansible_group: "{{ vm_user_name }}"
vm_my_email_address: "{{ vm_user_name }}@redhat.com"
vm_my_ssh_key: zigfreed-ssh-key
ansible_python_interpreter: /usr/bin/python3
```
Dependencies
------------

Example Playbook
----------------
```
---
- name: Create our vm
  hosts: localhost
  connection: local

  tasks:

    - name: Include the vm role
      tags:
        - create
      ansible.builtin.include_role:
        name: vm

or

---
- name: Remove our vm
  hosts: localhost
  connection: local

  tasks:

    - name: Include the vm role
      tags:
        - remove
      ansible.builtin.include_role:
        name: vm
```
License
-------

https://opensource.org/license/mit
