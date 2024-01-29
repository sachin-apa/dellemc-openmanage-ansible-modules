
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

.. _ansible_collections.dellemc.openmanage.ome_device_info_module:

.. Anchors: short name for ansible.builtin

.. Anchors: aliases



.. Title

dellemc.openmanage.ome_device_info module -- Retrieves the information of devices inventoried by OpenManage Enterprise
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. Collection note

.. note::
    This module is part of the `dellemc.openmanage collection <https://galaxy.ansible.com/dellemc/openmanage>`_ (version 8.5.0).

    To install it, use: :code:`ansible-galaxy collection install dellemc.openmanage`.
    You need further requirements to be able to use this module,
    see :ref:`Requirements <ansible_collections.dellemc.openmanage.ome_device_info_module_requirements>` for details.

    To use it in a playbook, specify: :code:`dellemc.openmanage.ome_device_info`.

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

- This module retrieves the list of devices in the inventory of OpenManage Enterprise along with the details of each device.


.. Aliases


.. Requirements

.. _ansible_collections.dellemc.openmanage.ome_device_info_module_requirements:

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

      .. _ansible_collections.dellemc.openmanage.ome_device_info_module__parameter-ca_path:

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
        <div class="ansibleOptionAnchor" id="parameter-fact_subset"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_info_module__parameter-fact_subset:

      .. rst-class:: ansible-option-title

      **fact_subset**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-fact_subset" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      \ :literal:`basic\_inventory`\  returns the list of the devices.

      \ :literal:`detailed\_inventory`\  returns the inventory details of specified devices.

      \ :literal:`subsystem\_health`\  returns the health status of specified devices.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`"basic\_inventory"` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`"detailed\_inventory"`
      - :ansible-option-choices-entry:`"subsystem\_health"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-hostname"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_info_module__parameter-hostname:

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

      .. _ansible_collections.dellemc.openmanage.ome_device_info_module__parameter-password:

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

      .. _ansible_collections.dellemc.openmanage.ome_device_info_module__parameter-port:

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

      .. _ansible_collections.dellemc.openmanage.ome_device_info_module__parameter-system_query_options:

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

      \ :emphasis:`system\_query\_options`\  applicable for the choices of the fact\_subset. Either \ :emphasis:`device\_id`\  or \ :emphasis:`device\_service\_tag`\  is mandatory for \ :literal:`detailed\_inventory`\  and \ :literal:`subsystem\_health`\  or both can be applicable.


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-system_query_options/device_id"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_info_module__parameter-system_query_options/device_id:

      .. rst-class:: ansible-option-title

      **device_id**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-system_query_options/device_id" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      A list of unique identifier is applicable for \ :literal:`detailed\_inventory`\  and \ :literal:`subsystem\_health`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-system_query_options/device_service_tag"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_info_module__parameter-system_query_options/device_service_tag:

      .. rst-class:: ansible-option-title

      **device_service_tag**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-system_query_options/device_service_tag" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      A list of service tags are applicable for \ :literal:`detailed\_inventory`\  and \ :literal:`subsystem\_health`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-system_query_options/filter"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_info_module__parameter-system_query_options/filter:

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

      For \ :literal:`basic\_inventory`\ , it filters the collection of devices. \ :emphasis:`filter`\  query format should be aligned with OData standards.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-system_query_options/inventory_type"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_info_module__parameter-system_query_options/inventory_type:

      .. rst-class:: ansible-option-title

      **inventory_type**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-system_query_options/inventory_type" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      For \ :literal:`detailed\_inventory`\ , it returns details of the specified inventory type.


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-timeout"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_info_module__parameter-timeout:

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

      .. _ansible_collections.dellemc.openmanage.ome_device_info_module__parameter-username:

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

      .. _ansible_collections.dellemc.openmanage.ome_device_info_module__parameter-validate_certs:

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
    - name: Retrieve basic inventory of all devices
      dellemc.openmanage.ome_device_info:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"

    - name: Retrieve basic inventory for devices identified by IDs 33333 or 11111 using filtering
      dellemc.openmanage.ome_device_info:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        fact_subset: "basic_inventory"
        system_query_options:
          filter: "Id eq 33333 or Id eq 11111"

    - name: Retrieve inventory details of specified devices identified by IDs 11111 and 22222
      dellemc.openmanage.ome_device_info:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        fact_subset: "detailed_inventory"
        system_query_options:
          device_id:
            - 11111
            - 22222

    - name: Retrieve inventory details of specified devices identified by service tags MXL1234 and MXL4567
      dellemc.openmanage.ome_device_info:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        fact_subset: "detailed_inventory"
        system_query_options:
          device_service_tag:
            - MXL1234
            - MXL4567

    - name: Retrieve details of specified inventory type of specified devices identified by ID and service tags
      dellemc.openmanage.ome_device_info:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        fact_subset: "detailed_inventory"
        system_query_options:
          device_id:
            - 11111
          device_service_tag:
            - MXL1234
            - MXL4567
          inventory_type: "serverDeviceCards"

    - name: Retrieve subsystem health of specified devices identified by service tags
      dellemc.openmanage.ome_device_info:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        fact_subset: "subsystem_health"
        system_query_options:
          device_service_tag:
            - MXL1234
            - MXL4567




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
        <div class="ansibleOptionAnchor" id="return-device_info"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_info_module__return-device_info:

      .. rst-class:: ansible-option-title

      **device_info**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-device_info" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Returns the information collected from the Device.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` success

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"value": [{"Actions": null, "AssetTag": null, "ChassisServiceTag": null, "ConnectionState": true, "DeviceManagement": [{"DnsName": "dnsname.host.com", "InstrumentationName": "MX-12345", "MacAddress": "11:10:11:10:11:10", "ManagementId": 12345, "ManagementProfile": [{"HasCreds": 0, "ManagementId": 12345, "ManagementProfileId": 12345, "ManagementURL": "https://192.168.0.1:443", "Status": 1000, "StatusDateTime": "2019-01-21 06:30:08.501"}], "ManagementType": 2, "NetworkAddress": "192.168.0.1"}], "DeviceName": "MX-0003I", "DeviceServiceTag": "MXL1234", "DeviceSubscription": null, "LastInventoryTime": "2019-01-21 06:30:08.501", "LastStatusTime": "2019-01-21 06:30:02.492", "ManagedState": 3000, "Model": "PowerEdge MX7000", "PowerState": 17, "SlotConfiguration": {}, "Status": 4000, "SystemId": 2031, "Type": 2000}]}`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-msg"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_info_module__return-msg:

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

      Over all device information status.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` on error

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`"Failed to fetch the device information"`


      .. raw:: html

        </div>



..  Status (Presently only deprecated)


.. Authors

Authors
~~~~~~~

- Sajna Shetty (@Sajna-Shetty)
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

