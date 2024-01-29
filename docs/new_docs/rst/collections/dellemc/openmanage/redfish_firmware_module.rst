
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

.. _ansible_collections.dellemc.openmanage.redfish_firmware_module:

.. Anchors: short name for ansible.builtin

.. Anchors: aliases



.. Title

dellemc.openmanage.redfish_firmware module -- To perform a component firmware update using the image file available on the local or remote system
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. Collection note

.. note::
    This module is part of the `dellemc.openmanage collection <https://galaxy.ansible.com/dellemc/openmanage>`_ (version 8.5.0).

    To install it, use: :code:`ansible-galaxy collection install dellemc.openmanage`.
    You need further requirements to be able to use this module,
    see :ref:`Requirements <ansible_collections.dellemc.openmanage.redfish_firmware_module_requirements>` for details.

    To use it in a playbook, specify: :code:`dellemc.openmanage.redfish_firmware`.

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

- This module allows the firmware update of only one component at a time. If the module is run for more than one component, an error message is returned.
- Depending on the component, the firmware update is applied after an automatic or manual reboot.


.. Aliases


.. Requirements

.. _ansible_collections.dellemc.openmanage.redfish_firmware_module_requirements:

Requirements
------------
The below requirements are needed on the host that executes this module.

- python \>= 3.8.6
- urllib3






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
        <div class="ansibleOptionAnchor" id="parameter-baseuri"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_firmware_module__parameter-baseuri:

      .. rst-class:: ansible-option-title

      **baseuri**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-baseuri" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      IP address of the target out-of-band controller. For example- \<ipaddress\>:\<port\>.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-ca_path"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_firmware_module__parameter-ca_path:

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
        <div class="ansibleOptionAnchor" id="parameter-image_uri"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_firmware_module__parameter-image_uri:

      .. rst-class:: ansible-option-title

      **image_uri**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-image_uri" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Firmware Image location URI or local path.

      For example- \ http://<web_address>/components.exe\  or /home/firmware\_repo/component.exe.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-job_wait"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_firmware_module__parameter-job_wait:

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


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry-default:`true` :ansible-option-choices-default-mark:`← (default)`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-job_wait_timeout"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_firmware_module__parameter-job_wait_timeout:

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

      Note: If a firmware update needs a reboot, the job will get scheduled and waits for no of seconds specfied in \ :emphasis:`job\_wait\_time`\ . to reduce the wait time either give \ :emphasis:`job\_wait\_time`\  minimum or make \ :emphasis:`job\_wait`\ as false and retrigger.


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`3600`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-password"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_firmware_module__parameter-password:

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

      Password of the target out-of-band controller.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-timeout"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_firmware_module__parameter-timeout:

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
        <div class="ansibleOptionAnchor" id="parameter-transfer_protocol"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_firmware_module__parameter-transfer_protocol:

      .. rst-class:: ansible-option-title

      **transfer_protocol**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-transfer_protocol" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Protocol used to transfer the firmware image file. Applicable for URI based update.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"CIFS"`
      - :ansible-option-choices-entry:`"FTP"`
      - :ansible-option-choices-entry-default:`"HTTP"` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`"HTTPS"`
      - :ansible-option-choices-entry:`"NSF"`
      - :ansible-option-choices-entry:`"OEM"`
      - :ansible-option-choices-entry:`"SCP"`
      - :ansible-option-choices-entry:`"SFTP"`
      - :ansible-option-choices-entry:`"TFTP"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-username"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_firmware_module__parameter-username:

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

      Username of the target out-of-band controller.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-validate_certs"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_firmware_module__parameter-validate_certs:

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
   - Run this module from a system that has direct access to Redfish APIs.
   - This module supports both IPv4 and IPv6 addresses.
   - This module supports only iDRAC9 and above.
   - This module does not support \ :literal:`check\_mode`\ .

.. Seealso


.. Examples

Examples
--------

.. code-block:: yaml+jinja

    
    ---
    - name: Update the firmware from a single executable file available in a HTTP protocol
      dellemc.openmanage.redfish_firmware:
        baseuri: "192.168.0.1"
        username: "user_name"
        password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        image_uri: "http://192.168.0.2/firmware_repo/component.exe"
        transfer_protocol: "HTTP"

    - name: Update the firmware from a single executable file available in a HTTP protocol with job_Wait
      dellemc.openmanage.redfish_firmware:
        baseuri: "192.168.0.1"
        username: "user_name"
        password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        image_uri: "http://192.168.0.2/firmware_repo/component.exe"
        transfer_protocol: "HTTP"
        job_wait: true
        job_wait_timeout: 600

    - name: Update the firmware from a single executable file available in a local path
      dellemc.openmanage.redfish_firmware:
        baseuri: "192.168.0.1"
        username: "user_name"
        password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        image_uri: "/home/firmware_repo/component.exe"




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

      .. _ansible_collections.dellemc.openmanage.redfish_firmware_module__return-error_info:

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

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"error": {"@Message.ExtendedInfo": [{"Message": "Unable to complete the operation because the JSON data format entered is invalid.", "Resolution": "Do the following and the retry the operation: 1) Enter the correct JSON data format and retry the operation. 2) Make sure that no syntax error is present in JSON data format. 3) Make sure that a duplicate key is not present in JSON data format.", "Severity": "Critical"}, {"Message": "The request body submitted was malformed JSON and could not be parsed by the receiving service.", "Resolution": "Ensure that the request body is valid JSON and resubmit the request.", "Severity": "Critical"}], "code": "Base.1.2.GeneralError", "message": "A general error has occurred. See ExtendedInfo for more information."}}`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-msg"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_firmware_module__return-msg:

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

      Overall status of the firmware update task.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` always

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`"Successfully updated the firmware."`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-task"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_firmware_module__return-task:

      .. rst-class:: ansible-option-title

      **task**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-task" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Returns ID and URI of the created task.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` success

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"id": "JID\_XXXXXXXXXXXX", "uri": "/redfish/v1/TaskService/Tasks/JID\_XXXXXXXXXXXX"}`


      .. raw:: html

        </div>



..  Status (Presently only deprecated)


.. Authors

Authors
~~~~~~~

- Felix Stephen (@felixs88)
- Husniya Hameed (@husniya_hameed)
- Shivam Sharma (@Shivam-Sharma)
- Kritika Bhateja (@Kritika_Bhateja)
- Abhishek Sinha (@ABHISHEK-SINHA10)



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

