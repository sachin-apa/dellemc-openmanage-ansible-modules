
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

.. _ansible_collections.dellemc.openmanage.ome_device_group_module:

.. Anchors: short name for ansible.builtin

.. Anchors: aliases



.. Title

dellemc.openmanage.ome_device_group module -- Add or remove device(s) from a static device group on OpenManage Enterprise
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. Collection note

.. note::
    This module is part of the `dellemc.openmanage collection <https://galaxy.ansible.com/dellemc/openmanage>`_ (version 8.5.0).

    To install it, use: :code:`ansible-galaxy collection install dellemc.openmanage`.
    You need further requirements to be able to use this module,
    see :ref:`Requirements <ansible_collections.dellemc.openmanage.ome_device_group_module_requirements>` for details.

    To use it in a playbook, specify: :code:`dellemc.openmanage.ome_device_group`.

.. version_added

.. rst-class:: ansible-version-added

New in dellemc.openmanage 3.3.0

.. contents::
   :local:
   :depth: 1

.. Deprecated


Synopsis
--------

.. Description

- This module allows to add or remove device(s) from a static device group on OpenManage Enterprise.


.. Aliases


.. Requirements

.. _ansible_collections.dellemc.openmanage.ome_device_group_module_requirements:

Requirements
------------
The below requirements are needed on the host that executes this module.

- python \>= 3.8.6
- netaddr \>= 0.7.19






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

      .. _ansible_collections.dellemc.openmanage.ome_device_group_module__parameter-ca_path:

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
        <div class="ansibleOptionAnchor" id="parameter-device_ids"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_group_module__parameter-device_ids:

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

      List of ID(s) of the device(s) to be added or removed from the device group.

      \ :emphasis:`device\_ids`\  is mutually exclusive with \ :emphasis:`device\_service\_tags`\  and \ :emphasis:`ip\_addresses`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-device_service_tags"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_group_module__parameter-device_service_tags:

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

      List of service tag(s) of the device(s) to be added or removed from the device group.

      \ :emphasis:`device\_service\_tags`\  is mutually exclusive with \ :emphasis:`device\_ids`\  and \ :emphasis:`ip\_addresses`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-group_id"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_group_module__parameter-group_id:

      .. rst-class:: ansible-option-title

      **group_id**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-group_id" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      ID of the static device.

      \ :emphasis:`group\_id`\  is mutually exclusive with \ :emphasis:`name`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-hostname"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_group_module__parameter-hostname:

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
        <div class="ansibleOptionAnchor" id="parameter-ip_addresses"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_group_module__parameter-ip_addresses:

      .. rst-class:: ansible-option-title

      **ip_addresses**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-ip_addresses" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      List of IPs of the device(s) to be added or removed from the device group.

      \ :emphasis:`ip\_addresses`\  is mutually exclusive with \ :emphasis:`device\_ids`\  and \ :emphasis:`device\_service\_tags`\ .

      Supported  IP address range formats:

          - 192.35.0.1

          - 10.36.0.0-192.36.0.255

          - 192.37.0.0/24

          - fe80::ffff:ffff:ffff:ffff

          - fe80::ffff:192.0.2.0/125

          - fe80::ffff:ffff:ffff:1111-fe80::ffff:ffff:ffff:ffff

      \ :literal:`NOTE`\  Hostname is not supported.

      \ :literal:`NOTE`\  \ :emphasis:`ip\_addresses`\  requires python's netaddr packages to work on IP Addresses.

      \ :literal:`NOTE`\  This module reports success even if one of the IP addresses provided in the \ :emphasis:`ip\_addresses`\  list is available in OpenManage Enterprise.The module reports failure only if none of the IP addresses provided in the list are available in OpenManage Enterprise.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-name"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_group_module__parameter-name:

      .. rst-class:: ansible-option-title

      **name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Name of the static group.

      \ :emphasis:`name`\  is mutually exclusive with \ :emphasis:`group\_id`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-password"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_group_module__parameter-password:

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

      .. _ansible_collections.dellemc.openmanage.ome_device_group_module__parameter-port:

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
        <div class="ansibleOptionAnchor" id="parameter-state"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_group_module__parameter-state:

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

      \ :literal:`present`\  allows to add the device(s) to a static device group.

      \ :literal:`absent`\  allows to remove the device(s) from a static device group.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`"present"` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`"absent"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-timeout"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_group_module__parameter-timeout:

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

      .. _ansible_collections.dellemc.openmanage.ome_device_group_module__parameter-username:

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

      .. _ansible_collections.dellemc.openmanage.ome_device_group_module__parameter-validate_certs:

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
    - name: Add devices to a static device group by using the group name and device IDs
      dellemc.openmanage.ome_device_group:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        name: "Storage Services"
        device_ids:
          - 11111
          - 11112
          - 11113

    - name: Add devices to a static device group by using the group name and device service tags
      dellemc.openmanage.ome_device_group:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        name: "Storage Services"
        device_service_tags:
          - GHRT2RL
          - KJHDF3S
          - LKIJNG6

    - name: Add devices to a static device group by using the group ID and device service tags
      dellemc.openmanage.ome_device_group:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        group_id: 12345
        device_service_tags:
          - GHRT2RL
          - KJHDF3S

    - name: Add devices to a static device group by using the group name and IPv4 addresses
      dellemc.openmanage.ome_device_group:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        name: "Storage Services"
        ip_addresses:
          - 192.35.0.1
          - 192.35.0.5

    - name: Add devices to a static device group by using the group ID and IPv6 addresses
      dellemc.openmanage.ome_device_group:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        group_id: 12345
        ip_addresses:
          - fe80::ffff:ffff:ffff:ffff
          - fe80::ffff:ffff:ffff:2222

    - name: Add devices to a static device group by using the group ID and supported IPv4 and IPv6 address formats.
      dellemc.openmanage.ome_device_group:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        group_id: 12345
        ip_addresses:
          - 192.35.0.1
          - 10.36.0.0-192.36.0.255
          - 192.37.0.0/24
          - fe80::ffff:ffff:ffff:ffff
          - ::ffff:192.0.2.0/125
          - fe80::ffff:ffff:ffff:1111-fe80::ffff:ffff:ffff:ffff

    - name: Remove devices from a static device group by using the group name and device IDs
      dellemc.openmanage.ome_device_group:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        state: "absent"
        name: "Storage Services"
        device_ids:
          - 11111
          - 11112
          - 11113

    - name: Remove devices from a static device group by using the group name and device service tags
      dellemc.openmanage.ome_device_group:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        state: "absent"
        name: "Storage Services"
        device_service_tags:
          - GHRT2RL
          - KJHDF3S
          - LKIJNG6

    - name: Remove devices from a static device group by using the group ID and device service tags
      dellemc.openmanage.ome_device_group:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        state: "absent"
        group_id: 12345
        device_service_tags:
          - GHRT2RL
          - KJHDF3S

    - name: Remove devices from a static device group by using the group name and IPv4 addresses
      dellemc.openmanage.ome_device_group:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        state: "absent"
        name: "Storage Services"
        ip_addresses:
          - 192.35.0.1
          - 192.35.0.5

    - name: Remove devices from a static device group by using the group ID and IPv6 addresses
      dellemc.openmanage.ome_device_group:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        state: "absent"
        group_id: 12345
        ip_addresses:
          - fe80::ffff:ffff:ffff:ffff
          - fe80::ffff:ffff:ffff:2222

    - name: Remove devices from a static device group by using the group ID and supported IPv4 and IPv6 address formats.
      dellemc.openmanage.ome_device_group:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        state: "absent"
        group_id: 12345
        ip_addresses:
          - 192.35.0.1
          - 10.36.0.0-192.36.0.255
          - 192.37.0.0/24
          - fe80::ffff:ffff:ffff:ffff
          - ::ffff:192.0.2.0/125
          - fe80::ffff:ffff:ffff:1111-fe80::ffff:ffff:ffff:ffff




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

      .. _ansible_collections.dellemc.openmanage.ome_device_group_module__return-error_info:

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
        <div class="ansibleOptionAnchor" id="return-group_id"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_group_module__return-group_id:

      .. rst-class:: ansible-option-title

      **group_id**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-group_id" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      ID of the group.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` success

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`21078`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-ip_addresses_added"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_group_module__return-ip_addresses_added:

      .. rst-class:: ansible-option-title

      **ip_addresses_added**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-ip_addresses_added" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      IP Addresses which are added to the device group.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` success

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`["21078"]`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-msg"></div>

      .. _ansible_collections.dellemc.openmanage.ome_device_group_module__return-msg:

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

      Overall status of the device group settings.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` always

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`"['Successfully added member(s) to the device group.']"`


      .. raw:: html

        </div>



..  Status (Presently only deprecated)


.. Authors

Authors
~~~~~~~

- Felix Stephen (@felixs88)
- Sajna Shetty(@Sajna-Shetty)
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

