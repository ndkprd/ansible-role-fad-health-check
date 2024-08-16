# ansible-role-fad-health-check

## Description

Ansible role to manage FortiADC health check resources via REST API.

## Usage

### Hosts Example

```
[fortiadc]
fad1.ndkprd.com ansible_host=fad1.ndkprd.com 
```

### Playbook Example

Check out [tests](tests/) folder.

### About Tags

You can skip debug tasks by using `--skip-tags` against `debug` tag.

## License

MIT, use at your own risk.
