outime.teamspeak3-docker
========================

Install and use TeamSpeak3 in Docker.

Requirements
------------

Requires Ansible 2.3 or higher.

Role Variables
--------------

Available role variables can be retrieved from `defaults/main.yaml`.

Dependencies
------------

Docker :)

Example Playbook
----------------

```
- hosts: teamspeak
  become_user: root
  roles:
  - { role: outime.teamspeak3-docker, username: teamspeak, uid: 1000, host_volume: /home/teamspeak/teamspeak3-data, container_restart_policy: always }
```

License
-------

MIT

Author Information
------------------

Ruben Diaz (outime@gmail.com).
