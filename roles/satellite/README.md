satellite
=========
```
This role will turns our machine into a satellite server.
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
satellite_username: USERNAME
satellite_password: PASSWORD
satellite_organization: AmesCO
satellite_location: California
satellite_version: 6.15
satellite_user_list_vault: ames_user_list_vault.yml
satellite_sat6_fqdn: "{{ satellite_sat6_fqdn }}"
satellite_manifest: AmesCO-Satellite-manifest.zip
```
Dependencies
------------
```
amazon.aws
```
Example Playbook
----------------
```
- name: Do work on our new server
  hosts: satellite
  become: true
  become_user: root
  gather_facts: true
  vars:
    satellite_sat6_fqdn: sat.kona.services

  tasks:

    - name: Install satellite
      tags:
        - create
      ansible.builtin.include_role:
        name: satellite

```
License
-------

https://opensource.org/license/mit
