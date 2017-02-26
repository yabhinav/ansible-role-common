[![Build Status](https://travis-ci.org/yabhinav/ansible-role-common.svg?branch=master)](https://travis-ci.org/yabhinav/ansible-role-common)

Ansible Role: Common Generic Tasks 
=================================
This role performs generic specific tasks required by other roles like :

- Installing Python, Except and other basic linux packages.
- Install, configure and start NTP service.
- Disable Selinux.


Dependencies
------------

None.


Example Playbook
----------------

```yaml
- hosts: localhost
  become_user: True
  gather_facts: True
  
  roles:
    - yabhinav.common
```

Issues
------

- Selinux module fails if selinux is not installed [#21622 ](https://github.com/ansible/ansible/issues/21622). Do a stat check on selinux config file
- Ubuntu 12.04 older version of Jinj2=2.2 is causing [issues with ansible2.2](https://github.com/ansible/ansible/issues/20309) 
- Ubuntu 16.04 ansible_default_ipv4_address is not retrieved by ansible_facts.


License
-------

MIT


Author Information
------------------

Created by [Abhinav Yalamanchili](https://yabhinav.github.com)
