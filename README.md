ansible-role-deb_install_url
==========

Description
------------
Extremely simple role for downloading and installing debian packages from URLs
with ansible and installing with dpkg. I use this to download and install debs
for the silver searcher (ag) and vagrant for example.

Example usage
-------------
    - role: deb_install_url
      packages:
        - { url: 'https://github.com/downloads/ggreer/the_silver_searcher/',
            filename: the-silver-searcher_0.7.3-3_i386.deb }
        - { url: 'https://dl.bintray.com/mitchellh/vagrant/',
            filename: vagrant_1.5.3_x86_64.deb }
