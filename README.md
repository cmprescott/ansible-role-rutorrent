Ansible Role: ruTorrent
=========
[![Build Status](https://travis-ci.org/cmprescott/ansible-role-rutorrent.svg?branch=master)](https://travis-ci.org/cmprescott/ansible-role-rutorrent)

Downloads and installs the rutorrent php code. Templates config.php.

Requirements
------------

```shell
# Ansible version 2.0.0.2+
ansible --version

# OS
case $OSTYPE in
  # Linux needs apt
  "linux"*)
      apt --version;;
esac
```

Role Variables
--------------

```yaml
# ----- install -----
rutorrent_repo: https://github.com/Novik/ruTorrent.git
rutorrent_version: master
rutorrent_force_udpate: no

# ----- dir settings -----
rutorrent_dir_install: /var/www/rutorrent
rutorrent_dir_install_group: www-data
rutorrent_dir_install_owner: www-data

# ----- bin path settings -----
rutorrent_path_php: 
rutorrent_path_curl: /usr/bin/curl
rutorrent_path_gzip:
rutorrent_path_id: /usr/bin/id
rutorrent_path_stat: /usr/bin/stat
```

Dependencies
------------

None.

Example Playbook
----------------

```yaml
- hosts: torrent-servers
  roles:
     - role: cmprescott.ruTorrent
```

License
-------

BSD

Author Information
------------------

Prescott Chris
