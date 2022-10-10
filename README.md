# ansible_configure_pc

An ansible role for configuring my personal computer

## Requirements
------------

Collections:

- community.general

Roles:

- elliotweiser.osx-command-line-tools
- geerlingguy.mac.homebrew
- geerlingguy.docker
- lebergarrett.ansible_nfs_client
- lebergarrett.ansible_awscli

## Role Variables
--------------

| Variable            | Description                                                                                     | Type         | Required? | Default Value |
|---------------------|-------------------------------------------------------------------------------------------------|--------------|-----------|---------------|
| git_user            | git user name. e.g. 'Garrett Leber'                                                             | string       | y         |               |
| git_email           | git email. e.g. 'lebergarrett@gmail.com'                                                        | string       | y         |               |
| docker_users        | users to give access to docker daemon.                                                          | list(string) |           |               |
| sharedrive_location | location of nfs share to mount at /media/shared. e.g. 'truenasv2.kumpdev.com:/mnt/Primary/nfs'  | string       |           |               |
| wsl                 | whether or not you are installing in WSL(2)                                                     | bool         |           | false         |

## Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

## Example Playbook
----------------

```yml
- hosts: localhost
  roles:
    - role: lebergarrett.ansible_configure_pc
```

## License
-------

GPLv3
