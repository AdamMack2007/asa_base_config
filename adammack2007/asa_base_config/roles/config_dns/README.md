# Configure DNS

Configure DNS servers and lookup information

## Role Variables

- **dns_servers**: List of DNS servers to configure
- **enforce_compliance**: (yes/no) Whether to remove DNS servers not in the dns_servers list
- **dns_source_interface**: Interface to use for DNS lookups.

## Example Playbook

```
- name: Configure DNS
  hosts: all
  gather_facts: no

  roles:
    - config_dns
```
