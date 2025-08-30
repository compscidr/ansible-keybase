# ansible-keybase
[![Static Badge](https://img.shields.io/badge/Ansible_galaxy-Download-blue)](https://galaxy.ansible.com/ui/repo/published/compscidr/keybase/)
[![ansible lint](https://github.com/compscidr/ansible-keybase/actions/workflows/check.yml/badge.svg)](https://github.com/compscidr/ansible-keybase/actions/workflows/check.yml)
[![ansible lint rules](https://img.shields.io/badge/Ansible--lint-rules%20table-blue.svg)](https://ansible.readthedocs.io/projects/lint/rules/)

Ansible collection to install keybase

## Usage:
Add the collection to your meta/requirements.yml:
```
collections:
  - name: compscidr.keybase
    version: "<insert version here>"
```

Use the role(s) in a playbook:
```
- name: Install keybase
  hosts: all
  roles:
    - keybase
```