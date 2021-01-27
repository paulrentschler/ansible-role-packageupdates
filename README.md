paulrentschler.packageupdates
=============================

Ansible role to manage package updates.

Requirements
------------

None.


Role Variables
--------------

The following variables are available with defaults defined in `defaults/main.yml`:

Updating the installed packages can be a time consuming process. So repeative runs of this role go quickly, updating the packages is skipped by default.

    packageupdates_skip_updates: yes

Define this variable elsewhere and set it to `no` to ensure installed packages get updated.

The variable can also be set via a command line argument:

    --extra-vars="packageupdates_skip_updates=no"


Dependencies
------------

None.


Example Playbook
----------------

Setup the daily check but do not update packages

    - hosts: servers
      roles:
         - paulrentschler.packageupdates

Setup the daily check and update the packages

    - hosts: servers
      roles:
         - { role: paulrentschler.packageupdates,
             packageupdates_skip_updates: no
             }


License
-------

MIT


Author Information
------------------

Created by Paul Rentschler in 2021.
