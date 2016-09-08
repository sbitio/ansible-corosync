# *This role is abandoned.*

Corosync
========

Ansible role to configure Corosync.

Developed on CentOS 6.5 with Corosync version 1.4.1.

It manage CentOS and Debian packages and configuration. No further testing has
been done in Debian (yet). By the way, no CentOS specificity is present, so it
may work on Debian and even other OSes.

This role also provides a [module](library/corosync_service) to allow configuration of Corosync services.
See example playbook below for details.

You may also be interested in Pacemaker configuration. Checkout
[sbitmedia.pacemaker](https://galaxy.ansible.com/list#/roles/701).

Requirements
------------

Jinja2 `do` extension must be enabled. See [ansible.cfg](https://github.com/ansible/ansible/blob/devel/examples/ansible.cfg) for reference.

Role Variables
--------------

Almost all Corosync variables are supported. If you find anything missing
please post an issue.

See [`defaults/main.yml`](defaults/main.yml) for detailed reference.

Example Playbook
----------------

Configure Corosync and Pacemaker service:

```yaml
- hosts: cluster
  roles:
    - role: sbitmedia.corosync
      services:
        - service: pacemaker
          ver: 1
          user: root
          group: root
```

You can configure services explicitly from other roles or playbooks by using
 `corosync_service` module:

```yaml
- name: 2nd test
  corosync_service: name=something ver=1 user=nobody group=nobody
```

`user` and `group` are optional and defaults to root.

In order to use the module, make sure the role has been declared before, or add
it as dependency to your own roles.

License
-------

BSD

Author Information
------------------

Jonathan Araña Cruz - SB IT Media, S.L.

