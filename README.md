NYCRecords Common
=========

Setup the base requirements for a NYC Department of Records RHEL Server

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

```yaml
volumes:
  - device: /dev/<device_name>
    fstype: <Filesystem type (e.g. xfs)>
    path: <Mount Point>
    src: "UUID=<UUID for Volume"
```

Volumes is a list of dictionaries for formatting and mounting new volumes.

```yaml
setup_mount_points: true
```

Determines whether volumes and mount points should be setup using this role. Defaults to True.

```yaml
reformat_volumes: false
```

Determines whether this role should reformat all volumes when mounting as part of this role. Defaults to False.

```yaml
setup_proxy: true
```

Determines whether the role should setup the HTTP/HTTPS/FTP/NO_PROXY variables globally. Defaults to True.

```yaml
setup_https: true
```

Determines whether this role should create a CSR and self-signed cert for the server. CSR will be copied to the Ansible Control Node. Defaults to True.

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }
```

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
