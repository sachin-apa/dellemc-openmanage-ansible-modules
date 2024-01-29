
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

.. _ansible_collections.dellemc.openmanage.ome_smart_fabric_info_module:

.. Anchors: short name for ansible.builtin

.. Anchors: aliases



.. Title

dellemc.openmanage.ome_smart_fabric_info module -- Retrieves the information of smart fabrics inventoried by OpenManage Enterprise Modular
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. Collection note

.. note::
    This module is part of the `dellemc.openmanage collection <https://galaxy.ansible.com/dellemc/openmanage>`_ (version 8.5.0).

    To install it, use: :code:`ansible-galaxy collection install dellemc.openmanage`.
    You need further requirements to be able to use this module,
    see :ref:`Requirements <ansible_collections.dellemc.openmanage.ome_smart_fabric_info_module_requirements>` for details.

    To use it in a playbook, specify: :code:`dellemc.openmanage.ome_smart_fabric_info`.

.. version_added

.. rst-class:: ansible-version-added

New in dellemc.openmanage 7.1.0

.. contents::
   :local:
   :depth: 1

.. Deprecated


Synopsis
--------

.. Description

- This module retrieves the list of smart fabrics in the inventory of OpenManage Enterprise Modular.


.. Aliases


.. Requirements

.. _ansible_collections.dellemc.openmanage.ome_smart_fabric_info_module_requirements:

Requirements
------------
The below requirements are needed on the host that executes this module.

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
        <div class="ansibleOptionAnchor" id="parameter-ca_path"></div>

      .. _ansible_collections.dellemc.openmanage.ome_smart_fabric_info_module__parameter-ca_path:

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
        <div class="ansibleOptionAnchor" id="parameter-fabric_id"></div>

      .. _ansible_collections.dellemc.openmanage.ome_smart_fabric_info_module__parameter-fabric_id:

      .. rst-class:: ansible-option-title

      **fabric_id**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-fabric_id" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Unique Id of the fabric.

      \ :emphasis:`fabric\_id`\  is mutually exclusive with \ :emphasis:`fabric\_name`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-fabric_name"></div>

      .. _ansible_collections.dellemc.openmanage.ome_smart_fabric_info_module__parameter-fabric_name:

      .. rst-class:: ansible-option-title

      **fabric_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-fabric_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Name of the fabric.

      \ :emphasis:`fabric\_name`\  is mutually exclusive with \ :emphasis:`fabric\_id`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-hostname"></div>

      .. _ansible_collections.dellemc.openmanage.ome_smart_fabric_info_module__parameter-hostname:

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

      OpenManage Enterprise Modular IP address or hostname.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-password"></div>

      .. _ansible_collections.dellemc.openmanage.ome_smart_fabric_info_module__parameter-password:

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

      OpenManage Enterprise Modular password.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-port"></div>

      .. _ansible_collections.dellemc.openmanage.ome_smart_fabric_info_module__parameter-port:

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

      OpenManage Enterprise Modular HTTPS port.


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`443`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-timeout"></div>

      .. _ansible_collections.dellemc.openmanage.ome_smart_fabric_info_module__parameter-timeout:

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

      .. _ansible_collections.dellemc.openmanage.ome_smart_fabric_info_module__parameter-username:

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

      OpenManage Enterprise Modular username.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-validate_certs"></div>

      .. _ansible_collections.dellemc.openmanage.ome_smart_fabric_info_module__parameter-validate_certs:

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
   - Run this module from a system that has direct access to Dell OpenManage Enterprise Modular.
   - This module supports \ :literal:`check\_mode`\ .

.. Seealso


.. Examples

Examples
--------

.. code-block:: yaml+jinja

    
    ---
    - name: Retrieve details of all smart fabrics
      dellemc.openmanage.ome_smart_fabric_info:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"

    - name: Retrieve details of a specific smart fabric identified by its fabric ID
      dellemc.openmanage.ome_smart_fabric_info:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        fabric_id: "61c20a59-9ed5-4ae5-b850-5e5acf42d2f2"

    - name: Retrieve details of a specific smart fabric identified by its fabric name
      dellemc.openmanage.ome_smart_fabric_info:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        fabric_name: "f1"




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

      .. _ansible_collections.dellemc.openmanage.ome_smart_fabric_info_module__return-error_info:

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

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"error": {"@Message.ExtendedInfo": [{"Message": "Unable to complete the request because the resource URI does not exist or is not implemented.", "MessageArgs": [], "MessageId": "CGEN1006", "RelatedProperties": [], "Resolution": "Check the request resource URI. Refer to the OpenManage Enterprise-Modular User's Guide for more information about resource URI and its properties.", "Severity": "Critical"}], "code": "Base.1.0.GeneralError", "message": "A general error has occurred. See ExtendedInfo for more information."}}`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-msg"></div>

      .. _ansible_collections.dellemc.openmanage.ome_smart_fabric_info_module__return-msg:

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

      Status of smart fabric information retrieval.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` always

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`"Successfully retrieved the smart fabric information."`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-smart_fabric_info"></div>

      .. _ansible_collections.dellemc.openmanage.ome_smart_fabric_info_module__return-smart_fabric_info:

      .. rst-class:: ansible-option-title

      **smart_fabric_info**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-smart_fabric_info" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Returns the information about smart fabric.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` success

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`[{"Description": "Fabric f1", "FabricDesign": [{"Actions": {"#NetworkService.GetApplicableNodes": {"target": "/api/NetworkService/Fabrics('61c20a59-9ed5-4ae5-b850-5e5acf42d2f2')/FabricDesign/NetworkService.GetApplicableNodes"}, "Oem": {}}, "FabricDesignNode": [{"ChassisName": "Chassis-X", "NodeName": "Switch-B", "Slot": "Slot-A2", "Type": "WeaverSwitch"}, {"ChassisName": "Chassis-X", "NodeName": "Switch-A", "Slot": "Slot-A1", "Type": "WeaverSwitch"}], "Name": "2xMX9116n\_Fabric\_Switching\_Engines\_in\_same\_chassis", "NetworkLink": [{"DestinationInterface": "ethernet1/1/38", "DestinationNode": "Switch-B", "SourceInterface": "ethernet1/1/38", "SourceNode": "Switch-A"}, {"DestinationInterface": "ethernet1/1/37", "DestinationNode": "Switch-B", "SourceInterface": "ethernet1/1/37", "SourceNode": "Switch-A"}, {"DestinationInterface": "ethernet1/1/39", "DestinationNode": "Switch-B", "SourceInterface": "ethernet1/1/39", "SourceNode": "Switch-A"}, {"DestinationInterface": "ethernet1/1/40", "DestinationNode": "Switch-B", "SourceInterface": "ethernet1/1/40", "SourceNode": "Switch-A"}]}], "FabricDesignMapping": [{"DesignNode": "Switch-A", "PhysicalNode": "NODEID1"}, {"DesignNode": "Switch-B", "PhysicalNode": "NODEID2"}], "Health": {"Issues": [{"Category": "Audit", "DetailedDescription": "The SmartFabric is not healthy because the interface for an uplink mentioned in the message is not in operational status.", "Message": "The SmartFabric is not healthy because the interface JRWSV43:ethernet1/1/35 for uplink 1ad54420-b145-49a1-9779-21a579ef6f2d is not in operational status.", "MessageArgs": [], "MessageId": "NFAB0016", "Resolution": "Make sure that all the uplink interfaces are in operational status.", "Severity": "Warning", "TimeStamp": "2019-09-25T11:50:06Z"}, {"Category": "Audit", "DetailedDescription": "The SmartFabric is not healthy because one or more VLTi links are not connected.", "Message": "The SmartFabric is not healthy because all InterSwitch Links are not connected.", "MessageArgs": [], "MessageId": "NFAB0017", "Resolution": "Make sure that the VLTi cables for all ISLs are connected and operational as per the selected fabric design.", "Severity": "Warning", "TimeStamp": "2019-09-25T11:50:06Z"}, {"Category": "Audit", "DetailedDescription": "The SmartFabric is not healthy because the interface for an uplink mentioned in the message is not in operational status.", "Message": "The SmartFabric is not healthy because the interface 6H7J6Z2:ethernet1/1/35 for uplink 1ad54420-b145-49a1-9779-21a579ef6f2d is not in operational status.", "MessageArgs": [], "MessageId": "NFAB0016", "Resolution": "Make sure that all the uplink interfaces are in operational status.", "Severity": "Warning", "TimeStamp": "2019-09-25T11:50:06Z"}, {"Category": "Audit", "DetailedDescription": "The SmartFabric is not healthy because one or more of the uplink interfaces are not bonded.", "Message": "The SmartFabric is not healthy because the uplink 1ad54420-b145-49a1-9779-21a579ef6f2d interface 6H7J6Z2:ethernet1/1/35 is not bonded to the other interfaces in the uplink.", "MessageArgs": [], "MessageId": "NFAB0019", "Resolution": "Make sure that the Link Aggregation Control Protocol (LACP) is enabled on all ports on the remote switch to which the uplink ports from the fabric are connected.", "Severity": "Warning", "TimeStamp": "2019-09-25T11:50:06Z"}, {"Category": "Audit", "DetailedDescription": "The SmartFabric is not healthy because one or more of the uplink interfaces are not bonded.", "Message": "The SmartFabric is not healthy because the uplink 1ad54420-b145-49a1-9779-21a579ef6f2d interface JRWSV43:ethernet1/1/35 is not bonded to the other interfaces in the uplink.", "MessageArgs": [], "MessageId": "NFAB0019", "Resolution": "Make sure that the Link Aggregation Control Protocol (LACP) is enabled on all ports on the remote switch to which the uplink ports from the fabric are connected.", "Severity": "Warning", "TimeStamp": "2019-09-25T11:50:06Z"}], "Status": "4000"}, "Id": "61c20a59-9ed5-4ae5-b850-5e5acf42d2f2", "LifeCycleStatus": [{"Activity": "Create", "Status": "2060"}], "Multicast": [{"FloodRestrict": true, "IgmpVersion": "3", "MldVersion": "2"}], "Name": "f1", "OverrideLLDPConfiguration": "Disabled", "ScaleVLANProfile": "Enabled", "Servers": [{"ChassisServiceTag": "6H5S6Z2", "ConnectionState": true, "ConnectionStateReason": 101, "DeviceCapabilities": [1, 2, 3, 4, 7, 8, 9, 41, 10, 11, 12, 13, 14, 15, 208, 16, 17, 18, 212, 30, 31], "DeviceManagement": [{"DnsName": "iDRAC-6GZK6Z2", "InstrumentationName": "", "MacAddress": "4c:d9:8f:7a:7c:43", "ManagementId": 135185, "ManagementProfile": [{"AgentName": "iDRAC", "HasCreds": 0, "ManagementId": 135185, "ManagementProfileId": 135185, "ManagementURL": "https://[2607:f2b1:f081:9:4ed9:8fff:fe7a:7c43]:443/", "ProfileId": "WSMAN\_OOB", "Status": 1000, "StatusDateTime": "2019-10-29 09:30:38.552", "Version": "3.20.21.20"}], "ManagementType": 2, "NetworkAddress": "100.96.24.28"}, {"DnsName": "iDRAC-6GZK6Z2", "InstrumentationName": "", "MacAddress": "4c:d9:8f:7a:7c:43", "ManagementId": 135186, "ManagementProfile": [{"AgentName": "iDRAC", "HasCreds": 0, "ManagementId": 135186, "ManagementProfileId": 135186, "ManagementURL": "https://[2607:f2b1:f081:9:4ed9:8fff:fe7a:7c43]:443/", "ProfileId": "WSMAN\_OOB", "Status": 1000, "StatusDateTime": "2019-10-29 09:30:38.552", "Version": "3.20.21.20"}], "ManagementType": 2, "NetworkAddress": "[2607:f2b1:f081:9:4ed9:8fff:fe7a:7c43]"}], "DeviceName": "MX-6H5S6Z2:Sled-1", "DeviceServiceTag": "6GZK6Z2", "Enabled": true, "Id": 10071, "Identifier": "6GZK6Z2", "LastInventoryTime": "2019-10-29 09:30:38.552", "LastStatusTime": "2019-10-29 09:41:51.051", "ManagedState": 3000, "Model": "PowerEdge MX840c", "PowerState": 17, "SlotConfiguration": {"ChassisId": "10072", "ChassisName": "MX-6H5S6Z2", "ChassisServiceTag": "6H5S6Z2", "DeviceType": "1000", "SledBlockPowerOn": "None blocking", "SlotId": "10084", "SlotName": "Sled-1", "SlotNumber": "1", "SlotType": "2000"}, "Status": 1000, "SystemId": 1894, "Type": 1000}], "Summary": {"NodeCount": 2, "ServerCount": 1, "UplinkCount": 1}, "Switches": [{"ChassisServiceTag": "6H5S6Z2", "ConnectionState": true, "ConnectionStateReason": 101, "DeviceCapabilities": [1, 2, 3, 5, 7, 8, 9, 207, 18, 602, 603, 604, 605, 606, 607, 608, 609, 610, 611, 612, 613, 614, 615, 616, 617, 618, 619, 620, 621, 622], "DeviceManagement": [{"DnsName": "", "InstrumentationName": "MX9116n Fabric Engine", "MacAddress": "20:04:0F:4F:4E:04", "ManagementId": 135181, "ManagementProfile": [{"HasCreds": 0, "ManagementId": 135181, "ManagementProfileId": 135181, "ManagementURL": "", "ProfileId": "", "Status": 1000, "StatusDateTime": "2019-10-29 09:30:36.273"}], "ManagementType": 2, "NetworkAddress": "100.96.24.36"}, {"DnsName": "", "InstrumentationName": "MX9116n Fabric Engine", "MacAddress": "20:04:0F:4F:4E:04", "ManagementId": 135182, "ManagementProfile": [{"HasCreds": 0, "ManagementId": 135182, "ManagementProfileId": 135182, "ManagementURL": "", "ProfileId": "", "Status": 1000, "StatusDateTime": "2019-10-29 09:30:36.273"}], "ManagementType": 2, "NetworkAddress": ""}], "DeviceName": "MX-6H5S6Z2:IOM-A2", "DeviceServiceTag": "6H7J6Z2", "Enabled": true, "Id": 10074, "Identifier": "6H7J6Z2", "LastInventoryTime": "2019-10-29 09:30:36.332", "LastStatusTime": "2019-10-29 09:31:00.931", "ManagedState": 3000, "Model": "MX9116n Fabric Engine", "PowerState": 17, "SlotConfiguration": {"ChassisId": "10072", "ChassisName": "MX-6H5S6Z2", "ChassisServiceTag": "6H5S6Z2", "DeviceType": "4000", "SledBlockPowerOn": "null", "SlotId": "10079", "SlotName": "IOM-A2", "SlotNumber": "2", "SlotType": "4000"}, "Status": 1000, "SystemId": 2031, "Type": 4000}, {"ChassisServiceTag": "6H5S6Z2", "ConnectionState": true, "ConnectionStateReason": 101, "DeviceCapabilities": [1, 2, 3, 5, 7, 8, 9, 207, 18, 602, 603, 604, 605, 606, 607, 608, 609, 610, 611, 612, 613, 614, 615, 616, 617, 618, 619, 620, 621, 622], "DeviceManagement": [{"DnsName": "", "InstrumentationName": "MX9116n Fabric Engine", "MacAddress": "E8:B5:D0:52:61:46", "ManagementId": 135183, "ManagementProfile": [{"HasCreds": 0, "ManagementId": 135183, "ManagementProfileId": 135183, "ManagementURL": "", "ProfileId": "", "Status": 1000, "StatusDateTime": "2019-10-29 09:30:37.115"}], "ManagementType": 2, "NetworkAddress": "100.96.24.37"}, {"DnsName": "", "InstrumentationName": "MX9116n Fabric Engine", "MacAddress": "E8:B5:D0:52:61:46", "ManagementId": 135184, "ManagementProfile": [{"HasCreds": 0, "ManagementId": 135184, "ManagementProfileId": 135184, "ManagementURL": "", "ProfileId": "", "Status": 1000, "StatusDateTime": "2019-10-29 09:30:37.115"}], "ManagementType": 2, "NetworkAddress": ""}], "DeviceName": "MX-6H5S6Z2:IOM-A1", "DeviceServiceTag": "JRWSV43", "Enabled": true, "Id": 20881, "Identifier": "JRWSV43", "LastInventoryTime": "2019-10-29 09:30:37.172", "LastStatusTime": "2019-10-29 09:31:00.244", "ManagedState": 3000, "Model": "MX9116n Fabric Engine", "PowerState": 17, "SlotConfiguration": {"ChassisId": "10072", "ChassisName": "MX-6H5S6Z2", "ChassisServiceTag": "6H5S6Z2", "DeviceType": "4000", "SledBlockPowerOn": "null", "SlotId": "10078", "SlotName": "IOM-A1", "SlotNumber": "1", "SlotType": "4000"}, "Status": 1000, "SystemId": 2031, "Type": 4000}], "Uplinks": [{"Id": "1ad54420-b145-49a1-9779-21a579ef6f2d", "MediaType": "Ethernet", "Name": "u1", "NativeVLAN": 1, "Summary": {"NetworkCount": 1, "PortCount": 2}, "UfdEnable": "Disabled"}]}]`


      .. raw:: html

        </div>



..  Status (Presently only deprecated)


.. Authors

Authors
~~~~~~~

- Kritika Bhateja(@Kritka-Bhateja)



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

