# Ansible Role : EyesOfIndicator

Ansible Role for EyesOfIndicator.

Requirements
------------

CentOS 7 with minimal install.
Ansible < 2.6

Role Variables
--------------

* `eoi_container` - "eoi"
* `eoi_version` - "2.0"
* `eoi_image` -  "eyes/eoi"
* `eoi_port` - 3030
* `eoi_repo` - https://github.com/EyesOfNetworkCommunity/eyesofindicator
* `eoi_repo_dir` - "/tmp/eoi"
* `eoi_keep_updated` - yes
* `eoi_apks` - ""
* `eoi_gems` - ""
* `eoi_widgets` - ""

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
* **Guilalume Ona** - <guillaume.ona@axians.com> - [EyesOfNetwork Community](https://github.com/eyesofnetworkcommunity)
* **Sebastien Davoult** - <sebastien.davoult@axians.com> - [EyesOfNetwork Community](https://github.com/eyesofnetworkcommunity)
