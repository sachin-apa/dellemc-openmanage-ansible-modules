
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

.. _ansible_collections.dellemc.openmanage.ome_chassis_slots_module:

.. Anchors: short name for ansible.builtin

.. Anchors: aliases



.. Title

dellemc.openmanage.ome_chassis_slots module -- Rename sled slots on OpenManage Enterprise Modular
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. Collection note

.. note::
    This module is part of the `dellemc.openmanage collection <https://galaxy.ansible.com/dellemc/openmanage>`_ (version 8.5.0).

    To install it, use: :code:`ansible-galaxy collection install dellemc.openmanage`.
    You need further requirements to be able to use this module,
    see :ref:`Requirements <ansible_collections.dellemc.openmanage.ome_chassis_slots_module_requirements>` for details.

    To use it in a playbook, specify: :code:`dellemc.openmanage.ome_chassis_slots`.

.. version_added

.. rst-class:: ansible-version-added

New in dellemc.openmanage 3.6.0

.. contents::
   :local:
   :depth: 1

.. Deprecated


Synopsis
--------

.. Description

- This module allows to rename sled slots on OpenManage Enterprise Modular either using device id or device service tag or using chassis service tag and slot number.


.. Aliases


.. Requirements

.. _ansible_collections.dellemc.openmanage.ome_chassis_slots_module_requirements:

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

      .. _ansible_collections.dellemc.openmanage.ome_chassis_slots_module__parameter-ca_path:

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
        <div class="ansibleOptionAnchor" id="parameter-device_options"></div>

      .. _ansible_collections.dellemc.openmanage.ome_chassis_slots_module__parameter-device_options:

      .. rst-class:: ansible-option-title

      **device_options**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-device_options" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The ID or service tag of the sled in the slot and the new name for the slot.

      \ :emphasis:`device\_options`\  is mutually exclusive with \ :emphasis:`slot\_options`\ .


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-device_options/device_id"></div>

      .. _ansible_collections.dellemc.openmanage.ome_chassis_slots_module__parameter-device_options/device_id:

      .. rst-class:: ansible-option-title

      **device_id**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-device_options/device_id" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Device ID of the sled in the slot.

      This is mutually exclusive with \ :emphasis:`device\_service\_tag`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-device_options/device_service_tag"></div>

      .. _ansible_collections.dellemc.openmanage.ome_chassis_slots_module__parameter-device_options/device_service_tag:

      .. rst-class:: ansible-option-title

      **device_service_tag**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-device_options/device_service_tag" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Service tag of the sled in the slot.

      This is mutually exclusive with \ :emphasis:`device\_id`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-device_options/slot_name"></div>

      .. _ansible_collections.dellemc.openmanage.ome_chassis_slots_module__parameter-device_options/slot_name:

      .. rst-class:: ansible-option-title

      **slot_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-device_options/slot_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Provide name for the slot.


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-hostname"></div>

      .. _ansible_collections.dellemc.openmanage.ome_chassis_slots_module__parameter-hostname:

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

      .. _ansible_collections.dellemc.openmanage.ome_chassis_slots_module__parameter-password:

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

      .. _ansible_collections.dellemc.openmanage.ome_chassis_slots_module__parameter-port:

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
        <div class="ansibleOptionAnchor" id="parameter-slot_options"></div>

      .. _ansible_collections.dellemc.openmanage.ome_chassis_slots_module__parameter-slot_options:

      .. rst-class:: ansible-option-title

      **slot_options**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-slot_options" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The service tag of the chassis, slot number of the slot to be renamed, and the new name for the slot.

      \ :emphasis:`slot\_options`\  is mutually exclusive with \ :emphasis:`device\_options`\ .


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-slot_options/chassis_service_tag"></div>

      .. _ansible_collections.dellemc.openmanage.ome_chassis_slots_module__parameter-slot_options/chassis_service_tag:

      .. rst-class:: ansible-option-title

      **chassis_service_tag**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-slot_options/chassis_service_tag" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Service tag of the chassis.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-slot_options/slots"></div>

      .. _ansible_collections.dellemc.openmanage.ome_chassis_slots_module__parameter-slot_options/slots:

      .. rst-class:: ansible-option-title

      **slots**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-slot_options/slots" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=dictionary` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The slot number and the new name for the slot.


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-slot_options/slots/slot_name"></div>

      .. _ansible_collections.dellemc.openmanage.ome_chassis_slots_module__parameter-slot_options/slots/slot_name:

      .. rst-class:: ansible-option-title

      **slot_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-slot_options/slots/slot_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Provide name for the slot.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-slot_options/slots/slot_number"></div>

      .. _ansible_collections.dellemc.openmanage.ome_chassis_slots_module__parameter-slot_options/slots/slot_number:

      .. rst-class:: ansible-option-title

      **slot_number**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-slot_options/slots/slot_number" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The slot number of the slot to be renamed.


      .. raw:: html

        </div>



  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-timeout"></div>

      .. _ansible_collections.dellemc.openmanage.ome_chassis_slots_module__parameter-timeout:

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

      .. _ansible_collections.dellemc.openmanage.ome_chassis_slots_module__parameter-username:

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

      .. _ansible_collections.dellemc.openmanage.ome_chassis_slots_module__parameter-validate_certs:

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
   - This module initiates the refresh inventory task. It may take a minute for new names to be reflected. If the task exceeds 300 seconds to refresh, the task times out.
   - Run this module from a system that has direct access to Dell OpenManage Enterprise Modular.
   - This module supports \ :literal:`check\_mode`\ .

.. Seealso


.. Examples

Examples
--------

.. code-block:: yaml+jinja

    
    ---
    - name: Rename the slots in multiple chassis using slot number and chassis service tag
      dellemc.openmanage.ome_chassis_slots:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        slot_options:
          - chassis_service_tag: ABC1234
            slots:
              - slot_number: 1
                slot_name: sled_name_1
              - slot_number: 2
                slot_name: sled_name_2
          - chassis_service_tag: ABC1235
            slots:
              - slot_number: 1
                slot_name: sled_name_1
              - slot_number: 2
                slot_name: sled_name_2

    - name: Rename single slot name of the sled using sled ID
      dellemc.openmanage.ome_chassis_slots:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        device_options:
          - device_id: 10054
            slot_name: slot_device_name_1

    - name: Rename single slot name of the sled using sled service tag
      dellemc.openmanage.ome_chassis_slots:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        device_options:
          - device_service_tag: ABC1234
            slot_name: service_tag_slot

    - name: Rename multiple slot names of the devices
      dellemc.openmanage.ome_chassis_slots:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        device_options:
          - device_id: 10054
            slot_name: sled_name_1
          - device_service_tag: ABC1234
            slot_name: sled_name_2
          - device_id: 10055
            slot_name: sled_name_3
          - device_service_tag: PQR1234
            slot_name: sled_name_4




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

      .. _ansible_collections.dellemc.openmanage.ome_chassis_slots_module__return-error_info:

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

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"error": {"@Message.ExtendedInfo": [{"Message": "Unable to complete the operation because an invalid value is entered for the property Invalid json type: STRING for Edm.Int64 property: Id .", "MessageArgs": ["Invalid json type: STRING for Edm.Int64 property: Id"], "MessageId": "CGEN1014", "RelatedProperties": [], "Resolution": "Enter a valid value for the property and retry the operation. For more information about valid values, see the OpenManage Enterprise-Modular User's Guide available on the support site.", "Severity": "Critical"}], "code": "Base.1.0.GeneralError", "message": "A general error has occurred. See ExtendedInfo for more information."}}`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-msg"></div>

      .. _ansible_collections.dellemc.openmanage.ome_chassis_slots_module__return-msg:

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

      Overall status of the slot rename operation.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` always

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`"Successfully renamed the slot(s)."`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-rename_failed_slots"></div>

      .. _ansible_collections.dellemc.openmanage.ome_chassis_slots_module__return-rename_failed_slots:

      .. rst-class:: ansible-option-title

      **rename_failed_slots**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-rename_failed_slots" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Information of the valid slots that are not renamed.

      \ :literal:`JobStatus`\  is shown if rename job fails.

      \ :literal:`NOTE`\  Only slots which were not renamed are listed.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` if at least one slot renaming fails

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`[{"ChassisId": "12345", "ChassisName": "MX-ABCD123", "ChassisServiceTag": "ABCD123", "DeviceType": "4000", "JobId": 1234, "JobStatus": "Aborted", "SlotId": "10061", "SlotName": "c2", "SlotNumber": "1", "SlotType": "4000"}, {"ChassisId": "10053", "ChassisName": "MX-PQRS123", "ChassisServiceTag": "PQRS123", "DeviceType": "1000", "JobId": 0, "JobStatus": "HTTP Error 400: Bad Request", "SlotId": "10069", "SlotName": "b2", "SlotNumber": "3", "SlotType": "2000"}]`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-slot_info"></div>

      .. _ansible_collections.dellemc.openmanage.ome_chassis_slots_module__return-slot_info:

      .. rst-class:: ansible-option-title

      **slot_info**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-slot_info" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Information of the slots that are renamed successfully.

      The \ :literal:`DeviceServiceTag`\  and \ :literal:`DeviceId`\  options are available only if \ :emphasis:`device\_options`\  is used.

      \ :literal:`NOTE`\  Only the slots which were renamed are listed.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` if at least one slot renamed

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`[{"ChassisId": 10053, "ChassisServiceTag": "ABCD123", "DeviceName": "", "DeviceType": 1000, "JobId": 15746, "SlotId": "10072", "SlotName": "slot\_op2", "SlotNumber": "6", "SlotType": 2000}, {"ChassisId": 10053, "ChassisName": "MX-ABCD123", "ChassisServiceTag": "ABCD123", "DeviceType": "3000", "JobId": 15747, "SlotId": "10070", "SlotName": "slot\_op2", "SlotNumber": "4", "SlotType": "2000"}, {"ChassisId": "10053", "ChassisName": "MX-PQRS123", "ChassisServiceTag": "PQRS123", "DeviceId": "10054", "DeviceServiceTag": "XYZ5678", "DeviceType": "1000", "JobId": 15761, "SlotId": "10067", "SlotName": "a1", "SlotNumber": "1", "SlotType": "2000"}]`


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

