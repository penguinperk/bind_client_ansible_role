
An Ansible role to configure /etc/resolv.conf

Role Name
=========

An Ansible role that consigures DNS Resolver (resolv.conf)

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------


## Role Variables
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

## Example Playbooks
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

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
