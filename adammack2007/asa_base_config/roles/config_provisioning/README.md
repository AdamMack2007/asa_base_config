# Configure Provisioning

Provisions miscellaneous tasks as listed below:

- Configures hostname
- Configures SSH ciphers to High settings
- Configures SSH and console timeout values
- Configures Timezone

The hostname will be configured using the "inventory_hostname" var.

## Role Variables

- **gmt_offset**: Offset from GMT (Ex for MST "-7")

## Example Playbook

```
- name: Configure Provisioning
  hosts: all
  gather_facts: no

  roles:
    - config_provisioning
```
