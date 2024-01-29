
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

.. _ansible_collections.dellemc.openmanage.idrac_boot_role:

.. Anchors: aliases


.. Title

dellemc.openmanage.idrac_boot role -- Configure the boot order settings
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. Collection note

.. note::
    This role is part of the `dellemc.openmanage collection <https://galaxy.ansible.com/dellemc/openmanage>`_ (version 8.5.0).

    To install it use: :code:`ansible-galaxy collection install dellemc.openmanage`.

    To use it in a playbook, specify: :code:`dellemc.openmanage.idrac_boot`.

.. contents::
   :local:
   :depth: 2


.. Entry point title

Entry point ``main`` -- Configure the boot order settings
---------------------------------------------------------

.. version_added

.. rst-class:: ansible-version-added

New in dellemc.openmanage 8.0.0

.. Deprecated


Synopsis
^^^^^^^^

.. Description

- This role allows to configure the boot order settings.

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
        <div class="ansibleOptionAnchor" id="parameter-main--boot_options"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_boot_role__parameter-main__boot_options:

      .. rst-class:: ansible-option-title

      **boot_options**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--boot_options" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=dictionary`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Options to enable or disable the boot devices.

      This is mutually exclusive with \ :emphasis:`boot\_order`\ , \ :emphasis:`boot\_source\_override\_mode`\ , \ :emphasis:`boot\_source\_override\_enabled`\ , \ :emphasis:`boot\_source\_override\_target`\ , and \ :emphasis:`uefi\_target\_boot\_source\_override`\ .


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--boot_options/boot_option_reference"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_boot_role__parameter-main__boot_options/boot_option_reference:

      .. rst-class:: ansible-option-title

      **boot_option_reference**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--boot_options/boot_option_reference" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-main--boot_options/display_name"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_boot_role__parameter-main__boot_options/display_name:

      .. rst-class:: ansible-option-title

      **display_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--boot_options/display_name" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-main--boot_options/enabled"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_boot_role__parameter-main__boot_options/enabled:

      .. rst-class:: ansible-option-title

      **enabled**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--boot_options/enabled" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-main--boot_order"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_boot_role__parameter-main__boot_order:

      .. rst-class:: ansible-option-title

      **boot_order**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--boot_order" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      This option allows to set the boot devices in the required boot order sequence.

      This is mutually exclusive with \ :emphasis:`boot\_options`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--boot_source_override_enabled"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_boot_role__parameter-main__boot_source_override_enabled:

      .. rst-class:: ansible-option-title

      **boot_source_override_enabled**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--boot_source_override_enabled" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The state of the Boot Source Override feature.

      \ :literal:`disabled`\ , the system boots normally.

      \ :literal:`once`\ , the system boots 1 time to the \ :emphasis:`boot\_source\_override\_target`\ .

      \ :literal:`continuous`\ , the system boots to the target specified in the \ :emphasis:`boot\_source\_override\_target`\  until this property is set to Disabled.

      The state is set to \ :literal:`once`\  for the 1 time boot override and \ :literal:`continuous`\  for the remain-active-until—cancelled override. If the state is set \ :literal:`once`\   or \ :literal:`continuous`\ , the value is reset to \ :literal:`disabled`\  after the \ :emphasis:`boot\_source\_override\_target`\  actions have completed successfully.

      Changes to these options do not alter the BIOS persistent boot order configuration.

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
        <div class="ansibleOptionAnchor" id="parameter-main--boot_source_override_mode"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_boot_role__parameter-main__boot_source_override_mode:

      .. rst-class:: ansible-option-title

      **boot_source_override_mode**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--boot_source_override_mode" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The BIOS boot mode (either Legacy or UEFI) to be used when \ :emphasis:`boot\_source\_override\_target`\  boot source is booted.

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
        <div class="ansibleOptionAnchor" id="parameter-main--boot_source_override_target"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_boot_role__parameter-main__boot_source_override_target:

      .. rst-class:: ansible-option-title

      **boot_source_override_target**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--boot_source_override_target" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The boot source override targets the device to use during the next boot instead of the normal boot device.

      \ :literal:`pxe`\  performs PXE boot from the primary NIC.

      \ :literal:`floppy`\ , \ :literal:`cd`\ , \ :literal:`hdd`\ , and \ :literal:`sd\_card`\  performs boot from their devices respectively.

      \ :literal:`bios\_setup`\  performs boot into the native BIOS setup.

      \ :literal:`uefi\_http`\  performs boot from a URI over HTTP.

      \ :literal:`utilities`\  performs boot from the local utilities.

      \ :literal:`uefi\_target`\  performs boot from the UEFI device path found in \ :emphasis:`uefi\_target\_boot\_source\_override`\ .

      \ :literal:`none`\  if the \ :emphasis:`boot\_source\_override\_target`\  is set to a value other than \ :literal:`none`\  then the \ :emphasis:`boot\_source\_override\_enabled`\  is automatically set to \ :literal:`once`\ .

      Changes to these options do not alter the BIOS persistent boot order configuration.

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
        <div class="ansibleOptionAnchor" id="parameter-main--ca_path"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_boot_role__parameter-main__ca_path:

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
        <div class="ansibleOptionAnchor" id="parameter-main--hostname"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_boot_role__parameter-main__hostname:

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

      .. _ansible_collections.dellemc.openmanage.idrac_boot_role__parameter-main__https_port:

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

      .. _ansible_collections.dellemc.openmanage.idrac_boot_role__parameter-main__https_timeout:

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
        <div class="ansibleOptionAnchor" id="parameter-main--job_wait"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_boot_role__parameter-main__job_wait:

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
        <div class="ansibleOptionAnchor" id="parameter-main--job_wait_timeout"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_boot_role__parameter-main__job_wait_timeout:

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

      :ansible-option-default-bold:`Default:` :ansible-option-default:`900`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--password"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_boot_role__parameter-main__password:

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
        <div class="ansibleOptionAnchor" id="parameter-main--reset_type"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_boot_role__parameter-main__reset_type:

      .. rst-class:: ansible-option-title

      **reset_type**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--reset_type" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-main--resource_id"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_boot_role__parameter-main__resource_id:

      .. rst-class:: ansible-option-title

      **resource_id**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--resource_id" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-main--uefi_target_boot_source_override"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_boot_role__parameter-main__uefi_target_boot_source_override:

      .. rst-class:: ansible-option-title

      **uefi_target_boot_source_override**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--uefi_target_boot_source_override" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The UEFI device path of the device from which to boot when \ :emphasis:`boot\_source\_override\_target`\  is \ :literal:`uefi\_target`\ .

      If \ :emphasis:`boot\_source\_override\_target`\  is set to \ :literal:`uefi\_target`\ , then \ :emphasis:`boot\_source\_override\_enabled`\  cannot be set to c(continuous) because this setting is defined in UEFI as a one-time-boot setting.

      Changes to these options do not alter the BIOS persistent boot order configuration.

      This is required if \ :emphasis:`boot\_source\_override\_target`\  is \ :literal:`uefi\_target`\ .

      This is mutually exclusive with \ :emphasis:`boot\_options`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--username"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_boot_role__parameter-main__username:

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

      .. _ansible_collections.dellemc.openmanage.idrac_boot_role__parameter-main__validate_certs:

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

      If \ :literal:`False`\ , the SSL certificates will not be validated.

      Configure \ :literal:`False`\  only on personally controlled sites where self-signed certificates are used.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry-default:`true` :ansible-option-choices-default-mark:`← (default)`


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

