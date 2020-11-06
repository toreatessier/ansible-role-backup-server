# Ansible Role : Backup server

Ansible Role for Jakarta Project's backup servers.

Requirements
------------

- Debian 9 with minimal install
- SSH installed and sshd.service enabled
- **sudo** package installed
- One bridged interface using the **.20.45-47/26 IP**
- DNS set to 192.168.4.2 in */etc/resolv.conf*
- [User 'Ansible' already configured](https://github.com/nickjj/ansible-user)

**Note** : A template Debian 9 VM **with all requirements satisfied** is available [here](https://192.168.4.16/Equipe_1_Jakarta/debian9-template).

Example Playbook
----------------

```
- name: Deploy backup servers for Jakarta
  hosts: "{{hosts}}"
  remote_user: ansible
  tasks:
  - import_role:
      name: backup_server
      tasks_from: install
```

Author Information
------------------

* **Marco FRANCOIS** - <marco.francois@reseau.eseo.fr> - [Jakarta Project](https://192.168.4.16/Equipe_1_Jakarta/)
* **Toréa TESSIER** - <torea.tessier@reseau.eseo.fr> - [Jakarta Project](https://192.168.4.16/Equipe_1_Jakarta/)