Neutron DHCP agent OpenStack Ansible Role
=========

**Status**
* [![Build Status](https://travis-ci.org/openstack-ansible-galaxy/openstack-neutron_dhcp_agent.svg?branch=master)](https://travis-ci.org/openstack-ansible-galaxy/openstack-neutron_dhcp_agent) on master branch
* [![Build Status](https://travis-ci.org/openstack-ansible-galaxy/openstack-neutron_dhcp_agent.svg?branch=development)](https://travis-ci.org/openstack-ansible-galaxy/openstack-neutron_dhcp_agent) on development branch
* [![Ansible Galaxy](http://img.shields.io/badge/dguerri-openstack--neutron_dhcp_agent-blue.svg)](https://galaxy.ansible.com/list#/roles/1834) on Ansible Galaxy

OpenStack Neutron DHCP agent installation

_Tested on Ubuntu Precise (12.04) and Trusty (14.04)_

For RHEL/CentOS, RHOSP or RDO repositories are needed.

Requirements
------------

None

Role Variables
--------------

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

A complete Ansible playbook demo, which uses this role, is available on Github (openstack-ansible-galaxy/vagrant-ansible-openstack) <https://github.com/openstack-ansible-galaxy/vagrant-ansible-openstack>

---

Credits
-------
RedHat support implemented by Abel Boldú <abel.boldu@gmx.com>


License
-------

Apache

Author Information
------------------

Davide Guerri - davide.guerri@gmail.com
