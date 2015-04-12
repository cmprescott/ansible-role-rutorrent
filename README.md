Ansible Role: ruTorrent
=========
[![Build Status](https://travis-ci.org/cmprescott/ansible-role-rutorrent.svg?branch=master)](https://travis-ci.org/cmprescott/ansible-role-rutorrent)

Downloads and installs the rutorrent php code. Configures config.php by template.

Requirements
------------

Linux?

Role Variables
--------------

```
# -------------
# version
# -------------
rutorrent_version: rutorrent-3.6
# -------------
# download
# -------------
rutorrent_download_url: http://dl.bintray.com/novik65/generic/{{ rutorrent_version }}.tar.gz
rutorrent_download_dest: /tmp
# -------------
# dir settings
# -------------
rutorrent_dir_install: /var/www/rutorrent
rutorrent_dir_install_group: www-data
rutorrent_dir_install_owner: www-data
# -------------
# bin path settings
# -------------
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

    - hosts: torrent-servers
      roles:
         - role: ansible-role-rutorrent
            

License
-------

BSD

Author Information
------------------

Prescott Chris
