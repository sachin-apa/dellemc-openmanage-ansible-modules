
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

.. _ansible_collections.dellemc.openmanage.ome_discovery_module:

.. Anchors: short name for ansible.builtin

.. Anchors: aliases



.. Title

dellemc.openmanage.ome_discovery module -- Create, modify, or delete a discovery job on OpenManage Enterprise
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. Collection note

.. note::
    This module is part of the `dellemc.openmanage collection <https://galaxy.ansible.com/dellemc/openmanage>`_ (version 8.5.0).

    To install it, use: :code:`ansible-galaxy collection install dellemc.openmanage`.
    You need further requirements to be able to use this module,
    see :ref:`Requirements <ansible_collections.dellemc.openmanage.ome_discovery_module_requirements>` for details.

    To use it in a playbook, specify: :code:`dellemc.openmanage.ome_discovery`.

.. version_added

.. rst-class:: ansible-version-added

New in dellemc.openmanage 3.3.0

.. contents::
   :local:
   :depth: 1

.. Deprecated


Synopsis
--------

.. Description

- This module allows to create, modify, or delete a discovery job.


.. Aliases


.. Requirements

.. _ansible_collections.dellemc.openmanage.ome_discovery_module_requirements:

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

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-ca_path:

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
        <div class="ansibleOptionAnchor" id="parameter-community_string"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-community_string:

      .. rst-class:: ansible-option-title

      **community_string**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-community_string" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Enable the use of SNMP community strings to receive SNMP traps using Application Settings in OpenManage Enterprise. This option is available only for the discovered iDRAC servers and MX7000 chassis.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`false` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-cron"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-cron:

      .. rst-class:: ansible-option-title

      **cron**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-cron" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Provide a cron expression based on Quartz cron format.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets:

      .. rst-class:: ansible-option-title

      **discovery_config_targets**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Provide the list of discovery targets.

      Each discovery target is a set of \ :emphasis:`network\_address\_detail`\ , \ :emphasis:`device\_types`\ , and one or more protocol credentials.

      This is mandatory when \ :emphasis:`state`\  is \ :literal:`present`\ .

      \ :literal:`WARNING`\  Modification of this field is not supported, this field is overwritten every time. Ensure to provide all the required details for this field.


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/device_types"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/device_types:

      .. rst-class:: ansible-option-title

      **device_types**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/device_types" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Provide the type of devices to be discovered.

      The accepted types are SERVER, CHASSIS, NETWORK SWITCH, and STORAGE.

      A combination or all of the above can be provided.

      Supported protocols for each device type are:

      SERVER - \ :emphasis:`wsman`\ , \ :emphasis:`redfish`\ , \ :emphasis:`snmp`\ , \ :emphasis:`ipmi`\ , \ :emphasis:`ssh`\ , and \ :emphasis:`vmware`\ .

      CHASSIS - \ :emphasis:`wsman`\ , and \ :emphasis:`redfish`\ .

      NETWORK SWITCH - \ :emphasis:`snmp`\ .

      STORAGE - \ :emphasis:`storage`\ , and \ :emphasis:`snmp`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/ipmi"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/ipmi:

      .. rst-class:: ansible-option-title

      **ipmi**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/ipmi" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Intelligent Platform Management Interface (IPMI)


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/ipmi/kgkey"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/ipmi/kgkey:

      .. rst-class:: ansible-option-title

      **kgkey**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/ipmi/kgkey" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      KgKey for the IPMI protocol.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/ipmi/password"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/ipmi/password:

      .. rst-class:: ansible-option-title

      **password**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/ipmi/password" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Provide a password for the protocol.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/ipmi/retries"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/ipmi/retries:

      .. rst-class:: ansible-option-title

      **retries**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/ipmi/retries" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enter the number of repeated attempts required to discover a device.


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`3`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/ipmi/timeout"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/ipmi/timeout:

      .. rst-class:: ansible-option-title

      **timeout**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/ipmi/timeout" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enter the time in seconds after which a job must stop running.


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`60`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/ipmi/username"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/ipmi/username:

      .. rst-class:: ansible-option-title

      **username**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/ipmi/username" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Provide a username for the protocol.


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/network_address_detail"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/network_address_detail:

      .. rst-class:: ansible-option-title

      **network_address_detail**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/network_address_detail" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Provide the list of IP addresses, host names, or the range of IP addresses of the devices to be discovered or included.

      Sample Valid IP Range Formats

         192.35.0.0

         192.36.0.0-10.36.0.255

         192.37.0.0/24

         2345:f2b1:f083:135::5500/118

         2345:f2b1:f083:135::a500-2607:f2b1:f083:135::a600

         hostname.domain.tld

         hostname

         2345:f2b1:f083:139::22a

      Sample Invalid IP Range Formats

         192.35.0.\*

         192.36.0.0-255

         192.35.0.0/255.255.255.0

      \ :literal:`NOTE`\  The range size for the number of IP addresses is limited to 16,385 (0x4001).

      \ :literal:`NOTE`\  Both IPv6 and IPv6 CIDR formats are supported.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/redfish"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/redfish:

      .. rst-class:: ansible-option-title

      **redfish**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/redfish" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      REDFISH protocol.


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/redfish/ca_check"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/redfish/ca_check:

      .. rst-class:: ansible-option-title

      **ca_check**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/redfish/ca_check" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enable the Certificate Authority (CA) check.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`false` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/redfish/certificate_data"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/redfish/certificate_data:

      .. rst-class:: ansible-option-title

      **certificate_data**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/redfish/certificate_data" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Provide certificate data for the CA check.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/redfish/cn_check"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/redfish/cn_check:

      .. rst-class:: ansible-option-title

      **cn_check**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/redfish/cn_check" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enable the Common Name (CN) check.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`false` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/redfish/domain"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/redfish/domain:

      .. rst-class:: ansible-option-title

      **domain**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/redfish/domain" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Provide a domain for the protocol.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/redfish/password"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/redfish/password:

      .. rst-class:: ansible-option-title

      **password**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/redfish/password" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Provide a password for the protocol.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/redfish/port"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/redfish/port:

      .. rst-class:: ansible-option-title

      **port**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/redfish/port" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enter the port number that the job must use to discover the devices.


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`443`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/redfish/retries"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/redfish/retries:

      .. rst-class:: ansible-option-title

      **retries**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/redfish/retries" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enter the number of repeated attempts required to discover a device.


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`3`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/redfish/timeout"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/redfish/timeout:

      .. rst-class:: ansible-option-title

      **timeout**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/redfish/timeout" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enter the time in seconds after which a job must stop running.


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`60`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/redfish/username"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/redfish/username:

      .. rst-class:: ansible-option-title

      **username**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/redfish/username" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Provide a username for the protocol.


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/snmp"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/snmp:

      .. rst-class:: ansible-option-title

      **snmp**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/snmp" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Simple Network Management Protocol (SNMP).


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/snmp/community"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/snmp/community:

      .. rst-class:: ansible-option-title

      **community**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/snmp/community" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Community string for the SNMP protocol.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/snmp/port"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/snmp/port:

      .. rst-class:: ansible-option-title

      **port**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/snmp/port" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enter the port number that the job must use to discover the devices.


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`161`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/snmp/retries"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/snmp/retries:

      .. rst-class:: ansible-option-title

      **retries**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/snmp/retries" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enter the number of repeated attempts required to discover a device.


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`3`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/snmp/timeout"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/snmp/timeout:

      .. rst-class:: ansible-option-title

      **timeout**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/snmp/timeout" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enter the time in seconds after which a job must stop running.


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`3`

      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/ssh"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/ssh:

      .. rst-class:: ansible-option-title

      **ssh**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/ssh" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Secure Shell (SSH).


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/ssh/check_known_hosts"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/ssh/check_known_hosts:

      .. rst-class:: ansible-option-title

      **check_known_hosts**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/ssh/check_known_hosts" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Verify the known host key.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`false` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/ssh/is_sudo_user"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/ssh/is_sudo_user:

      .. rst-class:: ansible-option-title

      **is_sudo_user**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/ssh/is_sudo_user" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Use the SUDO option.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`false` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/ssh/password"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/ssh/password:

      .. rst-class:: ansible-option-title

      **password**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/ssh/password" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Provide a password for the protocol.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/ssh/port"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/ssh/port:

      .. rst-class:: ansible-option-title

      **port**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/ssh/port" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enter the port number that the job must use to discover the devices.


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`22`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/ssh/retries"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/ssh/retries:

      .. rst-class:: ansible-option-title

      **retries**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/ssh/retries" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enter the number of repeated attempts required to discover a device.


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`3`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/ssh/timeout"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/ssh/timeout:

      .. rst-class:: ansible-option-title

      **timeout**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/ssh/timeout" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enter the time in seconds after which a job must stop running.


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`60`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/ssh/username"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/ssh/username:

      .. rst-class:: ansible-option-title

      **username**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/ssh/username" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Provide a username for the protocol.


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/storage"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/storage:

      .. rst-class:: ansible-option-title

      **storage**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/storage" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      HTTPS Storage protocol.


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/storage/ca_check"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/storage/ca_check:

      .. rst-class:: ansible-option-title

      **ca_check**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/storage/ca_check" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enable the Certificate Authority (CA) check.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`false` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/storage/certificate_data"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/storage/certificate_data:

      .. rst-class:: ansible-option-title

      **certificate_data**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/storage/certificate_data" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Provide certificate data for the CA check.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/storage/cn_check"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/storage/cn_check:

      .. rst-class:: ansible-option-title

      **cn_check**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/storage/cn_check" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enable the Common Name (CN) check.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`false` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/storage/domain"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/storage/domain:

      .. rst-class:: ansible-option-title

      **domain**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/storage/domain" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Provide a domain for the protocol.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/storage/password"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/storage/password:

      .. rst-class:: ansible-option-title

      **password**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/storage/password" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Provide a password for the protocol.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/storage/port"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/storage/port:

      .. rst-class:: ansible-option-title

      **port**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/storage/port" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enter the port number that the job must use to discover the devices.


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`443`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/storage/retries"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/storage/retries:

      .. rst-class:: ansible-option-title

      **retries**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/storage/retries" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enter the number of repeated attempts required to discover a device.


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`3`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/storage/timeout"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/storage/timeout:

      .. rst-class:: ansible-option-title

      **timeout**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/storage/timeout" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enter the time in seconds after which a job must stop running.


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`60`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/storage/username"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/storage/username:

      .. rst-class:: ansible-option-title

      **username**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/storage/username" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Provide a username for the protocol.


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/vmware"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/vmware:

      .. rst-class:: ansible-option-title

      **vmware**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/vmware" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      VMWARE protocol.


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/vmware/ca_check"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/vmware/ca_check:

      .. rst-class:: ansible-option-title

      **ca_check**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/vmware/ca_check" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enable the Certificate Authority (CA) check.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`false` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/vmware/certificate_data"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/vmware/certificate_data:

      .. rst-class:: ansible-option-title

      **certificate_data**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/vmware/certificate_data" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Provide certificate data for the CA check.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/vmware/cn_check"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/vmware/cn_check:

      .. rst-class:: ansible-option-title

      **cn_check**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/vmware/cn_check" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enable the Common Name (CN) check.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`false` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/vmware/domain"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/vmware/domain:

      .. rst-class:: ansible-option-title

      **domain**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/vmware/domain" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Provide a domain for the protocol.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/vmware/password"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/vmware/password:

      .. rst-class:: ansible-option-title

      **password**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/vmware/password" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Provide a password for the protocol.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/vmware/port"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/vmware/port:

      .. rst-class:: ansible-option-title

      **port**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/vmware/port" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enter the port number that the job must use to discover the devices.


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`443`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/vmware/retries"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/vmware/retries:

      .. rst-class:: ansible-option-title

      **retries**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/vmware/retries" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enter the number of repeated attempts required to discover a device.


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`3`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/vmware/timeout"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/vmware/timeout:

      .. rst-class:: ansible-option-title

      **timeout**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/vmware/timeout" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enter the time in seconds after which a job must stop running.


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`60`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/vmware/username"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/vmware/username:

      .. rst-class:: ansible-option-title

      **username**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/vmware/username" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Provide a username for the protocol.


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/wsman"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/wsman:

      .. rst-class:: ansible-option-title

      **wsman**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/wsman" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Web Services-Management (WS-Man).


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/wsman/ca_check"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/wsman/ca_check:

      .. rst-class:: ansible-option-title

      **ca_check**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/wsman/ca_check" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enable the Certificate Authority (CA) check.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`false` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/wsman/certificate_data"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/wsman/certificate_data:

      .. rst-class:: ansible-option-title

      **certificate_data**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/wsman/certificate_data" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Provide certificate data for the CA check.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/wsman/cn_check"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/wsman/cn_check:

      .. rst-class:: ansible-option-title

      **cn_check**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/wsman/cn_check" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enable the Common Name (CN) check.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`false` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/wsman/domain"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/wsman/domain:

      .. rst-class:: ansible-option-title

      **domain**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/wsman/domain" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Provide a domain for the protocol.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/wsman/password"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/wsman/password:

      .. rst-class:: ansible-option-title

      **password**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/wsman/password" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Provide a password for the protocol.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/wsman/port"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/wsman/port:

      .. rst-class:: ansible-option-title

      **port**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/wsman/port" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enter the port number that the job must use to discover the devices.


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`443`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/wsman/retries"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/wsman/retries:

      .. rst-class:: ansible-option-title

      **retries**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/wsman/retries" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enter the number of repeated attempts required to discover a device.


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`3`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/wsman/timeout"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/wsman/timeout:

      .. rst-class:: ansible-option-title

      **timeout**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/wsman/timeout" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enter the time in seconds after which a job must stop running.


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`60`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_config_targets/wsman/username"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_config_targets/wsman/username:

      .. rst-class:: ansible-option-title

      **username**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_config_targets/wsman/username" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Provide a username for the protocol.


      .. raw:: html

        </div>



  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_id"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_id:

      .. rst-class:: ansible-option-title

      **discovery_id**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_id" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      ID of the discovery configuration group.

      This value is DiscoveryConfigGroupId in the return values under discovery\_status.

      It is mutually exclusive with \ :emphasis:`discovery\_job\_name`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_job_name"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-discovery_job_name:

      .. rst-class:: ansible-option-title

      **discovery_job_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_job_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Name of the discovery configuration job.

      It is mutually exclusive with \ :emphasis:`discovery\_id`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-email_recipient"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-email_recipient:

      .. rst-class:: ansible-option-title

      **email_recipient**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-email_recipient" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Enter the email address to which notifications are to be sent about the discovery job status. Configure the SMTP settings to allow sending notifications to an email address.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-hostname"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-hostname:

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

      OpenManage Enterprise IP address or hostname.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-ignore_partial_failure"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-ignore_partial_failure:

      .. rst-class:: ansible-option-title

      **ignore_partial_failure**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-ignore_partial_failure" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Provides the option to ignore partial failures. Partial failures occur when there is a combination of both discovered and undiscovered IPs.

      If \ :literal:`false`\ , then the partial failure is not ignored, and the module will error out.

      If \ :literal:`true`\ , then the partial failure is ignored.

      This option is only applicable if \ :emphasis:`job\_wait`\  is \ :literal:`true`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`false` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-job_wait"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-job_wait:

      .. rst-class:: ansible-option-title

      **job_wait**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-job_wait" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Provides the option to wait for job completion.

      This option is applicable when \ :emphasis:`state`\  is \ :literal:`present`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry-default:`true` :ansible-option-choices-default-mark:`← (default)`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-job_wait_timeout"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-job_wait_timeout:

      .. rst-class:: ansible-option-title

      **job_wait_timeout**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-job_wait_timeout" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The maximum wait time of \ :emphasis:`job\_wait`\  in seconds. The job is tracked only for this duration.

      This option is applicable when \ :emphasis:`job\_wait`\  is \ :literal:`true`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`10800`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-new_name"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-new_name:

      .. rst-class:: ansible-option-title

      **new_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-new_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      New name of the discovery configuration job.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-password"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-password:

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

      OpenManage Enterprise password.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-port"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-port:

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

      OpenManage Enterprise HTTPS port.


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`443`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-schedule"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-schedule:

      .. rst-class:: ansible-option-title

      **schedule**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-schedule" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Provides the option to schedule the discovery job.

      If \ :literal:`RunLater`\  is selected, then \ :emphasis:`cron`\  must be specified.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`"RunNow"` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`"RunLater"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-state"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-state:

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

      \ :literal:`present`\  creates a discovery job or modifies an existing discovery job.

      \ :emphasis:`discovery\_job\_name`\  is mandatory for the creation of a new discovery job.

      If multiple discoveries of the same \ :emphasis:`discovery\_job\_name`\  exist, then the new discovery job will not be created.

      \ :literal:`absent`\  deletes an existing discovery job(s) with the specified \ :emphasis:`discovery\_job\_name`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`"present"` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`"absent"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-timeout"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-timeout:

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
        <div class="ansibleOptionAnchor" id="parameter-trap_destination"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-trap_destination:

      .. rst-class:: ansible-option-title

      **trap_destination**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-trap_destination" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Enable OpenManage Enterprise to receive the incoming SNMP traps from the discovered devices.

      This is effective only for servers discovered by using their iDRAC interface.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`false` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-username"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-username:

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

      OpenManage Enterprise username.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-validate_certs"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__parameter-validate_certs:

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
   - This module does not support \ :literal:`check\_mode`\ .
   - If \ :emphasis:`state`\  is \ :literal:`present`\ , then Idempotency is not supported.

.. Seealso


.. Examples

Examples
--------

.. code-block:: yaml+jinja

    
    ---
    - name: Discover servers in a range
      dellemc.openmanage.ome_discovery:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        discovery_job_name: "Discovery_server_1"
        discovery_config_targets:
          - network_address_detail:
              - 192.96.24.1-192.96.24.255
            device_types:
              - SERVER
            wsman:
              username: user
              password: password

    - name: Discover chassis in a range
      dellemc.openmanage.ome_discovery:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        discovery_job_name: "Discovery_chassis_1"
        discovery_config_targets:
          - network_address_detail:
              - 192.96.24.1-192.96.24.255
            device_types:
              - CHASSIS
            wsman:
              username: user
              password: password

    - name: Discover switches in a range
      dellemc.openmanage.ome_discovery:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        discovery_job_name: "Discover_switch_1"
        discovery_config_targets:
          - network_address_detail:
              - 192.96.24.1-192.96.24.255
            device_types:
              - NETWORK SWITCH
            snmp:
              community: snmp_creds

    - name: Discover storage in a range
      dellemc.openmanage.ome_discovery:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        discovery_job_name: "Discover_storage_1"
        discovery_config_targets:
          - network_address_detail:
              - 192.96.24.1-192.96.24.255
            device_types:
              - STORAGE
            storage:
              username: user
              password: password
            snmp:
              community: snmp_creds

    - name: Delete a discovery job
      dellemc.openmanage.ome_discovery:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        state: "absent"
        discovery_job_name: "Discovery-123"

    - name: Schedule the discovery of multiple devices ignoring partial failure and enable trap to receive alerts
      dellemc.openmanage.ome_discovery:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        state: "present"
        discovery_job_name: "Discovery-123"
        discovery_config_targets:
          - network_address_detail:
              - 192.96.24.1-192.96.24.255
              - 192.96.0.0/24
              - 192.96.26.108
            device_types:
              - SERVER
              - CHASSIS
              - STORAGE
              - NETWORK SWITCH
            wsman:
              username: wsman_user
              password: wsman_pwd
            redfish:
              username: redfish_user
              password: redfish_pwd
            snmp:
              community: snmp_community
          - network_address_detail:
              - 192.96.25.1-192.96.25.255
              - ipmihost
              - esxiserver
              - sshserver
            device_types:
              - SERVER
            ssh:
              username: ssh_user
              password: ssh_pwd
            vmware:
              username: vm_user
              password: vmware_pwd
            ipmi:
              username: ipmi_user
              password: ipmi_pwd
        schedule: RunLater
        cron: "0 0 9 ? * MON,WED,FRI *"
        ignore_partial_failure: true
        trap_destination: true
        community_string: true
        email_recipient: test_email@company.com

    - name: Discover servers with ca check enabled
      dellemc.openmanage.ome_discovery:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        discovery_job_name: "Discovery_server_ca1"
        discovery_config_targets:
          - network_address_detail:
              - 192.96.24.108
            device_types:
              - SERVER
            wsman:
              username: user
              password: password
              ca_check: true
              certificate_data: "{{ lookup('ansible.builtin.file', '/path/to/certificate_data_file') }}"

    - name: Discover chassis with ca check enabled data
      dellemc.openmanage.ome_discovery:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        discovery_job_name: "Discovery_chassis_ca1"
        discovery_config_targets:
          - network_address_detail:
              - 192.96.24.108
            device_types:
              - CHASSIS
            redfish:
              username: user
              password: password
              ca_check: true
              certificate_data: "-----BEGIN CERTIFICATE-----\r\n
              ABCDEFGHIJKLMNOPQRSTUVWXYZaqwertyuiopasdfghjklzxcvbnmasdasagasvv\r\n
              ABCDEFGHIJKLMNOPQRSTUVWXYZaqwertyuiopasdfghjklzxcvbnmasdasagasvv\r\n
              ABCDEFGHIJKLMNOPQRSTUVWXYZaqwertyuiopasdfghjklzxcvbnmasdasagasvv\r\n
              aqwertyuiopasdfghjklzxcvbnmasdasagasvv=\r\n
              -----END CERTIFICATE-----"




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
        <div class="ansibleOptionAnchor" id="return-discovery_ids"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__return-discovery_ids:

      .. rst-class:: ansible-option-title

      **discovery_ids**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-discovery_ids" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      IDs of the discoveries with duplicate names.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` when discoveries with duplicate name exist for \ :emphasis:`state`\  is \ :literal:`present`\ 

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`[1234, 5678]`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-discovery_status"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__return-discovery_status:

      .. rst-class:: ansible-option-title

      **discovery_status**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-discovery_status" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Details of the discovery job created or modified.

      If \ :emphasis:`job\_wait`\  is true, Completed and Failed IPs are also listed.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` when \ :emphasis:`state`\  is \ :literal:`present`\ 

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"Completed": ["192.168.24.17", "192.168.24.20", "192.168.24.22"], "DiscoveredDevicesByType": [{"Count": 3, "DeviceType": "SERVER"}], "DiscoveryConfigDiscoveredDeviceCount": 3, "DiscoveryConfigEmailRecipient": "myemail@dell.com", "DiscoveryConfigExpectedDeviceCount": 9, "DiscoveryConfigGroupId": 125, "Failed": ["192.168.24.15", "192.168.24.16", "192.168.24.18", "192.168.24.19", "192.168.24.21", "host123"], "JobDescription": "D1", "JobEnabled": true, "JobEndTime": "2021-01-01 06:27:29.99", "JobId": 12666, "JobName": "D1", "JobNextRun": null, "JobProgress": "100", "JobSchedule": "startnow", "JobStartTime": "2021-01-01 06:24:10.071", "JobStatusId": 2090, "LastUpdateTime": "2021-01-01 06:27:30.001", "UpdatedBy": "admin"}`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-error_info"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__return-error_info:

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

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"error": {"@Message.ExtendedInfo": [{"Message": "Unable to process the request because an error occurred.", "MessageArgs": [], "MessageId": "GEN1234", "RelatedProperties": [], "Resolution": "Retry the operation. If the issue persists, contact your system administrator.", "Severity": "Critical"}], "code": "Base.1.0.GeneralError", "message": "A general error has occurred. See ExtendedInfo for more information."}}`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-job_detailed_status"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__return-job_detailed_status:

      .. rst-class:: ansible-option-title

      **job_detailed_status**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-job_detailed_status" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Detailed last execution history of a job.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` All time.

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`[{"ElapsedTime": "00:00:00", "EndTime": null, "ExecutionHistoryId": 564873, "Id": 656893, "IdBaseEntity": 0, "JobStatus": {"Id": 2050, "Name": "Running"}, "Key": "192.96.24.1", "Progress": "0", "StartTime": "2023-07-04 06:23:54.008", "Value": "Running\\nDiscovery of target 192.96.24.1 started.\\nDiscovery target resolved to IP  192.96.24.1 ."}]`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-msg"></div>

      .. _ansible_collections.dellemc.openmanage.ome_discovery_module__return-msg:

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

      Overall status of the discovery operation.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` always

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`"Successfully deleted 1 discovery job(s)."`


      .. raw:: html

        </div>



..  Status (Presently only deprecated)


.. Authors

Authors
~~~~~~~

- Jagadeesh N V (@jagadeeshnv)
- Sajna Shetty (@Sajna-Shetty)
- Abhishek Sinha (@Abhishek-Dell)



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

