
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

.. _ansible_collections.dellemc.openmanage.idrac_firmware_role:

.. Anchors: aliases


.. Title

dellemc.openmanage.idrac_firmware role -- Firmware update from a repository on a network share (CIFS, NFS, HTTP, HTTPS, FTP)
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. Collection note

.. note::
    This role is part of the `dellemc.openmanage collection <https://galaxy.ansible.com/dellemc/openmanage>`_ (version 8.5.0).

    To install it use: :code:`ansible-galaxy collection install dellemc.openmanage`.

    To use it in a playbook, specify: :code:`dellemc.openmanage.idrac_firmware`.

.. contents::
   :local:
   :depth: 2


.. Entry point title

Entry point ``main`` -- Firmware update from a repository on a network share (CIFS, NFS, HTTP, HTTPS, FTP)
----------------------------------------------------------------------------------------------------------

.. version_added

.. rst-class:: ansible-version-added

New in dellemc.openmanage 7.5.0

.. Deprecated


Synopsis
^^^^^^^^

.. Description

- Update the Firmware by connecting to a network share (CIFS, NFS, HTTP, HTTPS, FTP) that contains a catalog of available updates.

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
        <div class="ansibleOptionAnchor" id="parameter-main--apply_update"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_firmware_role__parameter-main__apply_update:

      .. rst-class:: ansible-option-title

      **apply_update**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--apply_update" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      If \ :emphasis:`apply\_update`\  is set to \ :literal:`true`\ , then the packages are applied.

      If \ :emphasis:`apply\_update`\  is set to \ :literal:`false`\ , no updates are applied, and a catalog report of packages is generated and returned.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry-default:`true` :ansible-option-choices-default-mark:`← (default)`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--ca_path"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_firmware_role__parameter-main__ca_path:

      .. rst-class:: ansible-option-title

      **ca_path**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--ca_path" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`path`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The Privacy Enhanced Mail (PEM) file that contains a CA certificate to be used for the validation.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--catalog_file_name"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_firmware_role__parameter-main__catalog_file_name:

      .. rst-class:: ansible-option-title

      **catalog_file_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--catalog_file_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Catalog file name relative to the \ :emphasis:`share\_name`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`"Catalog.xml"`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--hostname"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_firmware_role__parameter-main__hostname:

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

      iDRAC IP Address or hostname.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--http_timeout"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_firmware_role__parameter-main__http_timeout:

      .. rst-class:: ansible-option-title

      **http_timeout**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--http_timeout" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-main--https_port"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_firmware_role__parameter-main__https_port:

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
        <div class="ansibleOptionAnchor" id="parameter-main--ignore_cert_warning"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_firmware_role__parameter-main__ignore_cert_warning:

      .. rst-class:: ansible-option-title

      **ignore_cert_warning**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--ignore_cert_warning" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Specifies if certificate warnings are ignored when HTTPS share is used. If \ :literal:`true`\  option is set, then the certificate warnings are ignored.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry-default:`true` :ansible-option-choices-default-mark:`← (default)`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--job_wait"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_firmware_role__parameter-main__job_wait:

      .. rst-class:: ansible-option-title

      **job_wait**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--job_wait" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Whether to wait for job completion or not.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry-default:`true` :ansible-option-choices-default-mark:`← (default)`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--password"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_firmware_role__parameter-main__password:

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
        <div class="ansibleOptionAnchor" id="parameter-main--proxy_passwd"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_firmware_role__parameter-main__proxy_passwd:

      .. rst-class:: ansible-option-title

      **proxy_passwd**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--proxy_passwd" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The password for the proxy server.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--proxy_port"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_firmware_role__parameter-main__proxy_port:

      .. rst-class:: ansible-option-title

      **proxy_port**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--proxy_port" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The Port for the proxy server.

      This is required when \ :emphasis:`proxy\_support`\  is \ :literal:`ParametersProxy`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--proxy_server"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_firmware_role__parameter-main__proxy_server:

      .. rst-class:: ansible-option-title

      **proxy_server**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--proxy_server" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The IP address of the proxy server.

      This IP will not be validated. The download job will be created even for invalid \ :emphasis:`proxy\_server`\ . Please check the results of the job for error details.

      This is required when \ :emphasis:`proxy\_support`\  is \ :literal:`ParametersProxy`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--proxy_support"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_firmware_role__parameter-main__proxy_support:

      .. rst-class:: ansible-option-title

      **proxy_support**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--proxy_support" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Specifies if a proxy should be used.

      Proxy parameters are applicable on \ :literal:`HTTP`\ , \ :literal:`HTTPS`\ , and \ :literal:`FTP`\  share type of repositories.

      \ :literal:`ParametersProxy`\ , sets the proxy parameters for the current firmware operation.

      \ :literal:`DefaultProxy`\ , iDRAC uses the proxy values set by default.

      Default Proxy can be set in the Lifecycle Controller attributes using \ :ref:`dellemc.openmanage.idrac\_attributes <ansible_collections.dellemc.openmanage.idrac_attributes_module>`\ .

      \ :literal:`Off`\ , will not use the proxy.

      For iDRAC8 based servers, use proxy server with basic authentication.

      For iDRAC9 based servers, ensure that you use digest authentication for the proxy server, basic authentication is not supported.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"ParametersProxy"`
      - :ansible-option-choices-entry:`"DefaultProxy"`
      - :ansible-option-choices-entry-default:`"Off"` :ansible-option-choices-default-mark:`← (default)`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--proxy_type"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_firmware_role__parameter-main__proxy_type:

      .. rst-class:: ansible-option-title

      **proxy_type**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--proxy_type" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The proxy type of the proxy server.

      This is required when \ :emphasis:`proxy\_support`\  is \ :literal:`ParametersProxy`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"HTTP"`
      - :ansible-option-choices-entry:`"SOCKS"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--proxy_uname"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_firmware_role__parameter-main__proxy_uname:

      .. rst-class:: ansible-option-title

      **proxy_uname**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--proxy_uname" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The user name for the proxy server.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--reboot"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_firmware_role__parameter-main__reboot:

      .. rst-class:: ansible-option-title

      **reboot**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--reboot" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Provides the option to apply the update packages immediately or in the next reboot.

      If \ :emphasis:`reboot`\  is set to \ :literal:`true`\ ,  then the packages  are applied immediately.

      If \ :emphasis:`reboot`\  is set to \ :literal:`false`\ , then the packages are staged and applied in the next reboot.

      Packages that do not require a reboot are applied immediately irrespective of I (reboot).


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`false` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--share_name"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_firmware_role__parameter-main__share_name:

      .. rst-class:: ansible-option-title

      **share_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--share_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Network share path of update repository. CIFS, NFS, HTTP, HTTPS and FTP share types are supported.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--share_password"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_firmware_role__parameter-main__share_password:

      .. rst-class:: ansible-option-title

      **share_password**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--share_password" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Network share user password. This option is mandatory for CIFS Network Share.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--share_user"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_firmware_role__parameter-main__share_user:

      .. rst-class:: ansible-option-title

      **share_user**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--share_user" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Network share user in the format 'user@domain' or 'domain\\\\user' if user is part of a domain else 'user'. This option is mandatory for CIFS Network Share.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--username"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_firmware_role__parameter-main__username:

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

      iDRAC username with admin privileges.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--validate_certs"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_firmware_role__parameter-main__validate_certs:

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


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry-default:`true` :ansible-option-choices-default-mark:`← (default)`


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

