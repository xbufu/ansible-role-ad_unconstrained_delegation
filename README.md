Ansible Role: AD Unconstrained Delegation.
=========

An Ansible role to enable unconstrained delegation on a number of computers in the domain. Also creates login events for the specified users to cache credentials.

Requirements
------------

Needs to be run on the DC.

Role Variables
--------------

```yml
num_computers: 1
login_event_users:
  - username: 'ad01\administrator'
    password: Password!
```

Dependencies
------------

None.

Example Playbook
----------------

```yml
- hosts: pdc01
  roles:
    - role: xbufu.ad_unconstrained_delegation
      vars:
        num_computers: 1
        login_event_users:
          - username: 'ad01\administrator'
            password: Password!
```

License
-------

MIT / BSD

Author Information
------------------

Created by xbufu.
