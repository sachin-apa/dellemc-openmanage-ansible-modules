
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

.. _ansible_collections.dellemc.openmanage.ome_application_network_settings_module:

.. Anchors: short name for ansible.builtin

.. Anchors: aliases



.. Title

dellemc.openmanage.ome_application_network_settings module -- This module allows you to configure the session inactivity timeout settings
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. Collection note

.. note::
    This module is part of the `dellemc.openmanage collection <https://galaxy.ansible.com/dellemc/openmanage>`_ (version 8.5.0).

    To install it, use: :code:`ansible-galaxy collection install dellemc.openmanage`.
    You need further requirements to be able to use this module,
    see :ref:`Requirements <ansible_collections.dellemc.openmanage.ome_application_network_settings_module_requirements>` for details.

    To use it in a playbook, specify: :code:`dellemc.openmanage.ome_application_network_settings`.

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

- This module allows you to configure the session inactivity timeout settings on OpenManage Enterprise and OpenManage Enterprise Modular.


.. Aliases


.. Requirements

.. _ansible_collections.dellemc.openmanage.ome_application_network_settings_module_requirements:

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

      .. _ansible_collections.dellemc.openmanage.ome_application_network_settings_module__parameter-ca_path:

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
        <div class="ansibleOptionAnchor" id="parameter-hostname"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_network_settings_module__parameter-hostname:

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
        <div class="ansibleOptionAnchor" id="parameter-password"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_network_settings_module__parameter-password:

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

      .. _ansible_collections.dellemc.openmanage.ome_application_network_settings_module__parameter-port:

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
        <div class="ansibleOptionAnchor" id="parameter-session_inactivity_timeout"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_network_settings_module__parameter-session_inactivity_timeout:

      .. rst-class:: ansible-option-title

      **session_inactivity_timeout**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-session_inactivity_timeout" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Session inactivity timeout settings.


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-session_inactivity_timeout/api_sessions"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_network_settings_module__parameter-session_inactivity_timeout/api_sessions:

      .. rst-class:: ansible-option-title

      **api_sessions**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-session_inactivity_timeout/api_sessions" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The maximum number of API sessions to be allowed.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-session_inactivity_timeout/api_timeout"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_network_settings_module__parameter-session_inactivity_timeout/api_timeout:

      .. rst-class:: ansible-option-title

      **api_timeout**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-session_inactivity_timeout/api_timeout" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`float`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Duration of inactivity in minutes after which the API session ends.

      This is mutually exclusive with \ :emphasis:`universal\_timeout`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-session_inactivity_timeout/enable_universal_timeout"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_network_settings_module__parameter-session_inactivity_timeout/enable_universal_timeout:

      .. rst-class:: ansible-option-title

      **enable_universal_timeout**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-session_inactivity_timeout/enable_universal_timeout" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enable or disable the universal inactivity timeout.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-session_inactivity_timeout/gui_sessions"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_network_settings_module__parameter-session_inactivity_timeout/gui_sessions:

      .. rst-class:: ansible-option-title

      **gui_sessions**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-session_inactivity_timeout/gui_sessions" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The maximum number of GUI sessions to be allowed.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-session_inactivity_timeout/gui_timeout"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_network_settings_module__parameter-session_inactivity_timeout/gui_timeout:

      .. rst-class:: ansible-option-title

      **gui_timeout**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-session_inactivity_timeout/gui_timeout" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`float`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Duration of inactivity in minutes after which the web interface of Graphical User Interface (GUI) session ends.

      This is mutually exclusive with \ :emphasis:`universal\_timeout`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-session_inactivity_timeout/serial_sessions"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_network_settings_module__parameter-session_inactivity_timeout/serial_sessions:

      .. rst-class:: ansible-option-title

      **serial_sessions**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-session_inactivity_timeout/serial_sessions" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The maximum number of serial console sessions to be allowed.

      This is applicable only for OpenManage Enterprise Modular.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-session_inactivity_timeout/serial_timeout"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_network_settings_module__parameter-session_inactivity_timeout/serial_timeout:

      .. rst-class:: ansible-option-title

      **serial_timeout**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-session_inactivity_timeout/serial_timeout" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`float`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Duration of inactivity in minutes after which the serial console session ends.

      This is applicable only for OpenManage Enterprise Modular.

      This is mutually exclusive with \ :emphasis:`universal\_timeout`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-session_inactivity_timeout/ssh_sessions"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_network_settings_module__parameter-session_inactivity_timeout/ssh_sessions:

      .. rst-class:: ansible-option-title

      **ssh_sessions**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-session_inactivity_timeout/ssh_sessions" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The maximum number of SSH sessions to be allowed.

      This is applicable to OME-M only.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-session_inactivity_timeout/ssh_timeout"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_network_settings_module__parameter-session_inactivity_timeout/ssh_timeout:

      .. rst-class:: ansible-option-title

      **ssh_timeout**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-session_inactivity_timeout/ssh_timeout" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`float`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Duration of inactivity in minutes after which the SSH session ends.

      This is applicable only for OpenManage Enterprise Modular.

      This is mutually exclusive with \ :emphasis:`universal\_timeout`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-session_inactivity_timeout/universal_timeout"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_network_settings_module__parameter-session_inactivity_timeout/universal_timeout:

      .. rst-class:: ansible-option-title

      **universal_timeout**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-session_inactivity_timeout/universal_timeout" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`float`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Duration of inactivity in minutes after which all sessions end.

      This is applicable when \ :emphasis:`enable\_universal\_timeout`\  is \ :literal:`true`\ .

      This is mutually exclusive with \ :emphasis:`api\_timeout`\ , \ :emphasis:`gui\_timeout`\ , \ :emphasis:`ssh\_timeout`\  and \ :emphasis:`serial\_timeout`\ .


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-timeout"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_network_settings_module__parameter-timeout:

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

      .. _ansible_collections.dellemc.openmanage.ome_application_network_settings_module__parameter-username:

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

      .. _ansible_collections.dellemc.openmanage.ome_application_network_settings_module__parameter-validate_certs:

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
   - To configure other network settings such as network address, web server, and so on, refer to the respective OpenManage Enterprise application network setting modules.
   - This module supports \ :literal:`check\_mode`\ .

.. Seealso


.. Examples

Examples
--------

.. code-block:: yaml+jinja

    
    ---
    - name: Configure universal inactivity timeout
      ome_application_network_settings:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        session_inactivity_timeout:
          enable_universal_timeout: true
          universal_timeout: 30
          api_sessions: 90
          gui_sessions: 5
          ssh_sessions: 2
          serial_sessions: 1

    - name: Configure API and GUI timeout and sessions
      ome_application_network_settings:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        session_inactivity_timeout:
          api_timeout: 20
          api_sessions: 100
          gui_timeout: 25
          gui_sessions: 5

    - name: Configure timeout and sessions for all parameters
      ome_application_network_settings:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        session_inactivity_timeout:
          api_timeout: 20
          api_sessions: 100
          gui_timeout: 15
          gui_sessions: 5
          ssh_timeout: 30
          ssh_sessions: 2
          serial_timeout: 35
          serial_sessions: 1

    - name: Disable universal timeout and configure timeout and sessions for other parameters
      ome_application_network_settings:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        session_inactivity_timeout:
          enable_universal_timeout: false
          api_timeout: 20
          api_sessions: 100
          gui_timeout: 15
          gui_sessions: 5
          ssh_timeout: 30
          ssh_sessions: 2
          serial_timeout: 35
          serial_sessions: 1




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

      .. _ansible_collections.dellemc.openmanage.ome_application_network_settings_module__return-error_info:

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

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"error": {"@Message.ExtendedInfo": [{"Message": "The number of allowed concurrent sessions for API must be between 1 and 100 sessions.", "MessageArgs": ["API", "1", "100"], "MessageId": "CUSR1233", "RelatedProperties": [], "Resolution": "Enter values in the correct range and retry the operation.", "Severity": "Critical"}], "code": "Base.1.0.GeneralError", "message": "A general error has occurred. See ExtendedInfo for more information."}}`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-msg"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_network_settings_module__return-msg:

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

      Overall status of the Session timeout settings.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` always

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`"Successfully updated the session timeout settings."`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-session_inactivity_setting"></div>

      .. _ansible_collections.dellemc.openmanage.ome_application_network_settings_module__return-session_inactivity_setting:

      .. rst-class:: ansible-option-title

      **session_inactivity_setting**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-session_inactivity_setting" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Returned when session inactivity timeout settings are updated successfully.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` success

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`[{"MaxSessionTimeout": 86400000, "MaxSessions": 32, "MaxSessionsAllowed": 100, "MaxSessionsConfigurable": true, "MinSessionTimeout": 60000, "MinSessionsAllowed": 1, "SessionTimeout": 99600, "SessionTimeoutConfigurable": true, "SessionType": "API"}, {"MaxSessionTimeout": 7200000, "MaxSessions": 6, "MaxSessionsAllowed": 6, "MaxSessionsConfigurable": true, "MinSessionTimeout": 60000, "MinSessionsAllowed": 1, "SessionTimeout": 99600, "SessionTimeoutConfigurable": true, "SessionType": "GUI"}, {"MaxSessionTimeout": 10800000, "MaxSessions": 4, "MaxSessionsAllowed": 4, "MaxSessionsConfigurable": true, "MinSessionTimeout": 60000, "MinSessionsAllowed": 1, "SessionTimeout": 99600, "SessionTimeoutConfigurable": true, "SessionType": "SSH"}, {"MaxSessionTimeout": 86400000, "MaxSessions": 1, "MaxSessionsAllowed": 1, "MaxSessionsConfigurable": false, "MinSessionTimeout": 60000, "MinSessionsAllowed": 1, "SessionTimeout": 99600, "SessionTimeoutConfigurable": true, "SessionType": "Serial"}, {"MaxSessionTimeout": 86400000, "MaxSessions": 0, "MaxSessionsAllowed": 0, "MaxSessionsConfigurable": false, "MinSessionTimeout": -1, "MinSessionsAllowed": 0, "SessionTimeout": -1, "SessionTimeoutConfigurable": true, "SessionType": "UniversalTimeout"}]`


      .. raw:: html

        </div>



..  Status (Presently only deprecated)


.. Authors

Authors
~~~~~~~

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

