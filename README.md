Ansible ssh Debian
=====

This Ansible role installs and configures ssh on a Debian system.

Requirements
------------

This role requires Ansible 1.4 or higher

Role Variables
--------------

You can see the variables that can be passed to this role by checking the file `defaults/main.yml`.

Dependencies
------------

none

Example Playbook
-------------------------

All options:

    - {
        role: damko.ssh-debian,
            ssh_password_based: true,
            ssh_pub_key_root: /home/user/.ssh/id_rsa.pub,
            ssh_port: 22222,
    }

1. Ex. of simple ssh installation:

        - role: damko.ssh-debian

2. Ex. of ssh installation on port 22222:

        - {
            role: damko.ssh-debian,
                ssh_port: 22222,
        }

3. Ex. of ssh installation on port 22 with password authentication disabled.

        - {
            role: damko.ssh-debian,
                ssh_password_based: true,
                ssh_pub_key_root: /home/me/.ssh/id_rsa.pub,
        }

    With this configuration it will be possible for user "me" to get access to the machine as root via ssh without password authentication in this way:

        ssh root@ip

License
-------

BSD

Author Information
------------------

Damiano Venturin @damko
