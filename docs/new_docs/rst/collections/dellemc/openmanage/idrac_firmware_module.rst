
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

.. _ansible_collections.dellemc.openmanage.idrac_firmware_module:

.. Anchors: short name for ansible.builtin

.. Anchors: aliases



.. Title

dellemc.openmanage.idrac_firmware module -- Firmware update from a repository on a network share (CIFS, NFS, HTTP, HTTPS, FTP)
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. Collection note

.. note::
    This module is part of the `dellemc.openmanage collection <https://galaxy.ansible.com/dellemc/openmanage>`_ (version 8.5.0).

    To install it, use: :code:`ansible-galaxy collection install dellemc.openmanage`.
    You need further requirements to be able to use this module,
    see :ref:`Requirements <ansible_collections.dellemc.openmanage.idrac_firmware_module_requirements>` for details.

    To use it in a playbook, specify: :code:`dellemc.openmanage.idrac_firmware`.

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

- Update the Firmware by connecting to a network share (CIFS, NFS, HTTP, HTTPS, FTP) that contains a catalog of available updates.
- Network share should contain a valid repository of Update Packages (DUPs) and a catalog file describing the DUPs.
- All applicable updates contained in the repository are applied to the system.
- This feature is available only with iDRAC Enterprise License.


.. Aliases


.. Requirements

.. _ansible_collections.dellemc.openmanage.idrac_firmware_module_requirements:

Requirements
------------
The below requirements are needed on the host that executes this module.

- omsdk \>= 1.2.503
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
        <div class="ansibleOptionAnchor" id="parameter-apply_update"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_firmware_module__parameter-apply_update:

      .. rst-class:: ansible-option-title

      **apply_update**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-apply_update" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-ca_path"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_firmware_module__parameter-ca_path:

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
        <div class="ansibleOptionAnchor" id="parameter-catalog_file_name"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_firmware_module__parameter-catalog_file_name:

      .. rst-class:: ansible-option-title

      **catalog_file_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-catalog_file_name" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-idrac_ip"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_firmware_module__parameter-idrac_ip:

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

      .. _ansible_collections.dellemc.openmanage.idrac_firmware_module__parameter-idrac_password:
      .. _ansible_collections.dellemc.openmanage.idrac_firmware_module__parameter-idrac_pwd:

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

      .. _ansible_collections.dellemc.openmanage.idrac_firmware_module__parameter-idrac_port:

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

      .. _ansible_collections.dellemc.openmanage.idrac_firmware_module__parameter-idrac_user:

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
        <div class="ansibleOptionAnchor" id="parameter-ignore_cert_warning"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_firmware_module__parameter-ignore_cert_warning:

      .. rst-class:: ansible-option-title

      **ignore_cert_warning**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-ignore_cert_warning" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-job_wait"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_firmware_module__parameter-job_wait:

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

      Whether to wait for job completion or not.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry-default:`true` :ansible-option-choices-default-mark:`← (default)`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-proxy_passwd"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_firmware_module__parameter-proxy_passwd:

      .. rst-class:: ansible-option-title

      **proxy_passwd**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-proxy_passwd" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-proxy_port"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_firmware_module__parameter-proxy_port:

      .. rst-class:: ansible-option-title

      **proxy_port**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-proxy_port" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-proxy_server"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_firmware_module__parameter-proxy_server:

      .. rst-class:: ansible-option-title

      **proxy_server**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-proxy_server" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-proxy_support"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_firmware_module__parameter-proxy_support:

      .. rst-class:: ansible-option-title

      **proxy_support**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-proxy_support" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-proxy_type"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_firmware_module__parameter-proxy_type:

      .. rst-class:: ansible-option-title

      **proxy_type**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-proxy_type" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The proxy type of the proxy server.

      This is required when \ :emphasis:`proxy\_support`\  is \ :literal:`ParametersProxy`\ .

      Note: SOCKS4 proxy does not support IPv6 address.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"HTTP"`
      - :ansible-option-choices-entry:`"SOCKS"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-proxy_uname"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_firmware_module__parameter-proxy_uname:

      .. rst-class:: ansible-option-title

      **proxy_uname**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-proxy_uname" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-reboot"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_firmware_module__parameter-reboot:

      .. rst-class:: ansible-option-title

      **reboot**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-reboot" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-share_mnt"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_firmware_module__parameter-share_mnt:

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

      Local mount path of the network share with read-write permission for ansible user.

      This option is not applicable for HTTP, HTTPS, and FTP shares.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-share_name"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_firmware_module__parameter-share_name:

      .. rst-class:: ansible-option-title

      **share_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-share_name" title="Permalink to this option"></a>

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
        <div class="ansibleOptionAnchor" id="parameter-share_password"></div>
        <div class="ansibleOptionAnchor" id="parameter-share_pwd"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_firmware_module__parameter-share_password:
      .. _ansible_collections.dellemc.openmanage.idrac_firmware_module__parameter-share_pwd:

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

      Network share user password. This option is mandatory for CIFS Network Share.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-share_user"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_firmware_module__parameter-share_user:

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

      Network share user in the format 'user@domain' or 'domain\\\\user' if user is part of a domain else 'user'. This option is mandatory for CIFS Network Share.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-timeout"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_firmware_module__parameter-timeout:

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

      .. _ansible_collections.dellemc.openmanage.idrac_firmware_module__parameter-validate_certs:

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
   - Module will report success based on the iDRAC firmware update parent job status if there are no individual component jobs present.
   - For server with iDRAC firmware 5.00.00.00 and later, if the repository contains unsupported packages, then the module will return success with a proper message.
   - This module supports both IPv4 and IPv6 address for \ :emphasis:`idrac\_ip`\  and \ :emphasis:`share\_name`\ .
   - This module supports \ :literal:`check\_mode`\ .

.. Seealso


.. Examples

Examples
--------

.. code-block:: yaml+jinja

    
    ---
    - name: Update firmware from repository on a NFS Share
      dellemc.openmanage.idrac_firmware:
           idrac_ip: "192.168.0.1"
           idrac_user: "user_name"
           idrac_password: "user_password"
           ca_path: "/path/to/ca_cert.pem"
           share_name: "192.168.0.0:/share"
           reboot: true
           job_wait: true
           apply_update: true
           catalog_file_name: "Catalog.xml"

    - name: Update firmware from repository on a CIFS Share
      dellemc.openmanage.idrac_firmware:
           idrac_ip: "192.168.0.1"
           idrac_user: "user_name"
           idrac_password: "user_password"
           ca_path: "/path/to/ca_cert.pem"
           share_name: "full_cifs_path"
           share_user: "share_user"
           share_password: "share_password"
           reboot: true
           job_wait: true
           apply_update: true
           catalog_file_name: "Catalog.xml"

    - name: Update firmware from repository on a HTTP
      dellemc.openmanage.idrac_firmware:
           idrac_ip: "192.168.0.1"
           idrac_user: "user_name"
           idrac_password: "user_password"
           ca_path: "/path/to/ca_cert.pem"
           share_name: "http://downloads.dell.com"
           reboot: true
           job_wait: true
           apply_update: true

    - name: Update firmware from repository on a HTTPS
      dellemc.openmanage.idrac_firmware:
           idrac_ip: "192.168.0.1"
           idrac_user: "user_name"
           idrac_password: "user_password"
           ca_path: "/path/to/ca_cert.pem"
           share_name: "https://downloads.dell.com"
           reboot: true
           job_wait: true
           apply_update: true

    - name: Update firmware from repository on a HTTPS via proxy
      dellemc.openmanage.idrac_firmware:
           idrac_ip: "192.168.0.1"
           idrac_user: "user_name"
           idrac_password: "user_password"
           ca_path: "/path/to/ca_cert.pem"
           share_name: "https://downloads.dell.com"
           reboot: true
           job_wait: true
           apply_update: true
           proxy_support: ParametersProxy
           proxy_server: 192.168.1.10
           proxy_type: HTTP
           proxy_port: 80
           proxy_uname: "proxy_user"
           proxy_passwd: "proxy_pwd"

    - name: Update firmware from repository on a FTP
      dellemc.openmanage.idrac_firmware:
           idrac_ip: "192.168.0.1"
           idrac_user: "user_name"
           idrac_password: "user_password"
           ca_path: "/path/to/ca_cert.pem"
           share_name: "ftp://ftp.mydomain.com"
           reboot: true
           job_wait: true
           apply_update: true




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
        <div class="ansibleOptionAnchor" id="return-msg"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_firmware_module__return-msg:

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

      Overall firmware update status.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` always

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`"Successfully updated the firmware."`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-update_status"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_firmware_module__return-update_status:

      .. rst-class:: ansible-option-title

      **update_status**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-update_status" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Firmware Update job and progress details from the iDRAC.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` success

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"InstanceID": "JID\_XXXXXXXXXXXX", "JobStartTime": "NA", "JobState": "Completed", "Message": "Job completed successfully.", "MessageId": "REDXXX", "Name": "Repository Update", "Status": "Success"}`


      .. raw:: html

        </div>



..  Status (Presently only deprecated)


.. Authors

Authors
~~~~~~~

- Rajeev Arakkal (@rajeevarakkal)
- Felix Stephen (@felixs88)
- Jagadeesh N V (@jagadeeshnv)



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

