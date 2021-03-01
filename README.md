Netdata\_straight
=========

A pretty straightforward role to install netdata using curl | bash install

Requirements
------------

None

Role Variables
--------------

See [defaults/main.yml]

Dependencies
------------

None

Example Playbook
----------------

```
    - hosts: servers
      roles:
         - { role: ansible_straight, netdata_installer: kickstart-static64 }
```

License
-------

BSD

Author Information
------------------

Fretlink
