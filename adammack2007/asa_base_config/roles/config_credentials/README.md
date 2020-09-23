# Configure Credentials

Used to configure local credentials. The option to purge all accounts that are not the "primary_user" variable can be configured. See the Role Variables section for the variable details.

## Role Variables

- **purge_users**: (yes/no) Whether to purge all local users that are not specified under "primary_user".
- **primary_user**: The name of the user to keep, will not be purged.
- **local_pass**: The local password to configure for the admin user. Recommended to set this as a vaulted password or in Tower use a Custom Credential Type to encrypt this password.

## Example Playbook

```
- name: Configure Credentials
  hosts: all
  gather_facts: no

  roles:
    - config_credentials

```
