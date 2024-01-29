
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

.. _ansible_collections.dellemc.openmanage.redfish_firmware_rollback_module:

.. Anchors: short name for ansible.builtin

.. Anchors: aliases



.. Title

dellemc.openmanage.redfish_firmware_rollback module -- To perform a component firmware rollback using component name
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. Collection note

.. note::
    This module is part of the `dellemc.openmanage collection <https://galaxy.ansible.com/dellemc/openmanage>`_ (version 8.5.0).

    To install it, use: :code:`ansible-galaxy collection install dellemc.openmanage`.
    You need further requirements to be able to use this module,
    see :ref:`Requirements <ansible_collections.dellemc.openmanage.redfish_firmware_rollback_module_requirements>` for details.

    To use it in a playbook, specify: :code:`dellemc.openmanage.redfish_firmware_rollback`.

.. version_added

.. rst-class:: ansible-version-added

New in dellemc.openmanage 8.2.0

.. contents::
   :local:
   :depth: 1

.. Deprecated


Synopsis
--------

.. Description

- This module allows to rollback the firmware of different server components.
- Depending on the component, the firmware update is applied after an automatic or manual reboot.


.. Aliases


.. Requirements

.. _ansible_collections.dellemc.openmanage.redfish_firmware_rollback_module_requirements:

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
        <div class="ansibleOptionAnchor" id="parameter-baseuri"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_firmware_rollback_module__parameter-baseuri:

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

      .. _ansible_collections.dellemc.openmanage.redfish_firmware_rollback_module__parameter-ca_path:

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
        <div class="ansibleOptionAnchor" id="parameter-name"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_firmware_rollback_module__parameter-name:

      .. rst-class:: ansible-option-title

      **name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The name or regular expression of the component to match and is case-sensitive.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-password"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_firmware_rollback_module__parameter-password:

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
        <div class="ansibleOptionAnchor" id="parameter-reboot"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_firmware_rollback_module__parameter-reboot:

      .. rst-class:: ansible-option-title

      **reboot**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-reboot" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Reboot the server to apply the previous version of the firmware.

      \ :literal:`true`\  reboots the server to rollback the firmware to the available version.

      \ :literal:`false`\  schedules the rollback of firmware until the next restart.

      When \ :emphasis:`reboot`\  is \ :literal:`false`\ , some components update immediately, and the server may reboot. So, the module must wait till the server is accessible.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry-default:`true` :ansible-option-choices-default-mark:`← (default)`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-reboot_timeout"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_firmware_rollback_module__parameter-reboot_timeout:

      .. rst-class:: ansible-option-title

      **reboot_timeout**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-reboot_timeout" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Wait time in seconds. The module waits for this duration till the server reboots.


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`900`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-timeout"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_firmware_rollback_module__parameter-timeout:

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

      .. _ansible_collections.dellemc.openmanage.redfish_firmware_rollback_module__parameter-username:

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

      .. _ansible_collections.dellemc.openmanage.redfish_firmware_rollback_module__parameter-validate_certs:

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
   - For components that do not require a reboot, firmware rollback proceeds irrespective of \ :emphasis:`reboot`\  is \ :literal:`true`\  or \ :literal:`false`\ .
   - This module supports IPv4 and IPv6 addresses.
   - This module supports \ :literal:`check\_mode`\ .

.. Seealso


.. Examples

Examples
--------

.. code-block:: yaml+jinja

    
    ---
    - name: Rollback a BIOS component firmware
      dellemc.openmanage.redfish_firmware_rollback:
        baseuri: "192.168.0.1"
        username: "user_name"
        password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        name: "BIOS"

    - name: Rollback all NIC cards with a name starting from 'Broadcom Gigabit'.
      dellemc.openmanage.redfish_firmware_rollback:
        baseuri: "192.168.0.1:443"
        username: "user_name"
        password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        name: "Broadcom Gigabit Ethernet.*"

    - name: Rollback all the component firmware except BIOS component.
      dellemc.openmanage.redfish_firmware_rollback:
        baseuri: "192.168.0.1:443"
        username: "user_name"
        password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        name: "(?!BIOS).*"

    - name: Rollback all the available firmware component.
      dellemc.openmanage.redfish_firmware_rollback:
        baseuri: "192.168.0.1:443"
        username: "user_name"
        password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        name: ".*"




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

      .. _ansible_collections.dellemc.openmanage.redfish_firmware_rollback_module__return-error_info:

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

      Details of the HTTP error.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` on http error

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"error": {"@Message.ExtendedInfo": [{"Message": "InstanceID value provided for the update operation is invalid", "MessageArgs": [], "MessageArgs@odata.count": 0, "MessageId": "IDRAC.2.8.SUP024", "RelatedProperties": [], "RelatedProperties@odata.count": 0, "Resolution": "Enumerate inventory, copy the InstanceID value and provide that value for the update operation.", "Severity": "Warning"}], "code": "Base.1.12.GeneralError", "message": "A general error has occurred. See ExtendedInfo for more information"}}`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-msg"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_firmware_rollback_module__return-msg:

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

      Overall firmware rollback status.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` always

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`"Successfully completed the job for firmware rollback."`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-status"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_firmware_rollback_module__return-status:

      .. rst-class:: ansible-option-title

      **status**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-status" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Firmware rollback job and progress details from the iDRAC.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` success

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`[{"ActualRunningStartTime": "2023-08-04T12:26:55", "ActualRunningStopTime": "2023-08-04T12:32:35", "CompletionTime": "2023-08-04T12:32:35", "Description": "Job Instance", "EndTime": "TIME\_NA", "Id": "JID\_911698303631", "JobState": "Completed", "JobType": "FirmwareUpdate", "Message": "Job completed successfully.", "MessageArgs": [], "MessageId": "PR19", "Name": "Firmware Rollback: Firmware", "PercentComplete": 100, "StartTime": "2023-08-04T12:23:50", "TargetSettingsURI": null}]`


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

