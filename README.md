Corosync
========

This role manages corosync/pacemaker.

This role has been developed for Corosync 1.4.1 on CentOS 6.

Manage both CentOS and Debian packages, but no further testing has been done
in Debian (yet). By the way, no CentOS specificity is present, so it
may work on Debian and other OSes without much headache.

Requirements
------------

This role requires `do` jinja2 extension enabled. See [ansible.cfg](https://github.com/ansible/ansible/blob/devel/examples/ansible.cfg) for reference.

Role Variables
--------------

Almost all corosync variables are supported. If you find anything missing please post an issue.

Look [`defaults/main.yml`](defaults/main.yml) for detailed reference.

License
-------

BSD

Author Information
------------------

Jonathan Araña Cruz - SB IT Media, S.L.
