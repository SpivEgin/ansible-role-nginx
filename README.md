# Ansible Role: Nginx 0.1
[![Build Status](https://travis-ci.org/maruina/ansible-role-nginx.svg?branch=master)](https://travis-ci.org/maruina/ansible-role-nginx)  
An Ansible role that configure nginx.

## Download from Ansible Galaxy
```bash
ansible-galaxy install maruina.nginx
```

## Usage
```yaml
system_groups:
  - name: docker
    system: no
  - name: foo
    system: yes

system_groups_removed:
  - bar
  - another_group

system_users:
  - name: alice
    groups: docker, foo
    authorized:
      - ssh-rsa PUBLIC-KEY
      - ssh-rsa ANOTHER-PUBLIC-KEY
  - name: bob
    authorized:
      - ssh-rsa PUBLIC-KEY

system_users_removed:
    - harvey
    - mike
```

## Example Playbook
```yaml
    - hosts: all
      roles:
        - { role: maruina.nginx }
```

## License
MIT
