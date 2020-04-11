

Role Name
=========

An Ansible role that configure the  DNS Resolver (resolv.conf)

Requirements
------------

Currently only being tested on Freebsd 12 

Role Variables
--------------

### Defaults
| Variable Name | Required | Description | Default Value | Type |
| --- | :---: | --- | :---: | :---: |
|resolv_nameservers| yes | A list of up to 3 nameserver IP addresses | [] | list |
| resolv_domain | no | Local domain name | "" | string |
| resolv_search | no | List of up to 6 domains to search for host-name lookup | [] | list |
| resolv_sortlist | no | List of IP-address and netmask pairs to sort addresses returned by gethostbyname. | [] | list |
| resolv_options | no | List of options to modify certain internal resolver variables. | [] | list |


Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

### Role Invocation
```yaml
    - name: "Role Invocation - ahuffman.resolv Example"
      hosts: "all"
      roles:
        - role: "ahuffman.resolv"
          resolv_nameservers:
            - "8.8.8.8"
            - "8.8.4.4"
          resolv_domain: "foo.org"
          resolv_search:
            - "foo.bar"
            - "foobar.com"
          resolv_options:
            - "timeout:2"
```

License
-------

BSD

Author Information
------------------

PenguinPerk

#### Feedback, bug-reports, requests, ...

[Submit](https://github.com/penguinperk/bind_client_ansible_role/issues)

