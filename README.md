# Ansible Role : EyesOfIndicator

Ansible Role for EyesOfIndicator.

Requirements
------------

CentOS 7 with minimal install.

Role Variables
--------------

* `eoi_repo` - https://github.com/EyesOfNetworkCommunity/eyesofindicator
* `eoi_repo_dir` - "/tmp/eoi"
* `eoi_version` - "2.0"
* `eoi_keep_updated` - yes
* `eoi_image` - "eyes/eoi"

Example Playbook
----------------

```
- name: Install EyesOfIndicator Dashboarding 
  hosts: eyesofindicator
  remote_user: ansible
  become: true
  tasks:
  - import_role:
      name: eyesofindicator
      tasks_from: install
```

Author Information
------------------

* **Jean-Philippe Levy** - <jean-philippe.levy@axians.com> - [EyesOfNetwork Community](https://github.com/eyesofnetworkcommunity)
