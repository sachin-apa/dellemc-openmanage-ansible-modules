
.. Document meta

:orphan:

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

.. Anchors

.. _ansible_collections.dellemc.openmanage.idrac_storage_controller_role:

.. Anchors: aliases


.. Title

dellemc.openmanage.idrac_storage_controller role -- Configures the physical disk, virtual disk, and storage controller settings
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. Collection note

.. note::
    This role is part of the `dellemc.openmanage collection <https://galaxy.ansible.com/dellemc/openmanage>`_ (version 8.5.0).

    To install it use: :code:`ansible-galaxy collection install dellemc.openmanage`.

    To use it in a playbook, specify: :code:`dellemc.openmanage.idrac_storage_controller`.

.. contents::
   :local:
   :depth: 2


.. Entry point title

Entry point ``main`` -- Configures the physical disk, virtual disk, and storage controller settings
---------------------------------------------------------------------------------------------------

.. version_added

.. rst-class:: ansible-version-added

New in dellemc.openmanage 7.6.0

.. Deprecated


Synopsis
^^^^^^^^

.. Description

- This role allows the users to configure the settings of the physical disk, virtual disk, and storage controller on iDRAC9 based PowerEdge servers.

.. Requirements


.. Options

Parameters
^^^^^^^^^^

.. rst-class:: ansible-option-table

.. list-table::
  :width: 100%
  :widths: auto
  :header-rows: 1

  * - Parameter
    - Comments

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--apply_time"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_storage_controller_role__parameter-main__apply_time:

      .. rst-class:: ansible-option-title

      **apply_time**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--apply_time" title="Permalink to this option"></a>

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

      \ :literal:`AtMaintenanceWindowStart`\  Allows the user to apply the changes at the start of a maintenance window as specified in \ :emphasis:`maintenance\_window`\ .

      \ :literal:`InMaintenanceWindowOnReset`\  Allows the users to apply after a manual reset but within the maintenance window as specified in \ :emphasis:`maintenance\_window`\ .


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
        <div class="ansibleOptionAnchor" id="parameter-main--attributes"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_storage_controller_role__parameter-main__attributes:

      .. rst-class:: ansible-option-title

      **attributes**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--attributes" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Dictionary of controller attributes and value pair.

      This feature is only supported for iDRAC9 with firmware version 6.00.00.00 and above.

      \ :emphasis:`controller\_id`\  is required for this operation.

      \ :emphasis:`apply\_time`\  and \ :emphasis:`maintenance\_window`\  is applicable for \ :emphasis:`attributes`\ .

      Use \ https://I%28idrac_ip\ /redfish/v1/Schemas/DellOemStorageController.json) to view the attributes.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--ca_path"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_storage_controller_role__parameter-main__ca_path:

      .. rst-class:: ansible-option-title

      **ca_path**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--ca_path" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`path`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The Privacy Enhanced Mail (PEM) file that contains a CA certificate to be used for the validation.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--controller_id"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_storage_controller_role__parameter-main__controller_id:

      .. rst-class:: ansible-option-title

      **controller_id**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--controller_id" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The ID of the controller on which the operations need to be performed.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--disks"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_storage_controller_role__parameter-main__disks:

      .. rst-class:: ansible-option-title

      **disks**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--disks" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      List of physical disks that belongs to \ :emphasis:`controller\_id`\ .


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--disks/blink"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_storage_controller_role__parameter-main__disks/blink:

      .. rst-class:: ansible-option-title

      **blink**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--disks/blink" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Blinks the target physical disk and it always reports as changes found when check mode is enabled.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--disks/global_hot_spare"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_storage_controller_role__parameter-main__disks/global_hot_spare:

      .. rst-class:: ansible-option-title

      **global_hot_spare**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--disks/global_hot_spare" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Assigns a global hot spare or unassigns a hot spare.

      \ :literal:`true`\  assigns the disk as a global hot spare.

      \ :literal:`false`\  unassigns the disk as a hot spare.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--disks/id"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_storage_controller_role__parameter-main__disks/id:

      .. rst-class:: ansible-option-title

      **id**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--disks/id" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Fully Qualified Device Descriptor (FQDD) of the physical disk.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--disks/raid_state"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_storage_controller_role__parameter-main__disks/raid_state:

      .. rst-class:: ansible-option-title

      **raid_state**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--disks/raid_state" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Converts the disk form Non-Raid to Raid and vice versa.

      \ :literal:`raid`\  converts the physical disk to Raid.

      \ :literal:`nonraid`\  converts the physical disk to Non Raid.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"raid"`
      - :ansible-option-choices-entry:`"nonraid"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--disks/status"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_storage_controller_role__parameter-main__disks/status:

      .. rst-class:: ansible-option-title

      **status**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--disks/status" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Converts the disk form online to offline and vice versa.

      \ :literal:`online`\  converts the physical disk status to online.

      \ :literal:`offline`\  converts the physical disk status to offline.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"online"`
      - :ansible-option-choices-entry:`"offline"`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--hostname"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_storage_controller_role__parameter-main__hostname:

      .. rst-class:: ansible-option-title

      **hostname**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--hostname" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-main--https_port"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_storage_controller_role__parameter-main__https_port:

      .. rst-class:: ansible-option-title

      **https_port**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--https_port" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-main--https_timeout"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_storage_controller_role__parameter-main__https_timeout:

      .. rst-class:: ansible-option-title

      **https_timeout**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--https_timeout" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`




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
        <div class="ansibleOptionAnchor" id="parameter-main--key"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_storage_controller_role__parameter-main__key:

      .. rst-class:: ansible-option-title

      **key**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--key" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      A new security key passphrase that the encryption-capable controller uses to create the encryption key. The controller uses the encryption key to lock or unlock access to the Self-Encrypting Drive (SED). Only one encryption key can be created for each controller.

      This is mandatory when \ :emphasis:`set\_controller\_key`\  is \ :literal:`true`\ , \ :emphasis:`rekey`\  is \ :literal:`true`\ .

      The length of the key can be a maximum of 32 characters in length, where the expanded form of the special character is counted as a single character.

      The key must contain at least one character from each of the character classes are uppercase, lowercase, number, and special character.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--key_id"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_storage_controller_role__parameter-main__key_id:

      .. rst-class:: ansible-option-title

      **key_id**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--key_id" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      This is a user supplied text label associated with the passphrase.

      This is mandatory when \ :emphasis:`set\_controller\_key`\  is \ :literal:`true`\ , \ :emphasis:`rekey`\  is \ :literal:`true`\ .

      The length of \ :emphasis:`key\_id`\  can be a maximum of 32 characters in length and should not have any spaces.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--maintenance_window"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_storage_controller_role__parameter-main__maintenance_window:

      .. rst-class:: ansible-option-title

      **maintenance_window**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--maintenance_window" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-main--maintenance_window/duration"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_storage_controller_role__parameter-main__maintenance_window/duration:

      .. rst-class:: ansible-option-title

      **duration**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--maintenance_window/duration" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-main--maintenance_window/start_time"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_storage_controller_role__parameter-main__maintenance_window/start_time:

      .. rst-class:: ansible-option-title

      **start_time**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--maintenance_window/start_time" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The start time for the maintenance window to be scheduled.

      The format is YYYY-MM-DDThh:mm:ss\<offset\>

      \<offset\> is the time offset from UTC that the current timezone set in iDRAC in the format is +05:30 for IST.


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--mode"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_storage_controller_role__parameter-main__mode:

      .. rst-class:: ansible-option-title

      **mode**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--mode" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Encryption mode of the encryption capable controller.

      This option is mandatory when \ :emphasis:`rekey`\  is \ :literal:`true`\  and for enabling controller encryption.

      \ :literal:`SEKM`\  to choose mode as secure enterprise key manager.

      \ :literal:`LKM`\  to choose mode as local key management.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"LKM"`
      - :ansible-option-choices-entry:`"SEKM"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--old_key"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_storage_controller_role__parameter-main__old_key:

      .. rst-class:: ansible-option-title

      **old_key**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--old_key" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Security key passphrase used by the encryption-capable controller.

      This option is mandatory when \ :emphasis:`rekey`\  is \ :literal:`true`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--password"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_storage_controller_role__parameter-main__password:

      .. rst-class:: ansible-option-title

      **password**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--password" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-main--rekey"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_storage_controller_role__parameter-main__rekey:

      .. rst-class:: ansible-option-title

      **rekey**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--rekey" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Resets the key on the controller and it always reports as changes found when check mode is enabled.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--remove_key"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_storage_controller_role__parameter-main__remove_key:

      .. rst-class:: ansible-option-title

      **remove_key**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--remove_key" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Remove the key on controllers.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--reset_config"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_storage_controller_role__parameter-main__reset_config:

      .. rst-class:: ansible-option-title

      **reset_config**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--reset_config" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      To reset the controller.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--set_controller_key"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_storage_controller_role__parameter-main__set_controller_key:

      .. rst-class:: ansible-option-title

      **set_controller_key**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--set_controller_key" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Set the security key or enable controller encryption.

      If \ :emphasis:`mode`\  is provided controller encryption operation is performed, otherwise sets the controller security key.

      \ :emphasis:`key`\ , and \ :emphasis:`key\_id`\  are required for this operation.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--username"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_storage_controller_role__parameter-main__username:

      .. rst-class:: ansible-option-title

      **username**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--username" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-main--validate_certs"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_storage_controller_role__parameter-main__validate_certs:

      .. rst-class:: ansible-option-title

      **validate_certs**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--validate_certs" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      If \ :literal:`false`\ , the SSL certificates will not be validated.

      Configure \ :literal:`false`\  only on personally controlled sites where self-signed certificates are used.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry-default:`true` :ansible-option-choices-default-mark:`← (default)`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--volumes"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_storage_controller_role__parameter-main__volumes:

      .. rst-class:: ansible-option-title

      **volumes**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--volumes" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      List of volume that belongs to \ :emphasis:`controller\_id`\ .


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--volumes/blink"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_storage_controller_role__parameter-main__volumes/blink:

      .. rst-class:: ansible-option-title

      **blink**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--volumes/blink" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Blinks the target virtual disk and it always reports as changes found when check mode is enabled.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--volumes/dedicated_hot_spare"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_storage_controller_role__parameter-main__volumes/dedicated_hot_spare:

      .. rst-class:: ansible-option-title

      **dedicated_hot_spare**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--volumes/dedicated_hot_spare" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Fully Qualified Device Descriptor (FQDD) of the physical disk to assign the volume as a dedicated hot spare to a disk.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--volumes/encrypted"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_storage_controller_role__parameter-main__volumes/encrypted:

      .. rst-class:: ansible-option-title

      **encrypted**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--volumes/encrypted" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      To encrypt the virtual disk.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--volumes/expand_capacity_disk"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_storage_controller_role__parameter-main__volumes/expand_capacity_disk:

      .. rst-class:: ansible-option-title

      **expand_capacity_disk**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--volumes/expand_capacity_disk" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Fully Qualified Device Descriptor (FQDD) of the disk for expanding the capacity with the existing disk.

      \ :emphasis:`expand\_capacity\_size`\  is mutually exclusive with \ :emphasis:`expand\_capacity\_disk`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--volumes/expand_capacity_size"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_storage_controller_role__parameter-main__volumes/expand_capacity_size:

      .. rst-class:: ansible-option-title

      **expand_capacity_size**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--volumes/expand_capacity_size" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Capacity of the virtual disk to be expanded in MB.

      Check mode and Idempotency is not supported for \ :emphasis:`expand\_capacity\_size`\ .

      Minimum Online Capacity Expansion size must be greater than 100 MB of the current size.

      \ :emphasis:`expand\_capacity\_disk`\  is mutually exclusive with \ :emphasis:`expand\_capacity\_size`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--volumes/id"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_storage_controller_role__parameter-main__volumes/id:

      .. rst-class:: ansible-option-title

      **id**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--volumes/id" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Fully Qualified Device Descriptor (FQDD) of the volume.


      .. raw:: html

        </div>



.. Attributes


.. Notes


.. Seealso




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

