# ASA Base Configuration

Ansible network roles to perform a base configuration of Cisco ASA devices

## Usage

Any role with config\_\* will make configuration changes to the device.

Role name and functions:

- **config_acl**: Configure SSH management ACLs on devices.
- **config_credentials**: Update user credentials for local accounts
- **config_dns**: Configures DNS servers
- **config_ha**: Configures Active/Standby configuration
- **config_ntp**: Configures NTP servers
- **config_provisioning**: Configures misc changes: hostnames, ssh ciphers, login timeouts, etc
- **config_save**: Simple playbook to save the running configurations.
- **config_snmp**: Configures SNMPv3 on devices.
- **config_syslog**: Configures remote/local syslog settings.

## Information

Each role has a readme with the variables or information required as well as any recommendations.

## Example playbook

Configure just NTP servers

```
- name: Configure NTP Servers
  hosts: all
  gather_facts: no

  roles:
    - config_ntp
```

Include all roles to build the entire base configuration

```
- name: ASA Base Configuration
  hosts: all
  gather_facts: no

  roles:
    - config_provisioning
    - config_dns
    - config_ntp
    - config_snmp
    - config_syslog
    - config_credentials
    - config_ha
    - config_acl
    - config_save
```

## Recommendations

I strongly recommend testing in a lab first to ensure the changes comply with your desired state.
