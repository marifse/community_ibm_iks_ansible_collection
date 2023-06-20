.. -*- coding: utf-8 -*-
.. _module-ibm_container_update_master:

ibm_container_update_master
===========================

.. meta::
    :metadata_version: 1.1
    :status: ['preview']
    :supported_by: community

.. versionadded:: 1.0.0

The Delete the specified worker node from the cluster and new worker node will be added.

Requirements
------------

None.

Options
-------

``ibmcloud_api_key`` (required)
    The IBM Cloud API Key.

``resource_group_id`` (required)
    The Resource Group ID.

``config`` (required)
    Configuration

    ``cluster`` (required)
        The cluster id which needs to be monitored.

    ``force`` (required)
        The cluster id which needs to be monitored.

    ``version`` (required)
        The cluster id which needs to be monitored.

Examples
--------

Target the cluster which is present in the default resource group:

.. code-block:: yaml

    - name: Example playbook
      hosts: localhost
      tasks:
        - name: Update Master
          ibm_container_update_master:
            ibmcloud_api_key: "{{ name }}"
            resource_group_id: "{{ resource_group_id }}"
            config:
              cluster: "your-cluster-id"
              force: true
              version: "worker-id-name"
