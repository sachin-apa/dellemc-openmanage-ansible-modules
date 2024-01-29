
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

.. _ansible_collections.dellemc.openmanage.ome_firmware_baseline_compliance_info_module:

.. Anchors: short name for ansible.builtin

.. Anchors: aliases



.. Title

dellemc.openmanage.ome_firmware_baseline_compliance_info module -- Retrieves baseline compliance details on OpenManage Enterprise
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. Collection note

.. note::
    This module is part of the `dellemc.openmanage collection <https://galaxy.ansible.com/dellemc/openmanage>`_ (version 8.5.0).

    To install it, use: :code:`ansible-galaxy collection install dellemc.openmanage`.
    You need further requirements to be able to use this module,
    see :ref:`Requirements <ansible_collections.dellemc.openmanage.ome_firmware_baseline_compliance_info_module_requirements>` for details.

    To use it in a playbook, specify: :code:`dellemc.openmanage.ome_firmware_baseline_compliance_info`.

.. version_added

.. rst-class:: ansible-version-added

New in dellemc.openmanage 2.0.0

.. contents::
   :local:
   :depth: 1

.. Deprecated


Synopsis
--------

.. Description

- This module allows to retrieve firmware compliance for a list of devices, or against a specified baseline on OpenManage Enterprise.


.. Aliases


.. Requirements

.. _ansible_collections.dellemc.openmanage.ome_firmware_baseline_compliance_info_module_requirements:

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
        <div class="ansibleOptionAnchor" id="parameter-baseline_name"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_baseline_compliance_info_module__parameter-baseline_name:

      .. rst-class:: ansible-option-title

      **baseline_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-baseline_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Name of the baseline, for which the device compliance report is generated.

      This option is mandatory for generating baseline based device compliance report.

      \ :emphasis:`baseline\_name`\  is mutually exclusive with \ :emphasis:`device\_ids`\ , \ :emphasis:`device\_service\_tags`\  and \ :emphasis:`device\_group\_names`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-ca_path"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_baseline_compliance_info_module__parameter-ca_path:

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
        <div class="ansibleOptionAnchor" id="parameter-device_group_names"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_baseline_compliance_info_module__parameter-device_group_names:

      .. rst-class:: ansible-option-title

      **device_group_names**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-device_group_names" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      A list of group names for device based compliance report.

      Either \ :emphasis:`device\_ids`\ , \ :emphasis:`device\_service\_tags`\  or \ :emphasis:`device\_group\_names`\  is required to generate device based compliance report.

      \ :emphasis:`device\_group\_names`\  is mutually exclusive with \ :emphasis:`device\_ids`\ , \ :emphasis:`device\_service\_tags`\  and \ :emphasis:`baseline\_name`\ .

      Devices without reports are ignored.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-device_ids"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_baseline_compliance_info_module__parameter-device_ids:

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

      A list of unique identifier for device based compliance report.

      Either \ :emphasis:`device\_ids`\ , \ :emphasis:`device\_service\_tags`\  or \ :emphasis:`device\_group\_names`\  is required to generate device based compliance report.

      \ :emphasis:`device\_ids`\  is mutually exclusive with \ :emphasis:`device\_service\_tags`\ , \ :emphasis:`device\_group\_names`\  and \ :emphasis:`baseline\_name`\ .

      Devices without reports are ignored.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-device_service_tags"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_baseline_compliance_info_module__parameter-device_service_tags:

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

      A list of service tags for device based compliance report.

      Either \ :emphasis:`device\_ids`\ , \ :emphasis:`device\_service\_tags`\  or \ :emphasis:`device\_group\_names`\  is required to generate device based compliance report.

      \ :emphasis:`device\_service\_tags`\  is mutually exclusive with \ :emphasis:`device\_ids`\ , \ :emphasis:`device\_group\_names`\  and \ :emphasis:`baseline\_name`\ .

      Devices without reports are ignored.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-hostname"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_baseline_compliance_info_module__parameter-hostname:

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

      .. _ansible_collections.dellemc.openmanage.ome_firmware_baseline_compliance_info_module__parameter-password:

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

      .. _ansible_collections.dellemc.openmanage.ome_firmware_baseline_compliance_info_module__parameter-port:

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
        <div class="ansibleOptionAnchor" id="parameter-timeout"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_baseline_compliance_info_module__parameter-timeout:

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

      .. _ansible_collections.dellemc.openmanage.ome_firmware_baseline_compliance_info_module__parameter-username:

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

      .. _ansible_collections.dellemc.openmanage.ome_firmware_baseline_compliance_info_module__parameter-validate_certs:

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
   - Run this module from a system that has direct access to Dell OpenManage Enterprise.
   - This module supports \ :literal:`check\_mode`\ .

.. Seealso


.. Examples

Examples
--------

.. code-block:: yaml+jinja

    
    ---
    - name: Retrieves device based compliance report for specified device IDs
      dellemc.openmanage.ome_firmware_baseline_compliance_info:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        device_ids:
          - 11111
          - 22222

    - name: Retrieves device based compliance report for specified service Tags
      dellemc.openmanage.ome_firmware_baseline_compliance_info:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        device_service_tags:
          - MXL1234
          - MXL4567

    - name: Retrieves device based compliance report for specified group names
      dellemc.openmanage.ome_firmware_baseline_compliance_info:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        device_group_names:
          - "group1"
          - "group2"

    - name: Retrieves device compliance report for a specified baseline
      dellemc.openmanage.ome_firmware_baseline_compliance_info:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        baseline_name: "baseline_name"




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
        <div class="ansibleOptionAnchor" id="return-baseline_compliance_info"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_baseline_compliance_info_module__return-baseline_compliance_info:

      .. rst-class:: ansible-option-title

      **baseline_compliance_info**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-baseline_compliance_info" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Details of the baseline compliance report.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` success

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`[{"CatalogId": 53, "ComplianceSummary": {"ComplianceStatus": "CRITICAL", "NumberOfCritical": 2, "NumberOfDowngrade": 0, "NumberOfNormal": 0, "NumberOfWarning": 0}, "Description": "", "DeviceComplianceReports": [{"ComplianceStatus": "CRITICAL", "ComponentComplianceReports": [{"ComplianceDependencies": [], "ComplianceStatus": "DOWNGRADE", "Criticality": "Ok", "CurrentVersion": "OSC\_1.1", "Id": 1258, "ImpactAssessment": "", "Name": "OS COLLECTOR 2.1", "Path": "FOLDER04118304M/2/Diagnostics\_Application\_JCCH7\_WN64\_4.0\_A00\_01.EXE", "PrerequisiteInfo": "", "RebootRequired": false, "SourceName": "DCIM:INSTALLED#802\_\_OSCollector.Embedded.1", "TargetIdentifier": "101734", "UniqueIdentifier": "xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx", "UpdateAction": "DOWNGRADE", "Uri": "http://www.dell.com/support/home/us/en/19/Drivers/DriversDetails?driverId=XXXXX", "Version": "4.0"}, {"ComplianceDependencies": [], "ComplianceStatus": "CRITICAL", "Criticality": "Recommended", "CurrentVersion": "DN02", "Id": 1259, "ImpactAssessment": "", "Name": "TOSHIBA AL14SE 1.8 TB 2.5 12Gb 10K 512n SAS HDD Drive", "Path": "FOLDER04086111M/1/SAS-Drive\_Firmware\_VDGFM\_WN64\_DN03\_A00.EXE", "PrerequisiteInfo": "", "RebootRequired": true, "SourceName": "DCIM:INSTALLED#304\_C\_Disk.Bay.1:Enclosure.Internal.0-1:RAID.Integrated.1-1", "TargetIdentifier": "103730", "UniqueIdentifier": "xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx", "UpdateAction": "UPGRADE", "Uri": "http://www.dell.com/support/home/us/en/19/Drivers/DriversDetails?driverId=XXXXX", "Version": "DN03"}], "DeviceId": 11603, "DeviceModel": "PowerEdge R630", "DeviceName": null, "DeviceTypeId": 1000, "DeviceTypeName": "CPGCGS", "FirmwareStatus": "Non-Compliant", "Id": 194, "RebootRequired": true, "ServiceTag": "MXL1234"}], "DowngradeEnabled": true, "Id": 53, "Is64Bit": false, "LastRun": "2019-09-27 05:08:16.301", "Name": "baseline1", "RepositoryId": 43, "RepositoryName": "catalog2", "RepositoryType": "CIFS", "Targets": [{"Id": 11603, "Type": {"Id": 1000, "Name": "DEVICE"}}], "TaskId": 11710, "TaskStatusId": 0}]`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-error_info"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_baseline_compliance_info_module__return-error_info:

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

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"error": {"@Message.ExtendedInfo": [{"Message": "Unable to retrieve baseline list either because the device ID(s) entered are invalid", "Resolution": "Make sure the entered device ID(s) are valid and retry the operation.", "Severity": "Critical"}], "code": "Base.1.0.GeneralError", "message": "A general error has occurred. See ExtendedInfo for more information."}}`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-msg"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_baseline_compliance_info_module__return-msg:

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

      Overall baseline compliance report status.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` on error

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`"Failed to fetch the compliance baseline information."`


      .. raw:: html

        </div>



..  Status (Presently only deprecated)


.. Authors

Authors
~~~~~~~

- Sajna Shetty(@Sajna-Shetty)



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

