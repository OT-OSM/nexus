Ansible Role: Nexus
=====================================
An ansible role to install and configure Nexus on Ubuntu, Redhat and CentOS.

Version History
---------------

|**Date**| **Version**| **Description**| **Changed By** |
|----------|---------|---------------|-----------------|
|**6 February 2020** | v.3.20 | |
|**9 APril 2019** | v.3.15 | |

Salient Features
----------------

- This Role automates the Nexus setup.


Supported OS
------------

* Ubuntu
* RHEL
* CentOS

Dependencies
------------

* Java 8(64-bit)


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

Variable:- nexus_port: 8082|nexus_min_memory: 1200M|nexus_max_memory: 1200M|nexus_dir_mem_size: 2G|nexus_shared_dir: /opt/nexus_shared

Default Values:- host_name: 'host'|nexus_version: '3.20.0-01'|nexus_port: 8082|nexus_os_user: 'nexus'|nexus_os_group: 'nexus'|nexus_os_user_sh                 ell: '/bin/bash'|nexus_installation_dir: '/opt'|nexus_service_state: 'restarted'

Type:- Ubuntu| Redhat | CentOS

 
Example Playbook
----------------
```
---
- name: It will automate nexus setup
  hosts: server
  become: true
  roles:
    - role: osm_nexus3.2
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

* https://www.vogella.com/tutorials/Nexus/article.html

# Author Information

* mukesh tuteja

* 

