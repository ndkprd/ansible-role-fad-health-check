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
    fad_health_checks:
    - name: LB_HLTHCK_TCP_80
      type: tcp
      port: 80
      dest_addr_type: ipv4
      dest_addr_ipv4: 0.0.0.0
      dest_addr_ipv6: '::'
      up_retry: 1
      down_retry: 3
      interval: 10
      timeout: 5
    - name: LB_HLTHCK_TCP_443
      type: tcp
      port: 443
      dest_addr_type: ipv4
      dest_addr: 0.0.0.0
      up_retry: 1
      down_retry: 3
      interval: 10
      timeout: 5
  roles:
    - ndkprd.fad_health_check
```

### About Tags

You can skip debug tasks by using `--skip-tags` against `debug` tag.

## License

MIT, use at your own risk.