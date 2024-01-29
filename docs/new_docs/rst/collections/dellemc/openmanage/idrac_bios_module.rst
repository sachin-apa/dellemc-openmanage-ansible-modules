
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

.. _ansible_collections.dellemc.openmanage.idrac_bios_module:

.. Anchors: short name for ansible.builtin

.. Anchors: aliases



.. Title

dellemc.openmanage.idrac_bios module -- Modify and clear BIOS attributes, reset BIOS settings and configure boot sources
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. Collection note

.. note::
    This module is part of the `dellemc.openmanage collection <https://galaxy.ansible.com/dellemc/openmanage>`_ (version 8.5.0).

    To install it, use: :code:`ansible-galaxy collection install dellemc.openmanage`.
    You need further requirements to be able to use this module,
    see :ref:`Requirements <ansible_collections.dellemc.openmanage.idrac_bios_module_requirements>` for details.

    To use it in a playbook, specify: :code:`dellemc.openmanage.idrac_bios`.

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

- This module allows to modify the BIOS attributes. Also clears pending BIOS attributes and resets BIOS to default settings.
- Boot sources can be enabled or disabled. Boot sequence can be configured.


.. Aliases


.. Requirements

.. _ansible_collections.dellemc.openmanage.idrac_bios_module_requirements:

Requirements
------------
The below requirements are needed on the host that executes this module.

- omsdk \>= 1.2.490
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

      .. _ansible_collections.dellemc.openmanage.idrac_bios_module__parameter-apply_time:

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

      \ :literal:`AtMaintenanceWindowStart`\  Allows the user to apply at the start of a maintenance window as specified in \ :emphasis:`maintenance\_window`\ . A reboot job will be scheduled.

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

      .. _ansible_collections.dellemc.openmanage.idrac_bios_module__parameter-attributes:

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

      Dictionary of BIOS attributes and value pair. Attributes should be part of the Redfish Dell BIOS Attribute Registry. Use \ https://I%28idrac_ip\ /redfish/v1/Systems/System.Embedded.1/Bios) to view the Redfish URI.

      This is mutually exclusive with \ :emphasis:`boot\_sources`\ , \ :emphasis:`clear\_pending`\ , and \ :emphasis:`reset\_bios`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-boot_sources"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_bios_module__parameter-boot_sources:

      .. rst-class:: ansible-option-title

      **boot_sources**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-boot_sources" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=any`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      (deprecated)List of boot devices to set the boot sources settings.

      \ :emphasis:`boot\_sources`\  is mutually exclusive with \ :emphasis:`attributes`\ , \ :emphasis:`clear\_pending`\ , and \ :emphasis:`reset\_bios`\ .

      \ :emphasis:`job\_wait`\  is not applicable. The module waits till the completion of this task.

      This feature is deprecated, please use \ :ref:`dellemc.openmanage.idrac\_boot <ansible_collections.dellemc.openmanage.idrac_boot_module>`\  for configuring boot sources.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-ca_path"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_bios_module__parameter-ca_path:

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
        <div class="ansibleOptionAnchor" id="parameter-clear_pending"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_bios_module__parameter-clear_pending:

      .. rst-class:: ansible-option-title

      **clear_pending**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-clear_pending" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Allows the user to clear all pending BIOS attributes changes.

      \ :literal:`true`\  will discard any pending changes to bios attributes or remove job if in scheduled state.

      This operation will not create any job.

      \ :literal:`false`\  will not perform any operation.

      This is mutually exclusive with \ :emphasis:`boot\_sources`\ , \ :emphasis:`attributes`\ , and \ :emphasis:`reset\_bios`\ .

      \ :literal:`Note`\  Any BIOS job scheduled due to boot sources configuration will not be cleared.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-idrac_ip"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_bios_module__parameter-idrac_ip:

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

      .. _ansible_collections.dellemc.openmanage.idrac_bios_module__parameter-idrac_password:
      .. _ansible_collections.dellemc.openmanage.idrac_bios_module__parameter-idrac_pwd:

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

      .. _ansible_collections.dellemc.openmanage.idrac_bios_module__parameter-idrac_port:

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

      .. _ansible_collections.dellemc.openmanage.idrac_bios_module__parameter-idrac_user:

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

      .. _ansible_collections.dellemc.openmanage.idrac_bios_module__parameter-job_wait:

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

      This is applicable for \ :emphasis:`attributes`\  when \ :emphasis:`apply\_time`\  is \ :literal:`Immediate`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry-default:`true` :ansible-option-choices-default-mark:`← (default)`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-job_wait_timeout"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_bios_module__parameter-job_wait_timeout:

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

      :ansible-option-default-bold:`Default:` :ansible-option-default:`1200`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-maintenance_window"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_bios_module__parameter-maintenance_window:

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

      .. _ansible_collections.dellemc.openmanage.idrac_bios_module__parameter-maintenance_window/duration:

      .. rst-class:: ansible-option-title

      **duration**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-maintenance_window/duration" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The duration in seconds for the maintenance window.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-maintenance_window/start_time"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_bios_module__parameter-maintenance_window/start_time:

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
        <div class="ansibleOptionAnchor" id="parameter-reset_bios"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_bios_module__parameter-reset_bios:

      .. rst-class:: ansible-option-title

      **reset_bios**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-reset_bios" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Resets the BIOS to default settings and triggers a reboot of host system.

      This is applied to the host after the restart.

      This operation will not create any job.

      \ :literal:`false`\  will not perform any operation.

      This is mutually exclusive with \ :emphasis:`boot\_sources`\ , \ :emphasis:`attributes`\ , and \ :emphasis:`clear\_pending`\ .

      When \ :literal:`true`\ , this action will always report as changes found to be applicable.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-reset_type"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_bios_module__parameter-reset_type:

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

      \ :literal:`force\_restart`\  Forcefully reboot the host system.

      \ :literal:`graceful\_restart`\  Gracefully reboot the host system.

      This is applicable for \ :emphasis:`reset\_bios`\ , and \ :emphasis:`attributes`\  when \ :emphasis:`apply\_time`\  is \ :literal:`Immediate`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`"graceful\_restart"` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`"force\_restart"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-share_mnt"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_bios_module__parameter-share_mnt:

      .. rst-class:: ansible-option-title

      **share_mnt**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-share_mnt" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      (deprecated)Local mount path of the network share with read-write permission for ansible user. This option is mandatory for network shares.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-share_name"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_bios_module__parameter-share_name:

      .. rst-class:: ansible-option-title

      **share_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-share_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      (deprecated)Network share or a local path.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-share_password"></div>
        <div class="ansibleOptionAnchor" id="parameter-share_pwd"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_bios_module__parameter-share_password:
      .. _ansible_collections.dellemc.openmanage.idrac_bios_module__parameter-share_pwd:

      .. rst-class:: ansible-option-title

      **share_password**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-share_password" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-aliases:`aliases: share_pwd`

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      (deprecated)Network share user password. This option is mandatory for CIFS share.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-share_user"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_bios_module__parameter-share_user:

      .. rst-class:: ansible-option-title

      **share_user**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-share_user" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      (deprecated)Network share user name. Use the format 'user@domain' or domain//user if user is part of a domain. This option is mandatory for CIFS share.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-timeout"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_bios_module__parameter-timeout:

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

      .. _ansible_collections.dellemc.openmanage.idrac_bios_module__parameter-validate_certs:

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
   - omsdk is required to be installed only for \ :emphasis:`boot\_sources`\  operation.
   - This module requires 'Administrator' privilege for \ :emphasis:`idrac\_user`\ .
   - Run this module from a system that has direct access to Dell iDRAC.
   - This module supports both IPv4 and IPv6 address for \ :emphasis:`idrac\_ip`\ .
   - This module supports \ :literal:`check\_mode`\ .

.. Seealso


.. Examples

Examples
--------

.. code-block:: yaml+jinja

    
    ---
    - name: Configure generic attributes of the BIOS
      dellemc.openmanage.idrac_bios:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        attributes:
          BootMode: "Bios"
          OneTimeBootMode: "Enabled"
          BootSeqRetry: "Enabled"

    - name: Configure PXE generic attributes
      dellemc.openmanage.idrac_bios:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        attributes:
          PxeDev1EnDis: "Enabled"
          PxeDev1Protocol: "IPV4"
          PxeDev1VlanEnDis: "Enabled"
          PxeDev1VlanId: 1
          PxeDev1Interface: "NIC.Embedded.1-1-1"
          PxeDev1VlanPriority: 2

    - name: Configure BIOS attributes at Maintenance window
      dellemc.openmanage.idrac_bios:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        apply_time: AtMaintenanceWindowStart
        maintenance_window:
          start_time: "2022-09-30T05:15:40-05:00"
          duration: 600
        attributes:
          BootMode: "Bios"
          OneTimeBootMode: "Enabled"
          BootSeqRetry: "Enabled"

    - name: Clear pending BIOS attributes
      dellemc.openmanage.idrac_bios:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        clear_pending: true

    - name: Reset BIOS attributes to default settings.
      dellemc.openmanage.idrac_bios:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        validate_certs: false
        reset_bios: true

    - name: Configure boot sources
      dellemc.openmanage.idrac_bios:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        boot_sources:
          - Name: "NIC.Integrated.1-2-3"
            Enabled: true
            Index: 0

    - name: Configure multiple boot sources
      dellemc.openmanage.idrac_bios:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        boot_sources:
          - Name: "NIC.Integrated.1-1-1"
            Enabled: true
            Index: 0
          - Name: "NIC.Integrated.2-2-2"
            Enabled: true
            Index: 1
          - Name: "NIC.Integrated.3-3-3"
            Enabled: true
            Index: 2

    - name: Configure boot sources - Enabling
      dellemc.openmanage.idrac_bios:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        boot_sources:
          - Name: "NIC.Integrated.1-1-1"
            Enabled: true

    - name: Configure boot sources - Index
      dellemc.openmanage.idrac_bios:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        boot_sources:
          - Name: "NIC.Integrated.1-1-1"
            Index: 0




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

      .. _ansible_collections.dellemc.openmanage.idrac_bios_module__return-error_info:

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
        <div class="ansibleOptionAnchor" id="return-invalid_attributes"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_bios_module__return-invalid_attributes:

      .. rst-class:: ansible-option-title

      **invalid_attributes**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-invalid_attributes" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Dict of invalid attributes provided.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` on invalid attributes or values.

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"AcPwrRcvryUserDelay": "Integer out of valid range.", "AssetTag": "Attribute does not exist.", "BootSeqRetry": "Invalid value for Enumeration.", "Proc1Brand": "Read only Attribute cannot be modified.", "PxeDev1VlanId": "Not a valid integer."}`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-msg"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_bios_module__return-msg:

      .. rst-class:: ansible-option-title

      **msg**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-msg" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Status of the job for \ :emphasis:`boot\_sources`\  or status of the action performed on bios.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` success

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"CompletionTime": "2020-04-20T18:50:20", "Description": "Job Instance", "EndTime": null, "Id": "JID\_873888162305", "JobState": "Completed", "JobType": "ImportConfiguration", "Message": "Successfully imported and applied Server Configuration Profile.", "MessageArgs": [], "MessageId": "SYS053", "Name": "Import Configuration", "PercentComplete": 100, "StartTime": "TIME\_NOW", "Status": "Success", "TargetSettingsURI": null, "retval": true}`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-status_msg"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_bios_module__return-status_msg:

      .. rst-class:: ansible-option-title

      **status_msg**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-status_msg" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Overall status of the bios operation.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` success

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`"Successfully cleared pending BIOS attributes."`


      .. raw:: html

        </div>



..  Status (Presently only deprecated)


.. Authors

Authors
~~~~~~~

- Felix Stephen (@felixs88)
- Anooja Vardhineni (@anooja-vardhineni)
- Jagadeesh N V (@jagadeeshnv)
- Shivam Sharma (@shivam-sharma)



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

