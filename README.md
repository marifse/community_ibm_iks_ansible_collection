# IBM Cloud Ansible Collections

Ansible modules collection for IBM cloud.

## Getting Started
Below steps are follwed to install ansible collections for the IBM Cloud resources. All the resources are documented under the [Docs] directory.

## Prerequisites

1. [Install ansible].

2.  To install ansible on Ubuntu 20.04, run the below command: 

    ```
    sudo apt install ansible -y
    ```
    **Note**: These automation playbooks have been tested on ansible 2.9.6 on ubuntu 20.04.

## Install 

1. Build and Install collection
    
    ```
    ansible-galaxy collection build
    ```

    ```
    ansible-galaxy collection install collection_name.tar
    ```

### Example Projects

1. [Manage Storage Attachment](https://github.com/marifse/community.ansible.ibm.cloud/tree/main/examples/ibm_bare_metal_status_change)

2. [Manage Config Monitoring](https://github.com/marifse/community.ansible.ibm.cloud/tree/main/examples/ibm_floating_ip_actions)

3. [Manage IKS Cluster](https://github.com/marifse/community.ansible.ibm.cloud/tree/main/examples/ibm_loadbalancer_policy)

4. [Manage IKS Image Security](https://github.com/marifse/community.ansible.ibm.cloud/tree/main/examples/ibm_loadbalancer_policy_rule)

5. [Manage Ingress ALB for IKS](https://github.com/marifse/community.ansible.ibm.cloud/tree/main/examples/ibm_loadbalancer_policy_rule_update)

6. [Manage NLB Health Monitor](https://github.com/marifse/community.ansible.ibm.cloud/tree/main/examples/ibm_virtual_endpoint_gateway_ip_bind-unbind)

7. [Manage Private/Public Service Endpoints](https://github.com/marifse/community.ansible.ibm.cloud/tree/main/examples/ibm_vpc_private_ip_reserve)

8. [Manage Secrets for IKS](https://github.com/marifse/community.ansible.ibm.cloud/tree/main/examples/ibm_vpc_private_ip_reserve_update)


[Install ansible]: https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html
[Docs]: https://github.com/IBM-Cloud/ansible-collection-ibm/tree/master/docs

