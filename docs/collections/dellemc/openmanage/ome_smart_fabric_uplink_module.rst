
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

.. _ansible_collections.dellemc.openmanage.ome_smart_fabric_uplink_module:

.. Anchors: short name for ansible.builtin

.. Anchors: aliases



.. Title

dellemc.openmanage.ome_smart_fabric_uplink module -- Create, modify or delete a uplink for a fabric on OpenManage Enterprise Modular
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. Collection note

.. note::
    This module is part of the `dellemc.openmanage collection <https://galaxy.ansible.com/dellemc/openmanage>`_ (version 8.5.0).

    To install it, use: :code:`ansible-galaxy collection install dellemc.openmanage`.
    You need further requirements to be able to use this module,
    see :ref:`Requirements <ansible_collections.dellemc.openmanage.ome_smart_fabric_uplink_module_requirements>` for details.

    To use it in a playbook, specify: :code:`dellemc.openmanage.ome_smart_fabric_uplink`.

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

- This module allows to create, modify or delete an uplink for a fabric.


.. Aliases


.. Requirements

.. _ansible_collections.dellemc.openmanage.ome_smart_fabric_uplink_module_requirements:

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

      .. _ansible_collections.dellemc.openmanage.ome_smart_fabric_uplink_module__parameter-ca_path:

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
        <div class="ansibleOptionAnchor" id="parameter-description"></div>

      .. _ansible_collections.dellemc.openmanage.ome_smart_fabric_uplink_module__parameter-description:

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

      Provide a short description for the uplink to be created or modified.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-fabric_name"></div>

      .. _ansible_collections.dellemc.openmanage.ome_smart_fabric_uplink_module__parameter-fabric_name:

      .. rst-class:: ansible-option-title

      **fabric_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-fabric_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Provide the \ :emphasis:`fabric\_name`\  of the fabric for which the uplink is to be configured.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-hostname"></div>

      .. _ansible_collections.dellemc.openmanage.ome_smart_fabric_uplink_module__parameter-hostname:

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
        <div class="ansibleOptionAnchor" id="parameter-name"></div>

      .. _ansible_collections.dellemc.openmanage.ome_smart_fabric_uplink_module__parameter-name:

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

      Provide the \ :emphasis:`name`\  of the uplink to be created, modified or deleted.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-new_name"></div>

      .. _ansible_collections.dellemc.openmanage.ome_smart_fabric_uplink_module__parameter-new_name:

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

      Provide the new \ :emphasis:`new\_name`\  for the uplink.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-password"></div>

      .. _ansible_collections.dellemc.openmanage.ome_smart_fabric_uplink_module__parameter-password:

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

      .. _ansible_collections.dellemc.openmanage.ome_smart_fabric_uplink_module__parameter-port:

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
        <div class="ansibleOptionAnchor" id="parameter-primary_switch_ports"></div>

      .. _ansible_collections.dellemc.openmanage.ome_smart_fabric_uplink_module__parameter-primary_switch_ports:

      .. rst-class:: ansible-option-title

      **primary_switch_ports**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-primary_switch_ports" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The IOM slots to be connected to the primary switch.

      \ :emphasis:`primary\_switch\_service\_tag`\  is mandatory for this option.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-primary_switch_service_tag"></div>

      .. _ansible_collections.dellemc.openmanage.ome_smart_fabric_uplink_module__parameter-primary_switch_service_tag:

      .. rst-class:: ansible-option-title

      **primary_switch_service_tag**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-primary_switch_service_tag" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Service tag of the primary switch.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-secondary_switch_ports"></div>

      .. _ansible_collections.dellemc.openmanage.ome_smart_fabric_uplink_module__parameter-secondary_switch_ports:

      .. rst-class:: ansible-option-title

      **secondary_switch_ports**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-secondary_switch_ports" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The IOM slots to be connected to the secondary switch.

      \ :emphasis:`secondary\_switch\_service\_tag`\  is mandatory for this option.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-secondary_switch_service_tag"></div>

      .. _ansible_collections.dellemc.openmanage.ome_smart_fabric_uplink_module__parameter-secondary_switch_service_tag:

      .. rst-class:: ansible-option-title

      **secondary_switch_service_tag**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-secondary_switch_service_tag" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Service tag of the secondary switch.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-state"></div>

      .. _ansible_collections.dellemc.openmanage.ome_smart_fabric_uplink_module__parameter-state:

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

      \ :literal:`present`\  - Creates a new uplink with the provided \ :emphasis:`name`\ . - Modifies an existing uplink with the provided \ :emphasis:`name`\ .

      \ :literal:`absent`\  – Deletes the uplink with the provided \ :emphasis:`name`\ .

      \ :emphasis:`WARNING`\  Delete operation can impact the network infrastructure.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`"present"` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`"absent"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-tagged_networks"></div>

      .. _ansible_collections.dellemc.openmanage.ome_smart_fabric_uplink_module__parameter-tagged_networks:

      .. rst-class:: ansible-option-title

      **tagged_networks**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-tagged_networks" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      VLANs to be associated with the uplink \ :emphasis:`name`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-timeout"></div>

      .. _ansible_collections.dellemc.openmanage.ome_smart_fabric_uplink_module__parameter-timeout:

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
        <div class="ansibleOptionAnchor" id="parameter-ufd_enable"></div>

      .. _ansible_collections.dellemc.openmanage.ome_smart_fabric_uplink_module__parameter-ufd_enable:

      .. rst-class:: ansible-option-title

      **ufd_enable**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-ufd_enable" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Add or Remove the uplink to the Uplink Failure Detection (UFD) group. The UFD group identifies the loss of connectivity to the upstream switch and notifies the servers that are connected to the switch. During an uplink failure, the switch disables the corresponding downstream server ports. The downstream servers can then select alternate connectivity routes, if available.

      \ :emphasis:`WARNING`\  The firmware version of the I/O Module running the Fabric Manager must support this configuration feature. If not, uplink creation will be successful with an appropriate error message in response.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"Enabled"`
      - :ansible-option-choices-entry:`"Disabled"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-untagged_network"></div>

      .. _ansible_collections.dellemc.openmanage.ome_smart_fabric_uplink_module__parameter-untagged_network:

      .. rst-class:: ansible-option-title

      **untagged_network**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-untagged_network" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Specify the name of the VLAN to be added as untagged to the uplink.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-uplink_type"></div>

      .. _ansible_collections.dellemc.openmanage.ome_smart_fabric_uplink_module__parameter-uplink_type:

      .. rst-class:: ansible-option-title

      **uplink_type**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-uplink_type" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Specify the uplink type.

      \ :emphasis:`NOTE`\  The uplink type cannot be changed for an existing uplink.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"Ethernet"`
      - :ansible-option-choices-entry:`"FCoE"`
      - :ansible-option-choices-entry:`"FC Gateway"`
      - :ansible-option-choices-entry:`"FC Direct Attach"`
      - :ansible-option-choices-entry:`"Ethernet - No Spanning Tree"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-username"></div>

      .. _ansible_collections.dellemc.openmanage.ome_smart_fabric_uplink_module__parameter-username:

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

      .. _ansible_collections.dellemc.openmanage.ome_smart_fabric_uplink_module__parameter-validate_certs:

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
    - name: Create an Uplink
      dellemc.openmanage.ome_smart_fabric_uplink:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        state: "present"
        fabric_name: "fabric1"
        name: "uplink1"
        description: "CREATED from OMAM"
        uplink_type: "Ethernet"
        ufd_enable: "Enabled"
        primary_switch_service_tag: "ABC1234"
        primary_switch_ports:
          - ethernet1/1/13
          - ethernet1/1/14
        secondary_switch_service_tag: "XYZ1234"
        secondary_switch_ports:
          - ethernet1/1/13
          - ethernet1/1/14
        tagged_networks:
          - vlan1
          - vlan3
        untagged_network: vlan2
      tags: create_uplink

    - name: Modify an existing uplink
      dellemc.openmanage.ome_smart_fabric_uplink:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        state: "present"
        fabric_name: "fabric1"
        name: "uplink1"
        new_name: "uplink2"
        description: "Modified from OMAM"
        uplink_type: "Ethernet"
        ufd_enable: "Disabled"
        primary_switch_service_tag: "DEF1234"
        primary_switch_ports:
          - ethernet1/2/13
          - ethernet1/2/14
        secondary_switch_service_tag: "TUV1234"
        secondary_switch_ports:
          - ethernet1/2/13
          - ethernet1/2/14
        tagged_networks:
          - vlan11
          - vlan33
        untagged_network: vlan22
      tags: modify_uplink

    - name: Delete an Uplink
      dellemc.openmanage.ome_smart_fabric_uplink:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        state: "absent"
        fabric_name: "fabric1"
        name: "uplink1"
      tags: delete_uplink

    - name: Modify an Uplink name
      dellemc.openmanage.ome_smart_fabric_uplink:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        state: "present"
        fabric_name: "fabric1"
        name: "uplink1"
        new_name: "uplink2"
      tags: modify_uplink_name

    - name: Modify Uplink ports
      dellemc.openmanage.ome_smart_fabric_uplink:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        state: "present"
        fabric_name: "fabric1"
        name: "uplink1"
        description: "uplink ports modified"
        primary_switch_service_tag: "ABC1234"
        primary_switch_ports:
          - ethernet1/1/6
          - ethernet1/1/7
        secondary_switch_service_tag: "XYZ1234"
        secondary_switch_ports:
          - ethernet1/1/9
          - ethernet1/1/10
      tags: modify_ports

    - name: Modify Uplink networks
      dellemc.openmanage.ome_smart_fabric_uplink:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        state: "present"
        fabric_name: "fabric1"
        name: "create1"
        description: "uplink networks modified"
        tagged_networks:
          - vlan4
      tags: modify_networks




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
        <div class="ansibleOptionAnchor" id="return-additional_info"></div>

      .. _ansible_collections.dellemc.openmanage.ome_smart_fabric_uplink_module__return-additional_info:

      .. rst-class:: ansible-option-title

      **additional_info**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-additional_info" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Additional details of the fabric operation.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` when \ :emphasis:`state=present`\  and additional information present in response.

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"error": {"@Message.ExtendedInfo": [{"Message": "Unable to configure the Uplink Failure Detection mode on the uplink because the firmware version of the I/O Module running the Fabric Manager does not support the configuration feature.", "MessageArgs": [], "MessageId": "CDEV7151", "RelatedProperties": [], "Resolution": "Update the firmware version of the I/O Module running the Fabric Manager and retry the operation. For information about the recommended I/O Module firmware versions, see the OpenManage Enterprise-Modular User's Guide available on the support site.", "Severity": "Informational"}], "code": "Base.1.0.GeneralError", "message": "A general error has occurred. See ExtendedInfo for more information."}}`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-error_info"></div>

      .. _ansible_collections.dellemc.openmanage.ome_smart_fabric_uplink_module__return-error_info:

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

      .. _ansible_collections.dellemc.openmanage.ome_smart_fabric_uplink_module__return-msg:

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

      Overall status of the uplink operation.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` always

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`"Successfully modified the uplink."`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-uplink_id"></div>

      .. _ansible_collections.dellemc.openmanage.ome_smart_fabric_uplink_module__return-uplink_id:

      .. rst-class:: ansible-option-title

      **uplink_id**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-uplink_id" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Returns the ID when an uplink is created or modified.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` when \ :emphasis:`state=present`\ 

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`"ddc3d260-fd71-46a1-97f9-708e12345678"`


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

