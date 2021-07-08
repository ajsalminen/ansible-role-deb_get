deb_get
==========

Requirements
------------

rsync if using it to fetch the debs that are to be installed.

Description
------------
Extremely simple role for downloading Debian packages via HTTP or rsync and and
installing them in the same go. Useful for installing debs when there is no
package repository for the files, for example the silver searcher (ag) and
Vagrant are distributed this way.

Role Variables
--------------
deb_get_download_directory: The download directory for packages.
Defaults to /tmp.

Example playbook
-------------
    - hosts: servers
      roles:
        - role: deb_get
          packages:
            - { url: 'https://github.com/downloads/ggreer/the_silver_searcher/',
                filename: the-silver-searcher_0.7.3-3_i386.deb }
            - { rsync: 'server.example.com:/srv/packages/',
                filename: packagename_1.2.3_x86_64.deb }
            - { scp: '/path/to/storage',
                filename: packagename_1.2.3_x86_64.deb }

License
-------

MIT
