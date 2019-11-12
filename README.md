Role Name
=========

Installs and configures dnsmasq. It saves all configs as seperate files in /etc/dnsmasq.d

Requirements
------------

- Debian or Ubuntu

Role Variables
--------------

dnsmasq_config

Dependencies
------------

No dependencies

Example Playbook
----------------

```
- hosts: localhost
  roles:
          - dnsmasq
  vars:
      dnsmasq_config:
              - { name: "noname",  content: "lala" }
              - { name: "dhcp"
                  prio: "15"
                  content:|
                   long content
                }

```

License
-------

BSD

Author Information
------------------

Wolfgang Hotwagner
