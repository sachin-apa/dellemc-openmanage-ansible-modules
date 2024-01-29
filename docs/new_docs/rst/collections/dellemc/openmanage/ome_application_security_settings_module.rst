
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

.. _ansible_collections.dellemc.openmanage.ome_application_security_settings_module:

.. Anchors: short name for ansible.builtin

.. Anchors: aliases



.. Title

dellemc.openmanage.ome_application_security_settings module -- Configure the login security properties
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. Collection note

.. note::
    This module is part of the `dellemc.openmanage collection <https://galaxy.ansible.com/dellemc/openmanage>`_ (version 8.5.0).

    To install it, use: :code:`ansible-galaxy collection install dellemc.openmanage`.
    You need further requirements to be able to use this module,
    see :ref:`Requirements <ansible_collections.dellemc.openmanage.ome_application_security_settings_module_requirements>` for details.

    To use it in a playbook, specify: :code:`dellemc.openmanage.ome_application_security_settings`.

.. version_added

.. rst-class:: ansible-version-added

New in dellemc.openmanage 4.4.0

.. contents::
   :local:
   :depth: 1

.. Deprecated


Synopsis
--------

.. Description

- This module allows you to configure the login security properties on OpenManage Enterprise or OpenManage Enterprise Modular


.. Aliases


.. Requirements

.. _ansible_collections.dellemc.openmanage.ome_application_security_settings_module_requirements:

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

      .. _ansible_collections.dellemc.openmanage.ome_application_security_settings_module__parameter-ca_path:

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
        <div class="ansibleOptionAnchor" id="parameter-fips_mode_enable"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_security_settings_module__parameter-fips_mode_enable:

      .. rst-class:: ansible-option-title

      **fips_mode_enable**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-fips_mode_enable" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The FIPS mode is intended to meet the requirements of FIPS 140-2 level 1. For more information refer to the FIPS user guide

      This is applicable only for OpenManage Enterprise Modular only

      This is mutually exclusive with \ :emphasis:`restrict\_allowed\_ip\_range`\  and \ :emphasis:`login\_lockout\_policy`\ .

      \ :literal:`WARNING`\  Enabling or Disabling this option resets your chassis to default settings. This may cause change in IP settings and loss of network connectivity.

      \ :literal:`WARNING`\  The FIPS mode cannot be enabled on a lead chassis in a multi-chassis management configuration. To toggle enable FIPS on a lead chassis, delete the chassis group, enable FIPS and recreate the group.

      \ :literal:`WARNING`\  For a Standalone or member chassis, enabling the FIPS mode deletes any fabrics created. This may cause loss of network connectivity and data paths to the compute sleds.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-hostname"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_security_settings_module__parameter-hostname:

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

      .. _ansible_collections.dellemc.openmanage.ome_application_security_settings_module__parameter-job_wait:

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

      Provides an option to wait for job completion.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry-default:`true` :ansible-option-choices-default-mark:`← (default)`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-job_wait_timeout"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_security_settings_module__parameter-job_wait_timeout:

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

      :ansible-option-default-bold:`Default:` :ansible-option-default:`120`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-login_lockout_policy"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_security_settings_module__parameter-login_lockout_policy:

      .. rst-class:: ansible-option-title

      **login_lockout_policy**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-login_lockout_policy" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Locks the application after multiple unsuccessful login attempts.

      This is mutually exclusive with \ :emphasis:`fips\_mode\_enable`\ .


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-login_lockout_policy/by_ip_address"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_security_settings_module__parameter-login_lockout_policy/by_ip_address:

      .. rst-class:: ansible-option-title

      **by_ip_address**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-login_lockout_policy/by_ip_address" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enable or disable lockout policy settings based on the IP address. This restricts the number of unsuccessful login attempts from a specific IP address for a specific time interval.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-login_lockout_policy/by_user_name"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_security_settings_module__parameter-login_lockout_policy/by_user_name:

      .. rst-class:: ansible-option-title

      **by_user_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-login_lockout_policy/by_user_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enable or disable lockout policy settings based on the user name. This restricts the number of unsuccessful login attempts from a specific user for a specific time interval.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-login_lockout_policy/lockout_fail_count"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_security_settings_module__parameter-login_lockout_policy/lockout_fail_count:

      .. rst-class:: ansible-option-title

      **lockout_fail_count**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-login_lockout_policy/lockout_fail_count" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The number of unsuccessful login attempts that are allowed after which the appliance prevents log in from the specific  username or IP Address.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-login_lockout_policy/lockout_fail_window"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_security_settings_module__parameter-login_lockout_policy/lockout_fail_window:

      .. rst-class:: ansible-option-title

      **lockout_fail_window**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-login_lockout_policy/lockout_fail_window" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Lockout fail window is the time in seconds within which the lockout fail count event must occur to trigger the lockout penalty time. Enter the duration for which OpenManage Enterprise must display information about a failed attempt.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-login_lockout_policy/lockout_penalty_time"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_security_settings_module__parameter-login_lockout_policy/lockout_penalty_time:

      .. rst-class:: ansible-option-title

      **lockout_penalty_time**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-login_lockout_policy/lockout_penalty_time" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The duration of time, in seconds, that login attempts from the specific user or IP address must not be allowed.


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-password"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_security_settings_module__parameter-password:

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

      .. _ansible_collections.dellemc.openmanage.ome_application_security_settings_module__parameter-port:

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
        <div class="ansibleOptionAnchor" id="parameter-restrict_allowed_ip_range"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_security_settings_module__parameter-restrict_allowed_ip_range:

      .. rst-class:: ansible-option-title

      **restrict_allowed_ip_range**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-restrict_allowed_ip_range" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Restrict to allow inbound connections only from the specified IP address range.

      This is mutually exclusive with \ :emphasis:`fips\_mode\_enable`\ .

      \ :literal:`NOTE`\  When \ :emphasis:`restrict\_allowed\_ip\_range`\  is configured on the appliance, any inbound connection to the appliance, such as alert reception, firmware update, and network identities are blocked from the devices that are outside the specified IP address range. However, any outbound connection from the appliance will work on all devices.


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-restrict_allowed_ip_range/enable_ip_range"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_security_settings_module__parameter-restrict_allowed_ip_range/enable_ip_range:

      .. rst-class:: ansible-option-title

      **enable_ip_range**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-restrict_allowed_ip_range/enable_ip_range" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Allow connections based on the IP address range.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-restrict_allowed_ip_range/ip_range"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_security_settings_module__parameter-restrict_allowed_ip_range/ip_range:

      .. rst-class:: ansible-option-title

      **ip_range**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-restrict_allowed_ip_range/ip_range" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The IP address range in Classless Inter-Domain Routing (CIDR) format. For example: 192.168.100.14/24 or 2001:db8::/24


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-timeout"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_security_settings_module__parameter-timeout:

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

      .. _ansible_collections.dellemc.openmanage.ome_application_security_settings_module__parameter-username:

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

      .. _ansible_collections.dellemc.openmanage.ome_application_security_settings_module__parameter-validate_certs:

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
   - Run this module from a system that has direct access to Dell OpenManage Enterprise or OpenManage Enterprise Modular.
   - This module supports \ :literal:`check\_mode`\ .

.. Seealso


.. Examples

Examples
--------

.. code-block:: yaml+jinja

    
    ---
    - name: Configure restricted allowed IP range
      dellemc.openmanage.ome_application_security_settings:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        restrict_allowed_ip_range:
          enable_ip_range: true
          ip_range: 192.1.2.3/24

    - name: Configure login lockout policy
      dellemc.openmanage.ome_application_security_settings:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        login_lockout_policy:
          by_user_name: true
          by_ip_address: true
          lockout_fail_count: 3
          lockout_fail_window: 30
          lockout_penalty_time: 900

    - name: Configure restricted allowed IP range and login lockout policy with job wait time out of 60 seconds
      dellemc.openmanage.ome_application_security_settings:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        restrict_allowed_ip_range:
          enable_ip_range: true
          ip_range: 192.1.2.3/24
        login_lockout_policy:
          by_user_name: true
          by_ip_address: true
          lockout_fail_count: 3
          lockout_fail_window: 30
          lockout_penalty_time: 900
        job_wait_timeout: 60

    - name: Enable FIPS mode
      dellemc.openmanage.ome_application_security_settings:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        fips_mode_enable: true




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

      .. _ansible_collections.dellemc.openmanage.ome_application_security_settings_module__return-error_info:

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

      Details of http error.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` on http error

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"error": {"@Message.ExtendedInfo": [{"Message": "Unable to process the request because the domain information cannot be retrieved.", "MessageArgs": [], "MessageId": "CGEN8007", "RelatedProperties": [], "Resolution": "Verify the status of the database and domain configuration, and then retry the operation.", "Severity": "Critical"}], "code": "Base.1.0.GeneralError", "message": "A general error has occurred. See ExtendedInfo for more information."}}`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-job_id"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_security_settings_module__return-job_id:

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

      Job ID of the security configuration task.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` When security configuration properties are provided

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`10123`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-msg"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_security_settings_module__return-msg:

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

      Overall status of the login security configuration.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` always

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`"Successfully applied the security settings."`


      .. raw:: html

        </div>



..  Status (Presently only deprecated)


.. Authors

Authors
~~~~~~~

- Jagadeesh N V(@jagadeeshnv)



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

