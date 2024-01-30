
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

.. _ansible_collections.dellemc.openmanage.ome_configuration_compliance_baseline_module:

.. Anchors: short name for ansible.builtin

.. Anchors: aliases



.. Title

dellemc.openmanage.ome_configuration_compliance_baseline module -- Create, modify, and delete a configuration compliance baseline and remediate non-compliant devices on OpenManage Enterprise
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. Collection note

.. note::
    This module is part of the `dellemc.openmanage collection <https://galaxy.ansible.com/dellemc/openmanage>`_ (version 8.5.0).

    To install it, use: :code:`ansible-galaxy collection install dellemc.openmanage`.
    You need further requirements to be able to use this module,
    see :ref:`Requirements <ansible_collections.dellemc.openmanage.ome_configuration_compliance_baseline_module_requirements>` for details.

    To use it in a playbook, specify: :code:`dellemc.openmanage.ome_configuration_compliance_baseline`.

.. version_added

.. rst-class:: ansible-version-added

New in dellemc.openmanage 3.2.0

.. contents::
   :local:
   :depth: 1

.. Deprecated


Synopsis
--------

.. Description

- This module allows to create, modify, and delete a configuration compliance baseline on OpenManage Enterprise. This module also allows to remediate devices that are non-compliant with the baseline by changing the attributes of devices to match with the associated baseline attributes.


.. Aliases


.. Requirements

.. _ansible_collections.dellemc.openmanage.ome_configuration_compliance_baseline_module_requirements:

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

      .. _ansible_collections.dellemc.openmanage.ome_configuration_compliance_baseline_module__parameter-ca_path:

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

      .. _ansible_collections.dellemc.openmanage.ome_configuration_compliance_baseline_module__parameter-command:

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

      \ :literal:`create`\  creates a configuration baseline from an existing compliance template.\ :literal:`create`\  supports \ :literal:`check\_mode`\  or idempotency checking for only \ :emphasis:`names`\ .

      \ :literal:`modify`\  modifies an existing baseline.Only \ :emphasis:`names`\ , \ :emphasis:`description`\ , \ :emphasis:`device\_ids`\ , \ :emphasis:`device\_service\_tags`\ , and \ :emphasis:`device\_group\_names`\  can be modified

      \ :emphasis:`WARNING`\  When a baseline is modified, the provided \ :emphasis:`device\_ids`\ , \ :emphasis:`device\_group\_names`\ , and \ :emphasis:`device\_service\_tags`\  replaces the devices previously present in the baseline.

      \ :literal:`delete`\  deletes the list of configuration compliance baselines based on the baseline name. Invalid baseline names are ignored.

      \ :literal:`remediate`\  remediates devices that are non-compliant with the baseline by changing the attributes of devices to match with the associated baseline attributes.

      \ :literal:`remediate`\  is performed on all the non-compliant devices if either \ :emphasis:`device\_ids`\ , or \ :emphasis:`device\_service\_tags`\  is not provided.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`"create"` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`"modify"`
      - :ansible-option-choices-entry:`"delete"`
      - :ansible-option-choices-entry:`"remediate"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-description"></div>

      .. _ansible_collections.dellemc.openmanage.ome_configuration_compliance_baseline_module__parameter-description:

      .. rst-class:: ansible-option-title

      **description**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-description" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Description of the compliance baseline.

      This option is applicable when \ :emphasis:`command`\  is \ :literal:`create`\ , or \ :literal:`modify`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-device_group_names"></div>

      .. _ansible_collections.dellemc.openmanage.ome_configuration_compliance_baseline_module__parameter-device_group_names:

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

      Name of the target device group.

      This option is applicable when \ :emphasis:`command`\  is \ :literal:`create`\ , or \ :literal:`modify`\  and is mutually exclusive with \ :emphasis:`device\_ids`\  and \ :emphasis:`device\_service\_tag`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-device_ids"></div>

      .. _ansible_collections.dellemc.openmanage.ome_configuration_compliance_baseline_module__parameter-device_ids:

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

      IDs of the target devices.

      This option is applicable when \ :emphasis:`command`\  is \ :literal:`create`\ , \ :literal:`modify`\ , or \ :literal:`remediate`\ , and is mutually exclusive with \ :emphasis:`device\_service\_tag`\  and \ :emphasis:`device\_group\_names`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-device_service_tags"></div>

      .. _ansible_collections.dellemc.openmanage.ome_configuration_compliance_baseline_module__parameter-device_service_tags:

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

      Service tag of the target device.

      This option is applicable when \ :emphasis:`command`\  is \ :literal:`create`\ , \ :literal:`modify`\ , or \ :literal:`remediate`\  and is mutually exclusive with \ :emphasis:`device\_ids`\  and \ :emphasis:`device\_group\_names`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-hostname"></div>

      .. _ansible_collections.dellemc.openmanage.ome_configuration_compliance_baseline_module__parameter-hostname:

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

      OpenManage Enterprise IP address or hostname.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-job_wait"></div>

      .. _ansible_collections.dellemc.openmanage.ome_configuration_compliance_baseline_module__parameter-job_wait:

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

      This option is applicable when \ :emphasis:`command`\  is \ :literal:`create`\ , \ :literal:`modify`\ , or \ :literal:`remediate`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry-default:`true` :ansible-option-choices-default-mark:`← (default)`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-job_wait_timeout"></div>

      .. _ansible_collections.dellemc.openmanage.ome_configuration_compliance_baseline_module__parameter-job_wait_timeout:

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

      The maximum wait time of \ :emphasis:`job\_wait`\  in seconds.The job will only be tracked for this duration.

      This option is applicable when \ :emphasis:`job\_wait`\  is \ :literal:`true`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`10800`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-names"></div>

      .. _ansible_collections.dellemc.openmanage.ome_configuration_compliance_baseline_module__parameter-names:

      .. rst-class:: ansible-option-title

      **names**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-names" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Name(s) of the configuration compliance baseline.

      This option is applicable when \ :emphasis:`command`\  is \ :literal:`create`\ , \ :literal:`modify`\ , or \ :literal:`delete`\ .

      Provide the list of configuration compliance baselines names that are supported when \ :emphasis:`command`\  is \ :literal:`delete`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-new_name"></div>

      .. _ansible_collections.dellemc.openmanage.ome_configuration_compliance_baseline_module__parameter-new_name:

      .. rst-class:: ansible-option-title

      **new_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-new_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      New name of the compliance baseline to be modified.

      This option is applicable when \ :emphasis:`command`\  is \ :literal:`modify`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-password"></div>

      .. _ansible_collections.dellemc.openmanage.ome_configuration_compliance_baseline_module__parameter-password:

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

      OpenManage Enterprise password.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-port"></div>

      .. _ansible_collections.dellemc.openmanage.ome_configuration_compliance_baseline_module__parameter-port:

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

      OpenManage Enterprise HTTPS port.


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`443`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-template_id"></div>

      .. _ansible_collections.dellemc.openmanage.ome_configuration_compliance_baseline_module__parameter-template_id:

      .. rst-class:: ansible-option-title

      **template_id**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-template_id" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      ID of the deployment template to be used for creating a compliance baseline.

      This option is applicable when \ :emphasis:`command`\  is \ :literal:`create`\  and is mutually exclusive with \ :emphasis:`template\_name`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-template_name"></div>

      .. _ansible_collections.dellemc.openmanage.ome_configuration_compliance_baseline_module__parameter-template_name:

      .. rst-class:: ansible-option-title

      **template_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-template_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Name of the compliance template for creating the compliance baseline(s).

      Name of the deployment template to be used for creating a compliance baseline.

      This option is applicable when \ :emphasis:`command`\  is \ :literal:`create`\  and is mutually exclusive with \ :emphasis:`template\_id`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-timeout"></div>

      .. _ansible_collections.dellemc.openmanage.ome_configuration_compliance_baseline_module__parameter-timeout:

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

      .. _ansible_collections.dellemc.openmanage.ome_configuration_compliance_baseline_module__parameter-username:

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

      OpenManage Enterprise username.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-validate_certs"></div>

      .. _ansible_collections.dellemc.openmanage.ome_configuration_compliance_baseline_module__parameter-validate_certs:

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
   - This module supports \ :literal:`check\_mode`\ .
   - Ensure that the devices have the required licenses to perform the baseline compliance operations.

.. Seealso


.. Examples

Examples
--------

.. code-block:: yaml+jinja

    
    ---
    - name: Create a configuration compliance baseline using device IDs
      dellemc.openmanage.ome_configuration_compliance_baseline:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        names: "baseline1"
        template_name: "template1"
        description: "description of baseline"
        device_ids:
          - 1111
          - 2222

    - name: Create a configuration compliance baseline using device service tags
      dellemc.openmanage.ome_configuration_compliance_baseline:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        names: "baseline1"
        template_id: 1234
        description: "description of baseline"
        device_service_tags:
          - "SVCTAG1"
          - "SVCTAG2"

    - name: Create a configuration compliance baseline using group names
      dellemc.openmanage.ome_configuration_compliance_baseline:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        names: "baseline2"
        template_id: 2
        job_wait_timeout: 1000
        description: "description of baseline"
        device_group_names:
          - "Group1"
          - "Group2"

    - name: Delete the configuration compliance baselines
      dellemc.openmanage.ome_configuration_compliance_baseline:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        command: delete
        names:
          - baseline1
          - baseline2

    - name: Modify a configuration compliance baseline using group names
      dellemc.openmanage.ome_configuration_compliance_baseline:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        command: modify
        names: "baseline1"
        new_name: "baseline_update"
        template_name: "template2"
        description: "new description of baseline"
        job_wait_timeout: 1000
        device_group_names:
          - Group1

    - name: Remediate specific non-compliant devices to a configuration compliance baseline using device IDs
      dellemc.openmanage.ome_configuration_compliance_baseline:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        command: "remediate"
        names: "baseline1"
        device_ids:
          - 1111

    - name: Remediate specific non-compliant devices to a configuration compliance baseline using device service tags
      dellemc.openmanage.ome_configuration_compliance_baseline:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        command: "remediate"
        names: "baseline1"
        device_service_tags:
          - "SVCTAG1"
          - "SVCTAG2"

    - name: Remediate all the non-compliant devices to a configuration compliance baseline
      dellemc.openmanage.ome_configuration_compliance_baseline:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        command: "remediate"
        names: "baseline1"




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
        <div class="ansibleOptionAnchor" id="return-compliance_status"></div>

      .. _ansible_collections.dellemc.openmanage.ome_configuration_compliance_baseline_module__return-compliance_status:

      .. rst-class:: ansible-option-title

      **compliance_status**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-compliance_status" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Status of compliance baseline operation.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` when \ :emphasis:`command`\  is \ :literal:`create`\  or \ :literal:`modify`\ 

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"BaselineTargets": [{"Id": 1111, "Type": {"Id": 1000, "Name": "DEVICE"}}], "ConfigComplianceSummary": {"ComplianceStatus": "OK", "NumberOfCritical": 0, "NumberOfIncomplete": 0, "NumberOfNormal": 0, "NumberOfWarning": 0}, "Description": null, "Id": 13, "LastRun": "2021-02-27 13:15:13.751", "Name": "baseline1", "PercentageComplete": "100", "TaskId": 26584, "TaskStatus": 2070, "TemplateId": 102, "TemplateName": "one", "TemplateType": 2}`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-error_info"></div>

      .. _ansible_collections.dellemc.openmanage.ome_configuration_compliance_baseline_module__return-error_info:

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
        <div class="ansibleOptionAnchor" id="return-incompatible_devices"></div>

      .. _ansible_collections.dellemc.openmanage.ome_configuration_compliance_baseline_module__return-incompatible_devices:

      .. rst-class:: ansible-option-title

      **incompatible_devices**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-incompatible_devices" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Details of the devices which cannot be used to perform baseline compliance operations


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` when \ :emphasis:`device\_service\_tags`\  or \ :emphasis:`device\_ids`\  contains incompatible devices for \ :literal:`create`\  or \ :literal:`modify`\ 

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`[1234, 5678]`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-job_id"></div>

      .. _ansible_collections.dellemc.openmanage.ome_configuration_compliance_baseline_module__return-job_id:

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

      Task ID created when \ :emphasis:`command`\  is \ :literal:`remediate`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` when \ :emphasis:`command`\  is \ :literal:`remediate`\ 

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`14123`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-msg"></div>

      .. _ansible_collections.dellemc.openmanage.ome_configuration_compliance_baseline_module__return-msg:

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

      Overall status of the configuration compliance baseline operation.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` always

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`"Successfully created the configuration compliance baseline."`


      .. raw:: html

        </div>



..  Status (Presently only deprecated)


.. Authors

Authors
~~~~~~~

- Sajna Shetty(@Sajna-Shetty)
- Abhishek Sinha(@Abhishek-Dell)



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

