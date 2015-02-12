rutorrent
=========

Downloads and installs the rutorrent php code. Configures config.php by template.

Requirements
------------

Linux?

Role Variables
--------------

# -------------
# version
# -------------
rutorrent_version: 3.6
# -------------
# urls
# -------------
rutorrent_url_download: http://dl.bintray.com/novik65/generic/
# -------------
# directory settings
# -------------
rutorrent_directory_src_download: ~/Downloads/
rutorrent_directory_install: /var/www/
rutorrent_directory_install_group: www-data
rutorrent_directory_install_owner: www-data
# -------------
# bin path settings
# -------------
rutorrent_path_php: 
rutorrent_path_curl: /usr/bin/curl
rutorrent_path_gzip:
rutorrent_path_id:
rutorrent_path_stat: /usr/bin/stat

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
