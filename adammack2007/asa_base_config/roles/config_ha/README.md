# Configure HA

Used to configure HA peering.

## Role Variables

- **ha_peer**: (yes/no) Determines which node should be configured as active. Recommended to set this as host_var.

- **asa_failover_port**: Interface to use for failover link
- **asa_failover_key**: (Optional) Key to use for peering
- **asa_failover_ip_pri**: Primary (Active) IP to apply to primary node
- **asa_failover_ip_subnet**: Subnet mask to use for failover link
- **asa_failover_ip_sec**: Secondary (Standby) IP to apply to secondary node

## Example Playbook

```
- name: Configure HA
  hosts: all
  gather_facts: no

  roles:
    - config_ha

```
