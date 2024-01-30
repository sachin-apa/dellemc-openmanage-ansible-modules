
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

.. _ansible_collections.dellemc.openmanage.idrac_attributes_module:

.. Anchors: short name for ansible.builtin

.. Anchors: aliases



.. Title

dellemc.openmanage.idrac_attributes module -- Configure the iDRAC attributes.
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. Collection note

.. note::
    This module is part of the `dellemc.openmanage collection <https://galaxy.ansible.com/dellemc/openmanage>`_ (version 8.5.0).

    To install it, use: :code:`ansible-galaxy collection install dellemc.openmanage`.
    You need further requirements to be able to use this module,
    see :ref:`Requirements <ansible_collections.dellemc.openmanage.idrac_attributes_module_requirements>` for details.

    To use it in a playbook, specify: :code:`dellemc.openmanage.idrac_attributes`.

.. version_added

.. rst-class:: ansible-version-added

New in dellemc.openmanage 6.0.0

.. contents::
   :local:
   :depth: 1

.. Deprecated


Synopsis
--------

.. Description

- This module allows to configure the iDRAC attributes.


.. Aliases


.. Requirements

.. _ansible_collections.dellemc.openmanage.idrac_attributes_module_requirements:

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

      .. _ansible_collections.dellemc.openmanage.idrac_attributes_module__parameter-ca_path:

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
        <div class="ansibleOptionAnchor" id="parameter-idrac_attributes"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_attributes_module__parameter-idrac_attributes:

      .. rst-class:: ansible-option-title

      **idrac_attributes**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-idrac_attributes" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Dictionary of iDRAC attributes and value. The attributes should be part of the Integrated Dell Remote Access Controller Attribute Registry. To view the list of attributes in Attribute Registry for iDRAC9 and above, see, \ https://I%28idrac_ip\ /redfish/v1/Managers/iDRAC.Embedded.1/Oem/Dell/DellAttributes/iDRAC.Embedded.1) and \ https://I%28idrac_ip\ /redfish/v1/Registries/ManagerAttributeRegistry).

      For iDRAC8 based servers, derive the manager attribute name from Server Configuration Profile. If the manager attribute name in Server Configuration Profile is \<GroupName\>.\<Instance\>#\<AttributeName\> (for Example, 'SNMP.1#AgentCommunity') then the equivalent attribute name for Redfish is \<GroupName\>.\<Instance\>.\<AttributeName\> (for Example, 'SNMP.1.AgentCommunity').


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-idrac_ip"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_attributes_module__parameter-idrac_ip:

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

      .. _ansible_collections.dellemc.openmanage.idrac_attributes_module__parameter-idrac_password:
      .. _ansible_collections.dellemc.openmanage.idrac_attributes_module__parameter-idrac_pwd:

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

      .. _ansible_collections.dellemc.openmanage.idrac_attributes_module__parameter-idrac_port:

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

      .. _ansible_collections.dellemc.openmanage.idrac_attributes_module__parameter-idrac_user:

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
        <div class="ansibleOptionAnchor" id="parameter-lifecycle_controller_attributes"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_attributes_module__parameter-lifecycle_controller_attributes:

      .. rst-class:: ansible-option-title

      **lifecycle_controller_attributes**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-lifecycle_controller_attributes" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Dictionary of Lifecycle Controller attributes and value. The attributes should be part of the Integrated Dell Remote Access Controller Attribute Registry.To view the list of attributes in Attribute Registry for iDRAC9 and above, see, \ https://I%28idrac_ip\ /redfish/v1/Managers/iDRAC.Embedded.1/Oem/Dell/DellAttributes/LifecycleController.Embedded.1) and \ https://I%28idrac_ip\ /redfish/v1/Registries/ManagerAttributeRegistry).

      For iDRAC8 based servers, derive the manager attribute name from Server Configuration Profile. If the manager attribute name in Server Configuration Profile is \<GroupName\>.\<Instance\>#\<AttributeName\> (for Example, 'LCAttributes.1#AutoUpdate') then the equivalent attribute name for Redfish is \<GroupName\>.\<Instance\>.\<AttributeName\> (for Example, 'LCAttributes.1.AutoUpdate').


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-resource_id"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_attributes_module__parameter-resource_id:

      .. rst-class:: ansible-option-title

      **resource_id**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-resource_id" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-system_attributes"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_attributes_module__parameter-system_attributes:

      .. rst-class:: ansible-option-title

      **system_attributes**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-system_attributes" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Dictionary of System attributes and value. The attributes should be part of the Integrated Dell Remote Access Controller Attribute Registry. To view the list of attributes in Attribute Registry for iDRAC9 and above, see, \ https://I%28idrac_ip\ /redfish/v1/Managers/iDRAC.Embedded.1/Oem/Dell/DellAttributes/System.Embedded.1) and \ https://I%28idrac_ip\ /redfish/v1/Registries/ManagerAttributeRegistry).

      For iDRAC8 based servers, derive the manager attribute name from Server Configuration Profile. If the manager attribute name in Server Configuration Profile is \<GroupName\>.\<Instance\>#\<AttributeName\> (for Example, 'ThermalSettings.1#ThermalProfile') then the equivalent attribute name for Redfish is \<GroupName\>.\<Instance\>.\<AttributeName\> (for Example, 'ThermalSettings.1.ThermalProfile').


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-timeout"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_attributes_module__parameter-timeout:

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

      .. _ansible_collections.dellemc.openmanage.idrac_attributes_module__parameter-validate_certs:

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
   - For iDRAC8 based servers, the value provided for the attributes are not be validated. Ensure appropriate values are passed.

.. Seealso


.. Examples

Examples
--------

.. code-block:: yaml+jinja

    
    ---
    - name: Configure iDRAC attributes
      dellemc.openmanage.idrac_attributes:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        idrac_attributes:
          SNMP.1.AgentCommunity: public

    - name: Configure System attributes
      dellemc.openmanage.idrac_attributes:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        system_attributes:
          ThermalSettings.1.ThermalProfile: Sound Cap

    - name: Configure Lifecycle Controller attributes
      dellemc.openmanage.idrac_attributes:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        lifecycle_controller_attributes:
          LCAttributes.1.AutoUpdate: Enabled

    - name: Configure the iDRAC attributes for email alert settings.
      dellemc.openmanage.idrac_attributes:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        idrac_attributes:
          EmailAlert.1.CustomMsg: Display Message
          EmailAlert.1.Enable: Enabled
          EmailAlert.1.Address: test@test.com

    - name: Configure the iDRAC attributes for SNMP alert settings.
      dellemc.openmanage.idrac_attributes:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        idrac_attributes:
          SNMPAlert.1.Destination: 192.168.0.2
          SNMPAlert.1.State: Enabled
          SNMPAlert.1.SNMPv3Username: username

    - name: Configure the iDRAC attributes for SMTP alert settings.
      dellemc.openmanage.idrac_attributes:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        idrac_attributes:
          RemoteHosts.1.SMTPServerIPAddress: 192.168.0.3
          RemoteHosts.1.SMTPAuthentication: Enabled
          RemoteHosts.1.SMTPPort: 25
          RemoteHosts.1.SMTPUserName: username
          RemoteHosts.1.SMTPPassword: password

    - name: Configure the iDRAC attributes for webserver settings.
      dellemc.openmanage.idrac_attributes:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        idrac_attributes:
          WebServer.1.SSLEncryptionBitLength: 128-Bit or higher
          WebServer.1.TLSProtocol: TLS 1.1 and Higher

    - name: Configure the iDRAC attributes for SNMP settings.
      dellemc.openmanage.idrac_attributes:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        idrac_attributes:
          SNMP.1.SNMPProtocol: All
          SNMP.1.AgentEnable: Enabled
          SNMP.1.TrapFormat: SNMPv1
          SNMP.1.AlertPort: 162
          SNMP.1.AgentCommunity: public

    - name: Configure the iDRAC LC attributes for collecting system inventory.
      dellemc.openmanage.idrac_attributes:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        lifecycle_controller_attributes:
          LCAttributes.1.CollectSystemInventoryOnRestart: Enabled

    - name: Configure the iDRAC system attributes for LCD configuration.
      dellemc.openmanage.idrac_attributes:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        system_attributes:
          LCD.1.Configuration: Service Tag
          LCD.1.vConsoleIndication: Enabled
          LCD.1.FrontPanelLocking: Full-Access
          LCD.1.UserDefinedString: custom string

    - name: Configure the iDRAC attributes for Timezone settings.
      dellemc.openmanage.idrac_attributes:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        idrac_attributes:
          Time.1.Timezone: CST6CDT
          NTPConfigGroup.1.NTPEnable: Enabled
          NTPConfigGroup.1.NTP1: 192.168.0.5
          NTPConfigGroup.1.NTP2: 192.168.0.6
          NTPConfigGroup.1.NTP3: 192.168.0.7

    - name: Configure all attributes
      dellemc.openmanage.idrac_attributes:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        idrac_attributes:
          SNMP.1.AgentCommunity: test
          SNMP.1.AgentEnable: Enabled
          SNMP.1.DiscoveryPort: 161
        system_attributes:
          ServerOS.1.HostName: demohostname
        lifecycle_controller_attributes:
          LCAttributes.1.AutoUpdate: Disabled




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

      .. _ansible_collections.dellemc.openmanage.idrac_attributes_module__return-error_info:

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

      Error information of the operation.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` when attribute value is invalid.

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"error": {"@Message.ExtendedInfo": [{"Message": "The value 'false' for the property LCAttributes.1.BIOSRTDRequested is of a different type than the property can accept.", "MessageArgs": ["false", "LCAttributes.1.BIOSRTDRequested"], "MessageArgs@odata.count": 2, "MessageId": "Base.1.12.PropertyValueTypeError", "RelatedProperties": ["#/Attributes/LCAttributes.1.BIOSRTDRequested"], "RelatedProperties@odata.count": 1, "Resolution": "Correct the value for the property in the request body and resubmit the request if the operation failed.", "Severity": "Warning"}], "code": "Base.1.12.GeneralError", "message": "A general error has occurred. See ExtendedInfo for more information"}}`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-invalid_attributes"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_attributes_module__return-invalid_attributes:

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

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"LCAttributes.1.AutoUpdate": "Invalid value for Enumeration.", "LCAttributes.1.StorageHealthRollupStatus": "Read only Attribute cannot be modified.", "SNMP.1.AlertPort": "Not a valid integer.", "SNMP.1.AlertPorty": "Attribute does not exist.", "SysLog.1.PowerLogInterval": "Integer out of valid range.", "ThermalSettings.1.AirExhaustTemp": "Invalid value for Enumeration."}`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-msg"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_attributes_module__return-msg:

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

      Status of the attribute update operation.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` always

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`"Successfully updated the attributes."`


      .. raw:: html

        </div>



..  Status (Presently only deprecated)


.. Authors

Authors
~~~~~~~

- Husniya Abdul Hameed (@husniya-hameed)
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

