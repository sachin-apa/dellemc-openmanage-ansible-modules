
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

.. _ansible_collections.dellemc.openmanage.redfish_powerstate_module:

.. Anchors: short name for ansible.builtin

.. Anchors: aliases



.. Title

dellemc.openmanage.redfish_powerstate module -- Manage device power state
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. Collection note

.. note::
    This module is part of the `dellemc.openmanage collection <https://galaxy.ansible.com/dellemc/openmanage>`_ (version 8.5.0).

    To install it, use: :code:`ansible-galaxy collection install dellemc.openmanage`.
    You need further requirements to be able to use this module,
    see :ref:`Requirements <ansible_collections.dellemc.openmanage.redfish_powerstate_module_requirements>` for details.

    To use it in a playbook, specify: :code:`dellemc.openmanage.redfish_powerstate`.

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

- This module allows to manage the different power states of the specified device.


.. Aliases


.. Requirements

.. _ansible_collections.dellemc.openmanage.redfish_powerstate_module_requirements:

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
        <div class="ansibleOptionAnchor" id="parameter-baseuri"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_powerstate_module__parameter-baseuri:

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

      .. _ansible_collections.dellemc.openmanage.redfish_powerstate_module__parameter-ca_path:

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
        <div class="ansibleOptionAnchor" id="parameter-password"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_powerstate_module__parameter-password:

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
        <div class="ansibleOptionAnchor" id="parameter-reset_type"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_powerstate_module__parameter-reset_type:

      .. rst-class:: ansible-option-title

      **reset_type**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-reset_type" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      This option resets the device.

      If \ :literal:`ForceOff`\ , Turns off the device immediately.

      If \ :literal:`ForceOn`\ , Turns on the device immediately.

      If \ :literal:`ForceRestart`\ , Turns off the device immediately, and then restarts the device.

      If \ :literal:`GracefulRestart`\ , Performs graceful shutdown of the device, and then restarts the device.

      If \ :literal:`GracefulShutdown`\ , Performs a graceful shutdown of the device, and the turns off the device.

      If \ :literal:`Nmi`\ , Sends a diagnostic interrupt to the device. This is usually a non-maskable interrupt (NMI) on x86 device.

      If \ :literal:`On`\ , Turns on the device.

      If \ :literal:`PowerCycle`\ , Performs power cycle on the device.

      If \ :literal:`PushPowerButton`\ , Simulates the pressing of a physical power button on the device.

      When a power control operation is performed, which is not supported on the device, an error message is displayed with the list of operations that can be performed.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"ForceOff"`
      - :ansible-option-choices-entry:`"ForceOn"`
      - :ansible-option-choices-entry:`"ForceRestart"`
      - :ansible-option-choices-entry:`"GracefulRestart"`
      - :ansible-option-choices-entry:`"GracefulShutdown"`
      - :ansible-option-choices-entry:`"Nmi"`
      - :ansible-option-choices-entry:`"On"`
      - :ansible-option-choices-entry:`"PowerCycle"`
      - :ansible-option-choices-entry:`"PushPowerButton"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-resource_id"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_powerstate_module__parameter-resource_id:

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

      The unique identifier of the device being managed. For example- \ https://<I%28baseuri\ \>/redfish/v1/Systems/\<\ :emphasis:`resource\_id`\ \>).

      This option is mandatory for \ :emphasis:`base\_uri`\  with multiple devices.

      To get the device details, use the API \ https://<I%28baseuri\ \>/redfish/v1/Systems).


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-timeout"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_powerstate_module__parameter-timeout:

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

      .. _ansible_collections.dellemc.openmanage.redfish_powerstate_module__parameter-username:

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

      .. _ansible_collections.dellemc.openmanage.redfish_powerstate_module__parameter-validate_certs:

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
   - This module supports \ :literal:`check\_mode`\ .

.. Seealso


.. Examples

Examples
--------

.. code-block:: yaml+jinja

    
    ---
    - name: Manage power state of the first device
      dellemc.openmanage.redfish_powerstate:
           baseuri: "192.168.0.1"
           username: "username"
           password: "password"
           ca_path: "/path/to/ca_cert.pem"
           reset_type: "On"

    - name: Manage power state of a specified device
      dellemc.openmanage.redfish_powerstate:
           baseuri: "192.168.0.1"
           username: "username"
           password: "password"
           ca_path: "/path/to/ca_cert.pem"
           reset_type: "ForceOff"
           resource_id: "System.Embedded.1"




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

      .. _ansible_collections.dellemc.openmanage.redfish_powerstate_module__return-error_info:

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

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"error": {"@Message.ExtendedInfo": [{"Message": "Unable to complete the operation because the resource /redfish/v1/Systems/System.Embedded.1/Actions/ComputerSystem.Reset entered in not found.", "MessageArgs": ["/redfish/v1/Systems/System.Embedded.1/Actions/ComputerSystem.Reset"], "MessageArgs@odata.count": 1, "MessageId": "IDRAC.2.1.SYS403", "RelatedProperties": [], "RelatedProperties@odata.count": 0, "Resolution": "Enter the correct resource and retry the operation. For information about valid resource, see the Redfish Users Guide available on the support site.", "Severity": "Critical"}], "code": "Base.1.5.GeneralError", "message": "A general error has occurred. See ExtendedInfo for more information"}}`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-msg"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_powerstate_module__return-msg:

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

      Overall status of the reset operation.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` always

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`"Successfully performed the reset type operation 'On'."`


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

