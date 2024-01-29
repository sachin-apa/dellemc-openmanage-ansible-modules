
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

.. _ansible_collections.dellemc.openmanage.idrac_boot_module:

.. Anchors: short name for ansible.builtin

.. Anchors: aliases



.. Title

dellemc.openmanage.idrac_boot module -- Configure the boot order settings.
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. Collection note

.. note::
    This module is part of the `dellemc.openmanage collection <https://galaxy.ansible.com/dellemc/openmanage>`_ (version 8.5.0).

    To install it, use: :code:`ansible-galaxy collection install dellemc.openmanage`.
    You need further requirements to be able to use this module,
    see :ref:`Requirements <ansible_collections.dellemc.openmanage.idrac_boot_module_requirements>` for details.

    To use it in a playbook, specify: :code:`dellemc.openmanage.idrac_boot`.

.. version_added

.. rst-class:: ansible-version-added

New in dellemc.openmanage 6.1.0

.. contents::
   :local:
   :depth: 1

.. Deprecated


Synopsis
--------

.. Description

- This module allows to configure the boot order settings.


.. Aliases


.. Requirements

.. _ansible_collections.dellemc.openmanage.idrac_boot_module_requirements:

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
        <div class="ansibleOptionAnchor" id="parameter-boot_options"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_boot_module__parameter-boot_options:

      .. rst-class:: ansible-option-title

      **boot_options**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-boot_options" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Options to enable or disable the boot devices.

      This is mutually exclusive with \ :emphasis:`boot\_order`\ , \ :emphasis:`boot\_source\_override\_mode`\ , \ :emphasis:`boot\_source\_override\_enabled`\  \ :emphasis:`boot\_source\_override\_target`\ , and \ :emphasis:`uefi\_target\_boot\_source\_override`\ .


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-boot_options/boot_option_reference"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_boot_module__parameter-boot_options/boot_option_reference:

      .. rst-class:: ansible-option-title

      **boot_option_reference**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-boot_options/boot_option_reference" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      FQDD of the boot device.

      This is mutually exclusive with \ :emphasis:`display\_name`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-boot_options/display_name"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_boot_module__parameter-boot_options/display_name:

      .. rst-class:: ansible-option-title

      **display_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-boot_options/display_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Display name of the boot source device.

      This is mutually exclusive with \ :emphasis:`boot\_option\_reference`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-boot_options/enabled"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_boot_module__parameter-boot_options/enabled:

      .. rst-class:: ansible-option-title

      **enabled**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-boot_options/enabled" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enable or disable the boot device.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-boot_order"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_boot_module__parameter-boot_order:

      .. rst-class:: ansible-option-title

      **boot_order**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-boot_order" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      This option allows to set the boot devices in the required boot order sequences.

      This is mutually exclusive with \ :emphasis:`boot\_options`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-boot_source_override_enabled"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_boot_module__parameter-boot_source_override_enabled:

      .. rst-class:: ansible-option-title

      **boot_source_override_enabled**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-boot_source_override_enabled" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The state of the Boot Source Override feature.

      \ :literal:`disabled`\  The system boots normally.

      \ :literal:`once`\  The system boots (one time) to the \ :emphasis:`boot\_source\_override\_target`\ .

      \ :literal:`continuous`\  The system boots to the target specified in the \ :emphasis:`boot\_source\_override\_target`\  until this property is set to Disabled.

      The state is set to \ :literal:`once`\  for the one-time boot override and \ :literal:`continuous`\  for the remain-active-until—canceled override. If the state is set \ :literal:`once`\  or \ :literal:`continuous`\ , the value is reset to \ :literal:`disabled`\  after the \ :emphasis:`boot\_source\_override\_target`\  actions have completed successfully.

      Changes to this options do not alter the BIOS persistent boot order configuration.

      This is mutually exclusive with \ :emphasis:`boot\_options`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"continuous"`
      - :ansible-option-choices-entry:`"disabled"`
      - :ansible-option-choices-entry:`"once"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-boot_source_override_mode"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_boot_module__parameter-boot_source_override_mode:

      .. rst-class:: ansible-option-title

      **boot_source_override_mode**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-boot_source_override_mode" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The BIOS boot mode (either Legacy or UEFI) to be used when \ :emphasis:`boot\_source\_override\_target`\  boot source is booted from.

      \ :literal:`legacy`\  The system boot in non-UEFI(Legacy) boot mode to the \ :emphasis:`boot\_source\_override\_target`\ .

      \ :literal:`uefi`\  The system boot in UEFI boot mode to the \ :emphasis:`boot\_source\_override\_target`\ .

      This is mutually exclusive with \ :emphasis:`boot\_options`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"legacy"`
      - :ansible-option-choices-entry:`"uefi"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-boot_source_override_target"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_boot_module__parameter-boot_source_override_target:

      .. rst-class:: ansible-option-title

      **boot_source_override_target**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-boot_source_override_target" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The boot source override target device to use during the next boot instead of the normal boot device.

      \ :literal:`pxe`\  performs PXE boot from the primary NIC.

      \ :literal:`floppy`\ , \ :literal:`cd`\ , \ :literal:`hdd`\ , \ :literal:`sd\_card`\  performs boot from their devices respectively.

      \ :literal:`bios\_setup`\  performs boot into the native BIOS setup.

      \ :literal:`utilities`\  performs boot from the local utilities.

      \ :literal:`uefi\_target`\  performs boot from the UEFI device path found in \ :emphasis:`uefi\_target\_boot\_source\_override`\ .

      If the \ :emphasis:`boot\_source\_override\_target`\  is set to a value other than \ :literal:`none`\  then the \ :emphasis:`boot\_source\_override\_enabled`\  is automatically set to \ :literal:`once`\ .

      Changes to this options do not alter the BIOS persistent boot order configuration.

      This is mutually exclusive with \ :emphasis:`boot\_options`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"uefi\_http"`
      - :ansible-option-choices-entry:`"sd\_card"`
      - :ansible-option-choices-entry:`"uefi\_target"`
      - :ansible-option-choices-entry:`"utilities"`
      - :ansible-option-choices-entry:`"bios\_setup"`
      - :ansible-option-choices-entry:`"hdd"`
      - :ansible-option-choices-entry:`"cd"`
      - :ansible-option-choices-entry:`"floppy"`
      - :ansible-option-choices-entry:`"pxe"`
      - :ansible-option-choices-entry:`"none"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-ca_path"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_boot_module__parameter-ca_path:

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
        <div class="ansibleOptionAnchor" id="parameter-idrac_ip"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_boot_module__parameter-idrac_ip:

      .. rst-class:: ansible-option-title

      **idrac_ip**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-idrac_ip" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      iDRAC IP Address.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-idrac_password"></div>
        <div class="ansibleOptionAnchor" id="parameter-idrac_pwd"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_boot_module__parameter-idrac_password:
      .. _ansible_collections.dellemc.openmanage.idrac_boot_module__parameter-idrac_pwd:

      .. rst-class:: ansible-option-title

      **idrac_password**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-idrac_password" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-aliases:`aliases: idrac_pwd`

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      iDRAC user password.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-idrac_port"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_boot_module__parameter-idrac_port:

      .. rst-class:: ansible-option-title

      **idrac_port**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-idrac_port" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      iDRAC port.


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`443`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-idrac_user"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_boot_module__parameter-idrac_user:

      .. rst-class:: ansible-option-title

      **idrac_user**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-idrac_user" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      iDRAC username.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-job_wait"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_boot_module__parameter-job_wait:

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

      This is applicable when \ :emphasis:`reset\_type`\  is \ :literal:`force\_reset`\  or \ :literal:`graceful\_reset`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry-default:`true` :ansible-option-choices-default-mark:`← (default)`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-job_wait_timeout"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_boot_module__parameter-job_wait_timeout:

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

      :ansible-option-default-bold:`Default:` :ansible-option-default:`900`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-reset_type"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_boot_module__parameter-reset_type:

      .. rst-class:: ansible-option-title

      **reset_type**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-reset_type" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      \ :literal:`none`\  Host system is not rebooted and \ :emphasis:`job\_wait`\  is not applicable.

      \ :literal:`force\_restart`\  Forcefully reboot the Host system.

      \ :literal:`graceful\_restart`\  Gracefully reboot the Host system.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`"graceful\_restart"` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`"force\_restart"`
      - :ansible-option-choices-entry:`"none"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-resource_id"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_boot_module__parameter-resource_id:

      .. rst-class:: ansible-option-title

      **resource_id**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-resource_id" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Redfish ID of the resource.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-timeout"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_boot_module__parameter-timeout:

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
        <div class="ansibleOptionAnchor" id="parameter-uefi_target_boot_source_override"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_boot_module__parameter-uefi_target_boot_source_override:

      .. rst-class:: ansible-option-title

      **uefi_target_boot_source_override**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-uefi_target_boot_source_override" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The UEFI device path of the device from which to boot when \ :emphasis:`boot\_source\_override\_target`\  is \ :literal:`uefi\_target`\ .

      \ :emphasis:`boot\_source\_override\_enabled`\  cannot be set to c(continuous) if \ :emphasis:`boot\_source\_override\_target`\  set to \ :literal:`uefi\_target`\  because this settings is defined in UEFI as a one-time-boot setting.

      Changes to this options do not alter the BIOS persistent boot order configuration.

      This is required if \ :emphasis:`boot\_source\_override\_target`\  is \ :literal:`uefi\_target`\ .

      This is mutually exclusive with \ :emphasis:`boot\_options`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-validate_certs"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_boot_module__parameter-validate_certs:

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
   - Run this module from a system that has direct access to Dell iDRAC.
   - This module supports \ :literal:`check\_mode`\ .

.. Seealso


.. Examples

Examples
--------

.. code-block:: yaml+jinja

    
    ---
    - name: Configure the system boot options settings.
      dellemc.openmanage.idrac_boot:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        boot_options:
          - display_name: Hard drive C
            enabled: true
          - boot_option_reference: NIC.PxeDevice.2-1
            enabled: true

    - name: Configure the boot order settings.
      dellemc.openmanage.idrac_boot:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        boot_order:
          - Boot0001
          - Boot0002
          - Boot0004
          - Boot0003

    - name: Configure the boot source override mode.
      dellemc.openmanage.idrac_boot:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        boot_source_override_mode: legacy
        boot_source_override_target: cd
        boot_source_override_enabled: once

    - name: Configure the UEFI target settings.
      dellemc.openmanage.idrac_boot:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        boot_source_override_mode: uefi
        boot_source_override_target: uefi_target
        uefi_target_boot_source_override: "VenHw(3A191845-5F86-4E78-8FCE-C4CFF59F9DAA)"

    - name: Configure the boot source override mode as pxe.
      dellemc.openmanage.idrac_boot:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        boot_source_override_mode: legacy
        boot_source_override_target: pxe
        boot_source_override_enabled: continuous




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
        <div class="ansibleOptionAnchor" id="return-boot"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_boot_module__return-boot:

      .. rst-class:: ansible-option-title

      **boot**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-boot" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Configured boot settings details.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` success

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"BootOptions": {"Description": "Collection of BootOptions", "Members": [{"BootOptionEnabled": false, "BootOptionReference": "HardDisk.List.1-1", "Description": "Current settings of the Legacy Boot option", "DisplayName": "Hard drive C:", "Id": "HardDisk.List.1-1", "Name": "Legacy Boot option", "UefiDevicePath": "VenHw(D6C0639F-C705-4EB9-AA4F-5802D8823DE6)"}], "Name": "Boot Options Collection"}, "BootOrder": ["HardDisk.List.1-1"], "BootSourceOverrideEnabled": "Disabled", "BootSourceOverrideMode": "Legacy", "BootSourceOverrideTarget": "None", "UefiTargetBootSourceOverride": null}`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-error_info"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_boot_module__return-error_info:

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
        <div class="ansibleOptionAnchor" id="return-job"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_boot_module__return-job:

      .. rst-class:: ansible-option-title

      **job**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-job" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Configured job details.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` success

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"ActualRunningStartTime": "2019-06-19T00:57:24", "ActualRunningStopTime": "2019-06-19T01:00:27", "CompletionTime": "2019-06-19T01:00:27", "Description": "Job Instance", "EndTime": "TIME\_NA", "Id": "JID\_609237056489", "JobState": "Completed", "JobType": "BIOSConfiguration", "Message": "Job completed successfully.", "MessageArgs": [], "MessageId": "PR19", "Name": "Configure: BIOS.Setup.1-1", "PercentComplete": 100, "StartTime": "2019-06-19T00:55:05", "TargetSettingsURI": null}`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-msg"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_boot_module__return-msg:

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

      Successfully updated the boot settings.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` success

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`"Successfully updated the boot settings."`


      .. raw:: html

        </div>



..  Status (Presently only deprecated)


.. Authors

Authors
~~~~~~~

- Felix Stephen (@felixs88)



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

