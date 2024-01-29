
.. Document meta

:orphan:

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

.. Anchors

.. _ansible_collections.dellemc.openmanage.idrac_certificate_role:

.. Anchors: aliases


.. Title

dellemc.openmanage.idrac_certificate role -- This role allows to generate certificate signing request, import, and export certificates on iDRAC
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. Collection note

.. note::
    This role is part of the `dellemc.openmanage collection <https://galaxy.ansible.com/dellemc/openmanage>`_ (version 8.5.0).

    To install it use: :code:`ansible-galaxy collection install dellemc.openmanage`.

    To use it in a playbook, specify: :code:`dellemc.openmanage.idrac_certificate`.

.. contents::
   :local:
   :depth: 2


.. Entry point title

Entry point ``main`` -- This role allows to generate certificate signing request, import, and export certificates on iDRAC
--------------------------------------------------------------------------------------------------------------------------

.. version_added

.. rst-class:: ansible-version-added

New in dellemc.openmanage 7.4.0

.. Deprecated


Synopsis
^^^^^^^^

.. Description

- Role to manage the iDRAC certificates - Generate CSR, Import/Export certificates, and Reset configuration - for PowerEdge servers.

.. Requirements


.. Options

Parameters
^^^^^^^^^^

.. rst-class:: ansible-option-table

.. list-table::
  :width: 100%
  :widths: auto
  :header-rows: 1

  * - Parameter
    - Comments

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--ca_path"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_certificate_role__parameter-main__ca_path:

      .. rst-class:: ansible-option-title

      **ca_path**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--ca_path" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The Privacy Enhanced Mail (PEM) file that contains a CA certificate to be used for the validation.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--cert_params"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_certificate_role__parameter-main__cert_params:

      .. rst-class:: ansible-option-title

      **cert_params**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--cert_params" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-main--cert_params/common_name"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_certificate_role__parameter-main__cert_params/common_name:

      .. rst-class:: ansible-option-title

      **common_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--cert_params/common_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The common name of the certificate.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--cert_params/country_code"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_certificate_role__parameter-main__cert_params/country_code:

      .. rst-class:: ansible-option-title

      **country_code**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--cert_params/country_code" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The country code of the country where the entity applying for certification is located.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--cert_params/email_address"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_certificate_role__parameter-main__cert_params/email_address:

      .. rst-class:: ansible-option-title

      **email_address**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--cert_params/email_address" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The email associated with the CSR.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--cert_params/locality_name"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_certificate_role__parameter-main__cert_params/locality_name:

      .. rst-class:: ansible-option-title

      **locality_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--cert_params/locality_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The city or other location where the entity applying for certification is located.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--cert_params/organization_name"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_certificate_role__parameter-main__cert_params/organization_name:

      .. rst-class:: ansible-option-title

      **organization_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--cert_params/organization_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The name associated with an organization.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--cert_params/organization_unit"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_certificate_role__parameter-main__cert_params/organization_unit:

      .. rst-class:: ansible-option-title

      **organization_unit**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--cert_params/organization_unit" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The name associated with an organizational unit. For example, department name.


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`"True"`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--cert_params/state_name"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_certificate_role__parameter-main__cert_params/state_name:

      .. rst-class:: ansible-option-title

      **state_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--cert_params/state_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      The state where the entity applying for certification is located.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--cert_params/subject_alt_name"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_certificate_role__parameter-main__cert_params/subject_alt_name:

      .. rst-class:: ansible-option-title

      **subject_alt_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--cert_params/subject_alt_name" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-main--certificate_path"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_certificate_role__parameter-main__certificate_path:

      .. rst-class:: ansible-option-title

      **certificate_path**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--certificate_path" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-main--certificate_type"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_certificate_role__parameter-main__certificate_type:

      .. rst-class:: ansible-option-title

      **certificate_type**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--certificate_type" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Type of the iDRAC certificate - \ :literal:`HTTPS`\  The Dell self-signed SSL certificate. - (CA) Certificate Authority(CA) signed SSL certificate. - \ :literal:`CSC`\  The custom signed SSL certificate. - \ :literal:`CLIENT\_TRUST\_CERTIFICATE`\  Client trust certificate.


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
        <div class="ansibleOptionAnchor" id="parameter-main--command"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_certificate_role__parameter-main__command:

      .. rst-class:: ansible-option-title

      **command**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--command" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      \ :literal:`generate\_csr`\ , generate CSR. This requires \ :emphasis:`cert\_params`\  and \ :emphasis:`certificate\_path`\ .


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
        <div class="ansibleOptionAnchor" id="parameter-main--hostname"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_certificate_role__parameter-main__hostname:

      .. rst-class:: ansible-option-title

      **hostname**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--hostname" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-main--https_port"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_certificate_role__parameter-main__https_port:

      .. rst-class:: ansible-option-title

      **https_port**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--https_port" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-main--https_timeout"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_certificate_role__parameter-main__https_timeout:

      .. rst-class:: ansible-option-title

      **https_timeout**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--https_timeout" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`




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
        <div class="ansibleOptionAnchor" id="parameter-main--passphrase"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_certificate_role__parameter-main__passphrase:

      .. rst-class:: ansible-option-title

      **passphrase**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--passphrase" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-main--password"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_certificate_role__parameter-main__password:

      .. rst-class:: ansible-option-title

      **password**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--password" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-main--reset"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_certificate_role__parameter-main__reset:

      .. rst-class:: ansible-option-title

      **reset**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--reset" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-main--resource_id"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_certificate_role__parameter-main__resource_id:

      .. rst-class:: ansible-option-title

      **resource_id**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--resource_id" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-main--username"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_certificate_role__parameter-main__username:

      .. rst-class:: ansible-option-title

      **username**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--username" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-main--validate_certs"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_certificate_role__parameter-main__validate_certs:

      .. rst-class:: ansible-option-title

      **validate_certs**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--validate_certs" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`




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
        <div class="ansibleOptionAnchor" id="parameter-main--wait"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_certificate_role__parameter-main__wait:

      .. rst-class:: ansible-option-title

      **wait**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--wait" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Maximum wait time for iDRAC to start after the reset, in seconds.

      This is applicable when \ :emphasis:`command`\  is \ :literal:`import`\  or \ :literal:`reset`\  and \ :emphasis:`reset`\  is \ :literal:`True`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`300`

      .. raw:: html

        </div>


.. Attributes


.. Notes


.. Seealso




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

