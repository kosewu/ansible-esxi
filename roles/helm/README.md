helm
=========

[![Build Status](https://travis-ci.org/devoperate/ansible-helm.svg?branch=master)](https://travis-ci.org/devoperate/ansible-helm)

Installs a desired release of Kubernetes Helm on Linux.

Requirements
------------

The target host needs to be running Linux. For Helm to be of any use, you'll also need a line of sight from the target host to your cluster's API endpoint.

Role Variables
--------------

Any version of Helm can be installed by changing the `helm_version` variable's value to just the SemVer of the version you want to install. Overriding this variable and re-running the role can up/downgrade Helm on the target host.

Dependencies
------------

See meta/main.yml.

Example Playbook
----------------

```yaml
- hosts: localhost
  roles:
    - role: devoperate.helm
      vars:
        helm_version: "2.14.0"
```

License
-------

See LICENSE.

Author Information
------------------

- [Claude Léveillé](https://cleveille.com)
