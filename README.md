# ansible-role-fortiadc-glb-host

## Description

Ansible role to manage FortiADC health check resources via REST API.

## Usage

### Hosts Example

```
[fortiadc]
fad1.ndkprd.com ansible_host=fad1.ndkprd.com 
```

### Needed Vars Example

### Playbook Example

```
---
# ./playbook.yaml

- name: Add global-load-balance host entry in FortiADC.      
  hosts: fortiadc
  become: true
  gather_facts: no
  vars:
  roles:
    - ndkprd.fad_health_check
```

### About Tags

You can skip debug tasks by using `--skip-tags` against `debug` tag.

## License

MIT, use at your own risk.