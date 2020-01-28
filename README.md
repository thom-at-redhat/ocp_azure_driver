[![Build Status](https://travis-ci.com/oasis-roles/ocp_azure_driver.svg?branch=master)](https://travis-ci.com/oasis-roles/ocp_azure_driver)

ocp_azure_driver
===========

Basic description for ocp_azure_driver

Requirements
------------

Ansible 2.4 or higher

Red Hat Enterprise Linux 7 or equivalent

Valid Red Hat Subscriptions

Role Variables
--------------

Currently the following variables are supported:

### General

* `ocp_azure_driver_become` - Default: true. If this role needs administrator
  privileges, then use the Ansible become functionality (based off sudo).
* `ocp_azure_driver_become_user` - Default: root. If the role uses the become
  functionality for privilege escalation, then this is the name of the target
  user to change to.

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: ocp_azure_driver-servers
  roles:
    - role: oasis_roles.ocp_azure_driver
```

License
-------

GPLv3

Author Information
------------------

Author Name <authoremail@domain.net>