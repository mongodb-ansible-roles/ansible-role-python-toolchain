Ansible role for python-toolchain
==================================

Installs the python toolchain

[![GitHub Actions](https://github.com/mongodb-ansible-roles/ansible-role-python-toolchain/workflows/Molecule%20Test/badge.svg)](https://github.com/mongodb-ansible-roles/ansible-role-python-toolchain/actions?query=workflow%3A%22Molecule+Test%22)
[![GitHub Actions](https://github.com/mongodb-ansible-roles/ansible-role-python-toolchain/workflows/Release/badge.svg)](https://github.com/mongodb-ansible-roles/ansible-role-python-toolchain/actions?query=workflow%3A%22Molecule+Test%22)

Requirements
------------

None

Role Variables
--------------

| Name | Description | Type | Default | Required |
|------|-------------|:----:|:-------:|:--------:|
| `python_toolchain_final_dest` | Location to install python toolchain | string | `/opt/python` | no |
| `python_toolchain_sha` | Version of the python toolchain to install | string | "ba92de2700c04ee2d4f82c3ffdfc33105140cb04" | no |
| `python_toolchain_url` | URL of the python toolchain to install | string | `https://s3.amazonaws.com/boxes.10gen.com/build/toolchain-drivers/mongo-python-driver/python-toolchain-{{ ansible_distribution | lower | replace('redhat', 'rhel') }}{{ ansible_distribution_version | replace('.', '') }}-{{ python_toolchain_sha }}.tar.gz` | no |

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: ansible-role-python-toolchain
```

License
-------

[Apache License](LICENSE)
