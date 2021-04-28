Netdata\_straight
=========

A pretty straightforward role to install netdata using curl | bash install

Requirements
------------

None

Role Variables
--------------

See [defaults/main.yml]

* `netdata_extra_config`: An array of application configurations. Defaults to `[]`
  * `name`: the name of the specified collector
  * `specific_task_file`: a task file to be included.
  * `apt_dependencies`: an array of package dependencies
  * `pip_dependencies`: an array of pip dependencies to be installed
  * `extra_groups`: an array of groups to add netdata user to
  * `read_files`: an array of file path to which netdata user should be granted access
  * `collector_type`: `python`, `node`, `go` or `charts`
  * `replace`: when a sensor is changed from one type to another allow ro remove the old configuration
  * `config`: the content of the configuration file as yaml to be put in `$type.d` config
  * `health_config`: the templates as in netdata acceptation for this collector, an array of templates configuration
    * `name`: the template name
    * `definition`: a list of string defining the template (like 'on: apache.requests')
* `netdata_alarms_overrides`: an array of override for default netdata templates
  * `name`: friendly name of the override (filesystem compatible)
  * `override`: the content of the override

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
