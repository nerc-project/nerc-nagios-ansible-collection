# NERC Nagios Role Collection

Collection of roles to deploy Nagios components on NERC infrastructure

## Roles

To use, update galaxy-requirements.yml

```sh
collections:
  - name: nerc.nagios
    type: git
    version: main
    source: https://github.com/nerc-project/nerc-nagios-ansible-collection.git
```

nrpe: Install nrpe container on a host to be monitored by the nagios server.

Example:

```sh
- name: deploy nrpe
  hosts: localhost
  gather_facts: false
  roles:
    - nerc.nagios.nrpe
```
