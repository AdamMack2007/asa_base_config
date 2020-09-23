# Configure ACL

Used to configure interface ACLs.

## Role Variables

- **ssh_allowed_subnets**: List of dictionaries to describe the network and interface to allow the network on. See defaults/main.yml for examples.

## Example Playbook

```
- name: Configure ACL
  hosts: all
  gather_facts: no

  roles:
    - config_acl

```
