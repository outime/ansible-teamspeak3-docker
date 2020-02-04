outime.teamspeak3-docker
========================

Install and use TeamSpeak3 in Docker. It uses [the official TeamSpeak Docker image](https://hub.docker.com/_/teamspeak) and currently assumes a mounted host volume containing TeamSpeak3 data.

Note that this automatically accepts TeamSpeak's license changes to keep the server running, as this was a common problem. If you want to change this behaviour, override the default `env_ts3server_license` (equivalent to `TS3SERVER_LICENSE` in the Docker image).

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
