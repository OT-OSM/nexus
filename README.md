Ansible Role: Nexus
=====================================
An ansible role to install and configure Nexus.

Version History
---------------

|**Date**| **Version**| **Description**| **Changed By** |
|----------|---------|---------------|-----------------|
|**6 February 2020** | v.3.20 | |

Salient Features
----------------

- This Role automates the Nexus setup.


Supported OS
------------

* Ubuntu
* RHEL


Dependencies
------------

* Java runtime versions other than 8 are not supported - do not use them.
* Only 64 bit Java is supported, do not use 32 bit Java.


Directory Layout
----------------
```
NEXUS

├── defaults
│   └── main.yml
├── handlers
│   └── main.yml
├── README.md
├── tasks
│   ├── install.yml
│   ├── main.yml
│   ├── RedHat.yml
│   └── Ubuntu.yml
├── templates
│   ├── nexus-default.properties.j2
│   ├── nexus-init.j2
│   ├── nexus.rc.j2
│   ├── nexus.service.j2
│   └── nexus.vmoptions.j2
└── vars
    └── main.yml

5 directories, 13 files


```

Role Variables
--------------

|**Variables**| **Default Values**| **Type**|
|----------|---------|---------------|-----------|
nexus_port|nexus_min_memory|nexus_max_memory|nexus_dir_mem_size|nexus_shared_dir
host_name|nexus_version|nexus_port|nexus_os_user|nexus_os_group|nexus_os_user_shell|nexus_installation_dir|nexus_service_state|
install.yml|main.yml|RedHat.yml|Ubuntu.yml

 
Example Playbook
----------------
```
---
- name: It will automate nexus setup
  hosts: server
  become: true
  roles:
    - role: osm_nexus3
...

$  ansible-playbook site.yml -i inventory

```

Inventory
----------
An inventory should look like this:-
```ini
[server]                 
192.xxx.x.xxx    ansible_user=ubuntu 
```

Future Proposed Changes
-----------------------


#References

# Author Information

* 
