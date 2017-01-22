Role Name
=========

Ansible role for [app-emulation/docker-machine] (https://packages.gentoo.org/packages/app-emulation/docker-machine) on [Gentoo Linux] (http://www.gentoo.org)

Requirements
------------

All requirements are satisfied by role itself

Role Variables
--------------

No variables are needed by this role

Dependencies
------------

This role doesn't depend on any other role.

Example Playbook
----------------

Setup yout docker-machine host

    - hosts: docker-machine
      roles:
         - { role: role-docker-machine }

License
-------

GPL3

Author Information
------------------

This role was created by Davide "CuB0" Rebeccani.