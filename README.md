Role Name
========

Install [Atlassian Crowd](https://www.atlassian.com/software/crowd)

Requirements
------------

A database, either PostgreSQL or MySQL, running somewhere.

Role Variables
--------------

All defined in defaults, so overrideable:

    crowd:
      version:   2.7.1
      baseurl:   http://www.atlassian.com/software/crowd/downloads/binary
      installer: atlassian-crowd-2.7.1.tar.gz
      user:      crowd
      # use postgresql or mysql
      dbconnector: postgresql
      packages:
        - java-1.7.0-openjdk
      tmp:       /var/tmp
      installto: /opt
      datadir:   /srv/crowd-data


Dependencies
------------


Example Playbook
-------------------------

    - hosts: crowd_servers
      roles:
         - { role: crowd }

License
-------

MIT/BSD

Author Information
------------------

Mark Phillips <mark@probably.co.uk>
http://probably.co.uk
