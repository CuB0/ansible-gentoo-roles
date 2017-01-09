Ansible Role: app-emulation/docker
=========

Ansible role for [app-emulation/docker] (https://packages.gentoo.org/packages/app-emulation/docker) on [Gentoo Linux] (http://www.gentoo.org)

Requirements
------------

All requirements are satisfied ba role itself

Role Variables
--------------

docker_storage_device: Describe the block device where docker storage will be prepared. Eg. /dev/sdb
docker_storage_type: Describe the type of docker storage. Valid options are: btrfs or lvm. If you don't define this variable you will end with localfile backed storage
docker_bridge_ip: Describe the IPv4 address of docker0 bridge. Eg. 192.168.1.1/24

Dependencies
------------

Thi role doesn't depend on any other role.

Example Playbook
----------------

Setup app-emulation/docker with local file backed storage and default bridge IP address:

    - hosts: docker
      roles:
         - { role: role-docker }

Setup app-emulation/docker with local file backed storage and 192.168.0.1/24 as bridge IP address:

    - hosts: docker
      roles:
         - { role: role-docker, docker_bridge_ip: 192.168.0.1/24 }

Setup app-emulation/docker with btrfs backed storage on /dev/sdb:

    - hosts: docker
      roles:
         - { role: role-docker, docker_storage_device: /dev/sdb, docker_storage_type :btrfs }

Setup app-emulation/docker with lvm backed storage on /dev/sdb:

    - hosts: docker
      roles:
         - { role: role-docker, docker_storage_device: /dev/sdb docker_storage_type: lvm }

License
-------

GPL3

Author Information
------------------

This role was created by Davide "CuB0" Rebeccani.