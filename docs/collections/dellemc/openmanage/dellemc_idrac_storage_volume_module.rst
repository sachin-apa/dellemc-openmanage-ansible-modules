
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

.. _ansible_collections.dellemc.openmanage.dellemc_idrac_storage_volume_module:

.. Anchors: short name for ansible.builtin

.. Anchors: aliases



.. Title

dellemc.openmanage.dellemc_idrac_storage_volume module -- Configures the RAID configuration attributes
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. Collection note

.. note::
    This module is part of the `dellemc.openmanage collection <https://galaxy.ansible.com/dellemc/openmanage>`_ (version 8.5.0).

    To install it, use: :code:`ansible-galaxy collection install dellemc.openmanage`.
    You need further requirements to be able to use this module,
    see :ref:`Requirements <ansible_collections.dellemc.openmanage.dellemc_idrac_storage_volume_module_requirements>` for details.

    To use it in a playbook, specify: :code:`dellemc.openmanage.dellemc_idrac_storage_volume`.

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

- This module is responsible for configuring the RAID attributes.


.. Aliases


.. Requirements

.. _ansible_collections.dellemc.openmanage.dellemc_idrac_storage_volume_module_requirements:

Requirements
------------
The below requirements are needed on the host that executes this module.

- omsdk \>= 1.2.488
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

      .. _ansible_collections.dellemc.openmanage.dellemc_idrac_storage_volume_module__parameter-ca_path:

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
        <div class="ansibleOptionAnchor" id="parameter-capacity"></div>

      .. _ansible_collections.dellemc.openmanage.dellemc_idrac_storage_volume_module__parameter-capacity:

      .. rst-class:: ansible-option-title

      **capacity**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-capacity" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`float`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Virtual disk size in GB.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-controller_id"></div>

      .. _ansible_collections.dellemc.openmanage.dellemc_idrac_storage_volume_module__parameter-controller_id:

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

      Fully Qualified Device Descriptor (FQDD) of the storage controller, for example 'RAID.Integrated.1-1'. Controller FQDD is required for \ :literal:`create`\  RAID configuration.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-disk_cache_policy"></div>

      .. _ansible_collections.dellemc.openmanage.dellemc_idrac_storage_volume_module__parameter-disk_cache_policy:

      .. rst-class:: ansible-option-title

      **disk_cache_policy**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-disk_cache_policy" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Disk Cache Policy.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`"Default"` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`"Enabled"`
      - :ansible-option-choices-entry:`"Disabled"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-idrac_ip"></div>

      .. _ansible_collections.dellemc.openmanage.dellemc_idrac_storage_volume_module__parameter-idrac_ip:

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

      .. _ansible_collections.dellemc.openmanage.dellemc_idrac_storage_volume_module__parameter-idrac_password:
      .. _ansible_collections.dellemc.openmanage.dellemc_idrac_storage_volume_module__parameter-idrac_pwd:

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

      .. _ansible_collections.dellemc.openmanage.dellemc_idrac_storage_volume_module__parameter-idrac_port:

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

      .. _ansible_collections.dellemc.openmanage.dellemc_idrac_storage_volume_module__parameter-idrac_user:

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
        <div class="ansibleOptionAnchor" id="parameter-media_type"></div>

      .. _ansible_collections.dellemc.openmanage.dellemc_idrac_storage_volume_module__parameter-media_type:

      .. rst-class:: ansible-option-title

      **media_type**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-media_type" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Media type.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"HDD"`
      - :ansible-option-choices-entry:`"SSD"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-number_dedicated_hot_spare"></div>

      .. _ansible_collections.dellemc.openmanage.dellemc_idrac_storage_volume_module__parameter-number_dedicated_hot_spare:

      .. rst-class:: ansible-option-title

      **number_dedicated_hot_spare**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-number_dedicated_hot_spare" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Number of Dedicated Hot Spare.


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`0`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-protocol"></div>

      .. _ansible_collections.dellemc.openmanage.dellemc_idrac_storage_volume_module__parameter-protocol:

      .. rst-class:: ansible-option-title

      **protocol**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-protocol" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Bus protocol.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"SAS"`
      - :ansible-option-choices-entry:`"SATA"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-raid_init_operation"></div>

      .. _ansible_collections.dellemc.openmanage.dellemc_idrac_storage_volume_module__parameter-raid_init_operation:

      .. rst-class:: ansible-option-title

      **raid_init_operation**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-raid_init_operation" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      This option represents initialization configuration operation to be performed on the virtual disk.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"None"`
      - :ansible-option-choices-entry:`"Fast"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-raid_reset_config"></div>

      .. _ansible_collections.dellemc.openmanage.dellemc_idrac_storage_volume_module__parameter-raid_reset_config:

      .. rst-class:: ansible-option-title

      **raid_reset_config**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-raid_reset_config" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      This option represents whether a reset config operation needs to be performed on the RAID controller. Reset Config operation deletes all the virtual disks present on the RAID controller.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"True"`
      - :ansible-option-choices-entry-default:`"False"` :ansible-option-choices-default-mark:`← (default)`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-read_cache_policy"></div>

      .. _ansible_collections.dellemc.openmanage.dellemc_idrac_storage_volume_module__parameter-read_cache_policy:

      .. rst-class:: ansible-option-title

      **read_cache_policy**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-read_cache_policy" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Read cache policy.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`"NoReadAhead"` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`"ReadAhead"`
      - :ansible-option-choices-entry:`"AdaptiveReadAhead"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-span_depth"></div>

      .. _ansible_collections.dellemc.openmanage.dellemc_idrac_storage_volume_module__parameter-span_depth:

      .. rst-class:: ansible-option-title

      **span_depth**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-span_depth" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Number of spans in the RAID configuration.

      \ :emphasis:`span\_depth`\  is required for \ :literal:`create`\  and its value depends on \ :emphasis:`volume\_type`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`1`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-span_length"></div>

      .. _ansible_collections.dellemc.openmanage.dellemc_idrac_storage_volume_module__parameter-span_length:

      .. rst-class:: ansible-option-title

      **span_length**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-span_length" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Number of disks in a span.

      \ :emphasis:`span\_length`\  is required for \ :literal:`create`\  and its value depends on \ :emphasis:`volume\_type`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`1`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-state"></div>

      .. _ansible_collections.dellemc.openmanage.dellemc_idrac_storage_volume_module__parameter-state:

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

      \ :literal:`create`\ , performs create volume operation.

      \ :literal:`delete`\ , performs remove volume operation.

      \ :literal:`view`\ , returns storage view.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"create"`
      - :ansible-option-choices-entry:`"delete"`
      - :ansible-option-choices-entry-default:`"view"` :ansible-option-choices-default-mark:`← (default)`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-stripe_size"></div>

      .. _ansible_collections.dellemc.openmanage.dellemc_idrac_storage_volume_module__parameter-stripe_size:

      .. rst-class:: ansible-option-title

      **stripe_size**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-stripe_size" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Stripe size value to be provided in multiples of 64 \* 1024.


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`65536`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-timeout"></div>

      .. _ansible_collections.dellemc.openmanage.dellemc_idrac_storage_volume_module__parameter-timeout:

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
        <div class="ansibleOptionAnchor" id="parameter-validate_certs"></div>

      .. _ansible_collections.dellemc.openmanage.dellemc_idrac_storage_volume_module__parameter-validate_certs:

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

      .. _ansible_collections.dellemc.openmanage.dellemc_idrac_storage_volume_module__parameter-volume_id:

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

      Fully Qualified Device Descriptor (FQDD) of the virtual disk, for example 'Disk.virtual.0:RAID.Slot.1-1'. This option is used to get the virtual disk information.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-volume_type"></div>

      .. _ansible_collections.dellemc.openmanage.dellemc_idrac_storage_volume_module__parameter-volume_type:

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

      Provide the the required RAID level.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`"RAID 0"` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`"RAID 1"`
      - :ansible-option-choices-entry:`"RAID 5"`
      - :ansible-option-choices-entry:`"RAID 6"`
      - :ansible-option-choices-entry:`"RAID 10"`
      - :ansible-option-choices-entry:`"RAID 50"`
      - :ansible-option-choices-entry:`"RAID 60"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-volumes"></div>

      .. _ansible_collections.dellemc.openmanage.dellemc_idrac_storage_volume_module__parameter-volumes:

      .. rst-class:: ansible-option-title

      **volumes**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-volumes" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      A list of virtual disk specific iDRAC attributes. This is applicable for \ :literal:`create`\  and \ :literal:`delete`\  operations.

      For \ :literal:`create`\  operation, name and drives are applicable options, other volume options can also be specified.

      The drives is a required option for \ :literal:`create`\  operation and accepts either location (list of drive slot) or id (list of drive fqdd).

      For \ :literal:`delete`\  operation, only name option is applicable.

      See the examples for more details.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-write_cache_policy"></div>

      .. _ansible_collections.dellemc.openmanage.dellemc_idrac_storage_volume_module__parameter-write_cache_policy:

      .. rst-class:: ansible-option-title

      **write_cache_policy**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-write_cache_policy" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Write cache policy.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`"WriteThrough"` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`"WriteBack"`
      - :ansible-option-choices-entry:`"WriteBackForce"`


      .. raw:: html

        </div>


.. Attributes


.. Notes

Notes
-----

.. note::
   - Run this module from a system that has direct access to Dell iDRAC.
   - This module supports both IPv4 and IPv6 address for \ :emphasis:`idrac\_ip`\ .
   - This module supports \ :literal:`check\_mode`\ .

.. Seealso


.. Examples

Examples
--------

.. code-block:: yaml+jinja

    
    ---
    - name: Create single volume
      dellemc.openmanage.dellemc_idrac_storage_volume:
        idrac_ip: "192.168.0.1"
        idrac_user: "username"
        idrac_password: "password"
        ca_path: "/path/to/ca_cert.pem"
        state: "create"
        controller_id: "RAID.Slot.1-1"
        volumes:
          - drives:
            location: [5]

    - name: Create multiple volume
      dellemc.openmanage.dellemc_idrac_storage_volume:
        idrac_ip: "192.168.0.1"
        idrac_user: "username"
        idrac_password: "password"
        ca_path: "/path/to/ca_cert.pem"
        raid_reset_config: "True"
        state: "create"
        controller_id: "RAID.Slot.1-1"
        volume_type: "RAID 1"
        span_depth: 1
        span_length: 2
        number_dedicated_hot_spare: 1
        disk_cache_policy: "Enabled"
        write_cache_policy: "WriteBackForce"
        read_cache_policy: "ReadAhead"
        stripe_size: 65536
        capacity: 100
        raid_init_operation: "Fast"
        volumes:
          - name: "volume_1"
            drives:
              id: ["Disk.Bay.1:Enclosure.Internal.0-1:RAID.Slot.1-1", "Disk.Bay.2:Enclosure.Internal.0-1:RAID.Slot.1-1"]
          - name: "volume_2"
            volume_type: "RAID 5"
            span_length: 3
            span_depth: 1
            drives:
              location: [7, 3, 5]
            disk_cache_policy: "Disabled"
            write_cache_policy: "WriteBack"
            read_cache_policy: "NoReadAhead"
            stripe_size: 131072
            capacity: "200"
            raid_init_operation: "None"

    - name: View all volume details
      dellemc.openmanage.dellemc_idrac_storage_volume:
        idrac_ip: "192.168.0.1"
        idrac_user: "username"
        idrac_password: "password"
        ca_path: "/path/to/ca_cert.pem"
        state: "view"

    - name: View specific volume details
      dellemc.openmanage.dellemc_idrac_storage_volume:
        idrac_ip: "192.168.0.1"
        idrac_user: "username"
        idrac_password: "password"
        ca_path: "/path/to/ca_cert.pem"
        state: "view"
        controller_id: "RAID.Slot.1-1"
        volume_id: "Disk.Virtual.0:RAID.Slot.1-1"

    - name: Delete single volume
      dellemc.openmanage.dellemc_idrac_storage_volume:
        idrac_ip: "192.168.0.1"
        idrac_user: "username"
        idrac_password: "password"
        ca_path: "/path/to/ca_cert.pem"
        state: "delete"
        volumes:
          - name: "volume_1"

    - name: Delete multiple volume
      dellemc.openmanage.dellemc_idrac_storage_volume:
        idrac_ip: "192.168.0.1"
        idrac_user: "username"
        idrac_password: "password"
        ca_path: "/path/to/ca_cert.pem"
        state: "delete"
        volumes:
          - name: "volume_1"
          - name: "volume_2"




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
        <div class="ansibleOptionAnchor" id="return-msg"></div>

      .. _ansible_collections.dellemc.openmanage.dellemc_idrac_storage_volume_module__return-msg:

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

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`"Successfully completed the view storage volume operation"`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-storage_status"></div>

      .. _ansible_collections.dellemc.openmanage.dellemc_idrac_storage_volume_module__return-storage_status:

      .. rst-class:: ansible-option-title

      **storage_status**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-storage_status" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Storage configuration job and progress details from the iDRAC.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` success

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"Id": "JID\_XXXXXXXXX", "JobState": "Completed", "JobType": "ImportConfiguration", "Message": "Successfully imported and applied Server Configuration Profile.", "MessageId": "XXX123", "Name": "Import Configuration", "PercentComplete": 100, "StartTime": "TIME\_NOW", "Status": "Success", "TargetSettingsURI": null, "retval": true}`


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

