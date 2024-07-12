ECGALAXY aws_cli role
=====================

This Ansible role installs the latest version of the [AWS CLI](https://aws.amazon.com/cli/).

The [Session Manager plugin](https://docs.aws.amazon.com/systems-manager/latest/userguide/session-manager-working-with-install-plugin.html)
is also installed (can be disabled by setting `awscli_ssm_install` to `false`).

Requirements
------------

- The `gpg` command, which can be provided by the `ecgalaxy.common_packages` role.

Role Variables
--------------

For the list of all the available variables check the files under `defaults/` and `vars/`.

Dependencies
------------

- optional: ecgalaxy.common_packages

Example Playbook
----------------

    - hosts: all
      roles:
        - ecgalaxy.bootstrap
        - ecgalaxy.common_packages
        - ecgalaxy.aws_cli

One-liner
---------

    bash <(curl -s https://code.europa.eu/-/snippets/1/raw/main/ansible-role.sh) ecgalaxy.aws_cli

See [ansible-role](https://code.europa.eu/-/snippets/1) for instructions.

Please verify the script integrity first.

Upgrading & Uninstalling
------------------------

In order to upgrade, reexecute this Ansible role after a new version has been released.

To uninstall, follow [those instructions](https://docs.aws.amazon.com/cli/latest/userguide/uninstall.html).

License
-------

Copyright the European Union 2022.

Licensed under the EUPL-1.2 or later.

Author Information
------------------

[ECGALAXY](https://code.europa.eu/groups/ecgalaxy/-/wikis/home) team.
