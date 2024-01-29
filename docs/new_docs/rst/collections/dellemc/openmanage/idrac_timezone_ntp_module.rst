
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

.. _ansible_collections.dellemc.openmanage.idrac_timezone_ntp_module:

.. Anchors: short name for ansible.builtin

.. Anchors: aliases



.. Title

dellemc.openmanage.idrac_timezone_ntp module -- Configures time zone and NTP on iDRAC
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. Collection note

.. note::
    This module is part of the `dellemc.openmanage collection <https://galaxy.ansible.com/dellemc/openmanage>`_ (version 8.5.0).

    To install it, use: :code:`ansible-galaxy collection install dellemc.openmanage`.
    You need further requirements to be able to use this module,
    see :ref:`Requirements <ansible_collections.dellemc.openmanage.idrac_timezone_ntp_module_requirements>` for details.

    To use it in a playbook, specify: :code:`dellemc.openmanage.idrac_timezone_ntp`.

.. version_added

.. rst-class:: ansible-version-added

New in dellemc.openmanage 2.1.0

.. contents::
   :local:
   :depth: 1

.. Deprecated

DEPRECATED
----------
:Removed in: major release after 2024-07-31
:Why: Replaced with \ :ref:`dellemc.openmanage.idrac\_attributes <ansible_collections.dellemc.openmanage.idrac_attributes_module>`\ .
:Alternative: Use \ :ref:`dellemc.openmanage.idrac\_attributes <ansible_collections.dellemc.openmanage.idrac_attributes_module>`\  instead.

Synopsis
--------

.. Description

- This module allows to configure time zone and NTP on iDRAC.


.. Aliases


.. Requirements

.. _ansible_collections.dellemc.openmanage.idrac_timezone_ntp_module_requirements:

Requirements
------------
The below requirements are needed on the host that executes this module.

- omsdk \>= 1.2.488
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
        <div class="ansibleOptionAnchor" id="parameter-ca_path"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_timezone_ntp_module__parameter-ca_path:

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
        <div class="ansibleOptionAnchor" id="parameter-enable_ntp"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_timezone_ntp_module__parameter-enable_ntp:

      .. rst-class:: ansible-option-title

      **enable_ntp**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-enable_ntp" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Allows to enable or disable NTP on iDRAC.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"Enabled"`
      - :ansible-option-choices-entry:`"Disabled"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-idrac_ip"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_timezone_ntp_module__parameter-idrac_ip:

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

      .. _ansible_collections.dellemc.openmanage.idrac_timezone_ntp_module__parameter-idrac_password:
      .. _ansible_collections.dellemc.openmanage.idrac_timezone_ntp_module__parameter-idrac_pwd:

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

      .. _ansible_collections.dellemc.openmanage.idrac_timezone_ntp_module__parameter-idrac_port:

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

      .. _ansible_collections.dellemc.openmanage.idrac_timezone_ntp_module__parameter-idrac_user:

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
        <div class="ansibleOptionAnchor" id="parameter-ntp_server_1"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_timezone_ntp_module__parameter-ntp_server_1:

      .. rst-class:: ansible-option-title

      **ntp_server_1**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-ntp_server_1" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The IP address of the NTP server 1.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-ntp_server_2"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_timezone_ntp_module__parameter-ntp_server_2:

      .. rst-class:: ansible-option-title

      **ntp_server_2**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-ntp_server_2" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The IP address of the NTP server 2.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-ntp_server_3"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_timezone_ntp_module__parameter-ntp_server_3:

      .. rst-class:: ansible-option-title

      **ntp_server_3**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-ntp_server_3" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The IP address of the NTP server 3.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-setup_idrac_timezone"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_timezone_ntp_module__parameter-setup_idrac_timezone:

      .. rst-class:: ansible-option-title

      **setup_idrac_timezone**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-setup_idrac_timezone" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Allows to configure time zone on iDRAC.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-share_mnt"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_timezone_ntp_module__parameter-share_mnt:

      .. rst-class:: ansible-option-title

      **share_mnt**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-share_mnt" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      (deprecated)Local mount path of the network share with read-write permission for ansible user. This option is mandatory for network shares.

      This option is deprecated and will be removed in the later version.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-share_name"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_timezone_ntp_module__parameter-share_name:

      .. rst-class:: ansible-option-title

      **share_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-share_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      (deprecated)Network share or a local path.

      This option is deprecated and will be removed in the later version.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-share_password"></div>
        <div class="ansibleOptionAnchor" id="parameter-share_pwd"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_timezone_ntp_module__parameter-share_password:
      .. _ansible_collections.dellemc.openmanage.idrac_timezone_ntp_module__parameter-share_pwd:

      .. rst-class:: ansible-option-title

      **share_password**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-share_password" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-aliases:`aliases: share_pwd`

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      (deprecated)Network share user password. This option is mandatory for CIFS share.

      This option is deprecated and will be removed in the later version.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-share_user"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_timezone_ntp_module__parameter-share_user:

      .. rst-class:: ansible-option-title

      **share_user**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-share_user" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      (deprecated)Network share user name. Use the format 'user@domain' or 'domain\\user' if user is part of a domain. This option is mandatory for CIFS share.

      This option is deprecated and will be removed in the later version.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-timeout"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_timezone_ntp_module__parameter-timeout:

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

      .. _ansible_collections.dellemc.openmanage.idrac_timezone_ntp_module__parameter-validate_certs:

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
   - This module requires 'Administrator' privilege for \ :emphasis:`idrac\_user`\ .
   - Run this module from a system that has direct access to Dell iDRAC.
   - This module supports both IPv4 and IPv6 address for \ :emphasis:`idrac\_ip`\ .
   - This module supports \ :literal:`check\_mode`\ .

.. Seealso


.. Examples

Examples
--------

.. code-block:: yaml+jinja

    
    ---
    - name: Configure time zone and NTP on iDRAC
      dellemc.openmanage.idrac_timezone_ntp:
           idrac_ip: "190.168.0.1"
           idrac_user: "user_name"
           idrac_password: "user_password"
           ca_path: "/path/to/ca_cert.pem"
           setup_idrac_timezone: "UTC"
           enable_ntp: Enabled
           ntp_server_1: "190.168.0.1"
           ntp_server_2: "190.168.0.2"
           ntp_server_3: "190.168.0.3"




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

      .. _ansible_collections.dellemc.openmanage.idrac_timezone_ntp_module__return-error_info:

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
        <div class="ansibleOptionAnchor" id="return-msg"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_timezone_ntp_module__return-msg:

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

      Overall status of the timezone and ntp configuration.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` always

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`"Successfully configured the iDRAC time settings."`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-timezone_ntp_status"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_timezone_ntp_module__return-timezone_ntp_status:

      .. rst-class:: ansible-option-title

      **timezone_ntp_status**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-timezone_ntp_status" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Job details of the time zone setting operation.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` success

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"@odata.context": "/redfish/v1/$metadata#DellJob.DellJob", "@odata.id": "/redfish/v1/Managers/iDRAC.Embedded.1/Jobs/JID\_861801613971", "@odata.type": "#DellJob.v1\_0\_0.DellJob", "CompletionTime": "2020-04-06T19:06:01", "Description": "Job Instance", "EndTime": null, "Id": "JID\_861801613971", "JobState": "Completed", "JobType": "ImportConfiguration", "Message": "Successfully imported and applied Server Configuration Profile.", "MessageArgs": [], "MessageId": "SYS053", "Name": "Import Configuration", "PercentComplete": 100, "StartTime": "TIME\_NOW", "Status": "Success", "TargetSettingsURI": null, "retval": true}`


      .. raw:: html

        </div>



..  Status (Presently only deprecated)

Status
------

.. Deprecated note

- This module will be removed in a major release after 2024-07-31.
  *[deprecated]*
- For more information see `DEPRECATED`_.


.. Authors

Authors
~~~~~~~

- Felix Stephen (@felixs88)
- Anooja Vardhineni (@anooja-vardhineni)



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

