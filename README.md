Ansible Role: Copy SSH public key 
=========

This role help copy ssh public key to vm or vms to be managed by Ansible

*Details*
- Remove the host from ~/.ssh/known_hosts
- Copy public key to VM or VMs

Requirements
------------
- sshpass

Role Variables
--------------

| Name           | Default value     | Requird | Description                        |
| -------------- | ----------------- | ------- | ---------------------------------- |
| target_vm      | undefined         | yes     | Single VM where public key copy    |
| target_vms     | undefined         | yes     | Multiple VMs where public key copy |
| target_vm_id   | root              | no      | VM id to login                     |
| target_vm_pw   | root              | no      | VM password to login               |
| ssh_public_key | ~/.ssh/id_rsa.pub | no      | Public key path                    |

*Note* 
You must specify one of target_vm or target_vms

Example Variables
-----------------

Single VM
```
target_vm: 192.168.10.1
```

Multiple VMs 
```
target_vms:
- 192.168.10.1
- 192.168.10.2
```

Dependencies
------------

None


Example Playbook
----------------
~~~
- name: Example Playbook
  hosts: localhost
  tasks:
    - import_role:
        name: Jooho.copy_ssh_pub_key
      vars:
        target_vm: 192.168.10.1
~~~

~~~
- name: Example Playbook
  hosts: localhost
  tasks:
    - import_role:
        name: Jooho.copy_ssh_pub_key
      vars:
        target_vms: 
        - 192.168.10.1
        - 192.168.10.2
~~~


License
-------

BSD

Author Information
------------------

This role was created in 2018 by [Jooho Lee](http://github.com/jooho).


