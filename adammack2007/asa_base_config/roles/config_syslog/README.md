# Configure Syslog

Configure syslog settings. If the "enforce_comliance" var is set to yes, it will remove any command that does not match the commands that are declared.

If TCP is enabled, "logging permit-hostdown" will automatically be added to prevent an unreachable syslog server from taking down the data plane.

## Role Variables

- **syslog_servers**: List of syslog servers to configure
- **syslog_port**: The port used to send logs.
- **syslog_protocol**:(tcp/udp) The protocol to use. If tcp "logging permit-hostdown" will be added automatically
- **syslog_secure**:(yes/no) Whether to enable TLS encryption
- **enforce_compliance**:(yes/no) Whether to remove syslog servers that are not in the syslog_servers list

## Example Playbook

```
- name: Configure Syslog
  hosts: all
  gather_facts: no

  roles:
    - config_syslog
```
