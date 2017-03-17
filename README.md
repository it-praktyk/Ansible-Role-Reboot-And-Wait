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

How many seconds reboot need to be delayed
`
reboot_delay = 10
`

Port what need to be checked for a server availability.
`
return_port = 22
`

Time in seconds when the first connection attempt will be started
`
return_delay = 40
`

Time in seconds how long the connection probes will be attempted
`
return_timeout = 300
`

Time in seconds how long started connection probe will be stopped
`
return_connect_timeout = 20
`

Variables started from 'return_' are used by [wait_for Ansible module](https://docs.ansible.com/ansible/wait_for_module.html). Please consult the module documentation if any additional information is needed. 


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

[TODO](TODO.md)
----
