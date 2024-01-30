
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

.. _ansible_collections.dellemc.openmanage.ome_profile_module:

.. Anchors: short name for ansible.builtin

.. Anchors: aliases



.. Title

dellemc.openmanage.ome_profile module -- Create, modify, delete, assign, unassign and migrate a profile on OpenManage Enterprise
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. Collection note

.. note::
    This module is part of the `dellemc.openmanage collection <https://galaxy.ansible.com/dellemc/openmanage>`_ (version 8.5.0).

    To install it, use: :code:`ansible-galaxy collection install dellemc.openmanage`.
    You need further requirements to be able to use this module,
    see :ref:`Requirements <ansible_collections.dellemc.openmanage.ome_profile_module_requirements>` for details.

    To use it in a playbook, specify: :code:`dellemc.openmanage.ome_profile`.

.. version_added

.. rst-class:: ansible-version-added

New in dellemc.openmanage 3.1.0

.. contents::
   :local:
   :depth: 1

.. Deprecated


Synopsis
--------

.. Description

- This module allows to create, modify, delete, assign, unassign, and migrate a profile on OpenManage Enterprise.


.. Aliases


.. Requirements

.. _ansible_collections.dellemc.openmanage.ome_profile_module_requirements:

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
        <div class="ansibleOptionAnchor" id="parameter-attributes"></div>

      .. _ansible_collections.dellemc.openmanage.ome_profile_module__parameter-attributes:

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

      Attributes for \ :literal:`modify`\  and \ :literal:`assign`\ .


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-attributes/Attributes"></div>

      .. _ansible_collections.dellemc.openmanage.ome_profile_module__parameter-attributes/attributes:

      .. rst-class:: ansible-option-title

      **Attributes**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-attributes/Attributes" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      List of attributes to be modified, when \ :emphasis:`command`\  is \ :literal:`modify`\ .

      List of attributes to be overridden when \ :emphasis:`command`\  is \ :literal:`assign`\ .

      Use the \ :emphasis:`Id`\  If the attribute Id is available. If not, use the comma separated I (DisplayName). For more details about using the \ :emphasis:`DisplayName`\ , see the example provided.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-attributes/Options"></div>

      .. _ansible_collections.dellemc.openmanage.ome_profile_module__parameter-attributes/options:

      .. rst-class:: ansible-option-title

      **Options**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-attributes/Options" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Provides the different shut down options.

      This is applicable when \ :emphasis:`command`\  is \ :literal:`assign`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-attributes/Schedule"></div>

      .. _ansible_collections.dellemc.openmanage.ome_profile_module__parameter-attributes/schedule:

      .. rst-class:: ansible-option-title

      **Schedule**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-attributes/Schedule" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Schedule for profile deployment.

      This is applicable when \ :emphasis:`command`\  is \ :literal:`assign`\ .


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-boot_to_network_iso"></div>

      .. _ansible_collections.dellemc.openmanage.ome_profile_module__parameter-boot_to_network_iso:

      .. rst-class:: ansible-option-title

      **boot_to_network_iso**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-boot_to_network_iso" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Details of the Share iso.

      Applicable when \ :emphasis:`command`\  is \ :literal:`create`\ , \ :literal:`assign`\ , and \ :literal:`modify`\ .


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-boot_to_network_iso/boot_to_network"></div>

      .. _ansible_collections.dellemc.openmanage.ome_profile_module__parameter-boot_to_network_iso/boot_to_network:

      .. rst-class:: ansible-option-title

      **boot_to_network**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-boot_to_network_iso/boot_to_network" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enable or disable a network share.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-boot_to_network_iso/iso_path"></div>

      .. _ansible_collections.dellemc.openmanage.ome_profile_module__parameter-boot_to_network_iso/iso_path:

      .. rst-class:: ansible-option-title

      **iso_path**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-boot_to_network_iso/iso_path" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Specify the full ISO path including the share name.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-boot_to_network_iso/iso_timeout"></div>

      .. _ansible_collections.dellemc.openmanage.ome_profile_module__parameter-boot_to_network_iso/iso_timeout:

      .. rst-class:: ansible-option-title

      **iso_timeout**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-boot_to_network_iso/iso_timeout" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Set the number of hours that the network ISO file will remain mapped to the target device(s).


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`1`
      - :ansible-option-choices-entry:`2`
      - :ansible-option-choices-entry-default:`4` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`8`
      - :ansible-option-choices-entry:`16`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-boot_to_network_iso/share_ip"></div>

      .. _ansible_collections.dellemc.openmanage.ome_profile_module__parameter-boot_to_network_iso/share_ip:

      .. rst-class:: ansible-option-title

      **share_ip**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-boot_to_network_iso/share_ip" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      IP address of the network share.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-boot_to_network_iso/share_password"></div>

      .. _ansible_collections.dellemc.openmanage.ome_profile_module__parameter-boot_to_network_iso/share_password:

      .. rst-class:: ansible-option-title

      **share_password**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-boot_to_network_iso/share_password" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      User password when \ :emphasis:`share\_type`\  is \ :literal:`CIFS`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-boot_to_network_iso/share_type"></div>

      .. _ansible_collections.dellemc.openmanage.ome_profile_module__parameter-boot_to_network_iso/share_type:

      .. rst-class:: ansible-option-title

      **share_type**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-boot_to_network_iso/share_type" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Type of network share.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"NFS"`
      - :ansible-option-choices-entry:`"CIFS"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-boot_to_network_iso/share_user"></div>

      .. _ansible_collections.dellemc.openmanage.ome_profile_module__parameter-boot_to_network_iso/share_user:

      .. rst-class:: ansible-option-title

      **share_user**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-boot_to_network_iso/share_user" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      User name when \ :emphasis:`share\_type`\  is \ :literal:`CIFS`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-boot_to_network_iso/workgroup"></div>

      .. _ansible_collections.dellemc.openmanage.ome_profile_module__parameter-boot_to_network_iso/workgroup:

      .. rst-class:: ansible-option-title

      **workgroup**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-boot_to_network_iso/workgroup" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      User workgroup when \ :emphasis:`share\_type`\  is \ :literal:`CIFS`\ .


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-ca_path"></div>

      .. _ansible_collections.dellemc.openmanage.ome_profile_module__parameter-ca_path:

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

      .. _ansible_collections.dellemc.openmanage.ome_profile_module__parameter-command:

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

      \ :literal:`create`\  creates new profiles.

      \ :literal:`modify`\  modifies an existing profile. Only \ :emphasis:`name`\ , \ :emphasis:`description`\ , \ :emphasis:`boot\_to\_network\_iso`\ , and \ :emphasis:`attributes`\  can be modified.

      \ :literal:`delete`\  deletes an existing profile.

      \ :literal:`assign`\  Deploys an existing profile on a target device and returns a task ID.

      \ :literal:`unassign`\  unassigns a profile from a specified target and returns a task ID.

      \ :literal:`migrate`\  migrates an existing profile and returns a task ID.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`"create"` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`"modify"`
      - :ansible-option-choices-entry:`"delete"`
      - :ansible-option-choices-entry:`"assign"`
      - :ansible-option-choices-entry:`"unassign"`
      - :ansible-option-choices-entry:`"migrate"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-description"></div>

      .. _ansible_collections.dellemc.openmanage.ome_profile_module__parameter-description:

      .. rst-class:: ansible-option-title

      **description**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-description" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Description of the profile.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-device_id"></div>

      .. _ansible_collections.dellemc.openmanage.ome_profile_module__parameter-device_id:

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

      ID of the target device.

      This is applicable when \ :emphasis:`command`\  is \ :literal:`assign`\  and \ :literal:`migrate`\ .

      This option is mutually exclusive with \ :emphasis:`device\_service\_tag`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-device_service_tag"></div>

      .. _ansible_collections.dellemc.openmanage.ome_profile_module__parameter-device_service_tag:

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

      Identifier of the target device.

      This is typically 7 to 8 characters in length.

      Applicable when \ :emphasis:`command`\  is \ :literal:`assign`\ , and \ :literal:`migrate`\ .

      This option is mutually exclusive with \ :emphasis:`device\_id`\ .

      If the device does not exist when \ :emphasis:`command`\  is \ :literal:`assign`\  then the profile is auto-deployed.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-filters"></div>

      .. _ansible_collections.dellemc.openmanage.ome_profile_module__parameter-filters:

      .. rst-class:: ansible-option-title

      **filters**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-filters" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Filters the profiles based on selected criteria.

      This is applicable when \ :emphasis:`command`\  is \ :literal:`delete`\  or \ :literal:`unassign`\ .

      This supports suboption \ :emphasis:`ProfileIds`\  which takes a list of profile IDs.

      This also supports OData filter expressions with the suboption \ :emphasis:`Filters`\ .

      See OpenManage Enterprise REST API guide for the filtering options available.

      \ :emphasis:`WARNING`\  When this option is used in case of \ :literal:`unassign`\ , task ID is not returned for any of the profiles affected.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-force"></div>

      .. _ansible_collections.dellemc.openmanage.ome_profile_module__parameter-force:

      .. rst-class:: ansible-option-title

      **force**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-force" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Provides the option to force the migration of a profile even if the source device cannot be contacted.

      This option is applicable when \ :emphasis:`command`\  is \ :literal:`migrate`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`false` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-hostname"></div>

      .. _ansible_collections.dellemc.openmanage.ome_profile_module__parameter-hostname:

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
        <div class="ansibleOptionAnchor" id="parameter-name"></div>

      .. _ansible_collections.dellemc.openmanage.ome_profile_module__parameter-name:

      .. rst-class:: ansible-option-title

      **name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Name of the profile.

      This is applicable for modify, delete, assign, unassign, and migrate operations.

      This option is mutually exclusive with \ :emphasis:`name\_prefix`\  and \ :emphasis:`number\_of\_profiles`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-name_prefix"></div>

      .. _ansible_collections.dellemc.openmanage.ome_profile_module__parameter-name_prefix:

      .. rst-class:: ansible-option-title

      **name_prefix**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-name_prefix" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The name provided when creating a profile is used a prefix followed by the number assigned to it by OpenManage Enterprise.

      This is applicable only for a create operation.

      This option is mutually exclusive with \ :emphasis:`name`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`"Profile"`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-new_name"></div>

      .. _ansible_collections.dellemc.openmanage.ome_profile_module__parameter-new_name:

      .. rst-class:: ansible-option-title

      **new_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-new_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      New name of the profile.

      Applicable when \ :emphasis:`command`\  is \ :literal:`modify`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-number_of_profiles"></div>

      .. _ansible_collections.dellemc.openmanage.ome_profile_module__parameter-number_of_profiles:

      .. rst-class:: ansible-option-title

      **number_of_profiles**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-number_of_profiles" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Provide the number of profiles to be created.

      This is applicable when \ :emphasis:`name\_prefix`\  is used with \ :literal:`create`\ .

      This option is mutually exclusive with \ :emphasis:`name`\ .

      Openmanage Enterprise can create a maximum of 100 profiles.


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`1`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-password"></div>

      .. _ansible_collections.dellemc.openmanage.ome_profile_module__parameter-password:

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

      .. _ansible_collections.dellemc.openmanage.ome_profile_module__parameter-port:

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
        <div class="ansibleOptionAnchor" id="parameter-template_id"></div>

      .. _ansible_collections.dellemc.openmanage.ome_profile_module__parameter-template_id:

      .. rst-class:: ansible-option-title

      **template_id**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-template_id" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      ID of the template.

      This is applicable when \ :emphasis:`command`\  is \ :literal:`create`\ .

      This option is mutually exclusive with \ :emphasis:`template\_name`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-template_name"></div>

      .. _ansible_collections.dellemc.openmanage.ome_profile_module__parameter-template_name:

      .. rst-class:: ansible-option-title

      **template_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-template_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Name of the template for creating the profile(s).

      This is applicable when \ :emphasis:`command`\  is \ :literal:`create`\ .

      This option is mutually exclusive with \ :emphasis:`template\_id`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-timeout"></div>

      .. _ansible_collections.dellemc.openmanage.ome_profile_module__parameter-timeout:

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

      .. _ansible_collections.dellemc.openmanage.ome_profile_module__parameter-username:

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

      .. _ansible_collections.dellemc.openmanage.ome_profile_module__parameter-validate_certs:

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
   - \ :literal:`assign`\  operation on a already assigned profile will not redeploy.

.. Seealso


.. Examples

Examples
--------

.. code-block:: yaml+jinja

    
    ---
    - name: Create two profiles from a template
      dellemc.openmanage.ome_profile:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        template_name: "template 1"
        name_prefix: "omam_profile"
        number_of_profiles: 2

    - name: Create profile with NFS share
      dellemc.openmanage.ome_profile:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        command: create
        template_name: "template 1"
        name_prefix: "omam_profile"
        number_of_profiles: 1
        boot_to_network_iso:
          boot_to_network: true
          share_type: NFS
          share_ip: "192.168.0.1"
          iso_path: "path/to/my_iso.iso"
          iso_timeout: 8

    - name: Create profile with CIFS share
      dellemc.openmanage.ome_profile:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        command: create
        template_name: "template 1"
        name_prefix: "omam_profile"
        number_of_profiles: 1
        boot_to_network_iso:
          boot_to_network: true
          share_type: CIFS
          share_ip: "192.168.0.2"
          share_user: "username"
          share_password: "password"
          workgroup: "workgroup"
          iso_path: "\\path\\to\\my_iso.iso"
          iso_timeout: 8

    - name: Modify profile name with NFS share and attributes
      dellemc.openmanage.ome_profile:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        command: modify
        name: "Profile 00001"
        new_name: "modified profile"
        description: "new description"
        boot_to_network_iso:
          boot_to_network: true
          share_type: NFS
          share_ip: "192.168.0.3"
          iso_path: "path/to/my_iso.iso"
          iso_timeout: 8
        attributes:
          Attributes:
            - Id: 4506
              Value: "server attr 1"
              IsIgnored: false
            - Id: 4507
              Value: "server attr 2"
              IsIgnored: false
            # Enter the comma separated string as appearing in the Detailed view on GUI
            # System -> Server Topology -> ServerTopology 1 Aisle Name
            - DisplayName: 'System, Server Topology, ServerTopology 1 Aisle Name'
              Value: Aisle 5
              IsIgnored: false

    - name: Delete a profile using profile name
      dellemc.openmanage.ome_profile:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        command: "delete"
        name: "Profile 00001"

    - name: Delete profiles using filters
      dellemc.openmanage.ome_profile:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        command: "delete"
        filters:
          SelectAll: true
          Filters: =contains(ProfileName,'Profile 00002')

    - name: Delete profiles using profile list filter
      dellemc.openmanage.ome_profile:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        command: "delete"
        filters:
          ProfileIds:
            - 17123
            - 16124

    - name: Assign a profile to target along with network share
      dellemc.openmanage.ome_profile:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        command: assign
        name: "Profile 00001"
        device_id: 12456
        boot_to_network_iso:
          boot_to_network: true
          share_type: NFS
          share_ip: "192.168.0.1"
          iso_path: "path/to/my_iso.iso"
          iso_timeout: 8
        attributes:
          Attributes:
            - Id: 4506
              Value: "server attr 1"
              IsIgnored: true
          Options:
            ShutdownType: 0
            TimeToWaitBeforeShutdown: 300
            EndHostPowerState: 1
            StrictCheckingVlan: true
          Schedule:
            RunNow: true
            RunLater: false

    - name: Unassign a profile using profile name
      dellemc.openmanage.ome_profile:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        command: "unassign"
        name: "Profile 00003"

    - name: Unassign profiles using filters
      dellemc.openmanage.ome_profile:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        command: "unassign"
        filters:
          SelectAll: true
          Filters: =contains(ProfileName,'Profile 00003')

    - name: Unassign profiles using profile list filter
      dellemc.openmanage.ome_profile:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        command: "unassign"
        filters:
          ProfileIds:
            - 17123
            - 16123

    - name: Migrate a profile
      dellemc.openmanage.ome_profile:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        command: "migrate"
        name: "Profile 00001"
        device_id: 12456




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

      .. _ansible_collections.dellemc.openmanage.ome_profile_module__return-error_info:

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

      .. _ansible_collections.dellemc.openmanage.ome_profile_module__return-job_id:

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

      Task ID created when \ :emphasis:`command`\  is \ :literal:`assign`\ , \ :literal:`migrate`\  or \ :literal:`unassign`\ .

      \ :literal:`assign`\  and \ :literal:`unassign`\  operations do not trigger a task if a profile is auto-deployed.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` when \ :emphasis:`command`\  is \ :literal:`assign`\ , \ :literal:`migrate`\  or \ :literal:`unassign`\ 

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`14123`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-msg"></div>

      .. _ansible_collections.dellemc.openmanage.ome_profile_module__return-msg:

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

      Overall status of the profile operation.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` always

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`"Successfully created 2 profile(s)."`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-profile_ids"></div>

      .. _ansible_collections.dellemc.openmanage.ome_profile_module__return-profile_ids:

      .. rst-class:: ansible-option-title

      **profile_ids**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-profile_ids" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      IDs of the profiles created.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` when \ :emphasis:`command`\  is \ :literal:`create`\ 

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`[1234, 5678]`


      .. raw:: html

        </div>



..  Status (Presently only deprecated)


.. Authors

Authors
~~~~~~~

- Jagadeesh N V (@jagadeeshnv)



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

