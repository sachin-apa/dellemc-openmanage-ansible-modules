
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

.. _ansible_collections.dellemc.openmanage.ome_firmware_catalog_module:

.. Anchors: short name for ansible.builtin

.. Anchors: aliases



.. Title

dellemc.openmanage.ome_firmware_catalog module -- Create, modify, or delete a firmware catalog on OpenManage Enterprise or OpenManage Enterprise Modular
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. Collection note

.. note::
    This module is part of the `dellemc.openmanage collection <https://galaxy.ansible.com/dellemc/openmanage>`_ (version 8.5.0).

    To install it, use: :code:`ansible-galaxy collection install dellemc.openmanage`.
    You need further requirements to be able to use this module,
    see :ref:`Requirements <ansible_collections.dellemc.openmanage.ome_firmware_catalog_module_requirements>` for details.

    To use it in a playbook, specify: :code:`dellemc.openmanage.ome_firmware_catalog`.

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

- This module allows to create, modify, or delete a firmware catalog on OpenManage Enterprise or OpenManage Enterprise Modular.


.. Aliases


.. Requirements

.. _ansible_collections.dellemc.openmanage.ome_firmware_catalog_module_requirements:

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

      .. _ansible_collections.dellemc.openmanage.ome_firmware_catalog_module__parameter-ca_path:

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
        <div class="ansibleOptionAnchor" id="parameter-catalog_description"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_catalog_module__parameter-catalog_description:

      .. rst-class:: ansible-option-title

      **catalog_description**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-catalog_description" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Description for the catalog.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-catalog_id"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_catalog_module__parameter-catalog_id:

      .. rst-class:: ansible-option-title

      **catalog_id**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-catalog_id" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=integer`

      :ansible-option-versionadded:`added in dellemc.openmanage 3.4.0`


      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      ID of the catalog.

      This option is mutually exclusive with \ :emphasis:`catalog\_name`\ .

      Provide the list of firmware catalog IDs that are supported when \ :emphasis:`state`\  is \ :literal:`absent`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-catalog_name"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_catalog_module__parameter-catalog_name:

      .. rst-class:: ansible-option-title

      **catalog_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-catalog_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Name of the firmware catalog to be created.

      This option is mutually exclusive with \ :emphasis:`catalog\_id`\ .

      Provide the list of firmware catalog names that are supported when \ :emphasis:`state`\  is \ :literal:`absent`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-check_certificate"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_catalog_module__parameter-check_certificate:

      .. rst-class:: ansible-option-title

      **check_certificate**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-check_certificate" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The certificate warnings are ignored when \ :emphasis:`repository\_type`\  is HTTPS. If \ :literal:`true`\ . If not, certificate warnings are not ignored.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`false` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-file_name"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_catalog_module__parameter-file_name:

      .. rst-class:: ansible-option-title

      **file_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-file_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Catalog file name associated with the \ :emphasis:`source\_path`\ .

      This option is ignored when \ :emphasis:`repository\_type`\  is \ :literal:`DELL\_ONLINE`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-hostname"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_catalog_module__parameter-hostname:

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
        <div class="ansibleOptionAnchor" id="parameter-job_wait"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_catalog_module__parameter-job_wait:

      .. rst-class:: ansible-option-title

      **job_wait**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-job_wait" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      :ansible-option-versionadded:`added in dellemc.openmanage 3.4.0`


      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Provides the option to wait for job completion.

      This option is applicable when \ :emphasis:`state`\  is \ :literal:`present`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry-default:`true` :ansible-option-choices-default-mark:`← (default)`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-job_wait_timeout"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_catalog_module__parameter-job_wait_timeout:

      .. rst-class:: ansible-option-title

      **job_wait_timeout**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-job_wait_timeout" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      :ansible-option-versionadded:`added in dellemc.openmanage 3.4.0`


      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The maximum wait time of \ :emphasis:`job\_wait`\  in seconds. The job is tracked only for this duration.

      This option is applicable when \ :emphasis:`job\_wait`\  is \ :literal:`true`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`600`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-new_catalog_name"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_catalog_module__parameter-new_catalog_name:

      .. rst-class:: ansible-option-title

      **new_catalog_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-new_catalog_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      :ansible-option-versionadded:`added in dellemc.openmanage 3.4.0`


      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      New name of the firmware catalog.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-password"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_catalog_module__parameter-password:

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

      .. _ansible_collections.dellemc.openmanage.ome_firmware_catalog_module__parameter-port:

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
        <div class="ansibleOptionAnchor" id="parameter-repository_domain"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_catalog_module__parameter-repository_domain:

      .. rst-class:: ansible-option-title

      **repository_domain**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-repository_domain" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Domain name of the repository.

      This option is ignored when \ :emphasis:`repository\_type`\  is \ :literal:`DELL\_ONLINE`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-repository_password"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_catalog_module__parameter-repository_password:

      .. rst-class:: ansible-option-title

      **repository_password**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-repository_password" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Password to access the repository.

      This option is mandatory when \ :emphasis:`repository\_type`\  is CIFS.

      This option is ignored when \ :emphasis:`repository\_type`\  is \ :literal:`DELL\_ONLINE`\ .

      \ :literal:`NOTE`\  The module always reports the changed status, when this is provided.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-repository_type"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_catalog_module__parameter-repository_type:

      .. rst-class:: ansible-option-title

      **repository_type**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-repository_type" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Type of repository. The supported types are NFS, CIFS, HTTP, HTTPS,and DELL\_ONLINE.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"NFS"`
      - :ansible-option-choices-entry:`"CIFS"`
      - :ansible-option-choices-entry:`"HTTP"`
      - :ansible-option-choices-entry:`"HTTPS"`
      - :ansible-option-choices-entry:`"DELL\_ONLINE"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-repository_username"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_catalog_module__parameter-repository_username:

      .. rst-class:: ansible-option-title

      **repository_username**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-repository_username" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      User name of the repository where the catalog is stored.

      This option is mandatory when \ :emphasis:`repository\_type`\  is CIFS.

      This option is ignored when \ :emphasis:`repository\_type`\  is \ :literal:`DELL\_ONLINE`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-source"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_catalog_module__parameter-source:

      .. rst-class:: ansible-option-title

      **source**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-source" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The IP address of the system where the firmware catalog is stored on the local network.

      By default, this option is set to downloads.dell.com when \ :emphasis:`repository\_type`\  is \ :literal:`DELL\_ONLINE`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-source_path"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_catalog_module__parameter-source_path:

      .. rst-class:: ansible-option-title

      **source_path**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-source_path" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Specify the complete path of the catalog file location without the file name.

      This is option ignored when \ :emphasis:`repository\_type`\  is \ :literal:`DELL\_ONLINE`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-state"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_catalog_module__parameter-state:

      .. rst-class:: ansible-option-title

      **state**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-state" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      :ansible-option-versionadded:`added in dellemc.openmanage 3.4.0`


      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      \ :literal:`present`\  creates or modifies a catalog.

      \ :literal:`absent`\  deletes an existing catalog.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`"present"` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`"absent"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-timeout"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_catalog_module__parameter-timeout:

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

      .. _ansible_collections.dellemc.openmanage.ome_firmware_catalog_module__parameter-username:

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

      .. _ansible_collections.dellemc.openmanage.ome_firmware_catalog_module__parameter-validate_certs:

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
   - If \ :emphasis:`repository\_password`\  is provided, then the module always reports the changed status.
   - Run this module from a system that has direct access to Dell OpenManage Enterprise or OpenManage Enterprise Modular.
   - This module supports IPv4 and IPv6 addresses.
   - This module supports \ :literal:`check\_mode`\ .

.. Seealso


.. Examples

Examples
--------

.. code-block:: yaml+jinja

    
    ---
    - name: Create a catalog from HTTPS repository
      dellemc.openmanage.ome_firmware_catalog:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        catalog_name: "catalog_name"
        catalog_description: "catalog_description"
        repository_type: "HTTPS"
        source: "downloads.dell.com"
        source_path: "catalog"
        file_name: "catalog.gz"
        check_certificate: true

    - name: Create a catalog from HTTP repository
      dellemc.openmanage.ome_firmware_catalog:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        catalog_name: "catalog_name"
        catalog_description: "catalog_description"
        repository_type: "HTTP"
        source: "downloads.dell.com"
        source_path: "catalog"
        file_name: "catalog.gz"

    - name: Create a catalog using CIFS share
      dellemc.openmanage.ome_firmware_catalog:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        catalog_name: "catalog_name"
        catalog_description: "catalog_description"
        repository_type: "CIFS"
        source: "192.167.0.1"
        source_path: "cifs/R940"
        file_name: "catalog.gz"
        repository_username: "repository_username"
        repository_password: "repository_password"
        repository_domain: "repository_domain"

    - name: Create a catalog using NFS share
      dellemc.openmanage.ome_firmware_catalog:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        catalog_name: "catalog_name"
        catalog_description: "catalog_description"
        repository_type: "NFS"
        source: "192.166.0.2"
        source_path: "/nfs/R940"
        file_name: "catalog.xml"

    - name: Create a catalog using repository from Dell.com
      dellemc.openmanage.ome_firmware_catalog:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        catalog_name: "catalog_name"
        catalog_description: "catalog_description"
        repository_type: "DELL_ONLINE"
        check_certificate: true

    - name: Modify a catalog using a repository from CIFS share
      dellemc.openmanage.ome_firmware_catalog:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        catalog_name: "catalog_name"
        catalog_description: "new catalog_description"
        repository_type: "CIFS"
        source: "192.167.0.2"
        source_path: "cifs/R941"
        file_name: "catalog1.gz"
        repository_username: "repository_username"
        repository_password: "repository_password"
        repository_domain: "repository_domain"

    - name: Modify a catalog using a repository from Dell.com
      dellemc.openmanage.ome_firmware_catalog:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        catalog_id: 10
        new_catalog_name: "new_catalog_name"
        repository_type: "DELL_ONLINE"
        catalog_description: "catalog_description"

    - name: Delete catalog using catalog name
      dellemc.openmanage.ome_firmware_catalog:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        state: absent
        catalog_name: ["catalog_name1", "catalog_name2"]

    - name: Delete catalog using catalog id
      dellemc.openmanage.ome_firmware_catalog:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        state: absent
        catalog_id: [11, 34]




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
        <div class="ansibleOptionAnchor" id="return-associated_baselines"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_catalog_module__return-associated_baselines:

      .. rst-class:: ansible-option-title

      **associated_baselines**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-associated_baselines" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      IDs of the baselines associated with catalog.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` When \ :emphasis:`state`\  is \ :literal:`absent`\ 

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`[{"BaselineId": 24, "BaselineName": "new"}, {"BaselineId": 25, "BaselineName": "c7"}, {"BaselineId": 27, "BaselineName": "c4"}]`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-catalog_id"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_catalog_module__return-catalog_id:

      .. rst-class:: ansible-option-title

      **catalog_id**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-catalog_id" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      IDs of the deleted catalog.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` When \ :emphasis:`state`\  is \ :literal:`absent`\ 

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`10123`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-catalog_status"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_catalog_module__return-catalog_status:

      .. rst-class:: ansible-option-title

      **catalog_status**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-catalog_status" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Details of the catalog operation.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` When \ :emphasis:`state`\  is \ :literal:`present`\ 

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"AssociatedBaselines": [], "BaseLocation": null, "BundlesCount": 0, "Filename": "catalog.gz", "Id": 12, "LastUpdated": null, "ManifestIdentifier": null, "ManifestVersion": null, "NextUpdate": null, "PredecessorIdentifier": null, "ReleaseDate": null, "ReleaseIdentifier": null, "Repository": {"CheckCertificate": true, "Description": "HTTPS Desc", "DomainName": null, "Id": null, "Name": "catalog4", "Password": null, "RepositoryType": "HTTPS", "Source": "company.com", "Username": null}, "Schedule": null, "SourcePath": "catalog", "Status": null, "TaskId": 10094}`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-error_info"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_catalog_module__return-error_info:

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

      Details of the http error.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` on http error

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"error": {"@Message.ExtendedInfo": [{"Message": "Unable to create or update the catalog because a repository with the same name already exists.", "Resolution": "Enter a different name and retry the operation.", "Severity": "Critical"}], "code": "Base.1.0.GeneralError", "message": "A general error has occurred. See ExtendedInfo for more information."}}`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-job_id"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_catalog_module__return-job_id:

      .. rst-class:: ansible-option-title

      **job_id**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-job_id" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Job ID of the catalog task.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` When catalog job is in a running state

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`10123`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-msg"></div>

      .. _ansible_collections.dellemc.openmanage.ome_firmware_catalog_module__return-msg:

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

      Overall status of the firmware catalog operation.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` always

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`"Successfully triggered the job to create a catalog with Task ID : 10094"`


      .. raw:: html

        </div>



..  Status (Presently only deprecated)


.. Authors

Authors
~~~~~~~

- Sajna Shetty(@Sajna-Shetty)
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

