
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

.. _ansible_collections.dellemc.openmanage.ome_job_info_module:

.. Anchors: short name for ansible.builtin

.. Anchors: aliases



.. Title

dellemc.openmanage.ome_job_info module -- Get job details for a given job ID or an entire job queue on OpenMange Enterprise
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. Collection note

.. note::
    This module is part of the `dellemc.openmanage collection <https://galaxy.ansible.com/dellemc/openmanage>`_ (version 8.5.0).

    To install it, use: :code:`ansible-galaxy collection install dellemc.openmanage`.
    You need further requirements to be able to use this module,
    see :ref:`Requirements <ansible_collections.dellemc.openmanage.ome_job_info_module_requirements>` for details.

    To use it in a playbook, specify: :code:`dellemc.openmanage.ome_job_info`.

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

- This module retrieves job details for a given job ID or an entire job queue on OpenMange Enterprise.


.. Aliases


.. Requirements

.. _ansible_collections.dellemc.openmanage.ome_job_info_module_requirements:

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

      .. _ansible_collections.dellemc.openmanage.ome_job_info_module__parameter-ca_path:

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
        <div class="ansibleOptionAnchor" id="parameter-fetch_execution_history"></div>

      .. _ansible_collections.dellemc.openmanage.ome_job_info_module__parameter-fetch_execution_history:

      .. rst-class:: ansible-option-title

      **fetch_execution_history**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-fetch_execution_history" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Fetches the execution history of the job.

      \ :emphasis:`fetch\_execution\_history`\  is only applicable when valid \ :emphasis:`job\_id`\  is given.

      When \ :literal:`true`\ , fetches all the execution history details.

      When \ :literal:`false`\ , fetches only the job info and last execution details.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`false` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-hostname"></div>

      .. _ansible_collections.dellemc.openmanage.ome_job_info_module__parameter-hostname:

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
        <div class="ansibleOptionAnchor" id="parameter-job_id"></div>

      .. _ansible_collections.dellemc.openmanage.ome_job_info_module__parameter-job_id:

      .. rst-class:: ansible-option-title

      **job_id**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-job_id" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Unique ID of the job.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-password"></div>

      .. _ansible_collections.dellemc.openmanage.ome_job_info_module__parameter-password:

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

      .. _ansible_collections.dellemc.openmanage.ome_job_info_module__parameter-port:

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
        <div class="ansibleOptionAnchor" id="parameter-system_query_options"></div>

      .. _ansible_collections.dellemc.openmanage.ome_job_info_module__parameter-system_query_options:

      .. rst-class:: ansible-option-title

      **system_query_options**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-system_query_options" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Options for pagination of the output.


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-system_query_options/filter"></div>

      .. _ansible_collections.dellemc.openmanage.ome_job_info_module__parameter-system_query_options/filter:

      .. rst-class:: ansible-option-title

      **filter**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-system_query_options/filter" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Filter records by the values supported.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-system_query_options/skip"></div>

      .. _ansible_collections.dellemc.openmanage.ome_job_info_module__parameter-system_query_options/skip:

      .. rst-class:: ansible-option-title

      **skip**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-system_query_options/skip" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Number of records to skip. Default value is 0.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-system_query_options/top"></div>

      .. _ansible_collections.dellemc.openmanage.ome_job_info_module__parameter-system_query_options/top:

      .. rst-class:: ansible-option-title

      **top**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-system_query_options/top" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Number of records to return. Default value is 100.


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-timeout"></div>

      .. _ansible_collections.dellemc.openmanage.ome_job_info_module__parameter-timeout:

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

      .. _ansible_collections.dellemc.openmanage.ome_job_info_module__parameter-username:

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

      .. _ansible_collections.dellemc.openmanage.ome_job_info_module__parameter-validate_certs:

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
    - name: Get all jobs details
      dellemc.openmanage.ome_job_info:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"

    - name: Get job details for id
      dellemc.openmanage.ome_job_info:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        job_id: 12345

    - name: Get filtered job details
      dellemc.openmanage.ome_job_info:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        system_query_options:
          top: 2
          skip: 1
          filter: "JobType/Id eq 8"

    - name: Get detail job execution history with last execution detail for a job.
      dellemc.openmanage.ome_job_info:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        job_id: 12345
        fetch_execution_history: true




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
        <div class="ansibleOptionAnchor" id="return-job_info"></div>

      .. _ansible_collections.dellemc.openmanage.ome_job_info_module__return-job_info:

      .. rst-class:: ansible-option-title

      **job_info**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-job_info" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Details of the OpenManage Enterprise jobs.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` success

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"value": [{"Builtin": false, "CreatedBy": "admin", "Editable": true, "EndTime": null, "ExecutionHistories": [{"EndTime": "2023-06-07 09:33:08.403", "ExecutedBy": "admin", "ExecutionHistoryDetails": [{"ElapsedTime": "00:00:00", "EndTime": "2023-06-07 09:33:08.189", "ExecutionHistoryId": 1243224, "Id": 1288519, "IdBaseEntity": 0, "JobStatus": {"Id": 2070, "Name": "Failed"}, "Key": "198.168.0.1", "Progress": "100", "StartTime": "2023-06-07 09:33:07.525", "Value": "Running\\nDiscovery of target 198.168.0.1 started .\\nDiscovery target resolved to IP  198.168.0.1 .\\n: ========== EEMI Code: CGEN1009 ==========\\nMessage: Unable to perform the requested action because the device management endpoint authentication over WSMAN, REDFISH failed. \\nRecommended actions: Make sure the credentials associated with the device management endpoint are valid and retry the operation.\\n=======================================\\nTask Failed. Completed With Errors."}, {"ElapsedTime": "00:00:00", "EndTime": "2023-06-07 09:33:08.313", "ExecutionHistoryId": 1243224, "Id": 1288518, "IdBaseEntity": 0, "JobStatus": {"Id": 2070, "Name": "Failed"}, "Key": "198.168.0.2", "Progress": "100", "StartTime": "2023-06-07 09:33:07.521", "Value": "Running\\nDiscovery of target 198.168.0.2 started. \\nDiscovery target resolved to IP  198.168.0.2 .\\n: ========== EEMI Code: CGEN1009 ==========\\nMessage: Unable to perform the requested action because the device management endpoint authentication over WSMAN, REDFISH failed. \\nRecommended actions: Make sure the credentials associated with the device management endpoint are valid and retry the operation.\\n=======================================\\nTask Failed. Completed With Errors."}], "Id": 1243224, "JobId": 10429, "JobName": "Discovery-201", "JobStatus": {"Id": 2070, "Name": "Failed"}, "LastUpdateTime": "2023-06-07 09:33:08.447185", "Progress": "100", "StartTime": "2023-06-07 09:33:07.148"}, {"EndTime": "2023-06-07 09:30:56.338", "ExecutedBy": "admin", "ExecutionHistoryDetails": [{"ElapsedTime": "00:00:00", "EndTime": "2023-06-07 09:30:56.085", "ExecutionHistoryId": 1243218, "Id": 1288512, "IdBaseEntity": 0, "JobStatus": {"Id": 2070, "Name": "Failed"}, "Key": "198.168.0.1", "Progress": "100", "StartTime": "2023-06-07 09:30:55.441", "Value": "Running\\nDiscovery of target 198.168.0.1 started. \\nDiscovery target resolved to IP  198.168.0.1 .\\n: ========== EEMI Code: CGEN1009 ==========\\nMessage: Unable to perform the requested action because the device management endpoint authentication over WSMAN, REDFISH failed. \\nRecommended actions: Make sure the credentials associated with the device management endpoint are valid and retry the operation.\\n=======================================\\nTask Failed. Completed With Errors."}, {"ElapsedTime": "00:00:00", "EndTime": "2023-06-07 09:30:56.21", "ExecutionHistoryId": 1243218, "Id": 1288511, "IdBaseEntity": 0, "JobStatus": {"Id": 2070, "Name": "Failed"}, "Key": "198.168.0.2", "Progress": "100", "StartTime": "2023-06-07 09:30:55.439", "Value": "Running\\nDiscovery of target 198.168.0.2 started. \\nDiscovery target resolved to IP  198.168.0.2 .\\n: ========== EEMI Code: CGEN1009 ==========\\nMessage: Unable to perform the requested action because the device management endpoint authentication over WSMAN, REDFISH failed. \\nRecommended actions: Make sure the credentials associated with the device management endpoint are valid and retry the operation.\\n=======================================\\nTask Failed. Completed With Errors."}], "Id": 1243218, "JobId": 10429, "JobName": "Discovery-201", "JobStatus": {"Id": 2070, "Name": "Failed"}, "LastUpdateTime": "2023-06-07 09:30:56.365294", "Progress": "100", "StartTime": "2023-06-07 09:30:55.064"}], "Id": 10429, "JobDescription": "Discovery-201", "JobName": "Discovery-201", "JobStatus": {"Id": 2080, "Name": "New"}, "JobType": {"Id": 101, "Internal": false, "Name": "Discovery\_Task"}, "LastExecutionDetail": {"ElapsedTime": null, "EndTime": "2023-06-07 09:33:08.189", "ExecutionHistoryId": 1243224, "Id": 1288519, "IdBaseEntity": 0, "JobStatus": {"Id": 2070, "Name": "Failed"}, "Key": "198.168.0.1", "Progress": "100", "StartTime": "2023-06-07 09:33:07.525", "Value": "Running\\nDiscovery of target 198.168.0.1 started. \\nDiscovery target resolved to IP  198.168.0.1 .\\n: ========== EEMI Code: CGEN1009 ==========\\nMessage: Unable to perform the requested action because the device management endpoint authentication over WSMAN, REDFISH failed. \\nRecommended actions: Make sure the credentials associated with the device management endpoint are valid and retry the operation. \\n=======================================\\nTask Failed. Completed With Errors."}, "LastRun": "2023-06-07 09:33:07.161", "LastRunStatus": {"Id": 2070, "Name": "Failed"}, "NextRun": null, "Params": [], "Schedule": "startnow", "StartTime": null, "State": "Enabled", "Targets": [], "UpdatedBy": "admin", "UserGenerated": true, "Visible": true}]}`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-msg"></div>

      .. _ansible_collections.dellemc.openmanage.ome_job_info_module__return-msg:

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

      Overall status of the job facts operation.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` always

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`"Successfully fetched the job info"`


      .. raw:: html

        </div>



..  Status (Presently only deprecated)


.. Authors

Authors
~~~~~~~

- Jagadeesh N V (@jagadeeshnv)
- Abhishek Sinha (@Abhishek-Dell)



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

