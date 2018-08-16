Ansible Role: OCP SSH ID COPY
=========

This role help copy ssh key to nodes for using ansible.


Requirements
------------
- sshpass


Role Variables
--------------
```
base_image:
  id: "test"
  pw: "test"

ssh_public_key: "~/.ssh/id_rsa.pub"
```
This role need to load credential information and it will use environment variable. please check the way from [here](https://github.com/Jooho/ansible-cheat-sheet/blob/master/docs/credential-info.md)

Dependencies
------------

None

Example Playbook
----------------
```
    - hosts: localhost
      roles:
          - role: jooho.ansible-role-ocp-ssh-id-copy
            ssh_id_copy_target: "10.10.10.1"

```
License
-------

BSD

Author Information
------------------

This role was created in 2018 by [Jooho Lee](http://github.com/jooho).

