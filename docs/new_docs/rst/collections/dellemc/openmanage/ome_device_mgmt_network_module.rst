
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

.. _ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module:

.. Anchors: short name for ansible.builtin

.. Anchors: aliases



.. Title

dellemc.openmanage.ome_device_mgmt_network module -- Configure network settings of devices on OpenManage Enterprise Modular
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. Collection note

.. note::
    This module is part of the `dellemc.openmanage collection <https://galaxy.ansible.com/dellemc/openmanage>`_ (version 8.5.0).

    To install it, use: :code:`ansible-galaxy collection install dellemc.openmanage`.
    You need further requirements to be able to use this module,
    see :ref:`Requirements <ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module_requirements>` for details.

    To use it in a playbook, specify: :code:`dellemc.openmanage.ome_device_mgmt_network`.

.. version_added

.. rst-class:: ansible-version-added

New in dellemc.openmanage 4.2.0

.. contents::
   :local:
   :depth: 1

.. Deprecated


Synopsis
--------

.. Description

- This module allows to configure network settings on Chassis, Servers, and I/O Modules on OpenManage Enterprise Modular.


.. Aliases


.. Requirements

.. _ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module_requirements:

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

      .. _ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module__parameter-ca_path:

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
        <div class="ansibleOptionAnchor" id="parameter-delay"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module__parameter-delay:

      .. rst-class:: ansible-option-title

      **delay**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-delay" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The time in seconds, after which settings are applied.

      This option is applicable only for Chassis.


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`0`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-device_id"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module__parameter-device_id:

      .. rst-class:: ansible-option-title

      **device_id**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-device_id" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      ID of the device.

      This option is mutually exclusive with \ :emphasis:`device\_service\_tag`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-device_service_tag"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module__parameter-device_service_tag:

      .. rst-class:: ansible-option-title

      **device_service_tag**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-device_service_tag" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Service tag of the device.

      This option is mutually exclusive with \ :emphasis:`device\_id`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-dns_configuration"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module__parameter-dns_configuration:

      .. rst-class:: ansible-option-title

      **dns_configuration**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-dns_configuration" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Domain Name System(DNS) settings.


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-dns_configuration/auto_negotiation"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module__parameter-dns_configuration/auto_negotiation:

      .. rst-class:: ansible-option-title

      **auto_negotiation**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-dns_configuration/auto_negotiation" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enables or disables the auto negation of the network speed.

      \ :literal:`NOTE`\ : Setting \ :emphasis:`auto\_negotiation`\  to false and choosing a network port speed may result in the chassis loosing link to the top of rack network switch, or to the neighboring chassis in case of MCM mode. It is recommended that the \ :emphasis:`auto\_negotiation`\  is set to \ :literal:`true`\  for most use cases.

      This is applicable when \ :emphasis:`use\_dhcp\_for\_dns\_domain\_name`\  is false.

      This is applicable only for Chassis.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-dns_configuration/dns_domain_name"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module__parameter-dns_configuration/dns_domain_name:

      .. rst-class:: ansible-option-title

      **dns_domain_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-dns_configuration/dns_domain_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Static DNS domain name

      This is applicable when \ :emphasis:`use\_dhcp\_for\_dns\_domain\_name`\  is false.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-dns_configuration/dns_name"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module__parameter-dns_configuration/dns_name:

      .. rst-class:: ansible-option-title

      **dns_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-dns_configuration/dns_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      DNS name for \ :emphasis:`hostname`\ 

      This is applicable when \ :emphasis:`register\_with\_dns`\  is true.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-dns_configuration/network_speed"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module__parameter-dns_configuration/network_speed:

      .. rst-class:: ansible-option-title

      **network_speed**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-dns_configuration/network_speed" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The speed of the network port.

      This is applicable when \ :emphasis:`auto\_negotiation`\  is false.

      \ :literal:`10\_MB`\  to select network speed of 10 MB.

      \ :literal:`100\_MB`\  to select network speed of 100 MB.

      This is applicable only for Chassis.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"10\_MB"`
      - :ansible-option-choices-entry:`"100\_MB"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-dns_configuration/register_with_dns"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module__parameter-dns_configuration/register_with_dns:

      .. rst-class:: ansible-option-title

      **register_with_dns**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-dns_configuration/register_with_dns" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Register/Unregister \ :emphasis:`dns\_name`\  on the DNS Server.

      \ :literal:`WARNING`\  This option cannot be updated if VLAN configuration changes.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-dns_configuration/use_dhcp_for_dns_domain_name"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module__parameter-dns_configuration/use_dhcp_for_dns_domain_name:

      .. rst-class:: ansible-option-title

      **use_dhcp_for_dns_domain_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-dns_configuration/use_dhcp_for_dns_domain_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Get the \ :emphasis:`dns\_domain\_name`\  using a DHCP server.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-dns_server_settings"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module__parameter-dns_server_settings:

      .. rst-class:: ansible-option-title

      **dns_server_settings**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-dns_server_settings" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      DNS server settings.

      This is applicable only for I/O Module.


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-dns_server_settings/alternate_dns_server1"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module__parameter-dns_server_settings/alternate_dns_server1:

      .. rst-class:: ansible-option-title

      **alternate_dns_server1**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-dns_server_settings/alternate_dns_server1" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enter the IP address of the first alternate DNS server.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-dns_server_settings/alternate_dns_server2"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module__parameter-dns_server_settings/alternate_dns_server2:

      .. rst-class:: ansible-option-title

      **alternate_dns_server2**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-dns_server_settings/alternate_dns_server2" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enter the IP address of the second alternate DNS server.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-dns_server_settings/preferred_dns_server"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module__parameter-dns_server_settings/preferred_dns_server:

      .. rst-class:: ansible-option-title

      **preferred_dns_server**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-dns_server_settings/preferred_dns_server" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enter the IP address of the preferred DNS server.


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-enable_nic"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module__parameter-enable_nic:

      .. rst-class:: ansible-option-title

      **enable_nic**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-enable_nic" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Enable or disable Network Interface Card (NIC) configuration of the device.

      This option is not applicable to I/O Module.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry-default:`true` :ansible-option-choices-default-mark:`← (default)`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-hostname"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module__parameter-hostname:

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

      OpenManage Enterprise Modular IP address or hostname.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-ipv4_configuration"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module__parameter-ipv4_configuration:

      .. rst-class:: ansible-option-title

      **ipv4_configuration**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-ipv4_configuration" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      IPv4 network configuration.

      \ :literal:`WARNING`\  Ensure that you have an alternate interface to access OpenManage Enterprise Modular because these options can change the current IPv4 address for \ :emphasis:`hostname`\ .


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-ipv4_configuration/enable_dhcp"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module__parameter-ipv4_configuration/enable_dhcp:

      .. rst-class:: ansible-option-title

      **enable_dhcp**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-ipv4_configuration/enable_dhcp" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enable or disable the automatic request to obtain an IPv4 address from the IPv4 Dynamic Host Configuration Protocol (DHCP) server.

      \ :literal:`NOTE`\  If this option is \ :literal:`true`\ , the values provided for \ :emphasis:`static\_ip\_address`\ , \ :emphasis:`static\_subnet\_mask`\ , and \ :emphasis:`static\_gateway`\  are not applied for these fields. However, the module may report changes.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-ipv4_configuration/enable_ipv4"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module__parameter-ipv4_configuration/enable_ipv4:

      .. rst-class:: ansible-option-title

      **enable_ipv4**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-ipv4_configuration/enable_ipv4" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enable or disable access to the network using IPv4.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-ipv4_configuration/static_alternate_dns_server"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module__parameter-ipv4_configuration/static_alternate_dns_server:

      .. rst-class:: ansible-option-title

      **static_alternate_dns_server**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-ipv4_configuration/static_alternate_dns_server" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Static IPv4 DNS alternate server

      This option is applicable when \ :emphasis:`use\_dhcp\_for\_dns\_server\_names`\  is false.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-ipv4_configuration/static_gateway"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module__parameter-ipv4_configuration/static_gateway:

      .. rst-class:: ansible-option-title

      **static_gateway**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-ipv4_configuration/static_gateway" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Static IPv4 gateway address

      This option is applicable when \ :emphasis:`enable\_dhcp`\  is false.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-ipv4_configuration/static_ip_address"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module__parameter-ipv4_configuration/static_ip_address:

      .. rst-class:: ansible-option-title

      **static_ip_address**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-ipv4_configuration/static_ip_address" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Static IPv4 address

      This option is applicable when \ :emphasis:`enable\_dhcp`\  is false.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-ipv4_configuration/static_preferred_dns_server"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module__parameter-ipv4_configuration/static_preferred_dns_server:

      .. rst-class:: ansible-option-title

      **static_preferred_dns_server**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-ipv4_configuration/static_preferred_dns_server" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Static IPv4 DNS preferred server

      This option is applicable when \ :emphasis:`use\_dhcp\_for\_dns\_server\_names`\  is false.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-ipv4_configuration/static_subnet_mask"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module__parameter-ipv4_configuration/static_subnet_mask:

      .. rst-class:: ansible-option-title

      **static_subnet_mask**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-ipv4_configuration/static_subnet_mask" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Static IPv4 subnet mask address

      This option is applicable when \ :emphasis:`enable\_dhcp`\  is false.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-ipv4_configuration/use_dhcp_to_obtain_dns_server_address"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module__parameter-ipv4_configuration/use_dhcp_to_obtain_dns_server_address:

      .. rst-class:: ansible-option-title

      **use_dhcp_to_obtain_dns_server_address**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-ipv4_configuration/use_dhcp_to_obtain_dns_server_address" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      This option allows to automatically request and obtain IPv4 address for the DNS Server from the DHCP server.

      This option is applicable when \ :emphasis:`enable\_dhcp`\  is true.

      \ :literal:`NOTE`\  If this option is \ :literal:`true`\ , the values provided for \ :emphasis:`static\_preferred\_dns\_server`\  and \ :emphasis:`static\_alternate\_dns\_server`\  are not applied for these fields. However, the module may report changes.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-ipv6_configuration"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module__parameter-ipv6_configuration:

      .. rst-class:: ansible-option-title

      **ipv6_configuration**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-ipv6_configuration" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      IPv6 network configuration.

      \ :literal:`WARNING`\  Ensure that you have an alternate interface to access OpenManage Enterprise Modular because these options can change the current IPv6 address for \ :emphasis:`hostname`\ .


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-ipv6_configuration/enable_auto_configuration"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module__parameter-ipv6_configuration/enable_auto_configuration:

      .. rst-class:: ansible-option-title

      **enable_auto_configuration**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-ipv6_configuration/enable_auto_configuration" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enable or disable the automatic request to obtain an IPv6 address from the IPv6 DHCP server or router advertisements(RA)

      If \ :emphasis:`enable\_auto\_configuration`\  is \ :literal:`true`\ , OpenManage Enterprise Modular retrieves IP configuration (IPv6 address, prefix, and gateway address) from a DHCPv6 server on the existing network.

      \ :literal:`NOTE`\  If this option is \ :literal:`true`\ , the values provided for \ :emphasis:`static\_ip\_address`\ , \ :emphasis:`static\_prefix\_length`\ , and \ :emphasis:`static\_gateway`\  are not applied for these fields. However, the module may report changes.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-ipv6_configuration/enable_ipv6"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module__parameter-ipv6_configuration/enable_ipv6:

      .. rst-class:: ansible-option-title

      **enable_ipv6**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-ipv6_configuration/enable_ipv6" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enable or disable access to the network using the IPv6.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-ipv6_configuration/static_alternate_dns_server"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module__parameter-ipv6_configuration/static_alternate_dns_server:

      .. rst-class:: ansible-option-title

      **static_alternate_dns_server**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-ipv6_configuration/static_alternate_dns_server" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Static IPv6 DNS alternate server

      This option is applicable when \ :emphasis:`use\_dhcp\_for\_dns\_server\_names`\  is false.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-ipv6_configuration/static_gateway"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module__parameter-ipv6_configuration/static_gateway:

      .. rst-class:: ansible-option-title

      **static_gateway**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-ipv6_configuration/static_gateway" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Static IPv6 gateway address

      This option is applicable when \ :emphasis:`enable\_auto\_configuration`\  is false.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-ipv6_configuration/static_ip_address"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module__parameter-ipv6_configuration/static_ip_address:

      .. rst-class:: ansible-option-title

      **static_ip_address**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-ipv6_configuration/static_ip_address" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Static IPv6 address

      This option is applicable when \ :emphasis:`enable\_auto\_configuration`\  is false.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-ipv6_configuration/static_preferred_dns_server"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module__parameter-ipv6_configuration/static_preferred_dns_server:

      .. rst-class:: ansible-option-title

      **static_preferred_dns_server**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-ipv6_configuration/static_preferred_dns_server" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Static IPv6 DNS preferred server

      This option is applicable when \ :emphasis:`use\_dhcp\_for\_dns\_server\_names`\  is false.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-ipv6_configuration/static_prefix_length"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module__parameter-ipv6_configuration/static_prefix_length:

      .. rst-class:: ansible-option-title

      **static_prefix_length**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-ipv6_configuration/static_prefix_length" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Static IPv6 prefix length

      This option is applicable when \ :emphasis:`enable\_auto\_configuration`\  is false.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-ipv6_configuration/use_dhcpv6_to_obtain_dns_server_address"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module__parameter-ipv6_configuration/use_dhcpv6_to_obtain_dns_server_address:

      .. rst-class:: ansible-option-title

      **use_dhcpv6_to_obtain_dns_server_address**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-ipv6_configuration/use_dhcpv6_to_obtain_dns_server_address" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      This option allows to automatically request and obtain a IPv6 address for the DNS server from the DHCP server.

      This option is applicable when \ :emphasis:`enable\_auto\_configuration`\  is true

      \ :literal:`NOTE`\  If this option is \ :literal:`true`\ , the values provided for \ :emphasis:`static\_preferred\_dns\_server`\  and \ :emphasis:`static\_alternate\_dns\_server`\  are not applied for these fields. However, the module may report changes.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-management_vlan"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module__parameter-management_vlan:

      .. rst-class:: ansible-option-title

      **management_vlan**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-management_vlan" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      VLAN configuration.


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-management_vlan/enable_vlan"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module__parameter-management_vlan/enable_vlan:

      .. rst-class:: ansible-option-title

      **enable_vlan**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-management_vlan/enable_vlan" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enable or disable VLAN for management.

      The VLAN configuration cannot be updated if the \ :emphasis:`register\_with\_dns`\  field under \ :emphasis:`dns\_configuration`\  is true.

      \ :literal:`WARNING`\  Ensure that the network cable is connected to the correct port after the VLAN configuration is changed. If not, the VLAN configuration changes may not be applied.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-management_vlan/vlan_id"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module__parameter-management_vlan/vlan_id:

      .. rst-class:: ansible-option-title

      **vlan_id**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-management_vlan/vlan_id" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      VLAN ID.

      The valid VLAN IDs are: 1 to 4000, and 4021 to 4094.

      This option is applicable when \ :emphasis:`enable\_vlan`\  is true.


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-password"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module__parameter-password:

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

      OpenManage Enterprise Modular password.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-port"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module__parameter-port:

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

      OpenManage Enterprise Modular HTTPS port.


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`443`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-timeout"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module__parameter-timeout:

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

      .. _ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module__parameter-username:

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

      OpenManage Enterprise Modular username.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-validate_certs"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module__parameter-validate_certs:

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
   - Run this module from a system that has direct access to Dell OpenManage Enterprise Modular.
   - This module supports \ :literal:`check\_mode`\ .

.. Seealso


.. Examples

Examples
--------

.. code-block:: yaml+jinja

    
    ---
    - name: Network settings for chassis
      dellemc.openmanage.ome_device_mgmt_network:
        hostname: 192.168.0.1
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        device_service_tag: CHAS123
        ipv4_configuration:
          enable_ipv4: true
          enable_dhcp: false
          static_ip_address: 192.168.0.2
          static_subnet_mask: 255.255.254.0
          static_gateway: 192.168.0.3
          use_dhcp_to_obtain_dns_server_address: false
          static_preferred_dns_server: 192.168.0.4
          static_alternate_dns_server: 192.168.0.5
        ipv6_configuration:
          enable_ipv6: true
          enable_auto_configuration: false
          static_ip_address: 2626:f2f2:f081:9:1c1c:f1f1:4747:1
          static_prefix_length: 10
          static_gateway: ffff::2607:f2b1:f081:9
          use_dhcpv6_to_obtain_dns_server_address: false
          static_preferred_dns_server: 2626:f2f2:f081:9:1c1c:f1f1:4747:3
          static_alternate_dns_server: 2626:f2f2:f081:9:1c1c:f1f1:4747:4
        dns_configuration:
          register_with_dns: true
          use_dhcp_for_dns_domain_name: false
          dns_name: "MX-SVCTAG"
          dns_domain_name: "dnslocaldomain"
          auto_negotiation: false
          network_speed: 100_MB

    - name: Network settings for server
      dellemc.openmanage.ome_device_mgmt_network:
        hostname: 192.168.0.1
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        device_service_tag: SRVR123
        ipv4_configuration:
          enable_ipv4: true
          enable_dhcp: false
          static_ip_address: 192.168.0.2
          static_subnet_mask: 255.255.254.0
          static_gateway: 192.168.0.3
          use_dhcp_to_obtain_dns_server_address: false
          static_preferred_dns_server: 192.168.0.4
          static_alternate_dns_server: 192.168.0.5
        ipv6_configuration:
          enable_ipv6: true
          enable_auto_configuration: false
          static_ip_address: 2626:f2f2:f081:9:1c1c:f1f1:4747:1
          static_prefix_length: 10
          static_gateway: ffff::2607:f2b1:f081:9
          use_dhcpv6_to_obtain_dns_server_address: false
          static_preferred_dns_server: 2626:f2f2:f081:9:1c1c:f1f1:4747:3
          static_alternate_dns_server: 2626:f2f2:f081:9:1c1c:f1f1:4747:4

    - name: Network settings for I/O module
      dellemc.openmanage.ome_device_mgmt_network:
        hostname: 192.168.0.1
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        device_service_tag: IOM1234
        ipv4_configuration:
          enable_ipv4: true
          enable_dhcp: false
          static_ip_address: 192.168.0.2
          static_subnet_mask: 255.255.254.0
          static_gateway: 192.168.0.3
        ipv6_configuration:
          enable_ipv6: true
          enable_auto_configuration: false
          static_ip_address: 2626:f2f2:f081:9:1c1c:f1f1:4747:1
          static_prefix_length: 10
          static_gateway: ffff::2607:f2b1:f081:9
        dns_server_settings:
          preferred_dns_server: 192.168.0.4
          alternate_dns_server1: 192.168.0.5

    - name: Management VLAN configuration of chassis using device id
      dellemc.openmanage.ome_device_mgmt_network:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        device_id: 12345
        management_vlan:
          enable_vlan: true
          vlan_id: 2345
        dns_configuration:
          register_with_dns: false




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

      .. _ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module__return-error_info:

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

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"error": {"@Message.ExtendedInfo": [{"Message": "Unable to complete the request because IPV4 Settings Capability is not Supported does not exist or is not applicable for the resource URI.", "MessageArgs": ["IPV4 Settings Capability is not Supported"], "MessageId": "CGEN1004", "RelatedProperties": [], "Resolution": "Check the request resource URI. Refer to the OpenManage Enterprise-Modular User's Guide for more information about resource URI and its properties.", "Severity": "Critical"}], "code": "Base.1.0.GeneralError", "message": "A general error has occurred. See ExtendedInfo for more information."}}`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-msg"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module__return-msg:

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

      Overall status of the network config operation.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` always

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`"Successfully applied the network settings."`


      .. raw:: html

        </div>



..  Status (Presently only deprecated)


.. Authors

Authors
~~~~~~~

- Jagadeesh N V(@jagadeeshnv)



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

