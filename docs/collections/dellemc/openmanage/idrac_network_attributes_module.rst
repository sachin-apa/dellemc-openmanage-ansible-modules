
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

.. _ansible_collections.dellemc.openmanage.idrac_network_attributes_module:

.. Anchors: short name for ansible.builtin

.. Anchors: aliases



.. Title

dellemc.openmanage.idrac_network_attributes module -- Configures the iDRAC network attributes
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. Collection note

.. note::
    This module is part of the `dellemc.openmanage collection <https://galaxy.ansible.com/dellemc/openmanage>`_ (version 8.5.0).

    To install it, use: :code:`ansible-galaxy collection install dellemc.openmanage`.
    You need further requirements to be able to use this module,
    see :ref:`Requirements <ansible_collections.dellemc.openmanage.idrac_network_attributes_module_requirements>` for details.

    To use it in a playbook, specify: :code:`dellemc.openmanage.idrac_network_attributes`.

.. version_added

.. rst-class:: ansible-version-added

New in dellemc.openmanage 8.4.0

.. contents::
   :local:
   :depth: 1

.. Deprecated


Synopsis
--------

.. Description

- This module allows you to configure the port and partition network attributes on the network interface cards.


.. Aliases


.. Requirements

.. _ansible_collections.dellemc.openmanage.idrac_network_attributes_module_requirements:

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
        <div class="ansibleOptionAnchor" id="parameter-apply_time"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_network_attributes_module__parameter-apply_time:

      .. rst-class:: ansible-option-title

      **apply_time**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-apply_time" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Apply time of the \ :emphasis:`network\_attributes`\  and \ :emphasis:`oem\_network\_attributes`\ .

      This is applicable only to \ :emphasis:`network\_attributes`\  and \ :emphasis:`oem\_network\_attributes`\ .

      \ :literal:`Immediate`\  allows the user to immediately reboot the host and apply the changes. \ :emphasis:`job\_wait`\  is applicable. This is applicable for \ :emphasis:`oem\_network\_attributes`\  and \ :emphasis:`job\_wait`\ .

      \ :literal:`OnReset`\  allows the user to apply the changes on the next reboot of the host server.

      \ :literal:`AtMaintenanceWindowStart`\  allows the user to apply at the start of a maintenance window as specified in \ :emphasis:`maintenance\_window`\ . A reboot job is scheduled.

      \ :literal:`InMaintenanceWindowOnReset`\  allows to apply after a manual reset but within the maintenance window as specified in \ :emphasis:`maintenance\_window`\ .

      This is not applicable for iDRAC8 and value will be ignored and will not have any impact for configuring \ :emphasis:`oem\_network\_attributes`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"Immediate"`
      - :ansible-option-choices-entry:`"OnReset"`
      - :ansible-option-choices-entry:`"AtMaintenanceWindowStart"`
      - :ansible-option-choices-entry:`"InMaintenanceWindowOnReset"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-ca_path"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_network_attributes_module__parameter-ca_path:

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
        <div class="ansibleOptionAnchor" id="parameter-clear_pending"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_network_attributes_module__parameter-clear_pending:

      .. rst-class:: ansible-option-title

      **clear_pending**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-clear_pending" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      This parameter allows you to clear all the pending OEM network attributes changes.

      \ :literal:`false`\  does not perform any operation.

      \ :literal:`true`\  discards any pending changes to network attributes, or if a job is in scheduled state, removes the job.

      \ :emphasis:`apply\_time`\  value will be ignored and will not have any impact for \ :emphasis:`clear\_pending`\  operation.

      This operation is not supported for iDRAC8.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`false` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-idrac_ip"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_network_attributes_module__parameter-idrac_ip:

      .. rst-class:: ansible-option-title

      **idrac_ip**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-idrac_ip" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      iDRAC IP Address.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-idrac_password"></div>
        <div class="ansibleOptionAnchor" id="parameter-idrac_pwd"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_network_attributes_module__parameter-idrac_password:
      .. _ansible_collections.dellemc.openmanage.idrac_network_attributes_module__parameter-idrac_pwd:

      .. rst-class:: ansible-option-title

      **idrac_password**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-idrac_password" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-aliases:`aliases: idrac_pwd`

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      iDRAC user password.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-idrac_port"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_network_attributes_module__parameter-idrac_port:

      .. rst-class:: ansible-option-title

      **idrac_port**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-idrac_port" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      iDRAC port.


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`443`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-idrac_user"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_network_attributes_module__parameter-idrac_user:

      .. rst-class:: ansible-option-title

      **idrac_user**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-idrac_user" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      iDRAC username.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-job_wait"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_network_attributes_module__parameter-job_wait:

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

      This is applicable when \ :emphasis:`apply\_time`\  is \ :literal:`Immediate`\  for \ :emphasis:`oem\_network\_attributes`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry-default:`true` :ansible-option-choices-default-mark:`← (default)`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-job_wait_timeout"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_network_attributes_module__parameter-job_wait_timeout:

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


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`1200`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-maintenance_window"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_network_attributes_module__parameter-maintenance_window:

      .. rst-class:: ansible-option-title

      **maintenance_window**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-maintenance_window" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      This option allows you to schedule the maintenance window.

      This is required when \ :emphasis:`apply\_time`\  is \ :literal:`AtMaintenanceWindowStart`\  or \ :literal:`InMaintenanceWindowOnReset`\ .


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-maintenance_window/duration"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_network_attributes_module__parameter-maintenance_window/duration:

      .. rst-class:: ansible-option-title

      **duration**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-maintenance_window/duration" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The duration in seconds for the maintenance window.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-maintenance_window/start_time"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_network_attributes_module__parameter-maintenance_window/start_time:

      .. rst-class:: ansible-option-title

      **start_time**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-maintenance_window/start_time" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The start time for the maintenance window to be scheduled.

      The format is YYYY-MM-DDThh:mm:ss\<offset\>

      \<offset\> is the time offset from UTC that the current timezone set in iDRAC in the format: +05:30 for IST.


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-network_adapter_id"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_network_attributes_module__parameter-network_adapter_id:

      .. rst-class:: ansible-option-title

      **network_adapter_id**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-network_adapter_id" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      FQDD of the network adapter device that represents the physical network adapter capable of connecting to a computer network.

      An example of FQDD of the network adapter is 'NIC.Mezzanine.1A'


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-network_attributes"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_network_attributes_module__parameter-network_attributes:

      .. rst-class:: ansible-option-title

      **network_attributes**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-network_attributes" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Dictionary of network attributes and value. To view the list of attributes and its structure, see the below API \ https://I%28idrac_ip\ /redfish/v1/Systems/System.Embedded.1/NetworkAdapters/\<network\_id\>/NetworkDeviceFunctions/ \<network\_port\_id\>/Settings) and \ https://<idrac_ip>/redfish/v1/Schemas/NetworkDeviceFunction.v1_8_0.json\ .

      \ :emphasis:`network\_attributes`\  is mutually exclusive with \ :emphasis:`oem\_network\_attributes`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-network_device_function_id"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_network_attributes_module__parameter-network_device_function_id:

      .. rst-class:: ansible-option-title

      **network_device_function_id**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-network_device_function_id" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      FQDD of the network adapter device function that represents a logical interface exposed by the network adapter.

      An example of FQDD of the network adapter device function is 'NIC.Mezzanine.1A-1-1'


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-oem_network_attributes"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_network_attributes_module__parameter-oem_network_attributes:

      .. rst-class:: ansible-option-title

      **oem_network_attributes**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-oem_network_attributes" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The attributes must be part of the Integrated Dell Remote Access Controller Attribute Registry. To view the list of attributes in Attribute Registry for iDRAC9 and newer versions. For more information, see, \ https://I%28idrac_ip\ /redfish/v1/Chassis/System.Embedded.1/NetworkAdapters/\<network\_id\>/NetworkDeviceFunctions/ \<network\_port\_id\>/Oem/Dell/DellNetworkAttributes/\<network\_port\_id\>) and \ https://I%28idrac_ip\ /redfish/v1/Registries/NetworkAttributesRegistry\_\<network\_port\_id\>/ NetworkAttributesRegistry\_network\_port\_id.json).

      For iDRAC8 based servers, derive the network attribute name from Server Configuration Profile.

      \ :emphasis:`oem\_network\_attributes`\  is mutually exclusive with \ :emphasis:`network\_attributes`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-resource_id"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_network_attributes_module__parameter-resource_id:

      .. rst-class:: ansible-option-title

      **resource_id**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-resource_id" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Id of the resource.

      If the value for resource ID is not provided, the module picks the first resource ID available from the list of system resources returned by the iDRAC.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-timeout"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_network_attributes_module__parameter-timeout:

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
        <div class="ansibleOptionAnchor" id="parameter-validate_certs"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_network_attributes_module__parameter-validate_certs:

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
   - Run this module from a system that has direct access to Dell iDRAC.
   - This module supports both IPv4 and IPv6 address.
   - This module supports \ :literal:`check\_mode`\ .

.. Seealso


.. Examples

Examples
--------

.. code-block:: yaml+jinja

    
    ---
    - name: Configure OEM network attributes
      dellemc.openmanage.idrac_network_attributes:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        network_id: "NIC.Integrated.1"
        network_port_id: "NIC.Integrated.1-1-1"
        apply_time: "Immediate"
        oem_network_attributes:
          BannerMessageTimeout: "4"

    - name: Configure OEM network attributes to apply on reset
      dellemc.openmanage.idrac_network_attributes:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        network_id: NIC.Integrated.1
        network_port_id: "NIC.Integrated.1-1-1"
        oem_network_attributes:
          BannerMessageTimeout: "4"
        apply_time: OnReset

    - name: Configure OEM network attributes to apply at maintainance window
      dellemc.openmanage.idrac_network_attributes:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        network_id: NIC.Integrated.1
        network_port_id: "NIC.Integrated.1-1-1"
        oem_network_attributes:
          BannerMessageTimeout: "4"
        apply_time: AtMaintenanceWindowStart
        maintenance_window:
          start_time: "2022-09-30T05:15:40-05:00"
          duration: 600

    - name: Clearing the pending attributes
      dellemc.openmanage.idrac_network_attributes:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        network_id: NIC.Integrated.1
        network_port_id: "NIC.Integrated.1-1-1"
        apply_time: "Immediate"
        clear_pending: true

    - name: Clearing the OEM pending attributes and apply the OEM network attributes
      dellemc.openmanage.idrac_network_attributes:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        network_id: NIC.Integrated.1
        network_port_id: "NIC.Integrated.1-1-1"
        apply_time: "Immediate"
        clear_pending: true
        oem_network_attributes:
          BannerMessageTimeout: "4"

    - name: Configure OEM network attributes and wait for the job
      dellemc.openmanage.idrac_network_attributes:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        network_id: NIC.Integrated.1
        network_port_id: "NIC.Integrated.1-1-1"
        apply_time: "Immediate"
        oem_network_attributes:
          LnkSpeed: "10MbpsHalf"
          WakeOnLan: "Enabled"
          VLanMode: "Enabled"
        job_wait: true
        job_wait_timeout: 2000

    - name: Configure redfish network attributes to update fiber channel on reset
      dellemc.openmanage.idrac_network_attributes:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        network_id: NIC.Integrated.1
        network_port_id: "NIC.Integrated.1-1-1"
        apply_time: OnReset
        network_attributes:
          Ethernet:
            VLAN:
              VLANEnable: true

    - name: Configure redfish network attributes to apply on reset
      dellemc.openmanage.idrac_network_attributes:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        network_id: NIC.Integrated.1
        network_port_id: "NIC.Integrated.1-1-1"
        network_attributes:
          Ethernet:
            VLAN:
              VLANEnable: true
        apply_time: OnReset

    - name: Configure redfish network attributes of iscsi to apply at maintainance window start
      dellemc.openmanage.idrac_network_attributes:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        network_id: NIC.Integrated.1
        network_port_id: "NIC.Integrated.1-1-1"
        network_attributes:
          iSCSIBoot:
            InitiatorIPAddress: 1.0.0.1
        apply_time: AtMaintenanceWindowStart
        maintenance_window:
          start_time: "2022-09-30T05:15:40-05:00"
          duration: 600

    - name: Configure redfish network attributes to apply at maintainance window on reset
      dellemc.openmanage.idrac_network_attributes:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        network_id: NIC.Integrated.1
        network_port_id: "NIC.Integrated.1-1-1"
        network_attributes:
          Ethernet:
            VLAN:
              VLANEnable: false
              VLANId: 1
        apply_time: AtMaintenanceWindowStart
        maintenance_window:
          start_time: "2022-09-30T05:15:40-05:00"
          duration: 600




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

      .. _ansible_collections.dellemc.openmanage.idrac_network_attributes_module__return-error_info:

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
        <div class="ansibleOptionAnchor" id="return-invalid_attributes"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_network_attributes_module__return-invalid_attributes:

      .. rst-class:: ansible-option-title

      **invalid_attributes**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-invalid_attributes" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Dictionary of invalid attributes provided that cannot be applied.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` On invalid attributes or values

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"IscsiInitiatorIpAddr": "Attribute is not valid.", "IscsiInitiatorSubnet": "Attribute is not valid."}`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-job_status"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_network_attributes_module__return-job_status:

      .. rst-class:: ansible-option-title

      **job_status**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-job_status" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Returns the output for status of the job.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` always

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"ActualRunningStartTime": null, "ActualRunningStopTime": null, "CompletionTime": null, "Description": "Job Instance", "EndTime": "TIME\_NA", "Id": "JID\_XXXXXXXXX", "JobState": "Scheduled", "JobType": "NICConfiguration", "Message": "Task successfully scheduled.", "MessageArgs": [], "MessageId": "JCP001", "Name": "Configure: NIC.Integrated.1-1-1", "PercentComplete": 0, "StartTime": "2023-08-07T06:21:24", "TargetSettingsURI": null}`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-msg"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_network_attributes_module__return-msg:

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

      Status of the attribute update operation.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` when network attributes is applied

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`"Successfully updated the network attributes."`


      .. raw:: html

        </div>



..  Status (Presently only deprecated)


.. Authors

Authors
~~~~~~~

- Abhishek Sinha(@ABHISHEK-SINHA10)



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

