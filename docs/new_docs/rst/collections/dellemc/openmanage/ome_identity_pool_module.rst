
.. Document meta

:orphan:

.. |antsibull-internal-nbsp| unicode:: 0xA0
    :trim:

.. role:: ansible-attribute-support-label
.. role:: ansible-attribute-support-property
.. role:: ansible-attribute-support-full
.. role:: ansible-attribute-support-partial
.. role:: ansible-attribute-support-none
.. role:: ansible-attribute-support-na
.. role:: ansible-option-type
.. role:: ansible-option-elements
.. role:: ansible-option-required
.. role:: ansible-option-versionadded
.. role:: ansible-option-aliases
.. role:: ansible-option-choices
.. role:: ansible-option-choices-default-mark
.. role:: ansible-option-default-bold
.. role:: ansible-option-configuration
.. role:: ansible-option-returned-bold
.. role:: ansible-option-sample-bold

.. Anchors

.. _ansible_collections.dellemc.openmanage.ome_identity_pool_module:

.. Anchors: short name for ansible.builtin

.. Anchors: aliases



.. Title

dellemc.openmanage.ome_identity_pool module -- Manages identity pool settings on OpenManage Enterprise
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. Collection note

.. note::
    This module is part of the `dellemc.openmanage collection <https://galaxy.ansible.com/dellemc/openmanage>`_ (version 8.5.0).

    To install it, use: :code:`ansible-galaxy collection install dellemc.openmanage`.
    You need further requirements to be able to use this module,
    see :ref:`Requirements <ansible_collections.dellemc.openmanage.ome_identity_pool_module_requirements>` for details.

    To use it in a playbook, specify: :code:`dellemc.openmanage.ome_identity_pool`.

.. version_added

.. rst-class:: ansible-version-added

New in dellemc.openmanage 2.1.0

.. contents::
   :local:
   :depth: 1

.. Deprecated


Synopsis
--------

.. Description

- This module allows to create, modify, or delete a single identity pool on OpenManage Enterprise.


.. Aliases


.. Requirements

.. _ansible_collections.dellemc.openmanage.ome_identity_pool_module_requirements:

Requirements
------------
The below requirements are needed on the host that executes this module.

- python \>= 3.8.6






.. Options

Parameters
----------

.. rst-class:: ansible-option-table

.. list-table::
  :width: 100%
  :widths: auto
  :header-rows: 1

  * - Parameter
    - Comments

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-ca_path"></div>

      .. _ansible_collections.dellemc.openmanage.ome_identity_pool_module__parameter-ca_path:

      .. rst-class:: ansible-option-title

      **ca_path**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-ca_path" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`path`

      :ansible-option-versionadded:`added in dellemc.openmanage 5.0.0`


      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The Privacy Enhanced Mail (PEM) file that contains a CA certificate to be used for the validation.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-ethernet_settings"></div>

      .. _ansible_collections.dellemc.openmanage.ome_identity_pool_module__parameter-ethernet_settings:

      .. rst-class:: ansible-option-title

      **ethernet_settings**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-ethernet_settings" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Applicable for creating and modifying an identity pool using Ethernet settings.

      \ :emphasis:`starting\_mac\_address`\  and \ :emphasis:`identity\_count`\  are required to create an identity pool.


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-ethernet_settings/identity_count"></div>

      .. _ansible_collections.dellemc.openmanage.ome_identity_pool_module__parameter-ethernet_settings/identity_count:

      .. rst-class:: ansible-option-title

      **identity_count**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-ethernet_settings/identity_count" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Number of MAC addresses.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-ethernet_settings/starting_mac_address"></div>

      .. _ansible_collections.dellemc.openmanage.ome_identity_pool_module__parameter-ethernet_settings/starting_mac_address:

      .. rst-class:: ansible-option-title

      **starting_mac_address**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-ethernet_settings/starting_mac_address" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Starting MAC address of the ethernet setting.


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-fc_settings"></div>

      .. _ansible_collections.dellemc.openmanage.ome_identity_pool_module__parameter-fc_settings:

      .. rst-class:: ansible-option-title

      **fc_settings**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-fc_settings" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Applicable for creating and modifying an identity pool using fibre channel(FC) settings.

      This option allows OpenManage Enterprise to generate a Worldwide port name (WWPN) and Worldwide node name (WWNN) address.

      The value 0x2001 is beginning to the starting address for the generation of a WWPN, and 0x2000 for a WWNN.

      \ :emphasis:`starting\_address`\  and \ :emphasis:`identity\_count`\  are required to create an identity pool.


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-fc_settings/identity_count"></div>

      .. _ansible_collections.dellemc.openmanage.ome_identity_pool_module__parameter-fc_settings/identity_count:

      .. rst-class:: ansible-option-title

      **identity_count**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-fc_settings/identity_count" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Number of MAC addresses.\ :emphasis:`identity\_count`\  is required to option to create FC settings.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-fc_settings/starting_address"></div>

      .. _ansible_collections.dellemc.openmanage.ome_identity_pool_module__parameter-fc_settings/starting_address:

      .. rst-class:: ansible-option-title

      **starting_address**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-fc_settings/starting_address" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Starting MAC Address of FC setting.\ :emphasis:`starting\_address`\  is required to option to create FC settings.


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-fcoe_settings"></div>

      .. _ansible_collections.dellemc.openmanage.ome_identity_pool_module__parameter-fcoe_settings:

      .. rst-class:: ansible-option-title

      **fcoe_settings**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-fcoe_settings" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Applicable for creating and modifying an identity pool using FCoE settings.

      \ :emphasis:`starting\_mac\_address`\  and \ :emphasis:`identity\_count`\  are required to create an identity pool.


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-fcoe_settings/identity_count"></div>

      .. _ansible_collections.dellemc.openmanage.ome_identity_pool_module__parameter-fcoe_settings/identity_count:

      .. rst-class:: ansible-option-title

      **identity_count**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-fcoe_settings/identity_count" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Number of MAC addresses.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-fcoe_settings/starting_mac_address"></div>

      .. _ansible_collections.dellemc.openmanage.ome_identity_pool_module__parameter-fcoe_settings/starting_mac_address:

      .. rst-class:: ansible-option-title

      **starting_mac_address**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-fcoe_settings/starting_mac_address" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Starting MAC Address of the FCoE setting.


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-hostname"></div>

      .. _ansible_collections.dellemc.openmanage.ome_identity_pool_module__parameter-hostname:

      .. rst-class:: ansible-option-title

      **hostname**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-hostname" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      OpenManage Enterprise or OpenManage Enterprise Modular IP address or hostname.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-iscsi_settings"></div>

      .. _ansible_collections.dellemc.openmanage.ome_identity_pool_module__parameter-iscsi_settings:

      .. rst-class:: ansible-option-title

      **iscsi_settings**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-iscsi_settings" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Applicable for creating and modifying an identity pool using ISCSI settings.

      \ :emphasis:`starting\_mac\_address`\ , \ :emphasis:`identity\_count`\ , \ :emphasis:`iqn\_prefix`\ , \ :emphasis:`ip\_range`\  and \ :emphasis:`subnet\_mask`\  are required to create an identity pool.


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-iscsi_settings/identity_count"></div>

      .. _ansible_collections.dellemc.openmanage.ome_identity_pool_module__parameter-iscsi_settings/identity_count:

      .. rst-class:: ansible-option-title

      **identity_count**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-iscsi_settings/identity_count" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Number of MAC addresses.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-iscsi_settings/initiator_config"></div>

      .. _ansible_collections.dellemc.openmanage.ome_identity_pool_module__parameter-iscsi_settings/initiator_config:

      .. rst-class:: ansible-option-title

      **initiator_config**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-iscsi_settings/initiator_config" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Applicable for creating and modifying an identity pool using iSCSI Initiator settings.


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-iscsi_settings/initiator_config/iqn_prefix"></div>

      .. _ansible_collections.dellemc.openmanage.ome_identity_pool_module__parameter-iscsi_settings/initiator_config/iqn_prefix:

      .. rst-class:: ansible-option-title

      **iqn_prefix**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-iscsi_settings/initiator_config/iqn_prefix" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      IQN prefix addresses.


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-iscsi_settings/initiator_ip_pool_settings"></div>

      .. _ansible_collections.dellemc.openmanage.ome_identity_pool_module__parameter-iscsi_settings/initiator_ip_pool_settings:

      .. rst-class:: ansible-option-title

      **initiator_ip_pool_settings**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-iscsi_settings/initiator_ip_pool_settings" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Applicable for creating and modifying an identity pool using ISCSI Initiator IP pool settings.


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-iscsi_settings/initiator_ip_pool_settings/gateway"></div>

      .. _ansible_collections.dellemc.openmanage.ome_identity_pool_module__parameter-iscsi_settings/initiator_ip_pool_settings/gateway:

      .. rst-class:: ansible-option-title

      **gateway**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-iscsi_settings/initiator_ip_pool_settings/gateway" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      IP address of gateway.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-iscsi_settings/initiator_ip_pool_settings/ip_range"></div>

      .. _ansible_collections.dellemc.openmanage.ome_identity_pool_module__parameter-iscsi_settings/initiator_ip_pool_settings/ip_range:

      .. rst-class:: ansible-option-title

      **ip_range**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-iscsi_settings/initiator_ip_pool_settings/ip_range" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Range of non-multicast IP addresses.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-iscsi_settings/initiator_ip_pool_settings/primary_dns_server"></div>

      .. _ansible_collections.dellemc.openmanage.ome_identity_pool_module__parameter-iscsi_settings/initiator_ip_pool_settings/primary_dns_server:

      .. rst-class:: ansible-option-title

      **primary_dns_server**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-iscsi_settings/initiator_ip_pool_settings/primary_dns_server" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      IP address of the primary DNS server.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-iscsi_settings/initiator_ip_pool_settings/secondary_dns_server"></div>

      .. _ansible_collections.dellemc.openmanage.ome_identity_pool_module__parameter-iscsi_settings/initiator_ip_pool_settings/secondary_dns_server:

      .. rst-class:: ansible-option-title

      **secondary_dns_server**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-iscsi_settings/initiator_ip_pool_settings/secondary_dns_server" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      IP address of the secondary DNS server.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-iscsi_settings/initiator_ip_pool_settings/subnet_mask"></div>

      .. _ansible_collections.dellemc.openmanage.ome_identity_pool_module__parameter-iscsi_settings/initiator_ip_pool_settings/subnet_mask:

      .. rst-class:: ansible-option-title

      **subnet_mask**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-iscsi_settings/initiator_ip_pool_settings/subnet_mask" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Subnet mask for \ :emphasis:`ip\_range`\ .


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-iscsi_settings/starting_mac_address"></div>

      .. _ansible_collections.dellemc.openmanage.ome_identity_pool_module__parameter-iscsi_settings/starting_mac_address:

      .. rst-class:: ansible-option-title

      **starting_mac_address**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-iscsi_settings/starting_mac_address" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Starting MAC address of the iSCSI setting.This is required option for iSCSI setting.


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-new_pool_name"></div>

      .. _ansible_collections.dellemc.openmanage.ome_identity_pool_module__parameter-new_pool_name:

      .. rst-class:: ansible-option-title

      **new_pool_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-new_pool_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      After creating an identity pool, \ :emphasis:`pool\_name`\  can be changed to \ :emphasis:`new\_pool\_name`\ .

      This option is ignored when creating an identity pool.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-password"></div>

      .. _ansible_collections.dellemc.openmanage.ome_identity_pool_module__parameter-password:

      .. rst-class:: ansible-option-title

      **password**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-password" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      OpenManage Enterprise or OpenManage Enterprise Modular password.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-pool_description"></div>

      .. _ansible_collections.dellemc.openmanage.ome_identity_pool_module__parameter-pool_description:

      .. rst-class:: ansible-option-title

      **pool_description**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-pool_description" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Description of the identity pool.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-pool_name"></div>

      .. _ansible_collections.dellemc.openmanage.ome_identity_pool_module__parameter-pool_name:

      .. rst-class:: ansible-option-title

      **pool_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-pool_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      This option is mandatory for \ :emphasis:`state`\  when creating, modifying and deleting an identity pool.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-port"></div>

      .. _ansible_collections.dellemc.openmanage.ome_identity_pool_module__parameter-port:

      .. rst-class:: ansible-option-title

      **port**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-port" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      OpenManage Enterprise or OpenManage Enterprise Modular HTTPS port.


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`443`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-state"></div>

      .. _ansible_collections.dellemc.openmanage.ome_identity_pool_module__parameter-state:

      .. rst-class:: ansible-option-title

      **state**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-state" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      \ :literal:`present`\  modifies an existing identity pool. If the provided I (pool\_name) does not exist, it creates an identity pool. - \ :literal:`absent`\  deletes an existing identity pool.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`"present"` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`"absent"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-timeout"></div>

      .. _ansible_collections.dellemc.openmanage.ome_identity_pool_module__parameter-timeout:

      .. rst-class:: ansible-option-title

      **timeout**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-timeout" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      :ansible-option-versionadded:`added in dellemc.openmanage 5.0.0`


      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The socket level timeout in seconds.


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`30`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-username"></div>

      .. _ansible_collections.dellemc.openmanage.ome_identity_pool_module__parameter-username:

      .. rst-class:: ansible-option-title

      **username**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-username" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      OpenManage Enterprise or OpenManage Enterprise Modular username.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-validate_certs"></div>

      .. _ansible_collections.dellemc.openmanage.ome_identity_pool_module__parameter-validate_certs:

      .. rst-class:: ansible-option-title

      **validate_certs**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-validate_certs" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      :ansible-option-versionadded:`added in dellemc.openmanage 5.0.0`


      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      If \ :literal:`false`\ , the SSL certificates will not be validated.

      Configure \ :literal:`false`\  only on personally controlled sites where self-signed certificates are used.

      Prior to collection version \ :literal:`5.0.0`\ , the \ :emphasis:`validate\_certs`\  is \ :literal:`false`\  by default.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry-default:`true` :ansible-option-choices-default-mark:`← (default)`


      .. raw:: html

        </div>


.. Attributes


.. Notes

Notes
-----

.. note::
   - Run this module from a system that has direct access to Dell OpenManage Enterprise.
   - This module supports \ :literal:`check\_mode`\ .

.. Seealso


.. Examples

Examples
--------

.. code-block:: yaml+jinja

    
    ---
    - name: Create an identity pool using ethernet, FCoE, iSCSI and FC settings
      dellemc.openmanage.ome_identity_pool:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        state: present
        pool_name: "pool1"
        pool_description: "Identity pool with Ethernet, FCoE, iSCSI and FC settings"
        ethernet_settings:
          starting_mac_address: "50:50:50:50:50:00"
          identity_count: 60
        fcoe_settings:
          starting_mac_address: "70:70:70:70:70:00"
          identity_count: 75
        iscsi_settings:
          starting_mac_address: "60:60:60:60:60:00"
          identity_count: 30
          initiator_config:
            iqn_prefix: "iqn.myprefix."
          initiator_ip_pool_settings:
            ip_range: "10.33.0.1-10.33.0.255"
            subnet_mask: "255.255.255.0"
            gateway: "192.168.4.1"
            primary_dns_server: "10.8.8.8"
            secondary_dns_server: "8.8.8.8"
        fc_settings:
          starting_address: "30:30:30:30:30:00"
          identity_count: 45

    - name: Create an identity pool using only ethernet settings
      dellemc.openmanage.ome_identity_pool:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        pool_name: "pool2"
        pool_description: "create identity pool with ethernet"
        ethernet_settings:
          starting_mac_address: "aa-bb-cc-dd-ee-aa"
          identity_count: 80

    - name: Modify an identity pool
      dellemc.openmanage.ome_identity_pool:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        pool_name: "pool2"
        new_pool_name: "pool3"
        pool_description: "modifying identity pool with ethernet and fcoe settings"
        ethernet_settings:
          starting_mac_address: "90-90-90-90-90-90"
          identity_count: 61
        fcoe_settings:
          starting_mac_address: "aabb.ccdd.5050"
          identity_count: 77

    - name: Modify an identity pool using iSCSI and FC settings
      dellemc.openmanage.ome_identity_pool:
        hostname: "{{hostname}}"
        username: "{{username}}"
        password: "{{password}}"
        ca_path: "/path/to/ca_cert.pem"
        pool_name: "pool_new"
        new_pool_name: "pool_new2"
        pool_description: "modifying identity pool with iscsi and fc settings"
        iscsi_settings:
          identity_count: 99
          initiator_config:
            iqn_prefix: "iqn1.myprefix2."
          initiator_ip_pool_settings:
            gateway: "192.168.4.5"
        fc_settings:
          starting_address: "10:10:10:10:10:10"
          identity_count: 98

    - name: Delete an identity pool
      dellemc.openmanage.ome_identity_pool:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        state: "absent"
        pool_name: "pool2"




.. Facts


.. Return values

Return Values
-------------
Common return values are documented :ref:`here <common_return_values>`, the following are the fields unique to this module:

.. rst-class:: ansible-option-table

.. list-table::
  :width: 100%
  :widths: auto
  :header-rows: 1

  * - Key
    - Description

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-error_info"></div>

      .. _ansible_collections.dellemc.openmanage.ome_identity_pool_module__return-error_info:

      .. rst-class:: ansible-option-title

      **error_info**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-error_info" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Details of the HTTP Error.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` on HTTP error

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"error": {"@Message.ExtendedInfo": [{"Message": "Unable to process the request because an error occurred: Ethernet-MAC Range overlap found (in this Identity Pool or in a different one) .", "MessageArgs": ["Ethernet-MAC Range overlap found (in this Identity Pool or in a different one)\\""], "MessageId": "CGEN6001", "RelatedProperties": [], "Resolution": "Retry the operation. If the issue persists, contact your system administrator.", "Severity": "Critical"}], "code": "Base.1.0.GeneralError", "message": "A general error has occurred. See ExtendedInfo for more information."}}`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-msg"></div>

      .. _ansible_collections.dellemc.openmanage.ome_identity_pool_module__return-msg:

      .. rst-class:: ansible-option-title

      **msg**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-msg" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Overall status of the identity pool operation.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` always

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`"Successfully created an identity pool."`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-pool_status"></div>

      .. _ansible_collections.dellemc.openmanage.ome_identity_pool_module__return-pool_status:

      .. rst-class:: ansible-option-title

      **pool_status**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-pool_status" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Details of the user operation, when \ :emphasis:`state`\  is \ :literal:`present`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` success

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"Id": 29, "IsSuccessful": true, "Issues": []}`


      .. raw:: html

        </div>



..  Status (Presently only deprecated)


.. Authors

Authors
~~~~~~~

- Sajna Shetty(@Sajna-Shetty)
- Deepak Joshi(@Dell-Deepak-Joshi))



.. Extra links

Collection links
~~~~~~~~~~~~~~~~

.. raw:: html

  <p class="ansible-links">
    <a href="https://github.com/dell/dellemc-openmanage-ansible-modules/issues" aria-role="button" target="_blank" rel="noopener external">Issue Tracker</a>
    <a href="https://github.com/dell/dellemc-openmanage-ansible-modules" aria-role="button" target="_blank" rel="noopener external">Homepage</a>
    <a href="https://github.com/dell/dellemc-openmanage-ansible-modules/tree/collections" aria-role="button" target="_blank" rel="noopener external">Repository (Sources)</a>
  </p>

.. Parsing errors

