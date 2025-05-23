# NERC Nagios Role Collection

Collection of roles to deploy Nagios components on NERC infrastructure

To use, update galaxy-requirements.yml

```sh
collections:
  - name: nerc.nagios
    type: git
    version: main
    source: https://github.com/nerc-project/nerc-nagios-ansible-collection.git
```

## Roles

### nrpe

Installs nrpe container on a host to be monitored by the nagios server.

Example:

```sh
- name: deploy nrpe
  hosts: localhost
    vars:
      nrpe_allow_addresses: 1.2.3.4
  gather_facts: false
  roles:
    - nerc.nagios.nrpe
```
