# Ansible Role: Install samba

[![Build Status](https://travis-ci.org/tschifftner/ansible-role-samba.svg)](https://travis-ci.org/tschifftner/ansible-role-samba)

Installs samba on Debian/Ubuntu linux servers.

## Requirements

None

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

```
samba_config_file: 'your/file/path.conf'
       
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
2.1              | Yes              | Yes             | Yes

## License

[MIT License](http://choosealicense.com/licenses/mit/)

## Author Information

 - [Tobias Schifftner](https://twitter.com/tschifftner), [ambimax® GmbH](https://www.ambimax.de)