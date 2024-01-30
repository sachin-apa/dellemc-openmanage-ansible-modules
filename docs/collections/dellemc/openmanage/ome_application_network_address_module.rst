
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

.. _ansible_collections.dellemc.openmanage.ome_application_network_address_module:

.. Anchors: short name for ansible.builtin

.. Anchors: aliases



.. Title

dellemc.openmanage.ome_application_network_address module -- Updates the network configuration on OpenManage Enterprise
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. Collection note

.. note::
    This module is part of the `dellemc.openmanage collection <https://galaxy.ansible.com/dellemc/openmanage>`_ (version 8.5.0).

    To install it, use: :code:`ansible-galaxy collection install dellemc.openmanage`.
    You need further requirements to be able to use this module,
    see :ref:`Requirements <ansible_collections.dellemc.openmanage.ome_application_network_address_module_requirements>` for details.

    To use it in a playbook, specify: :code:`dellemc.openmanage.ome_application_network_address`.

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

- This module allows the configuration of a DNS and an IPV4 or IPV6 network on OpenManage Enterprise.


.. Aliases


.. Requirements

.. _ansible_collections.dellemc.openmanage.ome_application_network_address_module_requirements:

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

      .. _ansible_collections.dellemc.openmanage.ome_application_network_address_module__parameter-ca_path:

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
        <div class="ansibleOptionAnchor" id="parameter-dns_configuration"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_network_address_module__parameter-dns_configuration:

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
        <div class="ansibleOptionAnchor" id="parameter-dns_configuration/dns_domain_name"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_network_address_module__parameter-dns_configuration/dns_domain_name:

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

      .. _ansible_collections.dellemc.openmanage.ome_application_network_address_module__parameter-dns_configuration/dns_name:

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
        <div class="ansibleOptionAnchor" id="parameter-dns_configuration/register_with_dns"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_network_address_module__parameter-dns_configuration/register_with_dns:

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

      This option cannot be updated if vLAN configuration changes.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-dns_configuration/use_dhcp_for_dns_domain_name"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_network_address_module__parameter-dns_configuration/use_dhcp_for_dns_domain_name:

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
        <div class="ansibleOptionAnchor" id="parameter-enable_nic"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_network_address_module__parameter-enable_nic:

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

      Enable or disable Network Interface Card (NIC) configuration.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry-default:`true` :ansible-option-choices-default-mark:`← (default)`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-hostname"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_network_address_module__parameter-hostname:

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
        <div class="ansibleOptionAnchor" id="parameter-interface_name"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_network_address_module__parameter-interface_name:

      .. rst-class:: ansible-option-title

      **interface_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-interface_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      If there are multiple interfaces, network configuration changes can be applied to a single interface using the interface name of the NIC.

      If this option is not specified, Primary interface is chosen by default.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-ipv4_configuration"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_network_address_module__parameter-ipv4_configuration:

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

      \ :emphasis:`Warning`\  Ensure that you have an alternate interface to access OpenManage Enterprise as these options can change the current IPv4 address for \ :emphasis:`hostname`\ .


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-ipv4_configuration/enable"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_network_address_module__parameter-ipv4_configuration/enable:

      .. rst-class:: ansible-option-title

      **enable**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-ipv4_configuration/enable" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-ipv4_configuration/enable_dhcp"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_network_address_module__parameter-ipv4_configuration/enable_dhcp:

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

      Enable or disable the automatic request to get an IPv4 address from the IPv4 Dynamic Host Configuration Protocol (DHCP) server

      If \ :emphasis:`enable\_dhcp`\  option is true, OpenManage Enterprise retrieves the IP configuration—IPv4 address, subnet mask, and gateway from a DHCP server on the existing network.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-ipv4_configuration/static_alternate_dns_server"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_network_address_module__parameter-ipv4_configuration/static_alternate_dns_server:

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

      .. _ansible_collections.dellemc.openmanage.ome_application_network_address_module__parameter-ipv4_configuration/static_gateway:

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

      .. _ansible_collections.dellemc.openmanage.ome_application_network_address_module__parameter-ipv4_configuration/static_ip_address:

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

      .. _ansible_collections.dellemc.openmanage.ome_application_network_address_module__parameter-ipv4_configuration/static_preferred_dns_server:

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

      .. _ansible_collections.dellemc.openmanage.ome_application_network_address_module__parameter-ipv4_configuration/static_subnet_mask:

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
        <div class="ansibleOptionAnchor" id="parameter-ipv4_configuration/use_dhcp_for_dns_server_names"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_network_address_module__parameter-ipv4_configuration/use_dhcp_for_dns_server_names:

      .. rst-class:: ansible-option-title

      **use_dhcp_for_dns_server_names**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-ipv4_configuration/use_dhcp_for_dns_server_names" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      This option allows to automatically request and obtain a DNS server IPv4 address from the DHCP server.

      This option is applicable when \ :emphasis:`enable\_dhcp`\  is true.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-ipv6_configuration"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_network_address_module__parameter-ipv6_configuration:

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

      \ :emphasis:`Warning`\  Ensure that you have an alternate interface to access OpenManage Enterprise as these options can change the current IPv6 address for \ :emphasis:`hostname`\ .


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-ipv6_configuration/enable"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_network_address_module__parameter-ipv6_configuration/enable:

      .. rst-class:: ansible-option-title

      **enable**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-ipv6_configuration/enable" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-ipv6_configuration/enable_auto_configuration"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_network_address_module__parameter-ipv6_configuration/enable_auto_configuration:

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

      Enable or disable the automatic request to get an IPv6 address from the IPv6 DHCP server or router advertisements(RA)

      If \ :emphasis:`enable\_auto\_configuration`\  is true, OME retrieves IP configuration-IPv6 address, prefix, and gateway, from a DHCPv6 server on the existing network


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-ipv6_configuration/static_alternate_dns_server"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_network_address_module__parameter-ipv6_configuration/static_alternate_dns_server:

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

      .. _ansible_collections.dellemc.openmanage.ome_application_network_address_module__parameter-ipv6_configuration/static_gateway:

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

      .. _ansible_collections.dellemc.openmanage.ome_application_network_address_module__parameter-ipv6_configuration/static_ip_address:

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

      .. _ansible_collections.dellemc.openmanage.ome_application_network_address_module__parameter-ipv6_configuration/static_preferred_dns_server:

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

      .. _ansible_collections.dellemc.openmanage.ome_application_network_address_module__parameter-ipv6_configuration/static_prefix_length:

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
        <div class="ansibleOptionAnchor" id="parameter-ipv6_configuration/use_dhcp_for_dns_server_names"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_network_address_module__parameter-ipv6_configuration/use_dhcp_for_dns_server_names:

      .. rst-class:: ansible-option-title

      **use_dhcp_for_dns_server_names**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-ipv6_configuration/use_dhcp_for_dns_server_names" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      This option allows to automatically request and obtain a DNS server IPv6 address from the DHCP server.

      This option is applicable when \ :emphasis:`enable\_auto\_configuration`\  is true


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-management_vlan"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_network_address_module__parameter-management_vlan:

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

      vLAN configuration.

      These settings are applicable for OpenManage Enterprise Modular.


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-management_vlan/enable_vlan"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_network_address_module__parameter-management_vlan/enable_vlan:

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

      Enable or disable vLAN for management.

      The vLAN configuration cannot be updated if the \ :emphasis:`register\_with\_dns`\  field under \ :emphasis:`dns\_configuration`\  is true.

      \ :emphasis:`WARNING`\  Ensure that the network cable is plugged to the correct port after the vLAN configuration changes have been made. If not, the configuration change may not be effective.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-management_vlan/vlan_id"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_network_address_module__parameter-management_vlan/vlan_id:

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

      vLAN ID.

      This option is applicable when \ :emphasis:`enable\_vlan`\  is true.


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-password"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_network_address_module__parameter-password:

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
        <div class="ansibleOptionAnchor" id="parameter-port"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_network_address_module__parameter-port:

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
        <div class="ansibleOptionAnchor" id="parameter-reboot_delay"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_network_address_module__parameter-reboot_delay:

      .. rst-class:: ansible-option-title

      **reboot_delay**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-reboot_delay" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The time in seconds, after which settings are applied.

      This option is not mandatory.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-timeout"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_network_address_module__parameter-timeout:

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

      .. _ansible_collections.dellemc.openmanage.ome_application_network_address_module__parameter-username:

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

      .. _ansible_collections.dellemc.openmanage.ome_application_network_address_module__parameter-validate_certs:

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
   - The configuration changes can only be applied to one interface at a time.
   - The system management consoles might be unreachable for some time after the configuration changes are applied.
   - This module supports \ :literal:`check\_mode`\ .

.. Seealso


.. Examples

Examples
--------

.. code-block:: yaml+jinja

    
    ---
    - name: IPv4 network configuration for primary interface
      dellemc.openmanage.ome_application_network_address:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        enable_nic: true
        ipv4_configuration:
          enable: true
          enable_dhcp: false
          static_ip_address: 192.168.0.2
          static_subnet_mask: 255.255.254.0
          static_gateway: 192.168.0.3
          use_dhcp_for_dns_server_names: false
          static_preferred_dns_server: 192.168.0.4
          static_alternate_dns_server: 192.168.0.5
        reboot_delay: 5

    - name: IPv6 network configuration for primary interface
      dellemc.openmanage.ome_application_network_address:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        ipv6_configuration:
          enable: true
          enable_auto_configuration: true
          static_ip_address: 2626:f2f2:f081:9:1c1c:f1f1:4747:1
          static_prefix_length: 10
          static_gateway: 2626:f2f2:f081:9:1c1c:f1f1:4747:2
          use_dhcp_for_dns_server_names: true
          static_preferred_dns_server: 2626:f2f2:f081:9:1c1c:f1f1:4747:3
          static_alternate_dns_server: 2626:f2f2:f081:9:1c1c:f1f1:4747:4

    - name: Management vLAN configuration for primary interface
      dellemc.openmanage.ome_application_network_address:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        management_vlan:
          enable_vlan: true
          vlan_id: 3344
        dns_configuration:
          register_with_dns: false
        reboot_delay: 1

    - name: DNS settings
      dellemc.openmanage.ome_application_network_address:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        ipv4_configuration:
          enable: true
          use_dhcp_for_dns_server_names: false
          static_preferred_dns_server: 192.168.0.4
          static_alternate_dns_server: 192.168.0.5
        dns_configuration:
          register_with_dns: true
          use_dhcp_for_dns_domain_name: false
          dns_name: "MX-SVCTAG"
          dns_domain_name: "dnslocaldomain"

    - name: Disbale nic interface eth1
      dellemc.openmanage.ome_application_network_address:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        enable_nic: false
        interface_name: eth1

    - name: Complete network settings for interface eth1
      dellemc.openmanage.ome_application_network_address:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        enable_nic: true
        interface_name: eth1
        ipv4_configuration:
          enable: true
          enable_dhcp: false
          static_ip_address: 192.168.0.2
          static_subnet_mask: 255.255.254.0
          static_gateway: 192.168.0.3
          use_dhcp_for_dns_server_names: false
          static_preferred_dns_server: 192.168.0.4
          static_alternate_dns_server: 192.168.0.5
        ipv6_configuration:
          enable: true
          enable_auto_configuration: true
          static_ip_address: 2626:f2f2:f081:9:1c1c:f1f1:4747:1
          static_prefix_length: 10
          static_gateway: ffff::2607:f2b1:f081:9
          use_dhcp_for_dns_server_names: true
          static_preferred_dns_server: 2626:f2f2:f081:9:1c1c:f1f1:4747:3
          static_alternate_dns_server: 2626:f2f2:f081:9:1c1c:f1f1:4747:4
        dns_configuration:
          register_with_dns: true
          use_dhcp_for_dns_domain_name: false
          dns_name: "MX-SVCTAG"
          dns_domain_name: "dnslocaldomain"
        reboot_delay: 5




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

      .. _ansible_collections.dellemc.openmanage.ome_application_network_address_module__return-error_info:

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

      Details of the HTTP error.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` on HTTP error

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"error": {"@Message.ExtendedInfo": [{"Message": "Unable to update the address configuration because a dependent field is missing for  Use DHCP for DNS Domain Name, Enable DHCP for ipv4 or Enable Autoconfig for ipv6 settings for valid configuration .", "MessageArgs": ["Use DHCP for DNS Domain Name, Enable DHCP for ipv4 or Enable Autoconfig for ipv6 settings for valid configuration"], "MessageId": "CAPP1304", "RelatedProperties": [], "Resolution": "Make sure that all dependent fields contain valid content and retry the operation.", "Severity": "Critical"}], "code": "Base.1.0.GeneralError", "message": "A general error has occurred. See ExtendedInfo for more information."}}`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-job_info"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_network_address_module__return-job_info:

      .. rst-class:: ansible-option-title

      **job_info**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-job_info" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Details of the job to update in case OME version is \>= 3.3.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` on success

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"Builtin": false, "CreatedBy": "system", "Editable": true, "EndTime": null, "Id": 14902, "JobDescription": "Generic OME runtime task", "JobName": "OMERealtime\_Task", "JobStatus": {"Id": 2080, "Name": "New"}, "JobType": {"Id": 207, "Internal": true, "Name": "OMERealtime\_Task"}, "LastRun": null, "LastRunStatus": {"Id": 2080, "Name": "New"}, "NextRun": null, "Params": [{"JobId": 14902, "Key": "Nmcli\_Update", "Value": "{\\"interfaceName\\":\\"eth0\\",\\"profileName\\":\\"eth0\\",\\"enableNIC\\":true, \\"ipv4Configuration\\":{\\"enable\\":true,\\"enableDHCP\\":true,\\"staticIPAddress\\":\\"\\", \\"staticSubnetMask\\":\\"\\",\\"staticGateway\\":\\"\\",\\"useDHCPForDNSServerNames\\":true, \\"staticPreferredDNSServer\\":\\"\\",\\"staticAlternateDNSServer\\":\\"\\"}, \\"ipv6Configuration\\":{\\"enable\\":false,\\"enableAutoConfiguration\\":true,\\"staticIPAddress\\":\\"\\", \\"staticPrefixLength\\":0,\\"staticGateway\\":\\"\\",\\"useDHCPForDNSServerNames\\":false, \\"staticPreferredDNSServer\\":\\"\\",\\"staticAlternateDNSServer\\":\\"\\"}, \\"managementVLAN\\":{\\"enableVLAN\\":false,\\"id\\":0},\\"dnsConfiguration\\":{\\"registerWithDNS\\":false, \\"dnsName\\":\\"\\",\\"useDHCPForDNSDomainName\\":false,\\"dnsDomainName\\":\\"\\",\\"fqdndomainName\\":\\"\\", \\"ipv4CurrentPreferredDNSServer\\":\\"\\",\\"ipv4CurrentAlternateDNSServer\\":\\"\\", \\"ipv6CurrentPreferredDNSServer\\":\\"\\",\\"ipv6CurrentAlternateDNSServer\\":\\"\\"}, \\"currentSettings\\":{\\"ipv4Address\\":[],\\"ipv4Gateway\\":\\"\\",\\"ipv4Dns\\":[],\\"ipv4Domain\\":\\"\\", \\"ipv6Address\\":[],\\"ipv6LinkLocalAddress\\":\\"\\",\\"ipv6Gateway\\":\\"\\",\\"ipv6Dns\\":[], \\"ipv6Domain\\":\\"\\"},\\"delay\\":0,\\"primaryInterface\\":true,\\"modifiedConfigs\\":{}}"}], "Schedule": "startnow", "StartTime": null, "State": "Enabled", "Targets": [], "UpdatedBy": null, "Visible": true}`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-msg"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_network_address_module__return-msg:

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

      Overall status of the network address configuration change.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` always

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`"Successfully updated network address configuration"`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-network_configuration"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_network_address_module__return-network_configuration:

      .. rst-class:: ansible-option-title

      **network_configuration**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-network_configuration" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Updated application network address configuration.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` on success

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"Delay": 0, "DnsConfiguration": {"DnsDomainName": "", "DnsName": "MX-SVCTAG", "RegisterWithDNS": false, "UseDHCPForDNSDomainName": true}, "EnableNIC": true, "InterfaceName": "eth0", "Ipv4Configuration": {"Enable": true, "EnableDHCP": false, "StaticAlternateDNSServer": "", "StaticGateway": "192.168.0.2", "StaticIPAddress": "192.168.0.3", "StaticPreferredDNSServer": "192.168.0.4", "StaticSubnetMask": "255.255.254.0", "UseDHCPForDNSServerNames": false}, "Ipv6Configuration": {"Enable": true, "EnableAutoConfiguration": true, "StaticAlternateDNSServer": "", "StaticGateway": "", "StaticIPAddress": "", "StaticPreferredDNSServer": "", "StaticPrefixLength": 0, "UseDHCPForDNSServerNames": true}, "ManagementVLAN": {"EnableVLAN": false, "Id": 1}, "PrimaryInterface": true}`


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

