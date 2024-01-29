
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

.. _ansible_collections.dellemc.openmanage.ome_device_local_access_configuration_module:

.. Anchors: short name for ansible.builtin

.. Anchors: aliases



.. Title

dellemc.openmanage.ome_device_local_access_configuration module -- Configure local access settings on OpenManage Enterprise Modular.
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. Collection note

.. note::
    This module is part of the `dellemc.openmanage collection <https://galaxy.ansible.com/dellemc/openmanage>`_ (version 8.5.0).

    To install it, use: :code:`ansible-galaxy collection install dellemc.openmanage`.
    You need further requirements to be able to use this module,
    see :ref:`Requirements <ansible_collections.dellemc.openmanage.ome_device_local_access_configuration_module_requirements>` for details.

    To use it in a playbook, specify: :code:`dellemc.openmanage.ome_device_local_access_configuration`.

.. version_added

.. rst-class:: ansible-version-added

New in dellemc.openmanage 4.4.0

.. contents::
   :local:
   :depth: 1

.. Deprecated


Synopsis
--------

.. Description

- This module allows to configure the local access settings of the power button, quick sync, KVM, LCD, and chassis direct access on OpenManage Enterprise Modular.


.. Aliases


.. Requirements

.. _ansible_collections.dellemc.openmanage.ome_device_local_access_configuration_module_requirements:

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

      .. _ansible_collections.dellemc.openmanage.ome_device_local_access_configuration_module__parameter-ca_path:

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
        <div class="ansibleOptionAnchor" id="parameter-chassis_power_button"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_local_access_configuration_module__parameter-chassis_power_button:

      .. rst-class:: ansible-option-title

      **chassis_power_button**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-chassis_power_button" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The settings for the chassis power button.


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-chassis_power_button/disabled_button_lcd_override_pin"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_local_access_configuration_module__parameter-chassis_power_button/disabled_button_lcd_override_pin:

      .. rst-class:: ansible-option-title

      **disabled_button_lcd_override_pin**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-chassis_power_button/disabled_button_lcd_override_pin" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The six digit LCD override pin to change the power state of the chassis.

      This is required when \ :emphasis:`enable\_lcd\_override\_pin`\  is \ :literal:`true`\ .

      The module will always report change when \ :emphasis:`disabled\_button\_lcd\_override\_pin`\  is \ :literal:`true`\ .

      The value must be specified in quotes. ex: "001100".


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-chassis_power_button/enable_chassis_power_button"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_local_access_configuration_module__parameter-chassis_power_button/enable_chassis_power_button:

      .. rst-class:: ansible-option-title

      **enable_chassis_power_button**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-chassis_power_button/enable_chassis_power_button" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enables or disables the chassis power button.

      If \ :literal:`false`\ , the chassis cannot be turn on or turn off using the power button.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-chassis_power_button/enable_lcd_override_pin"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_local_access_configuration_module__parameter-chassis_power_button/enable_lcd_override_pin:

      .. rst-class:: ansible-option-title

      **enable_lcd_override_pin**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-chassis_power_button/enable_lcd_override_pin" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enables or disables the LCD override pin.

      This is required when \ :emphasis:`enable\_chassis\_power\_button`\  is \ :literal:`false`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-device_id"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_local_access_configuration_module__parameter-device_id:

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

      The ID of the chassis for which the local access configuration to be updated.

      If the device ID is not specified, this module updates the local access settings for the \ :emphasis:`hostname`\ .

      \ :emphasis:`device\_id`\  is mutually exclusive with \ :emphasis:`device\_service\_tag`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-device_service_tag"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_local_access_configuration_module__parameter-device_service_tag:

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

      The service tag of the chassis for which the local access settings needs to be updated.

      If the device service tag is not specified, this module updates the local access settings for the \ :emphasis:`hostname`\ .

      \ :emphasis:`device\_service\_tag`\  is mutually exclusive with \ :emphasis:`device\_id`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-enable_chassis_direct_access"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_local_access_configuration_module__parameter-enable_chassis_direct_access:

      .. rst-class:: ansible-option-title

      **enable_chassis_direct_access**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-enable_chassis_direct_access" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Enables or disables the access to management consoles such as iDRAC and the management module of the device on the chassis.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-enable_kvm_access"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_local_access_configuration_module__parameter-enable_kvm_access:

      .. rst-class:: ansible-option-title

      **enable_kvm_access**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-enable_kvm_access" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Enables or disables the keyboard, video, and mouse (KVM) interfaces.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-hostname"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_local_access_configuration_module__parameter-hostname:

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
        <div class="ansibleOptionAnchor" id="parameter-lcd"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_local_access_configuration_module__parameter-lcd:

      .. rst-class:: ansible-option-title

      **lcd**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-lcd" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The settings for LCD.

      The \ :emphasis:`lcd`\  options are ignored if the LCD hardware is not present in the chassis.


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-lcd/lcd_access"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_local_access_configuration_module__parameter-lcd/lcd_access:

      .. rst-class:: ansible-option-title

      **lcd_access**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-lcd/lcd_access" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Option to configure the quick sync settings using LCD.

      \ :literal:`VIEW\_AND\_MODIFY`\  to set access level to view and modify.

      \ :literal:`VIEW\_ONLY`\  to set access level to view.

      \ :literal:`DISABLED`\  to disable the access.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"VIEW\_AND\_MODIFY"`
      - :ansible-option-choices-entry:`"VIEW\_ONLY"`
      - :ansible-option-choices-entry:`"DISABLED"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-lcd/lcd_language"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_local_access_configuration_module__parameter-lcd/lcd_language:

      .. rst-class:: ansible-option-title

      **lcd_language**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-lcd/lcd_language" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The language code in which the text on the LCD must be displayed.

      en to set English language.

      fr to set French language.

      de to set German language.

      es to set Spanish language.

      ja to set Japanese language.

      zh to set Chinese language.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-lcd/user_defined"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_local_access_configuration_module__parameter-lcd/user_defined:

      .. rst-class:: ansible-option-title

      **user_defined**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-lcd/user_defined" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The text to display on the LCD Home screen. The LCD Home screen is displayed when the system is reset to factory default settings. The user-defined text can have a maximum of 62 characters.


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-password"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_local_access_configuration_module__parameter-password:

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

      .. _ansible_collections.dellemc.openmanage.ome_device_local_access_configuration_module__parameter-port:

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
        <div class="ansibleOptionAnchor" id="parameter-quick_sync"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_local_access_configuration_module__parameter-quick_sync:

      .. rst-class:: ansible-option-title

      **quick_sync**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-quick_sync" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The settings for quick sync.

      The \ :emphasis:`quick\_sync`\  options are ignored if the quick sync hardware is not present.


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-quick_sync/enable_inactivity_timeout"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_local_access_configuration_module__parameter-quick_sync/enable_inactivity_timeout:

      .. rst-class:: ansible-option-title

      **enable_inactivity_timeout**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-quick_sync/enable_inactivity_timeout" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enables or disables the inactivity timeout.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-quick_sync/enable_quick_sync_wifi"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_local_access_configuration_module__parameter-quick_sync/enable_quick_sync_wifi:

      .. rst-class:: ansible-option-title

      **enable_quick_sync_wifi**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-quick_sync/enable_quick_sync_wifi" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enables or disables the Wi-Fi communication path to the chassis.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-quick_sync/enable_read_authentication"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_local_access_configuration_module__parameter-quick_sync/enable_read_authentication:

      .. rst-class:: ansible-option-title

      **enable_read_authentication**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-quick_sync/enable_read_authentication" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enables or disables the option to log in using your user credentials and to read the inventory in a secure data center.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-quick_sync/quick_sync_access"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_local_access_configuration_module__parameter-quick_sync/quick_sync_access:

      .. rst-class:: ansible-option-title

      **quick_sync_access**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-quick_sync/quick_sync_access" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Users with administrator privileges can set the following types of \ :emphasis:`quick\_sync\_access`\ .

      \ :literal:`READ\_WRITE`\  enables writing configuration using quick sync.

      \ :literal:`READ\_ONLY`\  enables read only access to Wi-Fi and Bluetooth Low Energy(BLE).

      \ :literal:`DISABLED`\  disables reading or writing configuration through quick sync.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"READ\_WRITE"`
      - :ansible-option-choices-entry:`"READ\_ONLY"`
      - :ansible-option-choices-entry:`"DISABLED"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-quick_sync/timeout_limit"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_local_access_configuration_module__parameter-quick_sync/timeout_limit:

      .. rst-class:: ansible-option-title

      **timeout_limit**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-quick_sync/timeout_limit" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Inactivity timeout in seconds or minutes.

      The range is 120 to 3600 in seconds, or 2 to 60 in minutes.

      This option is required when \ :emphasis:`enable\_inactivity\_timeout`\  is \ :literal:`true`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-quick_sync/timeout_limit_unit"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_local_access_configuration_module__parameter-quick_sync/timeout_limit_unit:

      .. rst-class:: ansible-option-title

      **timeout_limit_unit**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-quick_sync/timeout_limit_unit" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Inactivity timeout limit unit.

      \ :literal:`SECONDS`\  to set \ :emphasis:`timeout\_limit`\  in seconds.

      \ :literal:`MINUTES`\  to set \ :emphasis:`timeout\_limit`\  in minutes.

      This option is required when \ :emphasis:`enable\_inactivity\_timeout`\  is \ :literal:`true`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"SECONDS"`
      - :ansible-option-choices-entry:`"MINUTES"`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-timeout"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_local_access_configuration_module__parameter-timeout:

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

      .. _ansible_collections.dellemc.openmanage.ome_device_local_access_configuration_module__parameter-username:

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

      .. _ansible_collections.dellemc.openmanage.ome_device_local_access_configuration_module__parameter-validate_certs:

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
   - The module will always report change when \ :emphasis:`enable\_chassis\_power\_button`\  is \ :literal:`true`\ .

.. Seealso


.. Examples

Examples
--------

.. code-block:: yaml+jinja

    
    ---
    - name: Configure KVM, direct access and power button settings of the chassis using device ID.
      dellemc.openmanage.ome_device_local_access_configuration:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        device_id: 25011
        enable_kvm_access: true
        enable_chassis_direct_access: false
        chassis_power_button:
          enable_chassis_power_button: false
          enable_lcd_override_pin: true
          disabled_button_lcd_override_pin: "123456"

    - name: Configure Quick sync and LCD settings of the chassis using device service tag.
      dellemc.openmanage.ome_device_local_access_configuration:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        device_service_tag: GHRT2RL
        quick_sync:
          quick_sync_access: READ_ONLY
          enable_read_authentication: true
          enable_quick_sync_wifi: true
          enable_inactivity_timeout: true
          timeout_limit: 10
          timeout_limit_unit: MINUTES
        lcd:
          lcd_access: VIEW_ONLY
          lcd_language: en
          user_defined: "LCD Text"

    - name: Configure all local access settings of the host chassis.
      dellemc.openmanage.ome_device_local_access_configuration:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        enable_kvm_access: true
        enable_chassis_direct_access: false
        chassis_power_button:
          enable_chassis_power_button: false
          enable_lcd_override_pin: true
          disabled_button_lcd_override_pin: "123456"
        quick_sync:
          quick_sync_access: READ_WRITE
          enable_read_authentication: true
          enable_quick_sync_wifi: true
          enable_inactivity_timeout: true
          timeout_limit: 120
          timeout_limit_unit: SECONDS
        lcd:
          lcd_access: VIEW_MODIFY
          lcd_language: en
          user_defined: "LCD Text"




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

      .. _ansible_collections.dellemc.openmanage.ome_device_local_access_configuration_module__return-error_info:

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
        <div class="ansibleOptionAnchor" id="return-location_details"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_local_access_configuration_module__return-location_details:

      .. rst-class:: ansible-option-title

      **location_details**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-location_details" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      returned when local access settings are updated successfully.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` success

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"EnableChassisDirect": false, "EnableChassisPowerButton": false, "EnableKvmAccess": true, "EnableLcdOverridePin": false, "LcdAccess": "VIEW\_ONLY", "LcdCustomString": "LCD Text", "LcdLanguage": "en", "LcdOverridePin": "", "LcdPinLength": null, "LcdPresence": "Present", "LedPresence": null, "QuickSync": {"EnableInactivityTimeout": true, "EnableQuickSyncWifi": false, "EnableReadAuthentication": false, "QuickSyncAccess": "READ\_ONLY", "QuickSyncHardware": "Present", "TimeoutLimit": 7, "TimeoutLimitUnit": "MINUTES"}, "SettingType": "LocalAccessConfiguration"}`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-msg"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_local_access_configuration_module__return-msg:

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

      Overall status of the device local access settings.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` always

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`"Successfully updated the local access settings."`


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

