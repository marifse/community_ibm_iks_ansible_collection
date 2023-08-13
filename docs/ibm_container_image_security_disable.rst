ibm.container_image_security_disable module -- Delete a secret from an NLB subdomain in your cluster
===================================================

Note

This module is part of the ibm collection (version 1.0.0).

To install it, use: ansible-galaxy collection install ibm. You need further requirements to be able to use this module, see :ref:`Requirements <ansible_collections.ibm.ibm_container_image_security_disable_module_requirements>` for details.

To use it in a playbook, specify: `ibm.container_image_security_disable`.

Synopsis
--------

This module deletes a secret from an NLB subdomain in your cluster and prevents future renewal of the certificate.

Requirements
------------

The below requirements are needed on the host that executes this module.

No requirements needed.

Parameters
----------

Parameter | Choices/<font color="blue">Defaults</font> | Comments
--------- | --------- | --------
**ibmcloud_api_key** | <font color="blue">required</font> | The IBM Cloud API Key.
**resource_group_id** | <font color="blue">required</font> | The ResourceGroup ID
**config** | <font color="blue">required</font> | Configuration

**config** suboptions:

- **cluster**: <font color="blue">required</font> <font color="magenta">[default: null]</font>
        The cluster id which needs to be monitored.

Examples
--------

Example usage:

```yaml
- name: Delete secret from NLB subdomain in cluster
  ibm.container_image_security_disable:
    ibmcloud_api_key: "{{ ibmcloud_api_key }}"
    resource_group_id: "{{ resource_group_id }}"
    config:
      cluster: "Your Cluster ID"
