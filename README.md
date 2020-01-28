[![Build Status](https://travis-ci.com/oasis-roles/ocp_azure_driver.svg?branch=master)](https://travis-ci.com/oasis-roles/ocp_azure_driver)

ocp_azure_driver
===========

This role takes a previously provisioned bastion-vm and sets it up to install openshift on azure. It also configures
the azure infrastructure needed for a successful openshift install on azure.

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

The following environment variables must be set for this automation to work:
AZURE_SP_NAME = Service Principal Name
AZURE_TENANT_ID = Tenant ID
AZURE_SP_CLIENT_ID = Azure client ID
AZURE_SUBSCRIPTION_ID = Azure subscription ID

Dependencies
------------

None

Example Playbook
----------------

```yaml
- name: Configure driver vm
  hosts: ocp_azure_driver-servers
  user: root

  roles:
    - role: oasis_roles.ocp_azure_driver
```

License
-------

GPLv3

Author Information
------------------

PIQE Team
