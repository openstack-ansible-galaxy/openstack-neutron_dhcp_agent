Neutron dhcp agent
=========

OpenStack Neutron dhcp agent installation

_Tested on Ubuntu Precise (12.04) and Trusty (14.04)_

Requirements
------------

None

Role Variables
--------------

### Neutron (set by this role)

| Name | Default value | Description | Note |
|---   |---            |---          |---   |
|      |               |             |      |


### RabbitMQ (must exist)

| Name | Default value | Description | Note |
|---  |---  |---  |--- |
| `rabbit_hostname` | `localhost` | Hostname/IP address where the RabbitMQ service runs ||
| `rabbit_username` | `rabbit_username_default` | RabbitMQ username for glance ||
| `rabbit_pass` | `rabbit_pass_default` | RabbitMQ password for glance. ||


Dependencies
------------

None.

Example Playbook
----------------

    - hosts: network001
      roles:
        - role: openstack-neutron_dhcp_agent
          rabbit_username: "openstack-neutron"
          rabbit_pass: "{{ RABBIT_NEUTRON_PASS }}"

---

A complete Ansible playbook demo, which uses this role, is available on Github (dguerri/vagrant-ansible-openstack) <https://github.com/dguerri/vagrant-ansible-openstack>

---


License
-------

Apache

Author Information
------------------

Davide Guerri - davide.guerri@gmail.com
