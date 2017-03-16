Reboot and Wait
=========

Ansible role intended to reboot Linux based system with systemd as a system and service manager.

Using that role you can avoid errors like:

```
fatal: [10.0.15.50]: UNREACHABLE! => {"changed": false, "msg": "Failed to connect to the host via ssh: Shared connection to 10.0.15.50 closed.\r\n", "unreachable": true}

```

Requirements
------------

The role doesn't have any special requirements.

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

The role doesn't have any external dependencies.

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role:it-praktyk.reboot-and-wait }

License
-------

Copyright (c) 2016 Wojciech Sciesinski  
This role is licensed under The MIT License (MIT)  
Full license text: https://opensource.org/licenses/MIT 

Author Information
------------------

Author: Wojciech Sciesinski, wojciech[at]sciesinski[dot]net
Keywords: Ansible, systemd, reboot

Credits: Marcin Skarbek due to provided answer https://stackoverflow.com/questions/29955605/how-to-reboot-centos-7-with-ansible
