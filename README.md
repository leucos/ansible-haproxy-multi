haproxy-multi Ansible playbook
==============================

[![Travis
CI](http://img.shields.io/travis/leucos/ansible-haproxy-multi.svg?style=flat)](http://travis-ci.org/erasme/ansible-haproxy-multi)
[![Ansible
Galaxy](http://img.shields.io/badge/galaxy-leucos.ansible--haproxy--multi-660198.svg?style=flat)](https://galaxy.ansible.com/list#/roles/2909)

This playbook will install haproxy with a special init script that can read
configuration fragments in `/etc/haproxy/haproxy.conf.d/`

Requirements
------------

None

Role Variables
--------------

  - `haproxy_timeout_client`: Set the maximum inactivity time on the client side (defaumt: 50000ms)
  - `haproxy_timeout_connect`: Set the maximum time to wait for a connection attempt to a server to succeed (default: 5000ms)
  - `haproxy_timeout_server`: Set the maximum inactivity time on the server side (default: 50000ms)
  - `haproxy_stats_bind_interface`: Interface to bind to for the stats front end (default: "*")
  - `haproxy_stats_enable`: Whether stats are enabled (default: true)
  - `haproxy_stats_port`: Stats port (default: 8080)
  - `haproxy_stats_username`: Stats username (no defaults, role will fail if `haproxy_stats_enable` is set and `haproxy_stats_username` is not set)
  - `haproxy_stats_password`: Stats password (no defaults, role will fail if `haproxy_stats_enable` is set and `haproxy_stats_password` is not set)

Tags
----

  - haproxy: whole role
  - haproxy: config for the config files part

Dependencies
------------

None

Specs
-----

To run specs, issue:

```
vagrant up
vagrant ssh 'specs'
```

Example Playbook
----------------

TBD

License
-------

MIT

Author Information
------------------

@leucos
