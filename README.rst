ARA Records Ansible
===================
.. image:: doc/source/_static/ara-with-icon.png

ARA Records Ansible playbook runs and makes the recorded data available and
intuitive for users and systems.

ARA doesn't run your playbooks for you: it integrates with Ansible as a
callback plugin wherever it is.

Whether you are running Ansible from your personal laptop or a server, all
you need to do is to `install ARA`_, `configure Ansible to use ARA`_ and
you're good to go.

.. image:: doc/source/_static/reports.png

.. _install ARA: https://ara.readthedocs.io/en/latest/installation.html
.. _configure Ansible to use ARA: https://ara.readthedocs.io/en/latest/configuration.html

Quickstart
==========

::

    # Install ARA
    pip install ara

    # Load environment variables that inform Ansible to use ARA regardless
    # of its location or python version
    source <(python -m ara.setup.env)

    # Run your Ansible playbook or commands
    # ansible-playbook myplaybook.yml

    # Start the ARA standalone webserver
    ara-manage runserver
    # Browse http://127.0.0.1:9191

Refer to the documentation_ for more information.

.. _documentation: https://ara.readthedocs.io/en/latest/

ARA components
==============

ARA has four main components:

1. An `Ansible callback plugin`_ to record playbook runs into a local or remote database
2. The ara_record_ and ara_read_ pair of Ansible modules to record and read persistent data with ARA
3. A `CLI client`_ to query the database
4. A `dynamic, database-driven web interface`_ that can also be `generated and served from static files`_

.. _ARA: https://github.com/openstack/ara
.. _Ansible: https://www.ansible.com/
.. _Ansible callback plugin: https://ara.readthedocs.io/en/latest/configuration.html#ansible
.. _ara_record: https://ara.readthedocs.io/en/latest/usage.html#using-the-ara-record-module
.. _ara_read: https://ara.readthedocs.io/en/latest/usage.html#using-the-ara-read-module
.. _CLI client: https://ara.readthedocs.io/en/latest/usage.html#querying-the-database-with-the-cli
.. _dynamic, database-driven web interface: https://ara.readthedocs.io/en/latest/faq.html#what-does-the-web-interface-look-like
.. _generated and served from static files: https://ara.readthedocs.io/en/latest/usage.html#generating-a-static-html-version-of-the-web-application

What does the web interface look like ?
---------------------------------------

A video preview and explanation of the web interface is available on
YouTube_, featuring playbook runs from the OpenStack-Ansible_ project.

Otherwise, screenshots highlighting some of ARA's features are available in
`the frequently asked questions`_

.. _YouTube: https://www.youtube.com/watch?v=k3i8VPCanGo
.. _OpenStack-Ansible: https://github.com/openstack/openstack-ansible
.. _the frequently asked questions: https://ara.readthedocs.io/en/latest/faq.html#interface-preview

Community and getting help
==========================

You can chat with the ARA community on Slack and IRC.
The two are transparently bridged with teamchat_ which broadcasts messages from
one platform to the other.

In addition, you can also find ARA on Twitter: `@ARecordsAnsible <https://twitter.com/ARecordsAnsible>`_

**IRC**

- Server: `irc.freenode.net`_
- Channel: #ara

**Slack**

- https://arecordsansible.slack.com
- Join with the `Slack invitation <https://join.slack.com/t/arecordsansible/shared_invite/enQtMjMxNzI4ODAxMDQxLWU4MmZhZTI4ZjRjOTUwZTM2MzM3MzcwNDU1YzFmNzRlMzI0NTUzNDY1MWJlNThhM2I4ZTViZjUwZTRkNTBiM2I>`_

.. _teamchat: https://github.com/dmsimard/teamchat
.. _irc.freenode.net: https://webchat.freenode.net/

Contributing, testing, issues and bugs
======================================

Contributions to ARA are definitely welcome and much appreciated !

ARA does not use GitHub for issues or pull requests.

ARA uses the OpenStack infrastructure for code hosting and review as well as
project and bug/issue tracking.

The `contributor documentation`_ will get you started quickly if you need help
contributing !

* Submitted code reviews are available on **Gerrit**:
  https://review.openstack.org/#/q/project:openstack/ara
* Bugs, issues and feature tracking are available on **StoryBoard**:
  https://storyboard.openstack.org/#!/project/843

Each commit to ARA is reviewed and also rigorously tested to prevent
regressions. Here's our current testing coverage:

+-----------------+--------+--------+----------+--------+--------+
| -               | Fedora | CentOS | OpenSUSE | Debian | Ubuntu |
+=================+========+========+==========+========+========+
| Ansible 2.5.9   |        |  py27  |          |        |        |
+-----------------+--------+--------+----------+--------+--------+
| Ansible 2.6.5   |        |        |          |  py27  |        |
+-----------------+--------+--------+----------+--------+--------+
| Ansible 2.7.0   |  py35  |        |   py27   |        |  py35  |
+-----------------+--------+--------+----------+--------+--------+
| Ansible "devel" |  py35  |        |          |        |  py35  |
+-----------------+--------+--------+----------+--------+--------+

You might also be interested in reading the project manifesto_ in order to have
a good understanding of the project's core values and philosophy.

.. _contributor documentation: https://ara.readthedocs.io/en/latest/contributing.html
.. _manifesto: https://ara.readthedocs.io/en/latest/manifesto.html

Documentation
=============

`Frequently asked questions`_ and documentation on how to install_, configure_,
use_ to ARA is available on `readthedocs.io`_.

.. _Frequently asked questions: https://ara.readthedocs.io/en/latest/faq.html
.. _install: https://ara.readthedocs.io/en/latest/installation.html
.. _configure: https://ara.readthedocs.io/en/latest/configuration.html
.. _use: https://ara.readthedocs.io/en/latest/usage.html

.. _readthedocs.io: https://ara.readthedocs.io/en/latest/

Contributors
============

See contributors on GitHub_.

.. _GitHub: https://github.com/openstack/ara/graphs/contributors

Copyright
=========

::

    Copyright (c) 2018 Red Hat, Inc.

    ARA is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.

    ARA is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with ARA.  If not, see <http://www.gnu.org/licenses/>.
