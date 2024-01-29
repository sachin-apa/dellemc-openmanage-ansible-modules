
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

.. _ansible_collections.dellemc.openmanage.idrac_user_module:

.. Anchors: short name for ansible.builtin

.. Anchors: aliases



.. Title

dellemc.openmanage.idrac_user module -- Configure settings for user accounts
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. Collection note

.. note::
    This module is part of the `dellemc.openmanage collection <https://galaxy.ansible.com/dellemc/openmanage>`_ (version 8.5.0).

    To install it, use: :code:`ansible-galaxy collection install dellemc.openmanage`.
    You need further requirements to be able to use this module,
    see :ref:`Requirements <ansible_collections.dellemc.openmanage.idrac_user_module_requirements>` for details.

    To use it in a playbook, specify: :code:`dellemc.openmanage.idrac_user`.

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

- This module allows to perform the following,
- Add a new user account.
- Edit a user account.
- Enable or Disable a user account.


.. Aliases


.. Requirements

.. _ansible_collections.dellemc.openmanage.idrac_user_module_requirements:

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
        <div class="ansibleOptionAnchor" id="parameter-authentication_protocol"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_user_module__parameter-authentication_protocol:

      .. rst-class:: ansible-option-title

      **authentication_protocol**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-authentication_protocol" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      This option allows to configure one of the following authentication protocol types to authenticate the iDRAC user.

      Secure Hash Algorithm \ :literal:`SHA`\ .

      Message Digest 5 \ :literal:`MD5`\ .

      An authentication protocol is not configured if \ :literal:`None`\  is selected.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"None"`
      - :ansible-option-choices-entry:`"SHA"`
      - :ansible-option-choices-entry:`"MD5"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-ca_path"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_user_module__parameter-ca_path:

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
        <div class="ansibleOptionAnchor" id="parameter-custom_privilege"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_user_module__parameter-custom_privilege:

      .. rst-class:: ansible-option-title

      **custom_privilege**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-custom_privilege" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      :ansible-option-versionadded:`added in dellemc.openmanage 8.1.0`


      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The privilege level assigned to the user.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-enable"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_user_module__parameter-enable:

      .. rst-class:: ansible-option-title

      **enable**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-enable" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Provide the option to enable or disable a user from logging in to iDRAC.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-idrac_ip"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_user_module__parameter-idrac_ip:

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

      .. _ansible_collections.dellemc.openmanage.idrac_user_module__parameter-idrac_password:
      .. _ansible_collections.dellemc.openmanage.idrac_user_module__parameter-idrac_pwd:

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

      .. _ansible_collections.dellemc.openmanage.idrac_user_module__parameter-idrac_port:

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

      .. _ansible_collections.dellemc.openmanage.idrac_user_module__parameter-idrac_user:

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
        <div class="ansibleOptionAnchor" id="parameter-ipmi_lan_privilege"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_user_module__parameter-ipmi_lan_privilege:

      .. rst-class:: ansible-option-title

      **ipmi_lan_privilege**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-ipmi_lan_privilege" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The Intelligent Platform Management Interface LAN privilege level assigned to the user.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"Administrator"`
      - :ansible-option-choices-entry:`"Operator"`
      - :ansible-option-choices-entry:`"User"`
      - :ansible-option-choices-entry:`"No Access"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-ipmi_serial_privilege"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_user_module__parameter-ipmi_serial_privilege:

      .. rst-class:: ansible-option-title

      **ipmi_serial_privilege**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-ipmi_serial_privilege" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The Intelligent Platform Management Interface Serial Port privilege level assigned to the user.

      This option is only applicable for rack and tower servers.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"Administrator"`
      - :ansible-option-choices-entry:`"Operator"`
      - :ansible-option-choices-entry:`"User"`
      - :ansible-option-choices-entry:`"No Access"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-new_user_name"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_user_module__parameter-new_user_name:

      .. rst-class:: ansible-option-title

      **new_user_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-new_user_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Provide the \ :emphasis:`user\_name`\  for the account to be modified.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-privacy_protocol"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_user_module__parameter-privacy_protocol:

      .. rst-class:: ansible-option-title

      **privacy_protocol**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-privacy_protocol" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      This option allows to configure one of the following privacy encryption protocols for the iDRAC user.

      Data Encryption Standard \ :literal:`DES`\ .

      Advanced Encryption Standard \ :literal:`AES`\ .

      A privacy protocol is not configured if \ :literal:`None`\  is selected.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"None"`
      - :ansible-option-choices-entry:`"DES"`
      - :ansible-option-choices-entry:`"AES"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-privilege"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_user_module__parameter-privilege:

      .. rst-class:: ansible-option-title

      **privilege**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-privilege" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Following are the role-based privileges.

      A user with \ :literal:`Administrator`\  privilege can log in to iDRAC, and then configure iDRAC, configure users, clear logs, control and configure system, access virtual console, access virtual media, test alerts, and execute debug commands.

      A user with \ :literal:`Operator`\  privilege can log in to iDRAC, and then configure iDRAC, control and configure system, access virtual console, access virtual media, and execute debug commands.

      A user with \ :literal:`ReadOnly`\  privilege can only log in to iDRAC.

      A user with \ :literal:`None`\ , no privileges assigned.

      Will be ignored, if custom\_privilege parameter is provided.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"Administrator"`
      - :ansible-option-choices-entry:`"ReadOnly"`
      - :ansible-option-choices-entry:`"Operator"`
      - :ansible-option-choices-entry:`"None"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-protocol_enable"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_user_module__parameter-protocol_enable:

      .. rst-class:: ansible-option-title

      **protocol_enable**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-protocol_enable" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Enables protocol for the iDRAC user.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-sol_enable"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_user_module__parameter-sol_enable:

      .. rst-class:: ansible-option-title

      **sol_enable**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-sol_enable" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Enables Serial Over Lan (SOL) for an iDRAC user.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-state"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_user_module__parameter-state:

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

      Select \ :literal:`present`\  to create or modify a user account.

      Select \ :literal:`absent`\  to remove a user account.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`"present"` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`"absent"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-timeout"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_user_module__parameter-timeout:

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
        <div class="ansibleOptionAnchor" id="parameter-user_name"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_user_module__parameter-user_name:

      .. rst-class:: ansible-option-title

      **user_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-user_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Provide the \ :emphasis:`user\_name`\  of the account to be created, deleted or modified.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-user_password"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_user_module__parameter-user_password:

      .. rst-class:: ansible-option-title

      **user_password**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-user_password" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Provide the password for the user account. The password can be changed when the user account is modified.

      To ensure security, the \ :emphasis:`user\_password`\  must be at least eight characters long and must contain lowercase and upper-case characters, numbers, and special characters.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-validate_certs"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_user_module__parameter-validate_certs:

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
   - Run this module from a system that has direct access to Dell iDRAC.
   - This module supports \ :literal:`check\_mode`\ .

.. Seealso


.. Examples

Examples
--------

.. code-block:: yaml+jinja

    
    ---
    - name: Configure a new iDRAC user
      dellemc.openmanage.idrac_user:
        idrac_ip: 198.162.0.1
        idrac_user: idrac_user
        idrac_password: idrac_password
        ca_path: "/path/to/ca_cert.pem"
        state: present
        user_name: user_name
        user_password: user_password
        privilege: Administrator
        ipmi_lan_privilege: Administrator
        ipmi_serial_privilege: Administrator
        enable: true
        sol_enable: true
        protocol_enable: true
        authentication_protocol: SHA
        privacy_protocol: AES

    - name: Modify existing iDRAC user username and password
      dellemc.openmanage.idrac_user:
        idrac_ip: 198.162.0.1
        idrac_user: idrac_user
        idrac_password: idrac_password
        ca_path: "/path/to/ca_cert.pem"
        state: present
        user_name: user_name
        new_user_name: new_user_name
        user_password: user_password

    - name: Delete existing iDRAC user account
      dellemc.openmanage.idrac_user:
        idrac_ip: 198.162.0.1
        idrac_user: idrac_user
        idrac_password: idrac_password
        ca_path: "/path/to/ca_cert.pem"
        state: absent
        user_name: user_name




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

      .. _ansible_collections.dellemc.openmanage.idrac_user_module__return-error_info:

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

      .. _ansible_collections.dellemc.openmanage.idrac_user_module__return-msg:

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

      Status of the iDRAC user configuration.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` always

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`"Successfully created user account details."`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-status"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_user_module__return-status:

      .. rst-class:: ansible-option-title

      **status**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-status" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Configures the iDRAC users attributes.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` success

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"@Message.ExtendedInfo": [{"Message": "Successfully Completed Request", "MessageArgs": [], "MessageArgs@odata.count": 0, "MessageId": "Base.1.5.Success", "RelatedProperties": [], "RelatedProperties@odata.count": 0, "Resolution": "None", "Severity": "OK"}, {"Message": "The operation successfully completed.", "MessageArgs": [], "MessageArgs@odata.count": 0, "MessageId": "IDRAC.2.1.SYS413", "RelatedProperties": [], "RelatedProperties@odata.count": 0, "Resolution": "No response action is required.", "Severity": "Informational"}]}`


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

