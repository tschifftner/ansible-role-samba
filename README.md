# Ansible Role: Install samba

[![Build Status](https://travis-ci.org/tschifftner/ansible-role-samba.svg)](https://travis-ci.org/tschifftner/ansible-role-samba)

Installs samba on Debian/Ubuntu linux servers.

## Requirements

ansible 1.8+

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

```
samba_config: |
    [www]
       path = /var/www
       available = yes
       valid users = vagrant
       follow symlinks = no
       read only = no
       browseable = yes
       public = yes
       writable = yes
       hide dot files = no
       veto files = /.git/
       map archive = yes
       map system = yes
       map hidden = yes
       
samba_users:
  - name: vagrant
    password: vagrant

```

## Dependencies

None.

## Installation

```
$ ansible-galaxy install tschifftner.samba
```

## Example Playbook

    - hosts: server
      roles:
        - { role: tschifftner.samba }

## Supported OS
## Supported OS
Ansible          | Debian Jessie    | Ubuntu 14.04    | Ubuntu 12.04
:--------------: | :--------------: | :-------------: | :-------------: 
2.0              | Yes              | Yes             | Yes


## License

MIT / BSD

## Author Information

 - Tobias Schifftner, @tschifftner