# Ansible Role : EyesOfIndicator

Ansible Role for EyesOfIndicator.

Requirements
------------

CentOS 7 with minimal install.

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
* `eoi_samples` - yes
* `eoi_widgets` - ""
* `eoi_install_dir` - "/srv/eyesofindicator"
* `eoi_remove` - false

Example Playbook
----------------

```
- name: Install EyesOfIndicator Dashboarding 
  hosts: eyesofindicator
  remote_user: ansible
  become: true
  vars:
    import_dashboard_eon: false
  tasks:
  - import_role:
      name: eyesofindicator
      tasks_from: install
  - import_role:
      name: eyesofindicator
      tasks_from: dashboard_eon
    when: import_dashboard_eon
```

Author Information
------------------

* **Jean-Philippe Levy** - <jean-philippe.levy@axians.com> - [EyesOfNetwork Community](https://github.com/eyesofnetworkcommunity)
* **Guillaume Ona** - <guillaume.ona@axians.com> - [EyesOfNetwork Community](https://github.com/eyesofnetworkcommunity)
* **Sebastien Davoult** - <sebastien.davoult@axians.com> - [EyesOfNetwork Community](https://github.com/eyesofnetworkcommunity)
