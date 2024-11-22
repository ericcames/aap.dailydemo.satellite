Ansible Automation Platform Daily Demo for Satellite
=========
A demo designed to build the Satellite Infrastructure needed to showcase many of the use cases related to Satellite.  This builds a standalone Satellite server at Amazon and sets the admin password so you will be ready to go when the playbook is done building the infrastructure.

Day 0 - Configuration as code (CAC)
=========
Configuration as code give you an easy way to recover/move your ansible related artifacts to a new or existing platform.  That includes your hardcoded credentials.  The hardcoded credentials can be safely vaulted in an ansible vault file.  Check out the setup_demo.yml for the configurations for setting up this demo using configuration as code.  The current example is for the F5 daily Demo because the doesn't exist for this demo yet.  When it exists this section will be updated.

[setup_demo.yml](https://github.com/ericcames/aap.dailydemo.F5/blob/main/playbooks/setup_demo.yml "setup_demo.yml")<br>

Day 1 - Infrastructure as code (IAC)
=========

# The Satellite User Interface

![alt text](https://github.com/ericcames/aap.dailydemo.satellite/blob/main/images/satuipre.png "Pre Login")
![alt text](https://github.com/ericcames/aap.dailydemo.satellite/blob/main/images/satuipost.png "Post Login")

**The playbooks**

[Create Satellite](https://github.com/ericcames/aap.dailydemo.satellite/blob/main/playbooks/main-create.yml "main-create.yml")<br>
[Remove Satellite](https://github.com/ericcames/aap.dailydemo.satellite/blob/main/playbooks/main-remove.yml "main-remove.yml")<br>
![alt text](https://github.com/ericcames/aap.dailydemo.satellite/blob/main/images/satjob.png "Create")<br>

Tags used:
```
create
  or
remove
```

**The Credentials Types**

Red Hat Ansible Automation Platform<br>
Satellite Machine Credential<br>
![alt text](https://github.com/ericcames/aap.dailydemo.satellite/blob/main/images/satellitemachinecred.png "Machine Credential")<br>
Amazon Web Services Credential<br>

**The AAP Managed Inventory**

![alt text](https://github.com/ericcames/aap.dailydemo.satellite/blob/main/images/satinventory.png "AAP Managed Inventory")<br>
![alt text](https://github.com/ericcames/aap.dailydemo.satellite/blob/main/images/satlocalhost.png "localhost")<br>

Group name
```
satellite
```

**The Cleanup Schedule**
![alt text](https://github.com/ericcames/aap.dailydemo.satellite/blob/main/images/satellitecleanup.png "Satellite Daily Demo Cleanup")<br>

Day 2
=========

Looking for other Daily Demos?
=========

- [AAP Daily Demo Windows](https://github.com/ericcames/aap.dailydemo.windows "AAP Daily Demo Windows")
- [AAP Daily Demo Linux](https://github.com/ericcames/aap.dailydemo.linux "AAP Daily Demo Linux")
- [AAP Daily Demo F5](https://github.com/ericcames/aap.dailydemo.F5 "AAP Daily Demo F5")
- [AAP Daily Demo Panos](https://github.com/ericcames/aap.dailydemo.Panos "AAP Daily Demo Panos")
- [AAP Daily Demo Satellite](https://github.com/ericcames/aap.dailydemo.satellite "AAP Daily Demo Satellite")
