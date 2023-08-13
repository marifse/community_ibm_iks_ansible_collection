ibm.container_image_security_disable module -- Delete a secret from an NLB subdomain in your cluster
===================================================

Note

This module is part of the ibm collection (version 1.0.0).

To install it, use: ansible-galaxy collection install ibm. You need further requirements to be able to use this module, see :ref:`Requirements <ansible_collections.ibm.ibm_container_image_security_disable_module_requirements>` for details.

To use it in a playbook, specify: :code:`ibm.container_image_security_disable`.

.. contents::
   :local:
   :depth: 1

.. Deprecated

Synopsis
--------

This module deletes a secret from an NLB subdomain in your cluster and prevents future renewal of the certificate.

Requirements
------------

The below requirements are needed on the host that executes this module.

No requirements needed.



Parameters
----------


.. raw:: html

  <table class="colwidths-auto ansible-option-table docutils align-default" style="width: 100%">
  <thead>
  <tr class="row-odd">
    <th class="head"><p>Parameter</p></th>
    <th class="head"><p>Comments</p></th>
  </tr>
  </thead>
  <tbody>
  <tr class="row-even">
    <td><div class="ansible-option-cell">
      <div class="ansibleOptionAnchor" id="parameter-id"></div>
      <p class="ansible-option-title"><strong>ibmcloud_api_key</strong></p>
      <a class="ansibleOptionLink" href="#parameter-id" title="Permalink to this option"></a>
      <p class="ansible-option-type-line">
        <span class="ansible-option-type">string</span>
      </p>
    </div></td>
    <td><div class="ansible-option-cell">
      <p>Unique ID of the service ID.</p>
    </div></td>
  </tr>
  <tr class="row-odd">
    <td><div class="ansible-option-cell">
      <div class="ansibleOptionAnchor" id="parameter-include_activity"></div>
      <p class="ansible-option-title"><strong>include_activity</strong></p>
      <a class="ansibleOptionLink" href="#parameter-include_activity" title="Permalink to this option"></a>
      <p class="ansible-option-type-line">
        <span class="ansible-option-type">boolean</span>
      </p>
    </div></td>
    <td><div class="ansible-option-cell">
      <p>Defines if the entity&#x27;s activity is included in the response.
      Retrieving activity data is an expensive operation, so please only request this when needed.
      </p>
      <p class="ansible-option-line"><span class="ansible-option-choices">Choices:</span></p>
      <ul class="simple">
        <li><p><span class="ansible-option-choices-entry">false</span></p></li>
        <li><p><span class="ansible-option-choices-entry">true</span></p></li>
      </ul>
    </div></td>
  </tr>
  <tr class="row-even">
    <td><div class="ansible-option-cell">
      <div class="ansibleOptionAnchor" id="parameter-include_history"></div>
      <p class="ansible-option-title"><strong>include_history</strong></p>
      <a class="ansibleOptionLink" href="#parameter-include_history" title="Permalink to this option"></a>
      <p class="ansible-option-type-line">
        <span class="ansible-option-type">boolean</span>
      </p>
    </div></td>
    <td><div class="ansible-option-cell">
      <p>Defines if the entity history is included in the response.</p>
      <p class="ansible-option-line"><span class="ansible-option-choices">Choices:</span></p>
      <ul class="simple">
        <li><p><span class="ansible-option-choices-entry">false</span></p></li>
        <li><p><span class="ansible-option-choices-entry">true</span></p></li>
      </ul>
    </div></td>
  </tr>
  </tbody>
  </table>



.. Attributes


.. Notes


.. Seealso


.. Examples


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

Authors
~~~~~~~

- Muhammad Arif (@marifse)
