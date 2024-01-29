
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

.. _ansible_collections.dellemc.openmanage.ome_application_console_preferences_module:

.. Anchors: short name for ansible.builtin

.. Anchors: aliases



.. Title

dellemc.openmanage.ome_application_console_preferences module -- Configure console preferences on OpenManage Enterprise.
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. Collection note

.. note::
    This module is part of the `dellemc.openmanage collection <https://galaxy.ansible.com/dellemc/openmanage>`_ (version 8.5.0).

    To install it, use: :code:`ansible-galaxy collection install dellemc.openmanage`.
    You need further requirements to be able to use this module,
    see :ref:`Requirements <ansible_collections.dellemc.openmanage.ome_application_console_preferences_module_requirements>` for details.

    To use it in a playbook, specify: :code:`dellemc.openmanage.ome_application_console_preferences`.

.. version_added

.. rst-class:: ansible-version-added

New in dellemc.openmanage 5.2.0

.. contents::
   :local:
   :depth: 1

.. Deprecated


Synopsis
--------

.. Description

- This module allows user to configure the console preferences on OpenManage Enterprise.


.. Aliases


.. Requirements

.. _ansible_collections.dellemc.openmanage.ome_application_console_preferences_module_requirements:

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
        <div class="ansibleOptionAnchor" id="parameter-builtin_appliance_share"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_console_preferences_module__parameter-builtin_appliance_share:

      .. rst-class:: ansible-option-title

      **builtin_appliance_share**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-builtin_appliance_share" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The external network share that the appliance must access to complete operations.


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-builtin_appliance_share/cifs_options"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_console_preferences_module__parameter-builtin_appliance_share/cifs_options:

      .. rst-class:: ansible-option-title

      **cifs_options**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-builtin_appliance_share/cifs_options" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The SMB protocol version.

      \ :emphasis:`cifs\_options`\  is required \ :emphasis:`share\_options`\  is \ :literal:`CIFS`\ .

      \ :literal:`V1`\  to enable SMBv1.

      \ :literal:`V2`\  to enable SMBv2


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"V1"`
      - :ansible-option-choices-entry:`"V2"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-builtin_appliance_share/share_options"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_console_preferences_module__parameter-builtin_appliance_share/share_options:

      .. rst-class:: ansible-option-title

      **share_options**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-builtin_appliance_share/share_options" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The share options.

      \ :literal:`CIFS`\  to select CIFS share type.

      \ :literal:`HTTPS`\  to select HTTPS share type.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"CIFS"`
      - :ansible-option-choices-entry:`"HTTPS"`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-ca_path"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_console_preferences_module__parameter-ca_path:

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
        <div class="ansibleOptionAnchor" id="parameter-device_health"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_console_preferences_module__parameter-device_health:

      .. rst-class:: ansible-option-title

      **device_health**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-device_health" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The time after which the health of the devices must be automatically monitored and updated on the OpenManage Enterprise dashboard.


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-device_health/health_and_power_state_on_connection_lost"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_console_preferences_module__parameter-device_health/health_and_power_state_on_connection_lost:

      .. rst-class:: ansible-option-title

      **health_and_power_state_on_connection_lost**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-device_health/health_and_power_state_on_connection_lost" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The latest recorded device health.

      \ :literal:`last\_known`\  to display the latest recorded device health when the power connection was lost.

      \ :literal:`unknown`\  to display the latest recorded device health when the device status moved to unknown.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"last\_known"`
      - :ansible-option-choices-entry:`"unknown"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-device_health/health_check_interval"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_console_preferences_module__parameter-device_health/health_check_interval:

      .. rst-class:: ansible-option-title

      **health_check_interval**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-device_health/health_check_interval" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The frequency at which the device health must be recorded and data stored.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-device_health/health_check_interval_unit"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_console_preferences_module__parameter-device_health/health_check_interval_unit:

      .. rst-class:: ansible-option-title

      **health_check_interval_unit**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-device_health/health_check_interval_unit" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The time unit of the frequency at which the device health must be recorded and data stored.

      \ :literal:`Hourly`\  to set the frequency in hours.

      \ :literal:`Minutes`\  to set the frequency in minutes.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"Hourly"`
      - :ansible-option-choices-entry:`"Minutes"`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_settings"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_console_preferences_module__parameter-discovery_settings:

      .. rst-class:: ansible-option-title

      **discovery_settings**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_settings" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The device naming to be used by the OpenManage Enterprise to identify the discovered iDRACs and other devices.


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_settings/common_mac_addresses"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_console_preferences_module__parameter-discovery_settings/common_mac_addresses:

      .. rst-class:: ansible-option-title

      **common_mac_addresses**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_settings/common_mac_addresses" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The common MAC addresses separated by a comma.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_settings/general_device_naming"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_console_preferences_module__parameter-discovery_settings/general_device_naming:

      .. rst-class:: ansible-option-title

      **general_device_naming**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_settings/general_device_naming" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Applicable to all the discovered devices other than the iDRACs.

      \ :literal:`DNS`\  to use the DNS name.

      \ :literal:`NETBIOS`\  to use the NetBIOS name.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`"DNS"` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`"NETBIOS"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_settings/invalid_device_hostname"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_console_preferences_module__parameter-discovery_settings/invalid_device_hostname:

      .. rst-class:: ansible-option-title

      **invalid_device_hostname**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_settings/invalid_device_hostname" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The invalid hostnames separated by a comma.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-discovery_settings/server_device_naming"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_console_preferences_module__parameter-discovery_settings/server_device_naming:

      .. rst-class:: ansible-option-title

      **server_device_naming**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-discovery_settings/server_device_naming" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Applicable to iDRACs only.

      \ :literal:`IDRAC\_HOSTNAME`\  to use the iDRAC hostname.

      \ :literal:`IDRAC\_SYSTEM\_HOSTNAME`\  to use the system hostname.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"IDRAC\_HOSTNAME"`
      - :ansible-option-choices-entry-default:`"IDRAC\_SYSTEM\_HOSTNAME"` :ansible-option-choices-default-mark:`← (default)`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-email_sender_settings"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_console_preferences_module__parameter-email_sender_settings:

      .. rst-class:: ansible-option-title

      **email_sender_settings**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-email_sender_settings" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The email address of the user who is sending an email message.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-hostname"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_console_preferences_module__parameter-hostname:

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
        <div class="ansibleOptionAnchor" id="parameter-metrics_collection_settings"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_console_preferences_module__parameter-metrics_collection_settings:

      .. rst-class:: ansible-option-title

      **metrics_collection_settings**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-metrics_collection_settings" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The frequency of the PowerManager extension data maintenance and purging.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-mx7000_onboarding_preferences"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_console_preferences_module__parameter-mx7000_onboarding_preferences:

      .. rst-class:: ansible-option-title

      **mx7000_onboarding_preferences**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-mx7000_onboarding_preferences" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Alert-forwarding behavior on chassis when they are onboarded.

      \ :literal:`all`\  to receive all alert.

      \ :literal:`chassis`\  to receive chassis category alerts only.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"all"`
      - :ansible-option-choices-entry:`"chassis"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-password"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_console_preferences_module__parameter-password:

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

      .. _ansible_collections.dellemc.openmanage.ome_application_console_preferences_module__parameter-port:

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
        <div class="ansibleOptionAnchor" id="parameter-report_row_limit"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_console_preferences_module__parameter-report_row_limit:

      .. rst-class:: ansible-option-title

      **report_row_limit**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-report_row_limit" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The maximum number of rows that you can view on OpenManage Enterprise reports.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-server_initiated_discovery"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_console_preferences_module__parameter-server_initiated_discovery:

      .. rst-class:: ansible-option-title

      **server_initiated_discovery**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-server_initiated_discovery" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Server initiated discovery settings.


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-server_initiated_discovery/device_discovery_approval_policy"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_console_preferences_module__parameter-server_initiated_discovery/device_discovery_approval_policy:

      .. rst-class:: ansible-option-title

      **device_discovery_approval_policy**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-server_initiated_discovery/device_discovery_approval_policy" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Discovery approval policies.

      \ :literal:`Automatic`\  allows servers with iDRAC Firmware version 4.00.00.00, which are on the same network as the console, to be discovered automatically by the console.

      \ :literal:`Manual`\  for the servers to be discovered by the user manually.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"Automatic"`
      - :ansible-option-choices-entry:`"Manual"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-server_initiated_discovery/set_trap_destination"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_console_preferences_module__parameter-server_initiated_discovery/set_trap_destination:

      .. rst-class:: ansible-option-title

      **set_trap_destination**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-server_initiated_discovery/set_trap_destination" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Trap destination settings.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-timeout"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_console_preferences_module__parameter-timeout:

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
        <div class="ansibleOptionAnchor" id="parameter-trap_forwarding_format"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_console_preferences_module__parameter-trap_forwarding_format:

      .. rst-class:: ansible-option-title

      **trap_forwarding_format**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-trap_forwarding_format" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The trap forwarding format.

      \ :literal:`Original`\  to retain the trap data as is.

      \ :literal:`Normalized`\  to normalize the trap data.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"Original"`
      - :ansible-option-choices-entry:`"Normalized"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-username"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_console_preferences_module__parameter-username:

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

      .. _ansible_collections.dellemc.openmanage.ome_application_console_preferences_module__parameter-validate_certs:

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
   - This module supports \ :literal:`check\_mode`\ .

.. Seealso


.. Examples

Examples
--------

.. code-block:: yaml+jinja

    
    ---
    - name: Update Console preferences with all the settings.
      dellemc.openmanage.ome_application_console_preferences:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        report_row_limit: 123
        device_health:
          health_check_interval: 1
          health_check_interval_unit: Hourly
          health_and_power_state_on_connection_lost: last_known
        discovery_settings:
          general_device_naming: DNS
          server_device_naming: IDRAC_HOSTNAME
          invalid_device_hostname: "localhost"
          common_mac_addresses: "::"
        server_initiated_discovery:
          device_discovery_approval_policy: Automatic
          set_trap_destination: true
        mx7000_onboarding_preferences: all
        builtin_appliance_share:
          share_options: CIFS
          cifs_options: V1
        email_sender_settings: "admin@dell.com"
        trap_forwarding_format: Normalized
        metrics_collection_settings: 31

    - name: Update Console preferences with report and device health settings.
      dellemc.openmanage.ome_application_console_preferences:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        report_row_limit: 236
        device_health:
          health_check_interval: 10
          health_check_interval_unit: Hourly
          health_and_power_state_on_connection_lost: last_known

    - name: Update Console preferences with invalid device health settings.
      dellemc.openmanage.ome_application_console_preferences:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        device_health:
          health_check_interval: 65
          health_check_interval_unit: Minutes

    - name: Update Console preferences with discovery and built in appliance share settings.
      dellemc.openmanage.ome_application_console_preferences:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        discovery_settings:
          general_device_naming: DNS
          server_device_naming: IDRAC_SYSTEM_HOSTNAME
          invalid_device_hostname: "localhost"
          common_mac_addresses: "00:53:45:00:00:00"
        builtin_appliance_share:
          share_options: CIFS
          cifs_options: V1

    - name: Update Console preferences with server initiated discovery, mx7000 onboarding preferences, email sender,
        trap forwarding format, and metrics collection settings.
      dellemc.openmanage.ome_application_console_preferences:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        server_initiated_discovery:
          device_discovery_approval_policy: Automatic
          set_trap_destination: true
        mx7000_onboarding_preferences: chassis
        email_sender_settings: "admin@dell.com"
        trap_forwarding_format: Original
        metrics_collection_settings: 365




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
        <div class="ansibleOptionAnchor" id="return-console_preferences"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_console_preferences_module__return-console_preferences:

      .. rst-class:: ansible-option-title

      **console_preferences**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-console_preferences" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Details of the console preferences.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` on success

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`[{"DataType": "java.lang.String", "DefaultValue": "SLOT\_NAME", "GroupName": "DISCOVERY\_SETTING", "Name": "DEVICE\_PREFERRED\_NAME", "Value": "PREFER\_DNS,PREFER\_IDRAC\_SYSTEM\_HOSTNAME"}, {"DataType": "java.lang.String", "DefaultValue": "", "GroupName": "DISCOVERY\_SETTING", "Name": "INVALID\_DEVICE\_HOSTNAME", "Value": "localhost,localhost.localdomain,not defined,pv132t,pv136t,default,dell,idrac-"}, {"DataType": "java.lang.String", "DefaultValue": "", "GroupName": "DISCOVERY\_SETTING", "Name": "COMMON\_MAC\_ADDRESSES", "Value": "00:53:45:00:00:00,33:50:6F:45:30:30,50:50:54:50:30:30,00:00:FF:FF:FF:FF,20:41:53:59:4E:FF,00:00:00:00:00:00,20:41:53:59:4e:ff,00:00:00:00:00:00"}, {"DataType": "java.lang.String", "DefaultValue": "CIFS", "GroupName": "BUILT\_IN\_APPLIANCE\_SHARE\_SETTINGS", "Name": "SHARE\_TYPE", "Value": "CIFS"}, {"DataType": "java.lang.String", "DefaultValue": "AsIs", "GroupName": "", "Name": "TRAP\_FORWARDING\_SETTING", "Value": "Normalized"}, {"DataType": "java.lang.Integer", "DefaultValue": "365", "GroupName": "", "Name": "DATA\_PURGE\_INTERVAL", "Value": "3650000"}, {"DataType": "java.lang.String", "DefaultValue": "last\_known", "GroupName": "CONSOLE\_CONNECTION\_SETTING", "Name": "CONSOLE\_CONNECTION\_SETTING", "Value": "last\_known"}, {"DataType": "java.lang.String", "DefaultValue": "V2", "GroupName": "CIFS\_PROTOCOL\_SETTINGS", "Name": "MIN\_PROTOCOL\_VERSION", "Value": "V1"}, {"DataType": "java.lang.Integer", "DefaultValue": "2000", "GroupName": "", "Name": "ALERT\_ACKNOWLEDGEMENT\_VIEW", "Value": "2000"}, {"DataType": "java.lang.Boolean", "DefaultValue": "false", "GroupName": "CONSOLE\_UPDATE\_SETTING\_GROUP", "Name": "AUTO\_CONSOLE\_UPDATE\_AFTER\_DOWNLOAD", "Value": "false"}, {"DataType": "java.lang.Boolean", "DefaultValue": "false", "GroupName": "", "Name": "NODE\_INITIATED\_DISCOVERY\_SET\_TRAP\_DESTINATION", "Value": "false"}, {"DataType": "java.lang.Integer", "DefaultValue": "0", "GroupName": "", "Name": "REPORTS\_MAX\_RESULTS\_LIMIT", "Value": "2000000000000000000000000"}, {"DataType": "java.lang.String", "DefaultValue": "omcadmin@dell.com", "GroupName": "", "Name": "EMAIL\_SENDER", "Value": "admin1@dell.com@dell.com@dell.com"}, {"DataType": "java.lang.String", "DefaultValue": "all", "GroupName": "", "Name": "MX7000\_ONBOARDING\_PREF", "Value": "test\_chassis"}, {"DataType": "java.lang.String", "DefaultValue": "Automatic", "GroupName": "", "Name": "DISCOVERY\_APPROVAL\_POLICY", "Value": "Automatic\_test"}]`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-error_info"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_console_preferences_module__return-error_info:

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

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"error": {"@Message.ExtendedInfo": [{"Message": "Unable to complete the request because the resource URI does not exist or is not implemented.", "MessageArgs": [], "MessageId": "CGEN1006", "RelatedProperties": [], "Resolution": "Enter a valid URI and retry the operation.", "Severity": "Critical"}], "code": "Base.1.0.GeneralError", "message": "A general error has occurred. See ExtendedInfo for more information."}}`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-msg"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_console_preferences_module__return-msg:

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

      Overall status of the console preferences.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` always

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`"Successfully update the console preferences."`


      .. raw:: html

        </div>



..  Status (Presently only deprecated)


.. Authors

Authors
~~~~~~~

- Sachin Apagundi(@sachin-apa)
- Husniya Hameed (@husniya-hameed)



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

