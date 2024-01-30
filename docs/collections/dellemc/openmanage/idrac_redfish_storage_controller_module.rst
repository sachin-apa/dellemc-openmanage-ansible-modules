
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

.. _ansible_collections.dellemc.openmanage.idrac_redfish_storage_controller_module:

.. Anchors: short name for ansible.builtin

.. Anchors: aliases



.. Title

dellemc.openmanage.idrac_redfish_storage_controller module -- Configures the physical disk, virtual disk, and storage controller settings
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. Collection note

.. note::
    This module is part of the `dellemc.openmanage collection <https://galaxy.ansible.com/dellemc/openmanage>`_ (version 8.5.0).

    To install it, use: :code:`ansible-galaxy collection install dellemc.openmanage`.
    You need further requirements to be able to use this module,
    see :ref:`Requirements <ansible_collections.dellemc.openmanage.idrac_redfish_storage_controller_module_requirements>` for details.

    To use it in a playbook, specify: :code:`dellemc.openmanage.idrac_redfish_storage_controller`.

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

- This module allows the users to configure the settings of the physical disk, virtual disk, and storage controller.


.. Aliases


.. Requirements

.. _ansible_collections.dellemc.openmanage.idrac_redfish_storage_controller_module_requirements:

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
        <div class="ansibleOptionAnchor" id="parameter-apply_time"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_redfish_storage_controller_module__parameter-apply_time:

      .. rst-class:: ansible-option-title

      **apply_time**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-apply_time" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Apply time of the \ :emphasis:`attributes`\ .

      This is applicable only to \ :emphasis:`attributes`\ .

      \ :literal:`Immediate`\  Allows the user to immediately reboot the host and apply the changes. \ :emphasis:`job\_wait`\  is applicable.

      \ :literal:`OnReset`\  Allows the user to apply the changes on the next reboot of the host server.

      \ :literal:`AtMaintenanceWindowStart`\  Allows the user to apply at the start of a maintenance window as specified in \ :emphasis:`maintenance\_window`\ .

      \ :literal:`InMaintenanceWindowOnReset`\  Allows to apply after a manual reset but within the maintenance window as specified in \ :emphasis:`maintenance\_window`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`"Immediate"` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`"OnReset"`
      - :ansible-option-choices-entry:`"AtMaintenanceWindowStart"`
      - :ansible-option-choices-entry:`"InMaintenanceWindowOnReset"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-attributes"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_redfish_storage_controller_module__parameter-attributes:

      .. rst-class:: ansible-option-title

      **attributes**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-attributes" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Dictionary of controller attributes and value pair.

      This feature is only supported for iDRAC9 with firmware version 6.00.00.00 and above

      \ :emphasis:`controller\_id`\  is required for this operation.

      \ :emphasis:`apply\_time`\  and \ :emphasis:`maintenance\_window`\  is applicable for \ :emphasis:`attributes`\ .

      \ :emphasis:`attributes`\  is mutually exclusive with \ :emphasis:`command`\ .

      Use \ https://I%28idrac_ip\ /redfish/v1/Schemas/DellOemStorageController.json) to view the attributes.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-baseuri"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_redfish_storage_controller_module__parameter-baseuri:

      .. rst-class:: ansible-option-title

      **baseuri**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-baseuri" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      IP address of the target out-of-band controller. For example- \<ipaddress\>:\<port\>.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-ca_path"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_redfish_storage_controller_module__parameter-ca_path:

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
        <div class="ansibleOptionAnchor" id="parameter-command"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_redfish_storage_controller_module__parameter-command:

      .. rst-class:: ansible-option-title

      **command**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-command" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      These actions may require a system reset, depending on the capabilities of the controller.

      \ :literal:`ResetConfig`\  - Deletes all the virtual disks and unassigns all hot spares on physical disks. \ :emphasis:`controller\_id`\  is required for this operation.

      \ :literal:`AssignSpare`\  - Assigns a physical disk as a dedicated or global hot spare for a virtual disk. \ :emphasis:`target`\  is required for this operation.

      \ :literal:`SetControllerKey`\  - Sets the key on controllers, which is used to encrypt the drives in Local Key Management(LKM). \ :emphasis:`controller\_id`\ , \ :emphasis:`key`\ , and \ :emphasis:`key\_id`\  are required for this operation.

      \ :literal:`RemoveControllerKey`\  - Deletes the encryption key on the controller. \ :emphasis:`controller\_id`\  is required for this operation.

      \ :literal:`ReKey`\  - Resets the key on the controller and it always reports as changes found when check mode is enabled. \ :emphasis:`controller\_id`\ , \ :emphasis:`old\_key`\ , \ :emphasis:`key\_id`\ , and \ :emphasis:`key`\  is required for this operation.

      \ :literal:`UnassignSpare`\  - To unassign the Global or Dedicated hot spare. \ :emphasis:`target`\  is required for this operation.

      \ :literal:`EnableControllerEncryption`\  - To enable Local Key Management (LKM) or Secure Enterprise Key Manager (SEKM) on controllers that support encryption of the drives. \ :emphasis:`controller\_id`\ , \ :emphasis:`key`\ , and \ :emphasis:`key\_id`\  are required for this operation.

      \ :literal:`BlinkTarget`\  - Blinks the target virtual drive or physical disk and it always reports as changes found when check mode is enabled. \ :emphasis:`target`\  or \ :emphasis:`volume\_id`\  is required for this operation.

      \ :literal:`UnBlinkTarget`\  - Unblink the target virtual drive or physical disk and and it always reports as changes found when check mode is enabled. \ :emphasis:`target`\  or \ :emphasis:`volume\_id`\  is required for this operation.

      \ :literal:`ConvertToRAID`\  - Converts the disk form non-Raid to Raid. \ :emphasis:`target`\  is required for this operation.

      \ :literal:`ConvertToNonRAID`\  - Converts the disk form Raid to non-Raid. \ :emphasis:`target`\  is required for this operation.

      \ :literal:`ChangePDStateToOnline`\  - To set the disk status to online. \ :emphasis:`target`\  is required for this operation.

      \ :literal:`ChangePDStateToOffline`\  - To set the disk status to offline. \ :emphasis:`target`\  is required for this operation.

      \ :literal:`LockVirtualDisk`\  - To encrypt the virtual disk. \ :emphasis:`volume\_id`\  is required for this operation.

      \ :literal:`OnlineCapacityExpansion`\  - To expand the size of virtual disk. \ :emphasis:`volume\_id`\ , and \ :emphasis:`target`\  or \ :emphasis:`size`\  is required for this operation.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"ResetConfig"`
      - :ansible-option-choices-entry:`"AssignSpare"`
      - :ansible-option-choices-entry:`"SetControllerKey"`
      - :ansible-option-choices-entry:`"RemoveControllerKey"`
      - :ansible-option-choices-entry:`"ReKey"`
      - :ansible-option-choices-entry:`"UnassignSpare"`
      - :ansible-option-choices-entry:`"EnableControllerEncryption"`
      - :ansible-option-choices-entry:`"BlinkTarget"`
      - :ansible-option-choices-entry:`"UnBlinkTarget"`
      - :ansible-option-choices-entry:`"ConvertToRAID"`
      - :ansible-option-choices-entry:`"ConvertToNonRAID"`
      - :ansible-option-choices-entry:`"ChangePDStateToOnline"`
      - :ansible-option-choices-entry:`"ChangePDStateToOffline"`
      - :ansible-option-choices-entry:`"LockVirtualDisk"`
      - :ansible-option-choices-entry:`"OnlineCapacityExpansion"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-controller_id"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_redfish_storage_controller_module__parameter-controller_id:

      .. rst-class:: ansible-option-title

      **controller_id**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-controller_id" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Fully Qualified Device Descriptor (FQDD) of the storage controller. For example-'RAID.Slot.1-1'.

      This option is mandatory when \ :emphasis:`command`\  is \ :literal:`ResetConfig`\ , \ :literal:`SetControllerKey`\ , \ :literal:`RemoveControllerKey`\ , \ :literal:`ReKey`\ , or \ :literal:`EnableControllerEncryption`\ .

      This option is mandatory for \ :emphasis:`attributes`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-job_wait"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_redfish_storage_controller_module__parameter-job_wait:

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

      Provides the option if the module has to wait for the job to be completed.

      This is applicable for \ :emphasis:`attributes`\  when \ :emphasis:`apply\_time`\  is \ :literal:`Immediate`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`false` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-job_wait_timeout"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_redfish_storage_controller_module__parameter-job_wait_timeout:

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

      The maximum wait time of job completion in seconds before the job tracking is stopped.

      This option is applicable when \ :emphasis:`job\_wait`\  is \ :literal:`true`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`120`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-key"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_redfish_storage_controller_module__parameter-key:

      .. rst-class:: ansible-option-title

      **key**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-key" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      A new security key passphrase that the encryption-capable controller uses to create the encryption key. The controller uses the encryption key to lock or unlock access to the Self-Encrypting Drive (SED). Only one encryption key can be created for each controller.

      This is mandatory when \ :emphasis:`command`\  is \ :literal:`SetControllerKey`\ , \ :literal:`ReKey`\ , or \ :literal:`EnableControllerEncryption`\  and when \ :emphasis:`mode`\  is \ :literal:`LKM`\ .

      The length of the key can be a maximum of 32 characters in length, where the expanded form of the special character is counted as a single character.

      The key must contain at least one character from each of the character classes: uppercase, lowercase, number, and special character.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-key_id"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_redfish_storage_controller_module__parameter-key_id:

      .. rst-class:: ansible-option-title

      **key_id**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-key_id" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      This is a user supplied text label associated with the passphrase.

      This is mandatory when \ :emphasis:`command`\  is \ :literal:`SetControllerKey`\ , \ :literal:`ReKey`\ , or \ :literal:`EnableControllerEncryption`\  and when \ :emphasis:`mode`\  is \ :literal:`LKM`\ .

      The length of \ :emphasis:`key\_id`\  can be a maximum of 32 characters in length and should not have any spaces.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-maintenance_window"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_redfish_storage_controller_module__parameter-maintenance_window:

      .. rst-class:: ansible-option-title

      **maintenance_window**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-maintenance_window" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Option to schedule the maintenance window.

      This is required when \ :emphasis:`apply\_time`\  is \ :literal:`AtMaintenanceWindowStart`\  or \ :literal:`InMaintenanceWindowOnReset`\ .


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-maintenance_window/duration"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_redfish_storage_controller_module__parameter-maintenance_window/duration:

      .. rst-class:: ansible-option-title

      **duration**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-maintenance_window/duration" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The duration in seconds for the maintenance window.


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`900`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-maintenance_window/start_time"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_redfish_storage_controller_module__parameter-maintenance_window/start_time:

      .. rst-class:: ansible-option-title

      **start_time**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-maintenance_window/start_time" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The start time for the maintenance window to be scheduled.

      The format is YYYY-MM-DDThh:mm:ss\<offset\>

      \<offset\> is the time offset from UTC that the current timezone set in iDRAC in the format: +05:30 for IST.


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-mode"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_redfish_storage_controller_module__parameter-mode:

      .. rst-class:: ansible-option-title

      **mode**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-mode" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Encryption mode of the encryption capable controller.

      This option is applicable only when \ :emphasis:`command`\  is \ :literal:`ReKey`\  or \ :literal:`EnableControllerEncryption`\ .

      \ :literal:`SEKM`\  requires secure enterprise key manager license on the iDRAC.

      \ :literal:`LKM`\  to choose mode as local key mode.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`"LKM"` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`"SEKM"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-old_key"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_redfish_storage_controller_module__parameter-old_key:

      .. rst-class:: ansible-option-title

      **old_key**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-old_key" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Security key passphrase used by the encryption-capable controller.

      This option is mandatory when \ :emphasis:`command`\  is \ :literal:`ReKey`\  and \ :emphasis:`mode`\  is \ :literal:`LKM`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-password"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_redfish_storage_controller_module__parameter-password:

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

      Password of the target out-of-band controller.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-size"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_redfish_storage_controller_module__parameter-size:

      .. rst-class:: ansible-option-title

      **size**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-size" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Capacity of the virtual disk to be expanded in MB.

      Check mode and Idempotency is not supported for \ :emphasis:`size`\ .

      Minimum Online Capacity Expansion size must be greater than 100 MB of the current size.

      When \ :emphasis:`command`\  is \ :literal:`OnlineCapacityExpansion`\ , then \ :emphasis:`size`\  is mutually exclusive with \ :emphasis:`target`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-target"></div>
        <div class="ansibleOptionAnchor" id="parameter-drive_id"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_redfish_storage_controller_module__parameter-drive_id:
      .. _ansible_collections.dellemc.openmanage.idrac_redfish_storage_controller_module__parameter-target:

      .. rst-class:: ansible-option-title

      **target**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-target" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-aliases:`aliases: drive_id`

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Fully Qualified Device Descriptor (FQDD) of the target physical drive.

      This is mandatory when \ :emphasis:`command`\  is \ :literal:`AssignSpare`\ , \ :literal:`UnassisgnSpare`\ , \ :literal:`ChangePDStateToOnline`\ , \ :literal:`ChangePDStateToOffline`\ , \ :literal:`ConvertToRAID`\ , or \ :literal:`ConvertToNonRAID`\ .

      If \ :emphasis:`volume\_id`\  is not specified or empty, this physical drive will be assigned as a global hot spare when \ :emphasis:`command`\  is \ :literal:`AssignSpare`\ .

      When \ :emphasis:`command`\  is \ :literal:`OnlineCapacityExpansion`\ , then \ :emphasis:`target`\  is mutually exclusive with \ :emphasis:`size`\ .

      Notes: Global or Dedicated hot spare can be assigned only once for a physical disk, Re-assign cannot be done when \ :emphasis:`command`\  is \ :literal:`AssignSpare`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-timeout"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_redfish_storage_controller_module__parameter-timeout:

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

      .. _ansible_collections.dellemc.openmanage.idrac_redfish_storage_controller_module__parameter-username:

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

      Username of the target out-of-band controller.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-validate_certs"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_redfish_storage_controller_module__parameter-validate_certs:

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

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-volume_id"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_redfish_storage_controller_module__parameter-volume_id:

      .. rst-class:: ansible-option-title

      **volume_id**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-volume_id" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Fully Qualified Device Descriptor (FQDD) of the volume.

      Applicable if \ :emphasis:`command`\  is \ :literal:`AssignSpare`\ , \ :literal:`BlinkTarget`\ , \ :literal:`UnBlinkTarget`\  or \ :literal:`LockVirtualDisk`\ .

      \ :emphasis:`volume\_id`\  or \ :emphasis:`target`\  is required when the \ :emphasis:`command`\  is \ :literal:`BlinkTarget`\  or \ :literal:`UnBlinkTarget`\ , if both are specified \ :emphasis:`target`\  is considered.

      To know the number of volumes to which a hot spare can be assigned, refer iDRAC Redfish API documentation.


      .. raw:: html

        </div>


.. Attributes


.. Notes

Notes
-----

.. note::
   - Run this module from a system that has direct access to Dell iDRAC.
   - This module is supported on iDRAC9.
   - This module always reports as changes found when \ :emphasis:`command`\  is \ :literal:`ReKey`\ , \ :literal:`BlinkTarget`\ , and \ :literal:`UnBlinkTarget`\ .
   - This module supports \ :literal:`check\_mode`\ .

.. Seealso


.. Examples

Examples
--------

.. code-block:: yaml+jinja

    
    ---
    - name: Assign dedicated hot spare
      dellemc.openmanage.idrac_redfish_storage_controller:
        baseuri: "192.168.0.1:443"
        username: "user_name"
        password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        volume_id:
          - "Disk.Virtual.0:RAID.Slot.1-1"
        target: "Disk.Bay.0:Enclosure.Internal.0-1:RAID.Slot.1-1"
      tags:
        - assign_dedicated_hot_spare

    - name: Assign global hot spare
      dellemc.openmanage.idrac_redfish_storage_controller:
        baseuri: "192.168.0.1:443"
        username: "user_name"
        password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        target: "Disk.Bay.0:Enclosure.Internal.0-1:RAID.Slot.1-1"
      tags:
        - assign_global_hot_spare

    - name: Unassign hot spare
      dellemc.openmanage.idrac_redfish_storage_controller:
        baseuri: "192.168.0.1:443"
        username: "user_name"
        password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        target: "Disk.Bay.0:Enclosure.Internal.0-1:RAID.Slot.1-1"
        command: UnassignSpare
      tags:
        - un-assign-hot-spare

    - name: Set controller encryption key
      dellemc.openmanage.idrac_redfish_storage_controller:
        baseuri: "192.168.0.1:443"
        username: "user_name"
        password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        command: "SetControllerKey"
        controller_id: "RAID.Slot.1-1"
        key: "PassPhrase@123"
        key_id: "mykeyid123"
      tags:
        - set_controller_key

    - name: Rekey in LKM mode
      dellemc.openmanage.idrac_redfish_storage_controller:
        baseuri: "192.168.0.1:443"
        username: "user_name"
        password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        command: "ReKey"
        controller_id: "RAID.Slot.1-1"
        key: "NewPassPhrase@123"
        key_id: "newkeyid123"
        old_key: "OldPassPhrase@123"
      tags:
        - rekey_lkm

    - name: Rekey in SEKM mode
      dellemc.openmanage.idrac_redfish_storage_controller:
        baseuri: "192.168.0.1:443"
        username: "user_name"
        password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        command: "ReKey"
        controller_id: "RAID.Slot.1-1"
        mode: "SEKM"
      tags:
        - rekey_sekm

    - name: Remove controller key
      dellemc.openmanage.idrac_redfish_storage_controller:
        baseuri: "192.168.0.1:443"
        username: "user_name"
        password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        command: "RemoveControllerKey"
        controller_id: "RAID.Slot.1-1"
      tags:
        - remove_controller_key

    - name: Reset controller configuration
      dellemc.openmanage.idrac_redfish_storage_controller:
        baseuri: "192.168.0.1:443"
        username: "user_name"
        password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        command: "ResetConfig"
        controller_id: "RAID.Slot.1-1"
      tags:
        - reset_config

    - name: Enable controller encryption
      idrac_redfish_storage_controller:
        baseuri: "{{ baseuri }}"
        username: "{{ username }}"
        password: "{{ password }}"
        ca_path: "/path/to/ca_cert.pem"
        command: "EnableControllerEncryption"
        controller_id: "RAID.Slot.1-1"
        mode: "LKM"
        key: "your_Key@123"
        key_id: "your_Keyid@123"
      tags:
        - enable-encrypt

    - name: Blink physical disk.
      dellemc.openmanage.idrac_redfish_storage_controller:
        baseuri: "192.168.0.1:443"
        username: "user_name"
        password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        command: BlinkTarget
        target: "Disk.Bay.0:Enclosure.Internal.0-1:RAID.Slot.1-1"
      tags:
        - blink-target

    - name: Blink virtual drive.
      dellemc.openmanage.idrac_redfish_storage_controller:
        baseuri: "192.168.0.1:443"
        username: "user_name"
        password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        command: BlinkTarget
        volume_id: "Disk.Virtual.0:RAID.Slot.1-1"
      tags:
        - blink-volume

    - name: Unblink physical disk.
      dellemc.openmanage.idrac_redfish_storage_controller:
        baseuri: "192.168.0.1:443"
        username: "user_name"
        password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        command: UnBlinkTarget
        target: "Disk.Bay.0:Enclosure.Internal.0-1:RAID.Slot.1-1"
      tags:
        - unblink-target

    - name: Unblink virtual drive.
      dellemc.openmanage.idrac_redfish_storage_controller:
        baseuri: "192.168.0.1:443"
        username: "user_name"
        password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        command: UnBlinkTarget
        volume_id: "Disk.Virtual.0:RAID.Slot.1-1"
      tags:
        - unblink-drive

    - name: Convert physical disk to RAID
      dellemc.openmanage.idrac_redfish_storage_controller:
        baseuri: "192.168.0.1:443"
        username: "user_name"
        password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        command: "ConvertToRAID"
        target: "Disk.Bay.0:Enclosure.Internal.0-1:RAID.Slot.1-1"
      tags:
        - convert-raid

    - name: Convert physical disk to non-RAID
      dellemc.openmanage.idrac_redfish_storage_controller:
        baseuri: "192.168.0.1:443"
        username: "user_name"
        password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        command: "ConvertToNonRAID"
        target: "Disk.Bay.0:Enclosure.Internal.0-1:RAID.Slot.1-1"
      tags:
        - convert-non-raid

    - name: Change physical disk state to online.
      dellemc.openmanage.idrac_redfish_storage_controller:
        baseuri: "192.168.0.1:443"
        username: "user_name"
        password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        command: "ChangePDStateToOnline"
        target: "Disk.Bay.1:Enclosure.Internal.0-1:RAID.Slot.1-1"
      tags:
        - pd-state-online

    - name: Change physical disk state to offline.
      dellemc.openmanage.idrac_redfish_storage_controller:
        baseuri: "192.168.0.1:443"
        username: "user_name"
        password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        command: "ChangePDStateToOnline"
        target: "Disk.Bay.1:Enclosure.Internal.0-1:RAID.Slot.1-1"
      tags:
        - pd-state-offline

    - name: Lock virtual drive
      dellemc.openmanage.idrac_redfish_storage_controller:
        baseuri: "192.168.0.1:443"
        username: "user_name"
        password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        command: "LockVirtualDisk"
        volume_id: "Disk.Virtual.0:RAID.SL.3-1"
      tags:
        - lock

    - name: Online Capacity Expansion of a volume using target
      dellemc.openmanage.idrac_redfish_storage_controller:
        baseuri: "{{ baseuri }}"
        username: "{{ username }}"
        password: "{{ password }}"
        ca_path: "/path/to/ca_cert.pem"
        command: "OnlineCapacityExpansion"
        volume_id: "Disk.Virtual.0:RAID.Integrated.1-1"
        target:
          - "Disk.Bay.2:Enclosure.Internal.0-0:RAID.Integrated.1-1"
      tags:
        - oce_target

    - name: Online Capacity Expansion of a volume using size
      dellemc.openmanage.idrac_redfish_storage_controller:
        baseuri: "{{ baseuri }}"
        username: "{{ username }}"
        password: "{{ password }}"
        ca_path: "/path/to/ca_cert.pem"
        command: "OnlineCapacityExpansion"
        volume_id: "Disk.Virtual.0:RAID.Integrated.1-1"
        size: 362785
      tags:
        - oce_size

    - name: Set controller attributes.
      dellemc.openmanage.idrac_redfish_storage_controller:
        baseuri: "192.168.0.1:443"
        username: "user_name"
        password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        controller_id: "RAID.Slot.1-1"
        attributes:
          ControllerMode: "HBA"
        apply_time: "OnReset"
      tags:
        - controller-attribute

    - name: Configure controller attributes at Maintenance window
      dellemc.openmanage.idrac_redfish_storage_controller:
        baseuri: "192.168.0.1:443"
        username: "user_name"
        password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        controller_id: "RAID.Slot.1-1"
        attributes:
          CheckConsistencyMode: Normal
          CopybackMode: "Off"
          LoadBalanceMode: Disabled
        apply_time: AtMaintenanceWindowStart
        maintenance_window:
          start_time: "2022-09-30T05:15:40-05:00"
          duration: 1200




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

      .. _ansible_collections.dellemc.openmanage.idrac_redfish_storage_controller_module__return-error_info:

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

      Details of a http error.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` on http error

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"error": {"@Message.ExtendedInfo": [{"Message": "Unable to run the method because the requested HTTP method is not allowed.", "MessageArgs": [], "MessageArgs@odata.count": 0, "MessageId": "iDRAC.1.6.SYS402", "RelatedProperties": [], "RelatedProperties@odata.count": 0, "Resolution": "Enter a valid HTTP method and retry the operation. For information about valid methods, see the Redfish Users Guide available on the support site.", "Severity": "Informational"}], "code": "Base.1.0.GeneralError", "message": "A general error has occurred. See ExtendedInfo for more information"}}`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-msg"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_redfish_storage_controller_module__return-msg:

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

      Overall status of the storage controller configuration operation.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` always

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`"Successfully submitted the job that performs the AssignSpare operation"`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-status"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_redfish_storage_controller_module__return-status:

      .. rst-class:: ansible-option-title

      **status**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-status" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      status of the submitted job.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` always

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"ActualRunningStartTime": "2022-02-09T04:42:41", "ActualRunningStopTime": "2022-02-09T04:44:00", "CompletionTime": "2022-02-09T04:44:00", "Description": "Job Instance", "EndTime": "TIME\_NA", "Id": "JID\_444033604418", "JobState": "Completed", "JobType": "RealTimeNoRebootConfiguration", "Message": "Job completed successfully.", "MessageArgs": [], "MessageId": "PR19", "Name": "Configure: RAID.Integrated.1-1", "PercentComplete": 100, "StartTime": "2022-02-09T04:42:40", "TargetSettingsURI": null}`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-task"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_redfish_storage_controller_module__return-task:

      .. rst-class:: ansible-option-title

      **task**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-task" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      ID and URI resource of the job created.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` success

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"id": "JID\_XXXXXXXXXXXXX", "uri": "/redfish/v1/Managers/iDRAC.Embedded.1/Jobs/JID\_XXXXXXXXXXXXX"}`


      .. raw:: html

        </div>



..  Status (Presently only deprecated)


.. Authors

Authors
~~~~~~~

- Jagadeesh N V (@jagadeeshnv)
- Felix Stephen (@felixs88)
- Husniya Hameed (@husniya_hameed)
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

