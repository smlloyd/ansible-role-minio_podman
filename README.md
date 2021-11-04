[![Build Status](https://travis-ci.com/smlloyd/ansible-role-minio_podman.svg?branch=master)](https://travis-ci.com/smlloyd/ansible-role-minio_podman)

minio_podman
============

Ansible role to install and run minio with podman on EL 8 hosts.

---
**NOTE**

This role has been updated to create a pod with a minio container in it instead of just a single container. This may result in errors when using this role with old installations. To fix this, please remove the existing container and systemd unit files manually and rerun ansible.

---


Role Variables
--------------

To use this role three variables should be set for the storage location and key/secret:

    minio_podman_data_dir: /srv/minio
    minio_podman_root_user: CHANGEME
    minio_podman_root_password: CHANGEMECHANGEME
    minio_podman_env:
      - MINIO_REGION_NAME=us-east-1

Additional variables with their defaults can be found in `defaults/main.yml`.

Dependencies
------------

None.


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - smlloyd.minio_podman
           minio_podman_root_user: AKIAIOSFODNN7EXAMPLE
           minio_podman_root_password: wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY


License
-------

GPLv3
