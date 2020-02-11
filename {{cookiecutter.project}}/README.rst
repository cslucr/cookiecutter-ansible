
ansible
*******

.. image:: https://git.beta.ucr.ac.cr/{{ cookiecutter.author }}/{{ cookiecutter.project }}/badges/master/pipeline.svg
   :alt: pipeline

.. image:: https://travis-ci.com/{{ cookiecutter.author }}/{{ cookiecutter.project }}.svg
   :alt: travis

.. image:: https://readthedocs.org/projects/{{ cookiecutter.project }}/badge
   :alt: readthedocs

Ansible role to apply configuration.

Full documentation on `Readthedocs <https://{{ cookiecutter.project }}.readthedocs.io>`_.

Source code on:

`Github <https://github.com/{{ cookiecutter.author }}/{{ cookiecutter.project }}>`_.

`Gitlab <https://git.beta.ucr.ac.cr/{{ cookiecutter.author }}/{{ cookiecutter.project }}>`_.


Contents
********

* `Description <#Description>`_
* `Usage <#Usage>`_
* `Variables <#Variables>`_
   * `upgrade <#upgrade>`_
* `Requirements <#Requirements>`_
* `Compatibility <#Compatibility>`_
* `License <#License>`_
* `Links <#Links>`_
* `UML <#UML>`_
   * `Class <#class>`_
* `Author <#Author>`_

Description
***********

Ansible role to apply configuration.


Usage
*****

* To install and execute:

..

   ::

      ansible-galaxy install {{ cookiecutter.author }}.{{ cookiecutter.project }}
      ansible localhost -m include_role -a name={{ cookiecutter.author }}.{{ cookiecutter.project }} -K

* Passing variables:

..

   ::

      ansible localhost -m include_role -a name={{ cookiecutter.author }}.{{ cookiecutter.project }} -K \
          -e "upgrade: false"

* To include the role on a playbook:

..

   ::

      - hosts: servers
        roles:
            - {role: {{ cookiecutter.author }}.{{ cookiecutter.project }}}

* To include the role as dependency on another role:

..

   ::

      dependencies:
        - role: {{ cookiecutter.author }}.{{ cookiecutter.project }}
          upgrade: true

* To use the role from tasks:

..

   ::

      - name: Execute role task.
        import_role:
          name: {{ cookiecutter.author }}.{{ cookiecutter.project }}
        vars:
          upgrade: true

* To run tests:

..

   ::

      cd {{ cookiecutter.project }}
      chmod +x testme.sh
      ./testme.sh

   On some tests you may need to use *sudo* to succeed.


Variables
*********

The following variables are supported:


upgrade
=======

Boolean variable that defines if a system full upgrade is performed or
not.

If set to *true* a full system upgrade is executed.

This variable is set to *true* by default.

::

   # Including from terminal.
   ansible localhost -m include_role -a name={{ cookiecutter.author }}.{{ cookiecutter.project }} -K -e \
       "upgrade=false"

   # Including on a playbook.
   - hosts: servers
     roles:
       - role: {{ cookiecutter.author }}.{{ cookiecutter.project }}
         upgrade: false

   # To a playbook from terminal.
   ansible-playbook -i tests/inventory tests/test-playbook.yml -K -e \
       "upgrade=false"


Requirements
************

* `Ansible <https://www.ansible.com>`_ >= 2.8.

* `Jinja2 <https://palletsprojects.com/p/jinja/>`_.

* `Pip <https://pypi.org/project/pip/>`_.

* `Python <https://www.python.org/>`_.

If you want to run the tests, you will also need:

* `Docker <https://www.docker.com/>`_.

* `Molecule <https://molecule.readthedocs.io/>`_.


Compatibility
*************

* `Debian Buster <https://wiki.debian.org/DebianBuster>`_.

* `Debian Raspbian <https://raspbian.org/>`_.

* `Debian Stretch <https://wiki.debian.org/DebianStretch>`_.

* `Ubuntu Bionic <http://releases.ubuntu.com/18.04/>`_.

* `Ubuntu Xenial <http://releases.ubuntu.com/16.04/>`_.


License
*******

GPL 3. See the LICENSE file for more details.


Links
*****

`Github <https://github.com/{{ cookiecutter.author }}/{{ cookiecutter.project }}>`_.

`Gitlab <https://git.beta.ucr.ac.cr/{{ cookiecutter.author }}/{{ cookiecutter.project }}>`_.

`Readthedocs <https://{{ cookiecutter.project }}.readthedocs.io>`_.


UML
***


Class
=====

The class structure is shown below:

.. image:: https://git.beta.ucr.ac.cr/{{ cookiecutter.author }}/{{ cookiecutter.project }}/raw/master/img/class.png
   :alt: class


Author
******

.. image:: https://git.beta.ucr.ac.cr/{{ cookiecutter.author }}/{{ cookiecutter.project }}/raw/master/img/author.png
   :alt: author

Comunidad de Software Libre de la Universidad de Costa Rica.

