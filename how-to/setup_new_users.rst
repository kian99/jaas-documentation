JAAS: Setup New Users
=====================

This how-to describes how a new user can begin to use JAAS to deploy applications.

Prerequisites
-------------

For this how-to you will need the following:

- A running JAAS environment, see :doc:`our tutorial <../tutorial/deploy_jaas_microk8s>`.
- A controller connected to JAAS, see :doc:`our how-to <./add_controller>`. This how-to assumes you have added an LXD controller.

Login to JAAS
-------------

Login to JAAS for the first time:

.. code:: bash

    juju login test-jimm.localhost:443 -c jaas

Running ``juju controllers`` will now show you the ``jaas`` controller.
Commands like ``juju models`` will now work.

Cloud Credentials
-----------------

Before we can create a model, your user requires a set of cloud `credentials <https://juju.is/docs/juju/credential>`__.

View credentials available on your client:

.. code:: bash

    juju credentials --client

The output should resemble the following

.. code:: bash

    Client Credentials:
    Cloud      Credentials
    localhost  localhost*
    microk8s   microk8s*

We will upload credentials for LXD - the `localhost` credentials.

.. code:: bash

    juju update-credentials localhost --controller jimm

.. hint::

    For clouds like Openstack or public clouds, use the `juju add-credential` command to interactively
    add credentials to your client and controller.

Credentials are now available on the controller for your user to deploy models on the LXD cloud.

Deploy
------

Now we can deploy a model and application:

.. code:: bash

    juju add-model test-model
    juju deploy ubuntu

We've successfully added a set of cloud-credentials and deployed an application into a model.