Role Name
=========

This role help copy ssh key to nodes for using ansible.


Requirements
------------
- sshpass


Role Variables
--------------
```
base_image:
  id: "{{lookup('env', 'BASE_IMAGE_ID')}}"
  pw: "{{lookup('env', 'BASE_IMAGE_PW')}}"

ssh_public_key: "{{lookup('env', 'SSH_PUBLIC_KEY')}}"
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
          - role: ssh-id-copy
            ssh_id_copy_target: "target_vm"

```
License
-------

BSD

Author Information
------------------

This role was created in 2018 by [Jooho Lee](http://github.com/jooho).

