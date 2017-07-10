Ucarp Role for Ansible
======================

Install and configure Ucarp for Debian.

This role allow to setup several VIP on a single interface. For a single VIP by
NIC, use the simpler
[eNiXHosting.ansible-ucarp](https://github.com/eNiXHosting/ansible-ucarp).

Role Variables
--------------

See [defaults/main.yml](defaults/main.yml).

Usage
-----

```yaml
- hosts: servers
  become: yes
  vars:
    ucarp_addresses:
      - vhid: 123
        addr: 192.0.2.123
        pass: GoodPassword
        interface: eth0
  roles:
    - mathieumd.ucarp
```

License
-------

GPLv3

Similar Roles
-------------

This role was inspired by
[eNiXHosting.ansible-ucarp](https://github.com/eNiXHosting/ansible-ucarp) by
Laurent Corbes <laurent.corbes@enix.fr>.
