
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

.. _ansible_collections.dellemc.openmanage.idrac_certificates_module:

.. Anchors: short name for ansible.builtin

.. Anchors: aliases



.. Title

dellemc.openmanage.idrac_certificates module -- Configure certificates for iDRAC
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. Collection note

.. note::
    This module is part of the `dellemc.openmanage collection <https://galaxy.ansible.com/dellemc/openmanage>`_ (version 8.5.0).

    To install it, use: :code:`ansible-galaxy collection install dellemc.openmanage`.
    You need further requirements to be able to use this module,
    see :ref:`Requirements <ansible_collections.dellemc.openmanage.idrac_certificates_module_requirements>` for details.

    To use it in a playbook, specify: :code:`dellemc.openmanage.idrac_certificates`.

.. version_added

.. rst-class:: ansible-version-added

New in dellemc.openmanage 5.5.0

.. contents::
   :local:
   :depth: 1

.. Deprecated


Synopsis
--------

.. Description

- This module allows to generate certificate signing request, import, and export certificates on iDRAC.


.. Aliases


.. Requirements

.. _ansible_collections.dellemc.openmanage.idrac_certificates_module_requirements:

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

      .. _ansible_collections.dellemc.openmanage.idrac_certificates_module__parameter-ca_path:

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
        <div class="ansibleOptionAnchor" id="parameter-cert_params"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_certificates_module__parameter-cert_params:

      .. rst-class:: ansible-option-title

      **cert_params**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-cert_params" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Certificate parameters to generate signing request.


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-cert_params/common_name"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_certificates_module__parameter-cert_params/common_name:

      .. rst-class:: ansible-option-title

      **common_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-cert_params/common_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The common name of the certificate.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-cert_params/country_code"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_certificates_module__parameter-cert_params/country_code:

      .. rst-class:: ansible-option-title

      **country_code**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-cert_params/country_code" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The country code of the country where the entity applying for certification is located.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-cert_params/email_address"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_certificates_module__parameter-cert_params/email_address:

      .. rst-class:: ansible-option-title

      **email_address**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-cert_params/email_address" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The email associated with the CSR.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-cert_params/locality_name"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_certificates_module__parameter-cert_params/locality_name:

      .. rst-class:: ansible-option-title

      **locality_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-cert_params/locality_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The city or other location where the entity applying for certification is located.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-cert_params/organization_name"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_certificates_module__parameter-cert_params/organization_name:

      .. rst-class:: ansible-option-title

      **organization_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-cert_params/organization_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The name associated with an organization.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-cert_params/organization_unit"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_certificates_module__parameter-cert_params/organization_unit:

      .. rst-class:: ansible-option-title

      **organization_unit**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-cert_params/organization_unit" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The name associated with an organizational unit. For example department name.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-cert_params/state_name"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_certificates_module__parameter-cert_params/state_name:

      .. rst-class:: ansible-option-title

      **state_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-cert_params/state_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The state where the entity applying for certification is located.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-cert_params/subject_alt_name"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_certificates_module__parameter-cert_params/subject_alt_name:

      .. rst-class:: ansible-option-title

      **subject_alt_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-cert_params/subject_alt_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The alternative domain names associated with the request.


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`[]`

      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-certificate_path"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_certificates_module__parameter-certificate_path:

      .. rst-class:: ansible-option-title

      **certificate_path**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-certificate_path" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`path`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Absolute path of the certificate file if \ :emphasis:`command`\  is \ :literal:`import`\ .

      Directory path with write permissions if \ :emphasis:`command`\  is \ :literal:`generate\_csr`\  or \ :literal:`export`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-certificate_type"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_certificates_module__parameter-certificate_type:

      .. rst-class:: ansible-option-title

      **certificate_type**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-certificate_type" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Type of the iDRAC certificate.

      \ :literal:`HTTPS`\  The Dell self-signed SSL certificate.

      \ :literal:`CA`\  Certificate Authority(CA) signed SSL certificate.

      \ :literal:`CSC`\  The custom signed SSL certificate.

      \ :literal:`CLIENT\_TRUST\_CERTIFICATE`\  Client trust certificate.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`"HTTPS"` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`"CA"`
      - :ansible-option-choices-entry:`"CSC"`
      - :ansible-option-choices-entry:`"CLIENT\_TRUST\_CERTIFICATE"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-command"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_certificates_module__parameter-command:

      .. rst-class:: ansible-option-title

      **command**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-command" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      \ :literal:`generate\_csr`\ , generate CSR. This requires \ :emphasis:`cert\_params`\  and \ :emphasis:`certificate\_path`\ . This is applicable only for \ :literal:`HTTPS`\ 

      \ :literal:`import`\ , import the certificate file. This requires \ :emphasis:`certificate\_path`\ .

      \ :literal:`export`\ , export the certificate. This requires \ :emphasis:`certificate\_path`\ .

      \ :literal:`reset`\ , reset the certificate to default settings. This is applicable only for \ :literal:`HTTPS`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"import"`
      - :ansible-option-choices-entry:`"export"`
      - :ansible-option-choices-entry-default:`"generate\_csr"` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`"reset"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-idrac_ip"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_certificates_module__parameter-idrac_ip:

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

      .. _ansible_collections.dellemc.openmanage.idrac_certificates_module__parameter-idrac_password:
      .. _ansible_collections.dellemc.openmanage.idrac_certificates_module__parameter-idrac_pwd:

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

      .. _ansible_collections.dellemc.openmanage.idrac_certificates_module__parameter-idrac_port:

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

      .. _ansible_collections.dellemc.openmanage.idrac_certificates_module__parameter-idrac_user:

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
        <div class="ansibleOptionAnchor" id="parameter-passphrase"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_certificates_module__parameter-passphrase:

      .. rst-class:: ansible-option-title

      **passphrase**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-passphrase" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The passphrase string if the certificate to be imported is passphrase protected.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-reset"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_certificates_module__parameter-reset:

      .. rst-class:: ansible-option-title

      **reset**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-reset" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      To reset the iDRAC after the certificate operation.

      This is applicable when \ :emphasis:`command`\  is \ :literal:`import`\  or \ :literal:`reset`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry-default:`true` :ansible-option-choices-default-mark:`← (default)`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-resource_id"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_certificates_module__parameter-resource_id:

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

      Redfish ID of the resource.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-timeout"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_certificates_module__parameter-timeout:

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

      .. _ansible_collections.dellemc.openmanage.idrac_certificates_module__parameter-validate_certs:

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

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-wait"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_certificates_module__parameter-wait:

      .. rst-class:: ansible-option-title

      **wait**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-wait" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Maximum wait time for iDRAC to start after the reset, in seconds.

      This is applicable when \ :emphasis:`command`\  is \ :literal:`import`\  or \ :literal:`reset`\  and \ :emphasis:`reset`\  is \ :literal:`true`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`300`

      .. raw:: html

        </div>


.. Attributes


.. Notes

Notes
-----

.. note::
   - The certificate operations are supported on iDRAC firmware 5.10.10.00 and above.
   - Run this module from a system that has direct access to Dell iDRAC.
   - This module supports \ :literal:`check\_mode`\ .

.. Seealso


.. Examples

Examples
--------

.. code-block:: yaml+jinja

    
    ---
    - name: Generate HTTPS certificate signing request
      dellemc.openmanage.idrac_certificates:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        command: "generate_csr"
        certificate_type: "HTTPS"
        certificate_path: "/home/omam/mycerts"
        cert_params:
          common_name: "sample.domain.com"
          organization_unit: "OrgUnit"
          locality_name: "Bangalore"
          state_name: "Karnataka"
          country_code: "IN"
          email_address: "admin@domain.com"
          organization_name: "OrgName"
          subject_alt_name:
            - 192.198.2.1

    - name: Import a HTTPS certificate.
      dellemc.openmanage.idrac_certificates:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        command: "import"
        certificate_type: "HTTPS"
        certificate_path: "/path/to/cert.pem"

    - name: Export a HTTPS certificate.
      dellemc.openmanage.idrac_certificates:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        command: "export"
        certificate_type: "HTTPS"
        certificate_path: "/home/omam/mycert_dir"

    - name: Import a CSC certificate.
      dellemc.openmanage.idrac_certificates:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        command: "import"
        certificate_type: "CSC"
        certificate_path: "/path/to/cert.pem"

    - name: Export a Client trust certificate.
      dellemc.openmanage.idrac_certificates:
        idrac_ip: "192.168.0.1"
        idrac_user: "user_name"
        idrac_password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        command: "export"
        certificate_type: "CLIENT_TRUST_CERTIFICATE"
        certificate_path: "/home/omam/mycert_dir"




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
        <div class="ansibleOptionAnchor" id="return-certificate_path"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_certificates_module__return-certificate_path:

      .. rst-class:: ansible-option-title

      **certificate_path**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-certificate_path" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The csr or exported certificate file path


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` when \ :emphasis:`command`\  is \ :literal:`export`\  or \ :literal:`generate\_csr`\ 

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`"/home/ansible/myfiles/cert.pem"`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-error_info"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_certificates_module__return-error_info:

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

      .. _ansible_collections.dellemc.openmanage.idrac_certificates_module__return-msg:

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

      Status of the certificate configuration operation.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` always

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`"Successfully performed the operation generate\_csr."`


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

