
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

.. _ansible_collections.dellemc.openmanage.ome_device_quick_deploy_module:

.. Anchors: short name for ansible.builtin

.. Anchors: aliases



.. Title

dellemc.openmanage.ome_device_quick_deploy module -- Configure Quick Deploy settings on OpenManage Enterprise Modular.
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. Collection note

.. note::
    This module is part of the `dellemc.openmanage collection <https://galaxy.ansible.com/dellemc/openmanage>`_ (version 8.5.0).

    To install it, use: :code:`ansible-galaxy collection install dellemc.openmanage`.
    You need further requirements to be able to use this module,
    see :ref:`Requirements <ansible_collections.dellemc.openmanage.ome_device_quick_deploy_module_requirements>` for details.

    To use it in a playbook, specify: :code:`dellemc.openmanage.ome_device_quick_deploy`.

.. version_added

.. rst-class:: ansible-version-added

New in dellemc.openmanage 5.0.0

.. contents::
   :local:
   :depth: 1

.. Deprecated


Synopsis
--------

.. Description

- This module allows to configure the Quick Deploy settings of the server or IOM on OpenManage Enterprise Modular.


.. Aliases


.. Requirements

.. _ansible_collections.dellemc.openmanage.ome_device_quick_deploy_module_requirements:

Requirements
------------
The below requirements are needed on the host that executes this module.

- python \>= 3.9.6






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

      .. _ansible_collections.dellemc.openmanage.ome_device_quick_deploy_module__parameter-ca_path:

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
        <div class="ansibleOptionAnchor" id="parameter-device_id"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_quick_deploy_module__parameter-device_id:

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

      The ID of the chassis for which the Quick Deploy settings to be deployed.

      If the device ID is not specified, this module updates the Quick Deploy settings for the \ :emphasis:`hostname`\ .

      \ :emphasis:`device\_id`\  is mutually exclusive with \ :emphasis:`device\_service\_tag`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-device_service_tag"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_quick_deploy_module__parameter-device_service_tag:

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

      The service tag of the chassis for which the Quick Deploy settings to be deployed.

      If the device service tag is not specified, this module updates the Quick Deploy settings for the \ :emphasis:`hostname`\ .

      \ :emphasis:`device\_service\_tag`\  is mutually exclusive with \ :emphasis:`device\_id`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-hostname"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_quick_deploy_module__parameter-hostname:

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
        <div class="ansibleOptionAnchor" id="parameter-job_wait"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_quick_deploy_module__parameter-job_wait:

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

      Determines whether to wait for the job completion or not.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry-default:`true` :ansible-option-choices-default-mark:`← (default)`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-job_wait_timeout"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_quick_deploy_module__parameter-job_wait_timeout:

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

      :ansible-option-default-bold:`Default:` :ansible-option-default:`120`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-password"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_quick_deploy_module__parameter-password:

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

      .. _ansible_collections.dellemc.openmanage.ome_device_quick_deploy_module__parameter-port:

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
        <div class="ansibleOptionAnchor" id="parameter-quick_deploy_options"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_quick_deploy_module__parameter-quick_deploy_options:

      .. rst-class:: ansible-option-title

      **quick_deploy_options**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-quick_deploy_options" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The Quick Deploy settings for server and IOM quick deploy.


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-quick_deploy_options/ipv4_enabled"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_quick_deploy_module__parameter-quick_deploy_options/ipv4_enabled:

      .. rst-class:: ansible-option-title

      **ipv4_enabled**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-quick_deploy_options/ipv4_enabled" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enables or disables the IPv4 network.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-quick_deploy_options/ipv4_gateway"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_quick_deploy_module__parameter-quick_deploy_options/ipv4_gateway:

      .. rst-class:: ansible-option-title

      **ipv4_gateway**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-quick_deploy_options/ipv4_gateway" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      IPv4 gateway.

      \ :emphasis:`ipv4\_gateway`\  is required if \ :emphasis:`ipv4\_network\_type`\  is \ :literal:`Static`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-quick_deploy_options/ipv4_network_type"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_quick_deploy_module__parameter-quick_deploy_options/ipv4_network_type:

      .. rst-class:: ansible-option-title

      **ipv4_network_type**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-quick_deploy_options/ipv4_network_type" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      IPv4 network type.

      \ :emphasis:`ipv4\_network\_type`\  is required if \ :emphasis:`ipv4\_enabled`\  is \ :literal:`true`\ .

      \ :literal:`Static`\  to configure the static IP settings.

      \ :literal:`DHCP`\  to configure the Dynamic IP settings.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"Static"`
      - :ansible-option-choices-entry:`"DHCP"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-quick_deploy_options/ipv4_subnet_mask"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_quick_deploy_module__parameter-quick_deploy_options/ipv4_subnet_mask:

      .. rst-class:: ansible-option-title

      **ipv4_subnet_mask**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-quick_deploy_options/ipv4_subnet_mask" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      IPv4 subnet mask.

      \ :emphasis:`ipv4\_subnet\_mask`\  is required if \ :emphasis:`ipv4\_network\_type`\  is \ :literal:`Static`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-quick_deploy_options/ipv6_enabled"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_quick_deploy_module__parameter-quick_deploy_options/ipv6_enabled:

      .. rst-class:: ansible-option-title

      **ipv6_enabled**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-quick_deploy_options/ipv6_enabled" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enables or disables the IPv6 network.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-quick_deploy_options/ipv6_gateway"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_quick_deploy_module__parameter-quick_deploy_options/ipv6_gateway:

      .. rst-class:: ansible-option-title

      **ipv6_gateway**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-quick_deploy_options/ipv6_gateway" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      IPv6 gateway.

      \ :emphasis:`ipv6\_gateway`\  is required if \ :emphasis:`ipv6\_network\_type`\  is \ :literal:`Static`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-quick_deploy_options/ipv6_network_type"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_quick_deploy_module__parameter-quick_deploy_options/ipv6_network_type:

      .. rst-class:: ansible-option-title

      **ipv6_network_type**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-quick_deploy_options/ipv6_network_type" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      IPv6 network type.

      \ :emphasis:`ipv6\_network\_type`\  is required if \ :emphasis:`ipv6\_enabled`\  is \ :literal:`true`\ .

      \ :literal:`Static`\  to configure the static IP settings.

      \ :literal:`DHCP`\  to configure the Dynamic IP settings.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"Static"`
      - :ansible-option-choices-entry:`"DHCP"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-quick_deploy_options/ipv6_prefix_length"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_quick_deploy_module__parameter-quick_deploy_options/ipv6_prefix_length:

      .. rst-class:: ansible-option-title

      **ipv6_prefix_length**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-quick_deploy_options/ipv6_prefix_length" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      IPV6 prefix length.

      \ :emphasis:`ipv6\_prefix\_length`\  is required if \ :emphasis:`ipv6\_network\_type`\  is \ :literal:`Static`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-quick_deploy_options/password"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_quick_deploy_module__parameter-quick_deploy_options/password:

      .. rst-class:: ansible-option-title

      **password**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-quick_deploy_options/password" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The password to login to the server or IOM.

      The module will always report change when \ :emphasis:`password`\  option is added.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-quick_deploy_options/slots"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_quick_deploy_module__parameter-quick_deploy_options/slots:

      .. rst-class:: ansible-option-title

      **slots**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-quick_deploy_options/slots" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The slot configuration for the server or IOM.


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-quick_deploy_options/slots/slot_id"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_quick_deploy_module__parameter-quick_deploy_options/slots/slot_id:

      .. rst-class:: ansible-option-title

      **slot_id**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-quick_deploy_options/slots/slot_id" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The ID of the slot.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-quick_deploy_options/slots/slot_ipv4_address"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_quick_deploy_module__parameter-quick_deploy_options/slots/slot_ipv4_address:

      .. rst-class:: ansible-option-title

      **slot_ipv4_address**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-quick_deploy_options/slots/slot_ipv4_address" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The IPv4 address of the slot.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-quick_deploy_options/slots/slot_ipv6_address"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_quick_deploy_module__parameter-quick_deploy_options/slots/slot_ipv6_address:

      .. rst-class:: ansible-option-title

      **slot_ipv6_address**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-quick_deploy_options/slots/slot_ipv6_address" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The IPv6 address of the slot.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-quick_deploy_options/slots/vlan_id"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_quick_deploy_module__parameter-quick_deploy_options/slots/vlan_id:

      .. rst-class:: ansible-option-title

      **vlan_id**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-quick_deploy_options/slots/vlan_id" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The ID of the VLAN.


      .. raw:: html

        </div>



  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-setting_type"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_quick_deploy_module__parameter-setting_type:

      .. rst-class:: ansible-option-title

      **setting_type**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-setting_type" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The type of the Quick Deploy settings to be applied.

      \ :literal:`ServerQuickDeploy`\  to apply the server Quick Deploy settings.

      \ :literal:`IOMQuickDeploy`\  to apply the IOM Quick Deploy settings.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"ServerQuickDeploy"`
      - :ansible-option-choices-entry:`"IOMQuickDeploy"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-timeout"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_quick_deploy_module__parameter-timeout:

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

      .. _ansible_collections.dellemc.openmanage.ome_device_quick_deploy_module__parameter-username:

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

      .. _ansible_collections.dellemc.openmanage.ome_device_quick_deploy_module__parameter-validate_certs:

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
   - Run this module from a system that has direct access to OpenManage Enterprise Modular.
   - This module supports \ :literal:`check\_mode`\ .
   - The module will always report change when \ :emphasis:`password`\  option is added.
   - If the chassis is a member of a multi-chassis group and it is assigned as a backup lead chassis, the operations performed on the chassis using this module may conflict with the management operations performed on the chassis through the lead chassis.

.. Seealso


.. Examples

Examples
--------

.. code-block:: yaml+jinja

    
    ---
    - name: Configure server Quick Deploy settings of the chassis using device ID.
      dellemc.openmanage.ome_device_quick_deploy:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        device_id: 25011
        setting_type: ServerQuickDeploy
        ca_path: "/path/to/ca_cert.pem"
        quick_deploy_options:
          password: "password"
          ipv4_enabled: true
          ipv4_network_type: Static
          ipv4_subnet_mask: 255.255.255.0
          ipv4_gateway: 192.168.0.1
          ipv6_enabled: true
          ipv6_network_type: Static
          ipv6_prefix_length: 1
          ipv6_gateway: "::"
          slots:
            - slot_id: 1
              slot_ipv4_address: 192.168.0.2
              slot_ipv6_address: "::"
              vlan_id: 1
            - slot_id: 2
              slot_ipv4_address: 192.168.0.3
              slot_ipv6_address: "::"
              vlan_id: 2

    - name: Configure server Quick Deploy settings of the chassis using device service tag.
      dellemc.openmanage.ome_device_quick_deploy:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        device_service_tag: GHRT2RL
        setting_type: IOMQuickDeploy
        ca_path: "/path/to/ca_cert.pem"
        quick_deploy_options:
          password: "password"
          ipv4_enabled: true
          ipv4_network_type: Static
          ipv4_subnet_mask: 255.255.255.0
          ipv4_gateway: 192.168.0.1
          ipv6_enabled: true
          ipv6_network_type: Static
          ipv6_prefix_length: 1
          ipv6_gateway: "::"
          slots:
            - slot_id: 1
              slot_ipv4_address: 192.168.0.2
              slot_ipv6_address: "::"
              vlan_id: 1
            - slot_id: 2
              slot_ipv4_address: 192.168.0.3
              slot_ipv6_address: "::"
              vlan_id: 2




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

      .. _ansible_collections.dellemc.openmanage.ome_device_quick_deploy_module__return-error_info:

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
        <div class="ansibleOptionAnchor" id="return-job_id"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_quick_deploy_module__return-job_id:

      .. rst-class:: ansible-option-title

      **job_id**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-job_id" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The job ID of the submitted quick deploy job.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` when quick deploy job is submitted.

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`1234`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-msg"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_quick_deploy_module__return-msg:

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

      Overall status of the device quick deploy settings.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` always

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`"Successfully deployed the quick deploy settings."`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-quick_deploy_settings"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_quick_deploy_module__return-quick_deploy_settings:

      .. rst-class:: ansible-option-title

      **quick_deploy_settings**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-quick_deploy_settings" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      returned when quick deploy settings are deployed successfully.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` success

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"DeviceId": 25011, "IpV4Gateway": "192.168.0.1", "IpV4SubnetMask": "255.255.255.0", "IpV6Gateway": "::", "NetworkTypeV4": "Static", "NetworkTypeV6": "Static", "PrefixLength": "2", "ProtocolTypeV4": true, "ProtocolTypeV6": true, "SettingType": "ServerQuickDeploy", "slots": [{"DeviceCapabilities": [18, 17, 16, 15, 14, 13, 12, 11, 10, 9, 41, 8, 7, 4, 3, 2, 1, 31, 30], "DeviceIPV4Address": "192.168.0.2", "DeviceIPV6Address": "::", "DeviceId": 25011, "Dhcpipv4": "Disabled", "Dhcpipv6": "Disabled", "Ipv4Enabled": "Enabled", "Ipv6Enabled": "Enabled", "Model": "PowerEdge MX840c", "SlotIPV4Address": "192.168.0.2", "SlotIPV6Address": "::", "SlotId": 1, "SlotSelected": true, "SlotSettingsApplied": true, "SlotType": "2000", "Type": "1000", "VlanId": "1"}, {"DeviceId": 0, "Model": "", "SlotIPV4Address": "0.0.0.0", "SlotIPV6Address": "::", "SlotId": 2, "SlotSelected": false, "SlotSettingsApplied": false, "SlotType": "2000", "Type": "0"}, {"DeviceId": 0, "Model": "", "SlotIPV4Address": "0.0.0.0", "SlotIPV6Address": "::", "SlotId": 3, "SlotSelected": false, "SlotSettingsApplied": false, "SlotType": "2000", "Type": "0"}, {"DeviceId": 0, "Model": "", "SlotIPV4Address": "0.0.0.0", "SlotIPV6Address": "::", "SlotId": 4, "SlotSelected": false, "SlotSettingsApplied": false, "SlotType": "2000", "Type": "0"}, {"DeviceId": 0, "Model": "", "SlotIPV4Address": "0.0.0.0", "SlotIPV6Address": "::", "SlotId": 5, "SlotSelected": false, "SlotSettingsApplied": false, "SlotType": "2000", "Type": "0"}, {"DeviceId": 0, "Model": "", "SlotIPV4Address": "0.0.0.0", "SlotIPV6Address": "::", "SlotId": 6, "SlotSelected": false, "SlotSettingsApplied": false, "SlotType": "2000", "Type": "0"}, {"DeviceId": 0, "Model": "", "SlotIPV4Address": "0.0.0.0", "SlotIPV6Address": "::", "SlotId": 7, "SlotSelected": false, "SlotSettingsApplied": false, "SlotType": "2000", "Type": "0"}, {"DeviceId": 0, "Model": "", "SlotIPV4Address": "0.0.0.0", "SlotIPV6Address": "::", "SlotId": 8, "SlotSelected": false, "SlotSettingsApplied": false, "SlotType": "2000", "Type": "0"}]}`


      .. raw:: html

        </div>



..  Status (Presently only deprecated)


.. Authors

Authors
~~~~~~~

- Felix Stephen (@felixs88)
- Shivam Sharma (@ShivamSh3)



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

