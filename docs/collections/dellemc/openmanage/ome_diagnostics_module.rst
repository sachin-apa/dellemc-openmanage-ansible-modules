
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

.. _ansible_collections.dellemc.openmanage.ome_diagnostics_module:

.. Anchors: short name for ansible.builtin

.. Anchors: aliases



.. Title

dellemc.openmanage.ome_diagnostics module -- Export technical support logs(TSR) to network share location
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. Collection note

.. note::
    This module is part of the `dellemc.openmanage collection <https://galaxy.ansible.com/dellemc/openmanage>`_ (version 8.5.0).

    To install it, use: :code:`ansible-galaxy collection install dellemc.openmanage`.
    You need further requirements to be able to use this module,
    see :ref:`Requirements <ansible_collections.dellemc.openmanage.ome_diagnostics_module_requirements>` for details.

    To use it in a playbook, specify: :code:`dellemc.openmanage.ome_diagnostics`.

.. version_added

.. rst-class:: ansible-version-added

New in dellemc.openmanage 3.6.0

.. contents::
   :local:
   :depth: 1

.. Deprecated


Synopsis
--------

.. Description

- This module allows to export SupportAssist collection logs from OpenManage Enterprise and OpenManage Enterprise Modular and application logs from OpenManage Enterprise Modular to a CIFS or NFS share.


.. Aliases


.. Requirements

.. _ansible_collections.dellemc.openmanage.ome_diagnostics_module_requirements:

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
        <div class="ansibleOptionAnchor" id="parameter-ca_path"></div>

      .. _ansible_collections.dellemc.openmanage.ome_diagnostics_module__parameter-ca_path:

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
        <div class="ansibleOptionAnchor" id="parameter-device_group_name"></div>

      .. _ansible_collections.dellemc.openmanage.ome_diagnostics_module__parameter-device_group_name:

      .. rst-class:: ansible-option-title

      **device_group_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-device_group_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Name of the device group to export \ :literal:`support\_assist\_collection`\  or \ :literal:`supportassist\_collection`\  logs of all devices within the group.

      This is applicable for \ :literal:`support\_assist\_collection`\  and \ :literal:`supportassist\_collection`\  logs.

      This option is not applicable for OpenManage Enterprise Modular.

      This option is mutually exclusive with \ :emphasis:`device\_ids`\  and \ :emphasis:`device\_service\_tags`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-device_ids"></div>

      .. _ansible_collections.dellemc.openmanage.ome_diagnostics_module__parameter-device_ids:

      .. rst-class:: ansible-option-title

      **device_ids**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-device_ids" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      List of target device IDs.

      This is applicable for \ :literal:`support\_assist\_collection`\  and \ :literal:`supportassist\_collection`\  logs.

      This option is mutually exclusive with \ :emphasis:`device\_service\_tags`\  and \ :emphasis:`device\_group\_name`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-device_service_tags"></div>

      .. _ansible_collections.dellemc.openmanage.ome_diagnostics_module__parameter-device_service_tags:

      .. rst-class:: ansible-option-title

      **device_service_tags**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-device_service_tags" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      List of target identifier.

      This is applicable for \ :literal:`support\_assist\_collection`\  and \ :literal:`supportassist\_collection`\  logs.

      This option is mutually exclusive with \ :emphasis:`device\_ids`\  and \ :emphasis:`device\_group\_name`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-hostname"></div>

      .. _ansible_collections.dellemc.openmanage.ome_diagnostics_module__parameter-hostname:

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
        <div class="ansibleOptionAnchor" id="parameter-job_wait"></div>

      .. _ansible_collections.dellemc.openmanage.ome_diagnostics_module__parameter-job_wait:

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

      Whether to wait for the Job completion or not.

      The maximum wait time is \ :emphasis:`job\_wait\_timeout`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry-default:`true` :ansible-option-choices-default-mark:`← (default)`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-job_wait_timeout"></div>

      .. _ansible_collections.dellemc.openmanage.ome_diagnostics_module__parameter-job_wait_timeout:

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

      The maximum wait time of \ :emphasis:`job\_wait`\  in minutes.

      This option is applicable \ :emphasis:`job\_wait`\  is true.


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`60`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-lead_chassis_only"></div>

      .. _ansible_collections.dellemc.openmanage.ome_diagnostics_module__parameter-lead_chassis_only:

      .. rst-class:: ansible-option-title

      **lead_chassis_only**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-lead_chassis_only" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Extract the logs from Lead chassis only.

      \ :emphasis:`lead\_chassis\_only`\  is only applicable when \ :emphasis:`log\_type`\  is \ :literal:`application`\  on OpenManage Enterprise Modular.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`false` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-log_selectors"></div>

      .. _ansible_collections.dellemc.openmanage.ome_diagnostics_module__parameter-log_selectors:

      .. rst-class:: ansible-option-title

      **log_selectors**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-log_selectors" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      By default, the SupportAssist logs contain only hardware logs. To collect additional logs such as OS logs, RAID logs or Debug logs, specify the log types to be collected in the choices list.

      If the log types are not specified, only the hardware logs are exported.

      \ :literal:`OS\_LOGS`\  to collect OS Logs.

      \ :literal:`RAID\_LOGS`\  to collect RAID controller logs.

      \ :literal:`DEBUG\_LOGS`\  to collect Debug logs.

      This option is applicable only for \ :literal:`support\_assist\_collection`\  and \ :literal:`supportassist\_collection`\  of \ :emphasis:`log\_type`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"OS\_LOGS"`
      - :ansible-option-choices-entry:`"RAID\_LOGS"`
      - :ansible-option-choices-entry:`"DEBUG\_LOGS"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-log_type"></div>

      .. _ansible_collections.dellemc.openmanage.ome_diagnostics_module__parameter-log_type:

      .. rst-class:: ansible-option-title

      **log_type**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-log_type" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      \ :literal:`application`\  is applicable for OpenManage Enterprise Modular to export the application log bundle.

      \ :literal:`support\_assist\_collection`\  and \ :literal:`supportassist\_collection`\  is applicable for one or more devices to export SupportAssist logs.

      \ :literal:`support\_assist\_collection`\  and \ :literal:`supportassist\_collection`\  supports both OpenManage Enterprise and OpenManage Enterprise Modular.

      \ :literal:`support\_assist\_collection`\  and \ :literal:`supportassist\_collection`\  does not support export of \ :literal:`OS\_LOGS`\  from OpenManage Enterprise. If tried to export, the tasks will complete with errors, and the module fails.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"application"`
      - :ansible-option-choices-entry-default:`"support\_assist\_collection"` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`"supportassist\_collection"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-mask_sensitive_info"></div>

      .. _ansible_collections.dellemc.openmanage.ome_diagnostics_module__parameter-mask_sensitive_info:

      .. rst-class:: ansible-option-title

      **mask_sensitive_info**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-mask_sensitive_info" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Select this option to mask the personal identification information such as IPAddress, DNS, alert destination, email, gateway, inet6, MacAddress, netmask etc.

      This option is applicable for \ :literal:`application`\  of \ :emphasis:`log\_type`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`false` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-password"></div>

      .. _ansible_collections.dellemc.openmanage.ome_diagnostics_module__parameter-password:

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

      .. _ansible_collections.dellemc.openmanage.ome_diagnostics_module__parameter-port:

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
        <div class="ansibleOptionAnchor" id="parameter-share_address"></div>

      .. _ansible_collections.dellemc.openmanage.ome_diagnostics_module__parameter-share_address:

      .. rst-class:: ansible-option-title

      **share_address**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-share_address" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Network share IP address.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-share_domain"></div>

      .. _ansible_collections.dellemc.openmanage.ome_diagnostics_module__parameter-share_domain:

      .. rst-class:: ansible-option-title

      **share_domain**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-share_domain" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Network share domain name.

      This option is applicable for \ :literal:`CIFS`\  if \ :emphasis:`share\_type`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-share_name"></div>

      .. _ansible_collections.dellemc.openmanage.ome_diagnostics_module__parameter-share_name:

      .. rst-class:: ansible-option-title

      **share_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-share_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Network share path.

      Filename is auto generated and should not be provided as part of \ :emphasis:`share\_name`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-share_password"></div>

      .. _ansible_collections.dellemc.openmanage.ome_diagnostics_module__parameter-share_password:

      .. rst-class:: ansible-option-title

      **share_password**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-share_password" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Network share password

      This option is applicable for \ :literal:`CIFS`\  of \ :emphasis:`share\_type`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-share_type"></div>

      .. _ansible_collections.dellemc.openmanage.ome_diagnostics_module__parameter-share_type:

      .. rst-class:: ansible-option-title

      **share_type**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-share_type" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Network share type


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"NFS"`
      - :ansible-option-choices-entry:`"CIFS"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-share_user"></div>

      .. _ansible_collections.dellemc.openmanage.ome_diagnostics_module__parameter-share_user:

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

      Network share username.

      This option is applicable for \ :literal:`CIFS`\  of \ :emphasis:`share\_type`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-test_connection"></div>

      .. _ansible_collections.dellemc.openmanage.ome_diagnostics_module__parameter-test_connection:

      .. rst-class:: ansible-option-title

      **test_connection**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-test_connection" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Test the availability of the network share location.

      \ :emphasis:`job\_wait`\  and \ :emphasis:`job\_wait\_timeout`\  options are not applicable for \ :emphasis:`test\_connection`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`false` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-timeout"></div>

      .. _ansible_collections.dellemc.openmanage.ome_diagnostics_module__parameter-timeout:

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

      .. _ansible_collections.dellemc.openmanage.ome_diagnostics_module__parameter-username:

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

      .. _ansible_collections.dellemc.openmanage.ome_diagnostics_module__parameter-validate_certs:

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
   - Run this module from a system that has direct access to OpenManage Enterprise.
   - This module performs the test connection and device validations. It does not create a job for copying the logs in check mode and always reports as changes found.
   - This module supports \ :literal:`check\_mode`\ .

.. Seealso


.. Examples

Examples
--------

.. code-block:: yaml+jinja

    
    ---
    - name: Export application log using CIFS share location
      dellemc.openmanage.ome_diagnostics:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        share_type: CIFS
        share_address: "192.168.0.2"
        share_user: share_username
        share_password: share_password
        share_name: cifs_share
        log_type: application
        mask_sensitive_info: false
        test_connection: true

    - name: Export application log using NFS share location
      dellemc.openmanage.ome_diagnostics:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        share_address: "192.168.0.3"
        share_type: NFS
        share_name: nfs_share
        log_type: application
        mask_sensitive_info: true
        test_connection: true

    - name: Export SupportAssist log using CIFS share location
      dellemc.openmanage.ome_diagnostics:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        share_address: "192.168.0.3"
        share_user: share_username
        share_password: share_password
        share_name: cifs_share
        share_type: CIFS
        log_type: support_assist_collection
        device_ids: [10011, 10022]
        log_selectors: [OS_LOGS]
        test_connection: true

    - name: Export SupportAssist log using NFS share location
      dellemc.openmanage.ome_diagnostics:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        share_address: "192.168.0.3"
        share_type: NFS
        share_name: nfs_share
        log_type: support_assist_collection
        device_group_name: group_name
        test_connection: true




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

      .. _ansible_collections.dellemc.openmanage.ome_diagnostics_module__return-error_info:

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
        <div class="ansibleOptionAnchor" id="return-jog_status"></div>

      .. _ansible_collections.dellemc.openmanage.ome_diagnostics_module__return-jog_status:

      .. rst-class:: ansible-option-title

      **jog_status**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-jog_status" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Details of the export log operation status.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` success

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"Builtin": false, "CreatedBy": "root", "Editable": true, "EndTime": "None", "Id": 12778, "JobDescription": "Export device log", "JobName": "Export Log", "JobStatus": {"Id": 2080, "Name": "New"}, "JobType": {"Id": 18, "Internal": false, "Name": "DebugLogs\_Task"}, "LastRun": "2021-07-06 10:52:50.519", "LastRunStatus": {"Id": 2060, "Name": "Completed"}, "NextRun": "None", "Params": [{"JobId": 12778, "Key": "maskSensitiveInfo", "Value": "FALSE"}, {"JobId": 12778, "Key": "password", "Value": "tY86w7q92u0QzvykuF0gQQ"}, {"JobId": 12778, "Key": "userName", "Value": "administrator"}, {"JobId": 12778, "Key": "shareName", "Value": "iso"}, {"JobId": 12778, "Key": "OPERATION\_NAME", "Value": "EXTRACT\_LOGS"}, {"JobId": 12778, "Key": "shareType", "Value": "CIFS"}, {"JobId": 12778, "Key": "shareAddress", "Value": "100.96.32.142"}], "Schedule": "startnow", "StartTime": "None", "State": "Enabled", "Targets": [{"Data": "", "Id": 10053, "JobId": 12778, "TargetType": {"Id": 1000, "Name": "DEVICE"}}], "UpdatedBy": "None", "UserGenerated": true, "Visible": true}`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-msg"></div>

      .. _ansible_collections.dellemc.openmanage.ome_diagnostics_module__return-msg:

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

      Overall status of the export log.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` always

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`"Export log job completed successfully."`


      .. raw:: html

        </div>



..  Status (Presently only deprecated)


.. Authors

Authors
~~~~~~~

- Felix Stephen (@felixs88)
- Sachin Apagundi(@sachin-apa)



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

