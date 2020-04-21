minio_podman
============

Ansible role to install and run minio with podman on EL 8 hosts.


Role Variables
--------------

To use this role three variables should be set for the storage location and key/secret:

    minio_podman_data_dir: /srv/minio
    minio_podman_key: CHANGEME
    minio_podman_secret: CHANGEMECHANGEME


Dependencies
------------

None.


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - smlloyd.minio_podman


License
-------

GPLv4
