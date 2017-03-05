[![Build Status](https://travis-ci.org/yabhinav/ansible-role-common.svg?branch=master)](https://travis-ci.org/yabhinav/ansible-role-common)

Ansible Role: Common Generic Tasks 
=================================
This role performs generic specific tasks required by other roles like :

- Installing Python, Except and other basic linux packages.
- Install, configure and start NTP service.
- Disable Selinux.
- Disable Iptables/firewalld and ufw

These are pre-requisites for other roles that install ipaserver, ipaclient and hadoop applications


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

- Selinux module fails if selinux is not installed [#21622 ](https://github.com/ansible/ansible/issues/21622). Do a stat check if selinux config file exists or use ansible_selinux which tells if selinux is present ( and not enabled or running)
- Ubuntu 12.04 older version of Jinj2=2.2 is causing [issues with ansible2.2](https://github.com/ansible/ansible/issues/20309). Use  variables with full quotes as mentioned [here](https://github.com/yabhinav/ansible-role-common/issues/1)


License
-------

MIT


Author Information
------------------

Created by [Abhinav Yalamanchili](https://yabhinav.github.com)
