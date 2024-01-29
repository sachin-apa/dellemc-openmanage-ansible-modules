
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

.. _ansible_collections.dellemc.openmanage.redfish_storage_volume_module:

.. Anchors: short name for ansible.builtin

.. Anchors: aliases



.. Title

dellemc.openmanage.redfish_storage_volume module -- Manages the storage volume configuration
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. Collection note

.. note::
    This module is part of the `dellemc.openmanage collection <https://galaxy.ansible.com/dellemc/openmanage>`_ (version 8.5.0).

    To install it, use: :code:`ansible-galaxy collection install dellemc.openmanage`.
    You need further requirements to be able to use this module,
    see :ref:`Requirements <ansible_collections.dellemc.openmanage.redfish_storage_volume_module_requirements>` for details.

    To use it in a playbook, specify: :code:`dellemc.openmanage.redfish_storage_volume`.

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

- This module allows to create, modify, initialize, or delete a single storage volume.


.. Aliases


.. Requirements

.. _ansible_collections.dellemc.openmanage.redfish_storage_volume_module_requirements:

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

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_module__parameter-apply_time:

      .. rst-class:: ansible-option-title

      **apply_time**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-apply_time" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      :ansible-option-versionadded:`added in dellemc.openmanage 8.5.0`


      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Apply time of the Volume configuration.

      \ :literal:`Immediate`\  allows you to apply the volume configuration on the host server immediately and apply the changes. This is applicable for \ :emphasis:`job\_wait`\ .

      \ :literal:`OnReset`\  allows you to apply the changes on the next reboot of the host server.

      \ :emphasis:`apply\_time`\  has a default value based on the different types of the controller. For example, BOSS-S1 and BOSS-N1 controllers have a default value of \ :emphasis:`apply\_time`\  as \ :literal:`OnReset`\ , and PERC controllers have a default value of \ :emphasis:`apply\_time`\  as \ :literal:`Immediate`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"Immediate"`
      - :ansible-option-choices-entry:`"OnReset"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-baseuri"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_module__parameter-baseuri:

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
        <div class="ansibleOptionAnchor" id="parameter-block_size_bytes"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_module__parameter-block_size_bytes:

      .. rst-class:: ansible-option-title

      **block_size_bytes**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-block_size_bytes" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Block size in bytes.Only applicable when \ :emphasis:`state`\  is \ :literal:`present`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-ca_path"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_module__parameter-ca_path:

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
        <div class="ansibleOptionAnchor" id="parameter-capacity_bytes"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_module__parameter-capacity_bytes:

      .. rst-class:: ansible-option-title

      **capacity_bytes**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-capacity_bytes" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Volume size in bytes.

      Only applicable when \ :emphasis:`state`\  is \ :literal:`present`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-command"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_module__parameter-command:

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

      \ :literal:`initialize`\  initializes an existing storage volume for a specified \ :emphasis:`volume\_id`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"initialize"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-controller_id"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_module__parameter-controller_id:

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

      Fully Qualified Device Descriptor (FQDD) of the storage controller.

      For example- RAID.Slot.1-1.

      This option is mandatory when \ :emphasis:`state`\  is \ :literal:`present`\  while creating a volume.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-drives"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_module__parameter-drives:

      .. rst-class:: ansible-option-title

      **drives**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-drives" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      FQDD of the Physical disks.

      For example- Disk.Bay.0:Enclosure.Internal.0-1:RAID.Slot.1-1.

      Only applicable when \ :emphasis:`state`\  is \ :literal:`present`\  when creating a new volume.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-encrypted"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_module__parameter-encrypted:

      .. rst-class:: ansible-option-title

      **encrypted**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-encrypted" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Indicates whether volume is currently utilizing encryption or not.

      Only applicable when \ :emphasis:`state`\  is \ :literal:`present`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-encryption_types"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_module__parameter-encryption_types:

      .. rst-class:: ansible-option-title

      **encryption_types**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-encryption_types" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The following encryption types can be selected.

      \ :literal:`ControllerAssisted`\  The volume is encrypted by the storage controller entity.

      \ :literal:`NativeDriveEncryption`\  The volume utilizes the native drive encryption capabilities of the drive hardware.

      \ :literal:`SoftwareAssisted`\  The volume is encrypted by the software running on the system or the operating system.

      Only applicable when \ :emphasis:`state`\  is \ :literal:`present`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"NativeDriveEncryption"`
      - :ansible-option-choices-entry:`"ControllerAssisted"`
      - :ansible-option-choices-entry:`"SoftwareAssisted"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-force_reboot"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_module__parameter-force_reboot:

      .. rst-class:: ansible-option-title

      **force_reboot**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-force_reboot" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      :ansible-option-versionadded:`added in dellemc.openmanage 8.5.0`


      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Reboot the server forcefully to apply the changes when the normal reboot fails.

      \ :emphasis:`force\_reboot`\  is applicable only when \ :emphasis:`reboot\_server`\  is \ :literal:`true`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`false` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-initialize_type"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_module__parameter-initialize_type:

      .. rst-class:: ansible-option-title

      **initialize_type**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-initialize_type" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Initialization type of existing volume.

      Only applicable when \ :emphasis:`command`\  is \ :literal:`initialize`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`"Fast"` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`"Slow"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-job_wait"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_module__parameter-job_wait:

      .. rst-class:: ansible-option-title

      **job_wait**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-job_wait" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      :ansible-option-versionadded:`added in dellemc.openmanage 8.5.0`


      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      This parameter provides the option to wait for the job completion.

      This is applicable when \ :emphasis:`apply\_time`\  is \ :literal:`Immediate`\ .

      This is applicable when \ :emphasis:`apply\_time`\  is \ :literal:`OnReset`\  and \ :emphasis:`reboot\_server`\  is \ :literal:`true`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`false` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-job_wait_timeout"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_module__parameter-job_wait_timeout:

      .. rst-class:: ansible-option-title

      **job_wait_timeout**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-job_wait_timeout" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      :ansible-option-versionadded:`added in dellemc.openmanage 8.5.0`


      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      This parameter is the maximum wait time of \ :emphasis:`job\_wait`\  in seconds.

      This option is applicable when \ :emphasis:`job\_wait`\  is \ :literal:`true`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`1200`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-name"></div>
        <div class="ansibleOptionAnchor" id="parameter-volume_name"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_module__parameter-name:
      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_module__parameter-volume_name:

      .. rst-class:: ansible-option-title

      **name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-aliases:`aliases: volume_name`

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Name of the volume to be created.

      Only applicable when \ :emphasis:`state`\  is \ :literal:`present`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-oem"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_module__parameter-oem:

      .. rst-class:: ansible-option-title

      **oem**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-oem" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Includes OEM extended payloads.

      Only applicable when \ :emphasis:`state`\  is \ :emphasis:`present`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-optimum_io_size_bytes"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_module__parameter-optimum_io_size_bytes:

      .. rst-class:: ansible-option-title

      **optimum_io_size_bytes**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-optimum_io_size_bytes" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Stripe size value must be in multiples of 64 \* 1024.

      Only applicable when \ :emphasis:`state`\  is \ :literal:`present`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-password"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_module__parameter-password:

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
        <div class="ansibleOptionAnchor" id="parameter-raid_type"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_module__parameter-raid_type:

      .. rst-class:: ansible-option-title

      **raid_type**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-raid_type" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      :ansible-option-versionadded:`added in dellemc.openmanage 8.3.0`


      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      \ :literal:`RAID0`\  to create a RAID0 type volume.

      \ :literal:`RAID1`\  to create a RAID1 type volume.

      \ :literal:`RAID5`\  to create a RAID5 type volume.

      \ :literal:`RAID6`\  to create a RAID6 type volume.

      \ :literal:`RAID10`\  to create a RAID10 type volume.

      \ :literal:`RAID50`\  to create a RAID50 type volume.

      \ :literal:`RAID60`\  to create a RAID60 type volume.

      \ :emphasis:`raid\_type`\  is mutually exclusive with \ :emphasis:`volume\_type`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"RAID0"`
      - :ansible-option-choices-entry:`"RAID1"`
      - :ansible-option-choices-entry:`"RAID5"`
      - :ansible-option-choices-entry:`"RAID6"`
      - :ansible-option-choices-entry:`"RAID10"`
      - :ansible-option-choices-entry:`"RAID50"`
      - :ansible-option-choices-entry:`"RAID60"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-reboot_server"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_module__parameter-reboot_server:

      .. rst-class:: ansible-option-title

      **reboot_server**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-reboot_server" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      :ansible-option-versionadded:`added in dellemc.openmanage 8.5.0`


      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Reboot the server to apply the changes.

      \ :emphasis:`reboot\_server`\  is applicable only when \ :emphasis:`apply\_timeout`\  is \ :literal:`OnReset`\  or when the default value for the apply time of the controller is \ :literal:`OnReset`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`false` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-state"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_module__parameter-state:

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

      \ :literal:`present`\  creates a storage volume for the specified I (controller\_id), or modifies the storage volume for the specified I (volume\_id). "Note: Modification of an existing volume properties depends on drive and controller capabilities".

      \ :literal:`absent`\  deletes the volume for the specified \ :emphasis:`volume\_id`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"present"`
      - :ansible-option-choices-entry:`"absent"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-timeout"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_module__parameter-timeout:

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

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_module__parameter-username:

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

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_module__parameter-validate_certs:

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

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_module__parameter-volume_id:

      .. rst-class:: ansible-option-title

      **volume_id**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-volume_id" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      FQDD of existing volume.

      For example- Disk.Virtual.4:RAID.Slot.1-1.

      This option is mandatory in the following scenarios,

      \ :emphasis:`state`\  is \ :literal:`present`\ , when updating a volume.

      \ :emphasis:`state`\  is \ :literal:`absent`\ , when deleting a volume.

      \ :emphasis:`command`\  is \ :literal:`initialize`\ , when initializing a volume.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-volume_type"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_module__parameter-volume_type:

      .. rst-class:: ansible-option-title

      **volume_type**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-volume_type" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      One of the following volume types must be selected to create a volume.

      \ :literal:`NonRedundant`\  The volume is a non-redundant storage device.

      \ :literal:`Mirrored`\  The volume is a mirrored device.

      \ :literal:`StripedWithParity`\  The volume is a device which uses parity to retain redundant information.

      \ :literal:`SpannedMirrors`\  The volume is a spanned set of mirrored devices.

      \ :literal:`SpannedStripesWithParity`\  The volume is a spanned set of devices which uses parity to retain redundant information.

      \ :emphasis:`volume\_type`\  is mutually exclusive with \ :emphasis:`raid\_type`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"NonRedundant"`
      - :ansible-option-choices-entry:`"Mirrored"`
      - :ansible-option-choices-entry:`"StripedWithParity"`
      - :ansible-option-choices-entry:`"SpannedMirrors"`
      - :ansible-option-choices-entry:`"SpannedStripesWithParity"`


      .. raw:: html

        </div>


.. Attributes


.. Notes

Notes
-----

.. note::
   - Run this module from a system that has direct access to Redfish APIs.
   - This module supports \ :literal:`check\_mode`\ .
   - This module always reports changes when \ :emphasis:`name`\  and \ :emphasis:`volume\_id`\  are not specified. Either \ :emphasis:`name`\  or \ :emphasis:`volume\_id`\  is required to support \ :literal:`check\_mode`\ .
   - This module supports IPv4 and IPv6 addresses.

.. Seealso


.. Examples

Examples
--------

.. code-block:: yaml+jinja

    
    ---
    - name: Create a volume with supported options
      dellemc.openmanage.redfish_storage_volume:
        baseuri: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        state: "present"
        volume_type: "Mirrored"
        name: "VD0"
        controller_id: "RAID.Slot.1-1"
        drives:
          - Disk.Bay.5:Enclosure.Internal.0-1:RAID.Slot.1-1
          - Disk.Bay.6:Enclosure.Internal.0-1:RAID.Slot.1-1
        block_size_bytes: 512
        capacity_bytes: 299439751168
        optimum_io_size_bytes: 65536
        encryption_types: NativeDriveEncryption
        encrypted: true

    - name: Create a volume with minimum options
      dellemc.openmanage.redfish_storage_volume:
        baseuri: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        state: "present"
        controller_id: "RAID.Slot.1-1"
        volume_type: "NonRedundant"
        drives:
          - Disk.Bay.1:Enclosure.Internal.0-1:RAID.Slot.1-1

    - name: Create a RAID0 on PERC controller on reset
      dellemc.openmanage.redfish_storage_volume:
        baseuri: "192.168.0.1"
        username: "username"
        password: "password"
        state: "present"
        controller_id: "RAID.Slot.1-1"
        raid_type: "RAID0"
        drives:
          - Disk.Bay.1:Enclosure.Internal.0-1:RAID.Slot.1-1
          - Disk.Bay.1:Enclosure.Internal.0-1:RAID.Slot.1-2
        apply_time: OnReset

    - name: Create a RAID0 on BOSS controller with restart
      dellemc.openmanage.redfish_storage_volume:
        baseuri: "192.168.0.1"
        username: "username"
        password: "password"
        state: "present"
        controller_id: "RAID.Slot.1-1"
        raid_type: "RAID0"
        drives:
          - Disk.Bay.1:Enclosure.Internal.0-1:RAID.Slot.1-1
          - Disk.Bay.1:Enclosure.Internal.0-1:RAID.Slot.1-2
        apply_time: OnReset
        reboot_server: true

    - name: Create a RAID0 on BOSS controller with force restart
      dellemc.openmanage.redfish_storage_volume:
        baseuri: "192.168.0.1"
        username: "username"
        password: "password"
        state: "present"
        controller_id: "RAID.Slot.1-1"
        raid_type: "RAID0"
        drives:
          - Disk.Bay.1:Enclosure.Internal.0-1:RAID.Slot.1-1
          - Disk.Bay.1:Enclosure.Internal.0-1:RAID.Slot.1-2
        reboot_server: true
        force_reboot: true

    - name: Modify a volume's encryption type settings
      dellemc.openmanage.redfish_storage_volume:
        baseuri: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        state: "present"
        volume_id: "Disk.Virtual.5:RAID.Slot.1-1"
        encryption_types: "ControllerAssisted"
        encrypted: true

    - name: Delete an existing volume
      dellemc.openmanage.redfish_storage_volume:
        baseuri: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        state: "absent"
        volume_id: "Disk.Virtual.5:RAID.Slot.1-1"

    - name: Initialize an existing volume
      dellemc.openmanage.redfish_storage_volume:
        baseuri: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        command: "initialize"
        volume_id: "Disk.Virtual.6:RAID.Slot.1-1"
        initialize_type: "Slow"

    - name: Create a RAID6 volume
      dellemc.openmanage.redfish_storage_volume:
        baseuri: "192.168.0.1"
        username: "username"
        password: "password"
        state: "present"
        controller_id: "RAID.Slot.1-1"
        raid_type: "RAID6"
        drives:
          - Disk.Bay.1:Enclosure.Internal.0-1:RAID.Slot.1-1
          - Disk.Bay.1:Enclosure.Internal.0-1:RAID.Slot.1-2
          - Disk.Bay.1:Enclosure.Internal.0-1:RAID.Slot.1-3
          - Disk.Bay.1:Enclosure.Internal.0-1:RAID.Slot.1-4

    - name: Create a RAID60 volume
      dellemc.openmanage.redfish_storage_volume:
        baseuri: "192.168.0.1"
        username: "username"
        password: "password"
        state: "present"
        controller_id: "RAID.Slot.1-1"
        raid_type: "RAID60"
        drives:
          - Disk.Bay.1:Enclosure.Internal.0-1:RAID.Slot.1-1
          - Disk.Bay.1:Enclosure.Internal.0-1:RAID.Slot.1-2
          - Disk.Bay.1:Enclosure.Internal.0-1:RAID.Slot.1-3
          - Disk.Bay.1:Enclosure.Internal.0-1:RAID.Slot.1-4
          - Disk.Bay.1:Enclosure.Internal.0-1:RAID.Slot.1-5
          - Disk.Bay.1:Enclosure.Internal.0-1:RAID.Slot.1-6
          - Disk.Bay.1:Enclosure.Internal.0-1:RAID.Slot.1-7
          - Disk.Bay.1:Enclosure.Internal.0-1:RAID.Slot.1-8




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

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_module__return-error_info:

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

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"error": {"@Message.ExtendedInfo": [{"Message": "Unable to perform configuration operations because a configuration job for the device already exists.", "MessageArgs": [], "MessageArgs@odata.count": 0, "MessageId": "IDRAC.1.6.STOR023", "RelatedProperties": [], "RelatedProperties@odata.count": 0, "Resolution": "Wait for the current job for the device to complete or cancel the current job before attempting more configuration operations on the device.", "Severity": "Informational"}], "code": "Base.1.2.GeneralError", "message": "A general error has occurred. See ExtendedInfo for more information"}}`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-msg"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_module__return-msg:

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

      Overall status of the storage configuration operation.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` always

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`"Successfully submitted create volume task."`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-task"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_module__return-task:

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

      Returns ID and URI of the created task.


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

- Sajna Shetty(@Sajna-Shetty)
- Kritika Bhateja(@Kritika-Bhateja-03)



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

