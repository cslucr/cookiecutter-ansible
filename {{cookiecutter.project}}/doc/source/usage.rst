Usage
------------------------------------------------------------------------------

To install and execute:

.. substitution-code-block:: bash

 ansible-galaxy install |AUTHOR|.|PROJECT|
 ansible localhost -m include_role -a name=|AUTHOR|.|PROJECT| -K

Passing variables:

.. substitution-code-block:: bash

 ansible localhost -m include_role -a name=|AUTHOR|.|PROJECT| -K \
     |DEFAULT_ROLE_VARS|

To include the role on a playbook:

.. substitution-code-block:: bash

 - hosts: servers
   roles:
       - {role: |AUTHOR|.|PROJECT|}

To include the role as dependency on another role:

.. substitution-code-block:: bash

 dependencies:
   - role: |AUTHOR|.|PROJECT|
     |DEFAULT_VAR_NAME|: |DEFAULT_VAR_VALUE|

To use the role from tasks:

.. substitution-code-block:: bash

 - name: Execute role task.
   import_role:
     name: |AUTHOR|.|PROJECT|
   vars:
     |DEFAULT_VAR_NAME|: |DEFAULT_VAR_VALUE|

To run tests:

.. substitution-code-block:: bash

 cd |PROJECT|
 ./testme.sh


