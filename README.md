Role Name
=========

This role backs up the configuration of a network device if a backup does not exist and detects differences in the device's configuration with the previsous backup if it does exist.

The file is backed up to "{{ net_backup_root }}/{{ inventory_hostname }}"

Requirements
------------

Currently supports:
- ios
- nxos

Role Variables
--------------

    net_backup_root
    net_backup_force
    
Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: network
      connection: local
      gather_facts: no

      tasks:
        - include_role:
            name: net-backup
          vars:
            net_backup_root: /data/backups

License
-------

GPL-3.0
