
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

.. _ansible_collections.dellemc.openmanage.ome_firmware_module:

.. Anchors: short name for ansible.builtin

.. Anchors: aliases



.. Title

dellemc.openmanage.ome_firmware module -- Update firmware on PowerEdge devices and its components through OpenManage Enterprise
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. Collection note

.. note::
    This module is part of the `dellemc.openmanage collection <https://galaxy.ansible.com/dellemc/openmanage>`_ (version 8.5.0).

    To install it, use: :code:`ansible-galaxy collection install dellemc.openmanage`.
    You need further requirements to be able to use this module,
    see :ref:`Requirements <ansible_collections.dellemc.openmanage.ome_firmware_module_requirements>` for details.

    To use it in a playbook, specify: :code:`dellemc.openmanage.ome_firmware`.

.. version_added

.. rst-class:: ansible-version-added

New in dellemc.openmanage 2.0.0

.. contents::
   :local:
   :depth: 1

.. Deprecated


Synopsis
--------

.. Description

- This module updates the firmware of PowerEdge devices and all its components through OpenManage Enterprise.


.. Aliases


.. Requirements

.. _ansible_collections.dellemc.openmanage.ome_firmware_module_requirements:

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
        <div class="ansibleOptionAnchor" id="parameter-baseline_name"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_module__parameter-baseline_name:

      .. rst-class:: ansible-option-title

      **baseline_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-baseline_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Enter the baseline name to update the firmware of all devices or list of devices that are not complaint.

      This option is mutually exclusive with \ :emphasis:`dup\_file`\  and \ :emphasis:`device\_group\_names`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-ca_path"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_module__parameter-ca_path:

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
        <div class="ansibleOptionAnchor" id="parameter-components"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_module__parameter-components:

      .. rst-class:: ansible-option-title

      **components**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-components" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      List of components to be updated.

      If not provided, all components applicable are considered.

      This option is case sensitive.

      This is applicable to \ :emphasis:`device\_service\_tag`\ , \ :emphasis:`device\_id`\ , and \ :emphasis:`baseline\_name`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`[]`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-device_group_names"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_module__parameter-device_group_names:

      .. rst-class:: ansible-option-title

      **device_group_names**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-device_group_names" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Enter the name of the device group that contains the devices on which firmware needs to be updated.

      This option is mutually exclusive with \ :emphasis:`device\_id`\  and \ :emphasis:`device\_service\_tag`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-device_id"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_module__parameter-device_id:

      .. rst-class:: ansible-option-title

      **device_id**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-device_id" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      List of ids of the targeted device.

      Either \ :emphasis:`device\_id`\  or \ :emphasis:`device\_service\_tag`\  can be used individually or together.

      This option is mutually exclusive with \ :emphasis:`device\_group\_names`\  and \ :emphasis:`devices`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-device_service_tag"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_module__parameter-device_service_tag:

      .. rst-class:: ansible-option-title

      **device_service_tag**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-device_service_tag" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      List of service tags of the targeted devices.

      Either \ :emphasis:`device\_id`\  or \ :emphasis:`device\_service\_tag`\  can be used individually or together.

      This option is mutually exclusive with \ :emphasis:`device\_group\_names`\  and \ :emphasis:`devices`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-devices"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_module__parameter-devices:

      .. rst-class:: ansible-option-title

      **devices**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-devices" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      This option allows to select components on each device for firmware update.

      This option is mutually exclusive with \ :emphasis:`dup\_file`\ , \ :emphasis:`device\_group\_names`\ , \ :emphasis:`device\_id`\ , and \ :emphasis:`device\_service\_tag`\ .


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-devices/components"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_module__parameter-devices/components:

      .. rst-class:: ansible-option-title

      **components**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-devices/components" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The target components to be updated. If not specified, all applicable device components are considered.


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`[]`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-devices/id"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_module__parameter-devices/id:

      .. rst-class:: ansible-option-title

      **id**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-devices/id" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The id of the target device to be updated.

      This option is mutually exclusive with \ :emphasis:`service\_tag`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-devices/service_tag"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_module__parameter-devices/service_tag:

      .. rst-class:: ansible-option-title

      **service_tag**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-devices/service_tag" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The service tag of the target device to be updated.

      This option is mutually exclusive with \ :emphasis:`id`\ .


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-dup_file"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_module__parameter-dup_file:

      .. rst-class:: ansible-option-title

      **dup_file**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-dup_file" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`path`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The path of the Dell Update Package (DUP) file that contains the firmware or drivers required to update the target system device or individual device components.

      This is mutually exclusive with \ :emphasis:`baseline\_name`\ , \ :emphasis:`components`\ , and \ :emphasis:`devices`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-hostname"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_module__parameter-hostname:

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
        <div class="ansibleOptionAnchor" id="parameter-password"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_module__parameter-password:

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

      .. _ansible_collections.dellemc.openmanage.ome_firmware_module__parameter-port:

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
        <div class="ansibleOptionAnchor" id="parameter-reboot_type"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_module__parameter-reboot_type:

      .. rst-class:: ansible-option-title

      **reboot_type**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-reboot_type" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      :ansible-option-versionadded:`added in dellemc.openmanage 8.3.0`


      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      This option provides the choices to reboot the server immediately after the firmware update.

      This is applicable when \ :emphasis:`schedule`\  is \ :literal:`RebootNow`\ .

      \ :literal:`GracefulRebootForce`\  performs a graceful reboot with forced shutdown.

      \ :literal:`GracefulReboot`\  performs a graceful reboot without forced shutdown.

      \ :literal:`PowerCycle`\  performs a power cycle for a hard reset on the device.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"GracefulReboot"`
      - :ansible-option-choices-entry-default:`"GracefulRebootForce"` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`"PowerCycle"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-schedule"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_module__parameter-schedule:

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

      Select the schedule for the firmware update.

      if \ :literal:`StageForNextReboot`\  is chosen, the firmware will be staged and updated during the next reboot of the target device.

      if \ :literal:`RebootNow`\  will apply the firmware updates immediately.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`"RebootNow"` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`"StageForNextReboot"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-timeout"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_module__parameter-timeout:

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

      .. _ansible_collections.dellemc.openmanage.ome_firmware_module__parameter-username:

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

      .. _ansible_collections.dellemc.openmanage.ome_firmware_module__parameter-validate_certs:

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
    - name: Update firmware from DUP file using device ids
      dellemc.openmanage.ome_firmware:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        device_id:
          - 11111
          - 22222
        dup_file: "/path/Chassis-System-Management_Firmware_6N9WN_WN64_1.00.01_A00.EXE"

    - name: Update firmware from a DUP file using a device service tags
      dellemc.openmanage.ome_firmware:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        device_service_tag:
          - KLBR111
          - KLBR222
        dup_file: "/path/Network_Firmware_NTRW0_WN64_14.07.07_A00-00_01.EXE"

    - name: Update firmware from a DUP file using a device group names
      dellemc.openmanage.ome_firmware:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        device_group_names:
          - servers
        dup_file: "/path/BIOS_87V69_WN64_2.4.7.EXE"

    - name: Update firmware using baseline name
      dellemc.openmanage.ome_firmware:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        baseline_name: baseline_devices

    - name: Stage firmware for the next reboot using baseline name
      dellemc.openmanage.ome_firmware:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        baseline_name: baseline_devices
        schedule: StageForNextReboot

    - name: "Update firmware using baseline name and components."
      dellemc.openmanage.ome_firmware:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        baseline_name: baseline_devices
        components:
          - BIOS

    - name: Update firmware of device components from a DUP file using a device ids in a baseline
      dellemc.openmanage.ome_firmware:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        baseline_name: baseline_devices
        device_id:
          - 11111
          - 22222
        components:
          - iDRAC with Lifecycle Controller

    - name: Update firmware of device components from a baseline using a device service tags under a baseline
      dellemc.openmanage.ome_firmware:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        baseline_name: baseline_devices
        device_service_tag:
          - KLBR111
          - KLBR222
        components:
          - IOM-SAS

    - name: Update firmware using baseline name with a device id and required components
      dellemc.openmanage.ome_firmware:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        baseline_name: baseline_devices
        devices:
          - id: 12345
            components:
              - Lifecycle Controller
          - id: 12346
            components:
              - Enterprise UEFI Diagnostics
              - BIOS

    - name: "Update firmware using baseline name with a device service tag and required components."
      dellemc.openmanage.ome_firmware:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        baseline_name: baseline_devices
        devices:
          - service_tag: ABCDE12
            components:
              - PERC H740P Adapter
              - BIOS
          - service_tag: GHIJK34
            components:
              - OS Drivers Pack

    - name: "Update firmware using baseline name with a device service tag or device id and required components."
      dellemc.openmanage.ome_firmware:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        baseline_name: baseline_devices
        devices:
          - service_tag: ABCDE12
            components:
              - BOSS-S1 Adapter
              - PowerEdge Server BIOS
          - id: 12345
            components:
              - iDRAC with Lifecycle Controller

    - name: "Update firmware using baseline name and components and perform Powercycle."
      dellemc.openmanage.ome_firmware:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        baseline_name: baseline_devices
        components:
          - BIOS
        reboot_type: PowerCycle




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

      .. _ansible_collections.dellemc.openmanage.ome_firmware_module__return-error_info:

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
        <div class="ansibleOptionAnchor" id="return-msg"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_module__return-msg:

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

      Overall firmware update status.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` always

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`"Successfully submitted the firmware update job."`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-update_status"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_module__return-update_status:

      .. rst-class:: ansible-option-title

      **update_status**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-update_status" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The firmware update job and progress details from the OME.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` success

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"Builtin": false, "CreatedBy": "user", "Editable": true, "EndTime": "None", "Id": 11117, "JobDescription": "dup test", "JobName": "Firmware Update Task", "JobStatus": {"Id": 1111, "Name": "New"}, "JobType": {"Id": 5, "Internal": false, "Name": "Update\_Task"}, "LastRun": "None", "LastRunStatus": {"Id": 1111, "Name": "NotRun"}, "NextRun": "None", "Params": [{"JobId": 11111, "Key": "signVerify", "Value": "true"}, {"JobId": 11112, "Key": "stagingValue", "Value": "false"}, {"JobId": 11113, "Key": "complianceUpdate", "Value": "false"}, {"JobId": 11114, "Key": "operationName", "Value": "INSTALL\_FIRMWARE"}], "Schedule": "startnow", "StartTime": "None", "State": "Enabled", "Targets": [{"Data": "DCIM:INSTALLED#701\_\_NIC.Mezzanine.1A-1-1=1234567654321", "Id": 11115, "JobId": 11116, "TargetType": {"Id": 1000, "Name": "DEVICE"}}], "UpdatedBy": "None", "Visible": true}`


      .. raw:: html

        </div>



..  Status (Presently only deprecated)


.. Authors

Authors
~~~~~~~

- Felix Stephen (@felixs88)
- Jagadeesh N V (@jagadeeshnv)
- Abhishek Sinha (@ABHISHEK-SINHA10)



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

