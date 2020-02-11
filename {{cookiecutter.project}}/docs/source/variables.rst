Variables
------------------------------------------------------------------------------

The following variables are supported:

upgrade
..............................................................................

Boolean variable that defines if a system full upgrade is performed or not.

If set to *true* a full system upgrade is executed.

This variable is set to *true* by default.

.. substitution-code-block:: bash

 # Including from terminal.
 ansible localhost -m include_role -a name=|AUTHOR|.|PROJECT| -K -e \
     "upgrade=false"

 # Including on a playbook.
 - hosts: servers
   roles:
     - role: |AUTHOR|.|PROJECT|
       upgrade: false

 # To a playbook from terminal.
 ansible-playbook -i tests/inventory tests/test-playbook.yml -K -e \
     "upgrade=false"

