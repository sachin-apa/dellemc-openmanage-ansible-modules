
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

.. _ansible_collections.dellemc.openmanage.idrac_server_config_profile_module:

.. Anchors: short name for ansible.builtin

.. Anchors: aliases



.. Title

dellemc.openmanage.idrac_server_config_profile module -- Export or Import iDRAC Server Configuration Profile (SCP)
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. Collection note

.. note::
    This module is part of the `dellemc.openmanage collection <https://galaxy.ansible.com/dellemc/openmanage>`_ (version 8.5.0).

    To install it, use: :code:`ansible-galaxy collection install dellemc.openmanage`.
    You need further requirements to be able to use this module,
    see :ref:`Requirements <ansible_collections.dellemc.openmanage.idrac_server_config_profile_module_requirements>` for details.

    To use it in a playbook, specify: :code:`dellemc.openmanage.idrac_server_config_profile`.

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

- Export the Server Configuration Profile (SCP) from the iDRAC or import from a network share (CIFS, NFS, HTTP, HTTPS) or a local path.


.. Aliases


.. Requirements

.. _ansible_collections.dellemc.openmanage.idrac_server_config_profile_module_requirements:

Requirements
------------
The below requirements are needed on the host that executes this module.

- python \>= 3.9.14






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

      .. _ansible_collections.dellemc.openmanage.idrac_server_config_profile_module__parameter-ca_path:

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

      .. _ansible_collections.dellemc.openmanage.idrac_server_config_profile_module__parameter-command:

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

      If \ :literal:`import`\ , the module performs SCP import operation.

      If \ :literal:`export`\ , the module performs SCP export operation.

      If \ :literal:`preview`\ , the module performs SCP preview operation.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"import"`
      - :ansible-option-choices-entry-default:`"export"` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`"preview"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-end_host_power_state"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_server_config_profile_module__parameter-end_host_power_state:

      .. rst-class:: ansible-option-title

      **end_host_power_state**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-end_host_power_state" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      This option is applicable for \ :literal:`import`\  command.

      If \ :literal:`On`\ , End host power state is on.

      If \ :literal:`Off`\ , End host power state is off.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`"On"` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`"Off"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-export_format"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_server_config_profile_module__parameter-export_format:

      .. rst-class:: ansible-option-title

      **export_format**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-export_format" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Specify the output file format. This option is applicable for \ :literal:`export`\  command.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"JSON"`
      - :ansible-option-choices-entry-default:`"XML"` :ansible-option-choices-default-mark:`← (default)`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-export_use"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_server_config_profile_module__parameter-export_use:

      .. rst-class:: ansible-option-title

      **export_use**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-export_use" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      :ansible-option-versionadded:`added in dellemc.openmanage 7.3.0`


      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Specify the type of Server Configuration Profile (SCP) to be exported.

      This option is applicable when \ :emphasis:`command`\  is \ :literal:`export`\ .

      \ :literal:`Default`\  Creates a non-destructive snapshot of the configuration.

      \ :literal:`Replace`\  Replaces a server with another or restores the servers settings to a known baseline.

      \ :literal:`Clone`\  Clones settings from one server to another server with the identical hardware setup. All settings except I/O identity are updated (e.g. will reset RAID). The settings in this export will be destructive when uploaded to another system.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`"Default"` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`"Clone"`
      - :ansible-option-choices-entry:`"Replace"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-idrac_ip"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_server_config_profile_module__parameter-idrac_ip:

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

      .. _ansible_collections.dellemc.openmanage.idrac_server_config_profile_module__parameter-idrac_password:
      .. _ansible_collections.dellemc.openmanage.idrac_server_config_profile_module__parameter-idrac_pwd:

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

      .. _ansible_collections.dellemc.openmanage.idrac_server_config_profile_module__parameter-idrac_port:

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

      .. _ansible_collections.dellemc.openmanage.idrac_server_config_profile_module__parameter-idrac_user:

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
        <div class="ansibleOptionAnchor" id="parameter-ignore_certificate_warning"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_server_config_profile_module__parameter-ignore_certificate_warning:

      .. rst-class:: ansible-option-title

      **ignore_certificate_warning**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-ignore_certificate_warning" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      :ansible-option-versionadded:`added in dellemc.openmanage 7.3.0`


      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      If \ :literal:`ignore`\ , it ignores the certificate warnings.

      If \ :literal:`showerror`\ , it shows the certificate warnings.

      \ :emphasis:`ignore\_certificate\_warning`\  is considered only when \ :emphasis:`share\_name`\  is of type HTTPS and is supported only on iDRAC9.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`"ignore"` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`"showerror"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-import_buffer"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_server_config_profile_module__parameter-import_buffer:

      .. rst-class:: ansible-option-title

      **import_buffer**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-import_buffer" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      :ansible-option-versionadded:`added in dellemc.openmanage 7.3.0`


      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Used to import the buffer input of xml or json into the iDRAC.

      This option is applicable when \ :emphasis:`command`\  is \ :literal:`import`\  and \ :literal:`preview`\ .

      \ :emphasis:`import\_buffer`\  is mutually exclusive with \ :emphasis:`share\_name`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-include_in_export"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_server_config_profile_module__parameter-include_in_export:

      .. rst-class:: ansible-option-title

      **include_in_export**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-include_in_export" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      :ansible-option-versionadded:`added in dellemc.openmanage 7.3.0`


      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      This option is applicable when \ :emphasis:`command`\  is \ :literal:`export`\ .

      If \ :literal:`default`\ , it exports the default Server Configuration Profile.

      If \ :literal:`readonly`\ , it exports the SCP with readonly attributes.

      If \ :literal:`passwordhashvalues`\ , it exports the SCP with password hash values.

      If \ :literal:`customtelemetry`\ , exports the SCP with custom telemetry attributes supported only in the iDRAC9.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`"default"` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`"readonly"`
      - :ansible-option-choices-entry:`"passwordhashvalues"`
      - :ansible-option-choices-entry:`"customtelemetry"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-job_wait"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_server_config_profile_module__parameter-job_wait:

      .. rst-class:: ansible-option-title

      **job_wait**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-job_wait" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Whether to wait for job completion or not.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-proxy_password"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_server_config_profile_module__parameter-proxy_password:

      .. rst-class:: ansible-option-title

      **proxy_password**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-proxy_password" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      :ansible-option-versionadded:`added in dellemc.openmanage 7.3.0`


      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Proxy password to authenticate.

      \ :emphasis:`proxy\_password`\  is considered only when \ :emphasis:`share\_name`\  is of type HTTP or HTTPS and is supported only on iDRAC9.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-proxy_port"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_server_config_profile_module__parameter-proxy_port:

      .. rst-class:: ansible-option-title

      **proxy_port**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-proxy_port" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      :ansible-option-versionadded:`added in dellemc.openmanage 7.3.0`


      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Proxy port to authenticate.

      \ :emphasis:`proxy\_port`\  is required when \ :emphasis:`share\_name`\  is of type HTTPS or HTTP and \ :emphasis:`proxy\_support`\  is \ :literal:`true`\ .

      \ :emphasis:`proxy\_port`\  is considered only when \ :emphasis:`share\_name`\  is of type HTTP or HTTPS and is supported only on iDRAC9.


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`"80"`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-proxy_server"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_server_config_profile_module__parameter-proxy_server:

      .. rst-class:: ansible-option-title

      **proxy_server**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-proxy_server" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      :ansible-option-versionadded:`added in dellemc.openmanage 7.3.0`


      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      \ :emphasis:`proxy\_server`\  is required when \ :emphasis:`share\_name`\  is of type HTTPS or HTTP and \ :emphasis:`proxy\_support`\  is \ :literal:`true`\ .

      \ :emphasis:`proxy\_server`\  is considered only when \ :emphasis:`share\_name`\  is of type HTTP or HTTPS and is supported only on iDRAC9.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-proxy_support"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_server_config_profile_module__parameter-proxy_support:

      .. rst-class:: ansible-option-title

      **proxy_support**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-proxy_support" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      :ansible-option-versionadded:`added in dellemc.openmanage 7.3.0`


      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Proxy to be enabled or disabled.

      \ :emphasis:`proxy\_support`\  is considered only when \ :emphasis:`share\_name`\  is of type HTTP or HTTPS and is supported only on iDRAC9.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`false` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-proxy_type"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_server_config_profile_module__parameter-proxy_type:

      .. rst-class:: ansible-option-title

      **proxy_type**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-proxy_type" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      :ansible-option-versionadded:`added in dellemc.openmanage 7.3.0`


      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      \ :literal:`http`\  to select HTTP type proxy.

      \ :literal:`socks4`\  to select SOCKS4 type proxy.

      \ :emphasis:`proxy\_type`\  is considered only when \ :emphasis:`share\_name`\  is of type HTTP or HTTPS and is supported only on iDRAC9.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`"http"` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`"socks4"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-proxy_username"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_server_config_profile_module__parameter-proxy_username:

      .. rst-class:: ansible-option-title

      **proxy_username**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-proxy_username" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      :ansible-option-versionadded:`added in dellemc.openmanage 7.3.0`


      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Proxy username to authenticate.

      \ :emphasis:`proxy\_username`\  is considered only when \ :emphasis:`share\_name`\  is of type HTTP or HTTPS and is supported only on iDRAC9.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-scp_components"></div>
        <div class="ansibleOptionAnchor" id="parameter-target"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_server_config_profile_module__parameter-scp_components:
      .. _ansible_collections.dellemc.openmanage.idrac_server_config_profile_module__parameter-target:

      .. rst-class:: ansible-option-title

      **scp_components**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-scp_components" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-aliases:`aliases: target`

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      If \ :literal:`ALL`\ , this option exports or imports all components configurations from the SCP file.

      If \ :literal:`IDRAC`\ , this option exports or imports iDRAC configuration from the SCP file.

      If \ :literal:`BIOS`\ , this option exports or imports BIOS configuration from the SCP file.

      If \ :literal:`NIC`\ , this option exports or imports NIC configuration from the SCP file.

      If \ :literal:`RAID`\ , this option exports or imports RAID configuration from the SCP file.

      If \ :literal:`FC`\ , this option exports or imports FiberChannel configurations from the SCP file.

      If \ :literal:`InfiniBand`\ , this option exports or imports InfiniBand configuration from the SCP file.

      If \ :literal:`SupportAssist`\ , this option exports or imports SupportAssist configuration from the SCP file.

      If \ :literal:`EventFilters`\ , this option exports or imports EventFilters configuration from the SCP file.

      If \ :literal:`System`\ , this option exports or imports System configuration from the SCP file.

      If \ :literal:`LifecycleController`\ , this option exports or imports SupportAssist configuration from the SCP file.

      If \ :literal:`AHCI`\ , this option exports or imports EventFilters configuration from the SCP file.

      If \ :literal:`PCIeSSD`\ , this option exports or imports PCIeSSD configuration from the SCP file.

      When \ :emphasis:`command`\  is \ :literal:`export`\  or \ :literal:`import`\  \ :emphasis:`target`\  with multiple components is supported only on iDRAC9 with firmware 6.10.00.00 and above.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`"ALL"` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`"IDRAC"`
      - :ansible-option-choices-entry:`"BIOS"`
      - :ansible-option-choices-entry:`"NIC"`
      - :ansible-option-choices-entry:`"RAID"`
      - :ansible-option-choices-entry:`"FC"`
      - :ansible-option-choices-entry:`"InfiniBand"`
      - :ansible-option-choices-entry:`"SupportAssist"`
      - :ansible-option-choices-entry:`"EventFilters"`
      - :ansible-option-choices-entry:`"System"`
      - :ansible-option-choices-entry:`"LifecycleController"`
      - :ansible-option-choices-entry:`"AHCI"`
      - :ansible-option-choices-entry:`"PCIeSSD"`


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`["ALL"]`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-scp_file"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_server_config_profile_module__parameter-scp_file:

      .. rst-class:: ansible-option-title

      **scp_file**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-scp_file" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Name of the server configuration profile (SCP) file.

      This option is mandatory if \ :emphasis:`command`\  is \ :literal:`import`\ .

      The default format \<idrac\_ip\>\_YYmmdd\_HHMMSS\_scp is used if this option is not specified for \ :literal:`import`\ .

      \ :emphasis:`export\_format`\  is used if the valid extension file is not provided for \ :literal:`import`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-share_name"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_server_config_profile_module__parameter-share_name:

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

      Network share or local path.

      CIFS, NFS, HTTP, and HTTPS network share types are supported.

      \ :emphasis:`share\_name`\  is mutually exclusive with \ :emphasis:`import\_buffer`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-share_password"></div>
        <div class="ansibleOptionAnchor" id="parameter-share_pwd"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_server_config_profile_module__parameter-share_password:
      .. _ansible_collections.dellemc.openmanage.idrac_server_config_profile_module__parameter-share_pwd:

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

      Network share user password. This option is mandatory for CIFS Network Share.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-share_user"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_server_config_profile_module__parameter-share_user:

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

      Network share user in the format 'user@domain' or 'domain\\\\user' if user is part of a domain else 'user'. This option is mandatory for CIFS Network Share.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-shutdown_type"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_server_config_profile_module__parameter-shutdown_type:

      .. rst-class:: ansible-option-title

      **shutdown_type**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-shutdown_type" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      This option is applicable for \ :literal:`import`\  command.

      If \ :literal:`Graceful`\ , the job gracefully shuts down the operating system and turns off the server.

      If \ :literal:`Forced`\ , it forcefully shuts down the server.

      If \ :literal:`NoReboot`\ , the job that applies the SCP will pause until you manually reboot the server.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`"Graceful"` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`"Forced"`
      - :ansible-option-choices-entry:`"NoReboot"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-timeout"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_server_config_profile_module__parameter-timeout:

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

      .. _ansible_collections.dellemc.openmanage.idrac_server_config_profile_module__parameter-validate_certs:

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
   - This module requires 'Administrator' privilege for \ :emphasis:`idrac\_user`\ .
   - Run this module from a system that has direct access to Dell iDRAC.
   - This module supports \ :literal:`check\_mode`\ .
   - To import Server Configuration Profile (SCP) on the iDRAC8-based servers, the servers must have iDRAC Enterprise license or later.
   - For \ :literal:`import`\  operation, \ :literal:`check\_mode`\  is supported only when \ :emphasis:`target`\  is \ :literal:`ALL`\ .
   - This module supports IPv4 and IPv6 addresses.

.. Seealso


.. Examples

Examples
--------

.. code-block:: yaml+jinja

    
    ---
    - name: Export SCP with IDRAC components in JSON format to a local path
      dellemc.openmanage.idrac_server_config_profile:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        share_name: "/scp_folder"
        scp_components:
          - IDRAC
        scp_file: example_file
        export_format: JSON
        export_use: Clone
        job_wait: true

    - name: Import SCP with IDRAC components in JSON format from a local path
      dellemc.openmanage.idrac_server_config_profile:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        share_name: "/scp_folder"
        command: import
        scp_components:
          - IDRAC
        scp_file: example_file.json
        shutdown_type: Graceful
        end_host_power_state: "On"
        job_wait: false

    - name: Export SCP with BIOS components in XML format to a NFS share path with auto-generated file name
      dellemc.openmanage.idrac_server_config_profile:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        share_name: "192.168.0.2:/share"
        scp_components:
          - BIOS
        export_format: XML
        export_use: Default
        job_wait: true

    - name: Import SCP with BIOS components in XML format from a NFS share path
      dellemc.openmanage.idrac_server_config_profile:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        share_name: "192.168.0.2:/share"
        command: import
        scp_components:
          - BIOS
        scp_file: 192.168.0.1_20210618_162856.xml
        shutdown_type: NoReboot
        end_host_power_state: "Off"
        job_wait: false

    - name: Export SCP with RAID components in XML format to a CIFS share path with share user domain name
      dellemc.openmanage.idrac_server_config_profile:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        share_name: "\\\\192.168.0.2\\share"
        share_user: share_username@domain
        share_password: share_password
        scp_file: example_file.xml
        scp_components:
          - RAID
        export_format: XML
        export_use: Default
        job_wait: true

    - name: Import SCP with RAID components in XML format from a CIFS share path
      dellemc.openmanage.idrac_server_config_profile:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        share_name: "\\\\192.168.0.2\\share"
        share_user: share_username
        share_password: share_password
        command: import
        scp_components:
          - RAID
        scp_file: example_file.xml
        shutdown_type: Forced
        end_host_power_state: "On"
        job_wait: true

    - name: Export SCP with ALL components in JSON format to a HTTP share path
      dellemc.openmanage.idrac_server_config_profile:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        share_name: "http://192.168.0.3/share"
        share_user: share_username
        share_password: share_password
        scp_file: example_file.json
        scp_components:
          - ALL
        export_format: JSON
        job_wait: false

    - name: Import SCP with ALL components in JSON format from a HTTP share path
      dellemc.openmanage.idrac_server_config_profile:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        command: import
        share_name: "http://192.168.0.3/share"
        share_user: share_username
        share_password: share_password
        scp_file: example_file.json
        shutdown_type: Graceful
        end_host_power_state: "On"
        job_wait: true

    - name: Export SCP with ALL components in XML format to a HTTPS share path without SCP file name
      dellemc.openmanage.idrac_server_config_profile:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        share_name: "https://192.168.0.4/share"
        share_user: share_username
        share_password: share_password
        scp_components:
          - ALL
        export_format: XML
        export_use: Replace
        job_wait: true

    - name: Import SCP with ALL components in XML format from a HTTPS share path
      dellemc.openmanage.idrac_server_config_profile:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        command: import
        share_name: "https://192.168.0.4/share"
        share_user: share_username
        share_password: share_password
        scp_file: 192.168.0.1_20160618_164647.xml
        shutdown_type: Graceful
        end_host_power_state: "On"
        job_wait: false

    - name: Preview SCP with IDRAC components in XML format from a CIFS share path
      dellemc.openmanage.idrac_server_config_profile:
        idrac_ip: "{{ idrac_ip }}"
        idrac_user: "{{ idrac_user }}"
        idrac_password: "{{ idrac_password }}"
        ca_path: "/path/to/ca_cert.pem"
        share_name: "\\\\192.168.0.2\\share"
        share_user: share_username
        share_password: share_password
        command: preview
        scp_components:
          - ALL
        scp_file: example_file.xml
        job_wait: true

    - name: Preview SCP with IDRAC components in JSON format from a NFS share path
      dellemc.openmanage.idrac_server_config_profile:
        idrac_ip: "{{ idrac_ip }}"
        idrac_user: "{{ idrac_user }}"
        idrac_password: "{{ idrac_password }}"
        ca_path: "/path/to/ca_cert.pem"
        share_name: "192.168.0.2:/share"
        command: preview
        scp_components:
          - IDRAC
        scp_file: example_file.xml
        job_wait: true

    - name: Preview SCP with IDRAC components in XML format from a HTTP share path
      dellemc.openmanage.idrac_server_config_profile:
        idrac_ip: "{{ idrac_ip }}"
        idrac_user: "{{ idrac_user }}"
        idrac_password: "{{ idrac_password }}"
        ca_path: "/path/to/ca_cert.pem"
        share_name: "http://192.168.0.1/http-share"
        share_user: share_username
        share_password: share_password
        command: preview
        scp_components:
          - ALL
        scp_file: example_file.xml
        job_wait: true

    - name: Preview SCP with IDRAC components in XML format from a local path
      dellemc.openmanage.idrac_server_config_profile:
        idrac_ip: "{{ idrac_ip }}"
        idrac_user: "{{ idrac_user }}"
        idrac_password: "{{ idrac_password }}"
        ca_path: "/path/to/ca_cert.pem"
        share_name: "/scp_folder"
        command: preview
        scp_components:
          - IDRAC
        scp_file: example_file.json
        job_wait: false

    - name: Import SCP with IDRAC components in XML format from the XML content.
      dellemc.openmanage.idrac_server_config_profile:
        idrac_ip: "{{ idrac_ip }}"
        idrac_user: "{{ idrac_user }}"
        idrac_password: "{{ idrac_password }}"
        ca_path: "/path/to/ca_cert.pem"
        command: import
        scp_components:
          - IDRAC
        job_wait: true
        import_buffer: "<SystemConfiguration><Component FQDD='iDRAC.Embedded.1'><Attribute Name='IPMILan.1#Enable'>
          Disabled</Attribute></Component></SystemConfiguration>"

    - name: Export SCP with ALL components in XML format using HTTP proxy.
      dellemc.openmanage.idrac_server_config_profile:
        idrac_ip: "{{ idrac_ip }}"
        idrac_user: "{{ idrac_user }}"
        idrac_password: "{{ idrac_password }}"
        ca_path: "/path/to/ca_cert.pem"
        scp_components:
          - ALL
        share_name: "http://192.168.0.1/http-share"
        proxy_support: true
        proxy_server: 192.168.0.5
        proxy_port: 8080
        proxy_username: proxy_username
        proxy_password: proxy_password
        proxy_type: http
        include_in_export: passwordhashvalues
        job_wait: true

    - name: Import SCP with IDRAC and BIOS components in XML format using SOCKS4 proxy
      dellemc.openmanage.idrac_server_config_profile:
        idrac_ip: "{{ idrac_ip }}"
        idrac_user: "{{ idrac_user }}"
        idrac_password: "{{ idrac_password }}"
        ca_path: "/path/to/ca_cert.pem"
        command: import
        scp_components:
          - IDRAC
          - BIOS
        share_name: "https://192.168.0.1/http-share"
        proxy_support: true
        proxy_server: 192.168.0.6
        proxy_port: 8080
        proxy_type: socks4
        scp_file: filename.xml
        job_wait: true

    - name: Import SCP with IDRAC components in JSON format from the JSON content.
      dellemc.openmanage.idrac_server_config_profile:
        idrac_ip: "{{ idrac_ip }}"
        idrac_user: "{{ idrac_user }}"
        idrac_password: "{{ idrac_password }}"
        ca_path: "/path/to/ca_cert.pem"
        command: import
        scp_components:
          - IDRAC
        job_wait: true
        import_buffer: "{\"SystemConfiguration\": {\"Components\": [{\"FQDD\": \"iDRAC.Embedded.1\",\"Attributes\":
          [{\"Name\": \"SNMP.1#AgentCommunity\",\"Value\": \"public1\"}]}]}}"




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

      .. _ansible_collections.dellemc.openmanage.idrac_server_config_profile_module__return-error_info:

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

      .. _ansible_collections.dellemc.openmanage.idrac_server_config_profile_module__return-msg:

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

      Status of the import or export SCP job.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` always

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`"Successfully imported the Server Configuration Profile"`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-scp_status"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_server_config_profile_module__return-scp_status:

      .. rst-class:: ansible-option-title

      **scp_status**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-scp_status" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      SCP operation job and progress details from the iDRAC.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` success

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"Id": "JID\_XXXXXXXXX", "JobState": "Completed", "JobType": "ImportConfiguration", "Message": "Successfully imported and applied Server Configuration Profile.", "MessageArgs": [], "MessageId": "XXX123", "Name": "Import Configuration", "PercentComplete": 100, "StartTime": "TIME\_NOW", "Status": "Success", "TargetSettingsURI": null, "retval": true}`


      .. raw:: html

        </div>



..  Status (Presently only deprecated)


.. Authors

Authors
~~~~~~~

- Jagadeesh N V(@jagadeeshnv)
- Felix Stephen (@felixs88)
- Jennifer John (@Jennifer-John)
- Shivam Sharma (@ShivamSh3)



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

