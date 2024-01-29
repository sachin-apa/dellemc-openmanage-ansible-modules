
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

.. _ansible_collections.dellemc.openmanage.redfish_storage_volume_role:

.. Anchors: aliases


.. Title

dellemc.openmanage.redfish_storage_volume role -- Role to manage the storage volume configuration
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. Collection note

.. note::
    This role is part of the `dellemc.openmanage collection <https://galaxy.ansible.com/dellemc/openmanage>`_ (version 8.5.0).

    To install it use: :code:`ansible-galaxy collection install dellemc.openmanage`.

    To use it in a playbook, specify: :code:`dellemc.openmanage.redfish_storage_volume`.

.. contents::
   :local:
   :depth: 2


.. Entry point title

Entry point ``main`` -- Role to manage the storage volume configuration
-----------------------------------------------------------------------

.. version_added

.. rst-class:: ansible-version-added

New in dellemc.openmanage 7.5.0

.. Deprecated


Synopsis
^^^^^^^^

.. Description

- Role to create, modify, initialize, or delete a single storage volume.

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

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_role__parameter-main__apply_time:

      .. rst-class:: ansible-option-title

      **apply_time**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--apply_time" title="Permalink to this option"></a>

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

      \ :emphasis:`apply\_time`\  has a default value based on the different types of the controller.

      For example, BOSS-S1 and BOSS-N1 controllers have a default value of \ :emphasis:`apply\_time`\  as \ :literal:`OnReset`\ .

      PERC controllers have a default value of \ :emphasis:`apply\_time`\  as \ :literal:`Immediate`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"Immediate"`
      - :ansible-option-choices-entry:`"OnReset"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--block_size_bytes"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_role__parameter-main__block_size_bytes:

      .. rst-class:: ansible-option-title

      **block_size_bytes**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--block_size_bytes" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-main--ca_path"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_role__parameter-main__ca_path:

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
        <div class="ansibleOptionAnchor" id="parameter-main--capacity_bytes"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_role__parameter-main__capacity_bytes:

      .. rst-class:: ansible-option-title

      **capacity_bytes**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--capacity_bytes" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-main--command"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_role__parameter-main__command:

      .. rst-class:: ansible-option-title

      **command**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--command" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-main--controller_id"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_role__parameter-main__controller_id:

      .. rst-class:: ansible-option-title

      **controller_id**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--controller_id" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-main--drives"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_role__parameter-main__drives:

      .. rst-class:: ansible-option-title

      **drives**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--drives" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-main--encrypted"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_role__parameter-main__encrypted:

      .. rst-class:: ansible-option-title

      **encrypted**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--encrypted" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-main--encryption_types"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_role__parameter-main__encryption_types:

      .. rst-class:: ansible-option-title

      **encryption_types**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--encryption_types" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-main--force_reboot"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_role__parameter-main__force_reboot:

      .. rst-class:: ansible-option-title

      **force_reboot**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--force_reboot" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-main--hostname"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_role__parameter-main__hostname:

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

      iDRAC IP Address or hostname.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--https_port"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_role__parameter-main__https_port:

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

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_role__parameter-main__https_timeout:

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

      The HTTPS socket level timeout in seconds.


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`30`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--initialize_type"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_role__parameter-main__initialize_type:

      .. rst-class:: ansible-option-title

      **initialize_type**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--initialize_type" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-main--job_wait"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_role__parameter-main__job_wait:

      .. rst-class:: ansible-option-title

      **job_wait**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--job_wait" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-main--job_wait_timeout"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_role__parameter-main__job_wait_timeout:

      .. rst-class:: ansible-option-title

      **job_wait_timeout**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--job_wait_timeout" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The maximum wait time of \ :emphasis:`job\_wait`\  in seconds. The job is tracked only for this duration.

      This option is applicable when \ :emphasis:`job\_wait`\  is \ :literal:`True`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`1200`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--name"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_role__parameter-main__name:

      .. rst-class:: ansible-option-title

      **name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Name of the volume to be created.

      Only applicable when \ :emphasis:`state`\  is \ :literal:`present`\ .

      This will be deprecated. Please use \ :emphasis:`volume\_name`\  for specifying the volume name.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--oem"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_role__parameter-main__oem:

      .. rst-class:: ansible-option-title

      **oem**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--oem" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-main--optimum_io_size_bytes"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_role__parameter-main__optimum_io_size_bytes:

      .. rst-class:: ansible-option-title

      **optimum_io_size_bytes**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--optimum_io_size_bytes" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-main--password"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_role__parameter-main__password:

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
        <div class="ansibleOptionAnchor" id="parameter-main--raid_type"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_role__parameter-main__raid_type:

      .. rst-class:: ansible-option-title

      **raid_type**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--raid_type" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      One of the following raid types must be selected to create a volume for firmware version 4.40 and above.

      \ :literal:`RAID0`\  to create a RAID0 type volume.

      \ :literal:`RAID1`\  to create a RAID1 type volume.

      \ :literal:`RAID5`\  to create a RAID5 type volume.

      \ :literal:`RAID6`\  to create a RAID6 type volume.

      \ :literal:`RAID10`\  to create a RAID10 type volume.

      \ :literal:`RAID50`\  to create a RAID50 type volume.

      \ :literal:`RAID60`\  to create a RAID60 type volume.


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
        <div class="ansibleOptionAnchor" id="parameter-main--reboot_server"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_role__parameter-main__reboot_server:

      .. rst-class:: ansible-option-title

      **reboot_server**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--reboot_server" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-main--state"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_role__parameter-main__state:

      .. rst-class:: ansible-option-title

      **state**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--state" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-main--username"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_role__parameter-main__username:

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

      iDRAC username with admin privilages.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--validate_certs"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_role__parameter-main__validate_certs:

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
        <div class="ansibleOptionAnchor" id="parameter-main--volume_id"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_role__parameter-main__volume_id:

      .. rst-class:: ansible-option-title

      **volume_id**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--volume_id" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-main--volume_name"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_storage_volume_role__parameter-main__volume_name:

      .. rst-class:: ansible-option-title

      **volume_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--volume_name" title="Permalink to this option"></a>

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

