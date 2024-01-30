
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

.. _ansible_collections.dellemc.openmanage.idrac_import_server_config_profile_role:

.. Anchors: aliases


.. Title

dellemc.openmanage.idrac_import_server_config_profile role -- Import iDRAC Server Configuration Profile (SCP)
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. Collection note

.. note::
    This role is part of the `dellemc.openmanage collection <https://galaxy.ansible.com/dellemc/openmanage>`_ (version 8.5.0).

    To install it use: :code:`ansible-galaxy collection install dellemc.openmanage`.

    To use it in a playbook, specify: :code:`dellemc.openmanage.idrac_import_server_config_profile`.

.. contents::
   :local:
   :depth: 2


.. Entry point title

Entry point ``main`` -- Import iDRAC Server Configuration Profile (SCP)
-----------------------------------------------------------------------

.. version_added

.. rst-class:: ansible-version-added

New in dellemc.openmanage 7.4.0

.. Deprecated


Synopsis
^^^^^^^^

.. Description

- The role performs Import operation of Server Configuration Profile.

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
        <div class="ansibleOptionAnchor" id="parameter-main--ca_path"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_import_server_config_profile_role__parameter-main__ca_path:

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
        <div class="ansibleOptionAnchor" id="parameter-main--end_host_power_state"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_import_server_config_profile_role__parameter-main__end_host_power_state:

      .. rst-class:: ansible-option-title

      **end_host_power_state**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--end_host_power_state" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-main--hostname"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_import_server_config_profile_role__parameter-main__hostname:

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

      .. _ansible_collections.dellemc.openmanage.idrac_import_server_config_profile_role__parameter-main__https_port:

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

      .. _ansible_collections.dellemc.openmanage.idrac_import_server_config_profile_role__parameter-main__https_timeout:

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
        <div class="ansibleOptionAnchor" id="parameter-main--import_buffer"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_import_server_config_profile_role__parameter-main__import_buffer:

      .. rst-class:: ansible-option-title

      **import_buffer**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--import_buffer" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




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
        <div class="ansibleOptionAnchor" id="parameter-main--password"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_import_server_config_profile_role__parameter-main__password:

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
        <div class="ansibleOptionAnchor" id="parameter-main--share_parameters"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_import_server_config_profile_role__parameter-main__share_parameters:

      .. rst-class:: ansible-option-title

      **share_parameters**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--share_parameters" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Network share parameters.


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--share_parameters/ignore_certificate_warning"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_import_server_config_profile_role__parameter-main__share_parameters/ignore_certificate_warning:

      .. rst-class:: ansible-option-title

      **ignore_certificate_warning**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--share_parameters/ignore_certificate_warning" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

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

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--share_parameters/proxy_password"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_import_server_config_profile_role__parameter-main__share_parameters/proxy_password:

      .. rst-class:: ansible-option-title

      **proxy_password**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--share_parameters/proxy_password" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Proxy password to authenticate.

      \ :emphasis:`proxy\_password`\  is considered only when \ :emphasis:`share\_name`\  is of type HTTP or HTTPS and is supported only on iDRAC9.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--share_parameters/proxy_port"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_import_server_config_profile_role__parameter-main__share_parameters/proxy_port:

      .. rst-class:: ansible-option-title

      **proxy_port**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--share_parameters/proxy_port" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Proxy port to authenticate.

      \ :emphasis:`proxy\_port`\  is required when \ :emphasis:`share\_name`\  is of type HTTPS or HTTP and \ :emphasis:`proxy\_support`\  is \ :literal:`true`\ .

      \ :emphasis:`proxy\_port`\  is considered only when \ :emphasis:`share\_name`\  is of type HTTP or HTTPS and is supported only on iDRAC9.


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`80`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--share_parameters/proxy_server"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_import_server_config_profile_role__parameter-main__share_parameters/proxy_server:

      .. rst-class:: ansible-option-title

      **proxy_server**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--share_parameters/proxy_server" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      \ :emphasis:`proxy\_server`\  is required when \ :emphasis:`share\_name`\  is of type HTTPS or HTTP and \ :emphasis:`proxy\_support`\  is \ :literal:`true`\ .

      \ :emphasis:`proxy\_server`\  is considered only when \ :emphasis:`share\_name`\  is of type HTTP or HTTPS and is supported only on iDRAC9.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--share_parameters/proxy_support"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_import_server_config_profile_role__parameter-main__share_parameters/proxy_support:

      .. rst-class:: ansible-option-title

      **proxy_support**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--share_parameters/proxy_support" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Proxy to be enabled or disabled.

      \ :emphasis:`proxy\_support`\  is considered only when \ :emphasis:`share\_name`\  is of type HTTP or HTTPS and is supported only on iDRAC9.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`false` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--share_parameters/proxy_type"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_import_server_config_profile_role__parameter-main__share_parameters/proxy_type:

      .. rst-class:: ansible-option-title

      **proxy_type**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--share_parameters/proxy_type" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

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

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--share_parameters/proxy_username"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_import_server_config_profile_role__parameter-main__share_parameters/proxy_username:

      .. rst-class:: ansible-option-title

      **proxy_username**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--share_parameters/proxy_username" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Proxy username to authenticate.

      \ :emphasis:`proxy\_username`\  is considered only when \ :emphasis:`share\_name`\  is of type HTTP or HTTPS and is supported only on iDRAC9.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--share_parameters/scp_file"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_import_server_config_profile_role__parameter-main__share_parameters/scp_file:

      .. rst-class:: ansible-option-title

      **scp_file**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--share_parameters/scp_file" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Name of the server configuration profile (SCP) file.

      This option is mandatory if \ :emphasis:`command`\  is \ :literal:`import`\ .

      The default format \<idrac\_ip\>\_YYMMDD\_HHMMSS\_scp is used if this option is not specified for \ :literal:`import`\ .

      \ :emphasis:`export\_format`\  is used if the valid extension file is not provided for \ :literal:`export`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--share_parameters/share_name"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_import_server_config_profile_role__parameter-main__share_parameters/share_name:

      .. rst-class:: ansible-option-title

      **share_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--share_parameters/share_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Network share or local path.

      CIFS, NFS, HTTP, and HTTPS network share types are supported.

      \ :emphasis:`share\_name`\  is mutually exclusive with \ :emphasis:`import\_buffer`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--share_parameters/share_password"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_import_server_config_profile_role__parameter-main__share_parameters/share_password:

      .. rst-class:: ansible-option-title

      **share_password**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--share_parameters/share_password" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Network share user password. This option is mandatory for CIFS Network Share.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--share_parameters/share_user"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_import_server_config_profile_role__parameter-main__share_parameters/share_user:

      .. rst-class:: ansible-option-title

      **share_user**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--share_parameters/share_user" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Network share user in the format 'user@domain' or 'domain\\\\user' if user is part of a domain else 'user'. This option is mandatory for CIFS Network Share.


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--shutdown_type"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_import_server_config_profile_role__parameter-main__shutdown_type:

      .. rst-class:: ansible-option-title

      **shutdown_type**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--shutdown_type" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-main--target"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_import_server_config_profile_role__parameter-main__target:

      .. rst-class:: ansible-option-title

      **target**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--target" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      If \ :literal:`ALL`\ , this module exports or imports all components configurations from SCP file.

      If \ :literal:`IDRAC`\ , this module exports or imports iDRAC configuration from SCP file.

      If \ :literal:`BIOS`\ , this module exports or imports BIOS configuration from SCP file.

      If \ :literal:`NIC`\ , this module exports or imports NIC configuration from SCP file.

      If \ :literal:`RAID`\ , this module exports or imports RAID configuration from SCP file.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`"ALL"` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`"IDRAC"`
      - :ansible-option-choices-entry:`"BIOS"`
      - :ansible-option-choices-entry:`"NIC"`
      - :ansible-option-choices-entry:`"RAID"`


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`["ALL"]`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--username"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_import_server_config_profile_role__parameter-main__username:

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

      .. _ansible_collections.dellemc.openmanage.idrac_import_server_config_profile_role__parameter-main__validate_certs:

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

