
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

.. _ansible_collections.dellemc.openmanage.ome_template_module:

.. Anchors: short name for ansible.builtin

.. Anchors: aliases



.. Title

dellemc.openmanage.ome_template module -- Create, modify, deploy, delete, export, import and clone a template on OpenManage Enterprise
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. Collection note

.. note::
    This module is part of the `dellemc.openmanage collection <https://galaxy.ansible.com/dellemc/openmanage>`_ (version 8.5.0).

    To install it, use: :code:`ansible-galaxy collection install dellemc.openmanage`.
    You need further requirements to be able to use this module,
    see :ref:`Requirements <ansible_collections.dellemc.openmanage.ome_template_module_requirements>` for details.

    To use it in a playbook, specify: :code:`dellemc.openmanage.ome_template`.

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

- This module creates, modifies, deploys, deletes, exports, imports and clones a template on OpenManage Enterprise.


.. Aliases


.. Requirements

.. _ansible_collections.dellemc.openmanage.ome_template_module_requirements:

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
        <div class="ansibleOptionAnchor" id="parameter-attributes"></div>

      .. _ansible_collections.dellemc.openmanage.ome_template_module__parameter-attributes:

      .. rst-class:: ansible-option-title

      **attributes**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-attributes" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Payload data for the template operations. All the variables in this option are added as payload for \ :literal:`create`\ , \ :literal:`modify`\ , \ :literal:`deploy`\ , \ :literal:`import`\ , and \ :literal:`clone`\  operations. It takes the following attributes.

      Attributes: List of dictionaries of attributes (if any) to be modified in the deployment template. This is applicable when \ :emphasis:`command`\  is \ :literal:`deploy`\  and \ :literal:`modify`\ . Use the \ :emphasis:`Id`\  If the attribute Id is available. If not, use the comma separated I (DisplayName). For more details about using the \ :emphasis:`DisplayName`\ , see the example provided.

      Name: Name of the template. This is mandatory when \ :emphasis:`command`\  is \ :literal:`create`\ , \ :literal:`import`\ , \ :literal:`clone`\ , and optional when \ :emphasis:`command`\  is \ :literal:`modify`\ .

      Description: Description for the template. This is applicable when \ :emphasis:`command`\  is \ :literal:`create`\  or \ :literal:`modify`\ .

      Fqdds: This allows to create a template using components from a specified reference server. One or more, of the following values must be specified in a comma-separated string: iDRAC, System, BIOS, NIC, LifeCycleController, RAID, and EventFilters. If none of the values are specified, the default value 'All' is selected. This is applicable when I (command) is \ :literal:`create`\ .

      Options: Options to control device shutdown or end power state post template deployment. This is applicable for \ :literal:`deploy`\  operation.

      Schedule: Provides options to schedule the deployment task immediately, or at a specified time. This is applicable when \ :emphasis:`command`\  is \ :literal:`deploy`\ .

      NetworkBootIsoModel: Payload to specify the ISO deployment details. This is applicable when \ :emphasis:`command`\  is \ :literal:`deploy`\ .

      Content: The XML content of template. This is applicable when \ :emphasis:`command`\  is \ :literal:`import`\ .

      Type: Template type ID, indicating the type of device for which configuration is supported, such as chassis and servers. This is applicable when \ :emphasis:`command`\  is \ :literal:`import`\ .

      TypeId: Template type ID, indicating the type of device for which configuration is supported, such as chassis and servers. This is applicable when \ :emphasis:`command`\  is \ :literal:`create`\ .

      Refer OpenManage Enterprise API Reference Guide for more details.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-ca_path"></div>

      .. _ansible_collections.dellemc.openmanage.ome_template_module__parameter-ca_path:

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
        <div class="ansibleOptionAnchor" id="parameter-command"></div>
        <div class="ansibleOptionAnchor" id="parameter-state"></div>

      .. _ansible_collections.dellemc.openmanage.ome_template_module__parameter-command:
      .. _ansible_collections.dellemc.openmanage.ome_template_module__parameter-state:

      .. rst-class:: ansible-option-title

      **command**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-command" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-aliases:`aliases: state`

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      \ :literal:`create`\  creates a new template.

      \ :literal:`modify`\  modifies an existing template.

      \ :literal:`deploy`\  creates a template-deployment job.

      \ :literal:`delete`\  deletes an existing template.

      \ :literal:`export`\  exports an existing template.

      \ :literal:`import`\  creates a template from a specified configuration text in SCP XML format.

      \ :literal:`clone`\  creates a clone of a existing template.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`"create"` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`"modify"`
      - :ansible-option-choices-entry:`"deploy"`
      - :ansible-option-choices-entry:`"delete"`
      - :ansible-option-choices-entry:`"export"`
      - :ansible-option-choices-entry:`"import"`
      - :ansible-option-choices-entry:`"clone"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-device_group_names"></div>

      .. _ansible_collections.dellemc.openmanage.ome_template_module__parameter-device_group_names:

      .. rst-class:: ansible-option-title

      **device_group_names**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-device_group_names" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Specify the list of groups when I (command) is \ :literal:`deploy`\ .

      Provide at least one of the mandatory options \ :emphasis:`device\_id`\ , \ :emphasis:`device\_service\_tag`\ , or \ :emphasis:`device\_group\_names`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`[]`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-device_id"></div>

      .. _ansible_collections.dellemc.openmanage.ome_template_module__parameter-device_id:

      .. rst-class:: ansible-option-title

      **device_id**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-device_id" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Specify the list of targeted device ID(s) when \ :emphasis:`command`\  is \ :literal:`deploy`\ . When I (command) is \ :literal:`create`\ , specify the ID of a single device.

      Either \ :emphasis:`device\_id`\  or \ :emphasis:`device\_service\_tag`\  is mandatory or both can be applicable.


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`[]`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-device_service_tag"></div>

      .. _ansible_collections.dellemc.openmanage.ome_template_module__parameter-device_service_tag:

      .. rst-class:: ansible-option-title

      **device_service_tag**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-device_service_tag" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Specify the list of targeted device service tags when I (command) is \ :literal:`deploy`\ . When \ :emphasis:`command`\  is \ :literal:`create`\ , specify the service tag of a single device.

      Either \ :emphasis:`device\_id`\  or \ :emphasis:`device\_service\_tag`\  is mandatory or both can be applicable.


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`[]`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-hostname"></div>

      .. _ansible_collections.dellemc.openmanage.ome_template_module__parameter-hostname:

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

      .. _ansible_collections.dellemc.openmanage.ome_template_module__parameter-job_wait:

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

      This option is applicable when \ :emphasis:`command`\  is \ :literal:`create`\ , or \ :literal:`deploy`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry-default:`true` :ansible-option-choices-default-mark:`← (default)`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-job_wait_timeout"></div>

      .. _ansible_collections.dellemc.openmanage.ome_template_module__parameter-job_wait_timeout:

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
        <div class="ansibleOptionAnchor" id="parameter-password"></div>

      .. _ansible_collections.dellemc.openmanage.ome_template_module__parameter-password:

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

      .. _ansible_collections.dellemc.openmanage.ome_template_module__parameter-port:

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
        <div class="ansibleOptionAnchor" id="parameter-template_id"></div>

      .. _ansible_collections.dellemc.openmanage.ome_template_module__parameter-template_id:

      .. rst-class:: ansible-option-title

      **template_id**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-template_id" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      ID of the existing template.

      This option is applicable when \ :emphasis:`command`\  is \ :literal:`modify`\ , \ :literal:`deploy`\ , \ :literal:`delete`\ , \ :literal:`clone`\  and \ :literal:`export`\ .

      This option is mutually exclusive with \ :emphasis:`template\_name`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-template_name"></div>

      .. _ansible_collections.dellemc.openmanage.ome_template_module__parameter-template_name:

      .. rst-class:: ansible-option-title

      **template_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-template_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Name of the existing template.

      This option is applicable when \ :emphasis:`command`\  is \ :literal:`modify`\ , \ :literal:`deploy`\ , \ :literal:`delete`\ , \ :literal:`clone`\  and \ :literal:`export`\ .

      This option is mutually exclusive with \ :emphasis:`template\_id`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-template_view_type"></div>

      .. _ansible_collections.dellemc.openmanage.ome_template_module__parameter-template_view_type:

      .. rst-class:: ansible-option-title

      **template_view_type**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-template_view_type" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Select the type of view of the OME template.

      This is applicable when \ :emphasis:`command`\  is \ :literal:`create`\ ,\ :literal:`clone`\  and \ :literal:`import`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`"Deployment"` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`"Compliance"`
      - :ansible-option-choices-entry:`"Inventory"`
      - :ansible-option-choices-entry:`"Sample"`
      - :ansible-option-choices-entry:`"None"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-timeout"></div>

      .. _ansible_collections.dellemc.openmanage.ome_template_module__parameter-timeout:

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

      .. _ansible_collections.dellemc.openmanage.ome_template_module__parameter-username:

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

      .. _ansible_collections.dellemc.openmanage.ome_template_module__parameter-validate_certs:

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
    - name: Create a template from a reference device
      dellemc.openmanage.ome_template:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        device_id: 25123
        attributes:
          Name: "New Template"
          Description: "New Template description"

    - name: Modify template name, description, and attribute value
      dellemc.openmanage.ome_template:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        command: "modify"
        template_id: 12
        attributes:
          Name: "New Custom Template"
          Description: "Custom Template Description"
          # Attributes to be modified in the template.
          # For information on any attribute id, use API /TemplateService/Templates(Id)/Views(Id)/AttributeViewDetails
          # This section is optional
          Attributes:
            - Id: 1234
              Value: "Test Attribute"
              IsIgnored: false

    - name: Modify template name, description, and attribute using detailed view
      dellemc.openmanage.ome_template:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        command: "modify"
        template_id: 12
        attributes:
          Name: "New Custom Template"
          Description: "Custom Template Description"
          Attributes:
            # Enter the comma separated string as appearing in the Detailed view on GUI
            # NIC -> NIC.Integrated.1-1-1 -> NIC Configuration -> Wake On LAN1
            - DisplayName: 'NIC, NIC.Integrated.1-1-1, NIC Configuration, Wake On LAN'
              Value: Enabled
              IsIgnored: false
            # System -> LCD Configuration -> LCD 1 User Defined String for LCD
            - DisplayName: 'System, LCD Configuration, LCD 1 User Defined String for LCD'
              Value: LCD str by OMAM
              IsIgnored: false

    - name: Deploy template on multiple devices
      dellemc.openmanage.ome_template:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        command: "deploy"
        template_id: 12
        device_id:
          - 12765
          - 10173
        device_service_tag:
          - 'SVTG123'
          - 'SVTG456'

    - name: Deploy template on groups
      dellemc.openmanage.ome_template:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        command: "deploy"
        template_id: 12
        device_group_names:
          - server_group_1
          - server_group_2

    - name: Deploy template on multiple devices along with the attributes values to be modified on the target devices
      dellemc.openmanage.ome_template:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        command: "deploy"
        template_id: 12
        device_id:
          - 12765
          - 10173
        device_service_tag:
          - 'SVTG123'
        attributes:
          # Device specific attributes to be modified during deployment.
          # For information on any attribute id, use API /TemplateService/Templates(Id)/Views(Id)/AttributeViewDetails
          # This section is optional
          Attributes:
            # specific device where attribute to be modified at deployment run-time.
            # The DeviceId should be mentioned above in the 'device_id' section.
            # Service tags not allowed.
            - DeviceId: 12765
              Attributes:
                - Id: 15645
                  Value: "0.0.0.0"
                  IsIgnored: false
            - DeviceId: 10173
              Attributes:
                - Id: 18968,
                  Value: "hostname-1"
                  IsIgnored: false

    - name: Deploy template and Operating System (OS) on multiple devices
      dellemc.openmanage.ome_template:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        command: "deploy"
        template_id: 12
        device_id:
          - 12765
        device_service_tag:
          - 'SVTG123'
        attributes:
          # Include this to install OS on the devices.
          # This section is optional
          NetworkBootIsoModel:
            BootToNetwork: true
            ShareType: "NFS"
            IsoTimeout: 1 # allowable values(1,2,4,8,16) in hours
            IsoPath: "/home/iso_path/filename.iso"
            ShareDetail:
              IpAddress: "192.168.0.2"
              ShareName: "sharename"
              User: "share_user"
              Password: "share_password"
          Options:
            EndHostPowerState: 1
            ShutdownType: 0
            TimeToWaitBeforeShutdown: 300
          Schedule:
            RunLater: true
            RunNow: false

    - name: "Deploy template on multiple devices and changes the device-level attributes. After the template is deployed,
    install OS using its image"
      dellemc.openmanage.ome_template:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        command: "deploy"
        template_id: 12
        device_id:
          - 12765
          - 10173
        device_service_tag:
          - 'SVTG123'
          - 'SVTG456'
        attributes:
          Attributes:
            - DeviceId: 12765
              Attributes:
                - Id: 15645
                  Value: "0.0.0.0"
                  IsIgnored: false
            - DeviceId: 10173
              Attributes:
                - Id: 18968,
                  Value: "hostname-1"
                  IsIgnored: false
          NetworkBootIsoModel:
            BootToNetwork: true
            ShareType: "NFS"
            IsoTimeout: 1 # allowable values(1,2,4,8,16) in hours
            IsoPath: "/home/iso_path/filename.iso"
            ShareDetail:
              IpAddress: "192.168.0.2"
              ShareName: "sharename"
              User: "share_user"
              Password: "share_password"
          Options:
            EndHostPowerState: 1
            ShutdownType: 0
            TimeToWaitBeforeShutdown: 300
          Schedule:
            RunLater: true
            RunNow: false

    - name: Delete template
      dellemc.openmanage.ome_template:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        command: "delete"
        template_id: 12

    - name: Export a template
      dellemc.openmanage.ome_template:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        command: "export"
        template_id: 12

    # Start of example to export template to a local xml file
    - name: Export template to a local xml file
      dellemc.openmanage.ome_template:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        command: "export"
        template_name: "my_template"
      register: result
    - name: Save template into a file
      ansible.builtin.copy:
        content: "{{ result.Content}}"
        dest: "/path/to/exported_template.xml"
    # End of example to export template to a local xml file

    - name: Clone a template
      dellemc.openmanage.ome_template:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        command: "clone"
        template_id: 12
        attributes:
          Name: "New Cloned Template Name"

    - name: Import template from XML content
      dellemc.openmanage.ome_template:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        command: "import"
        attributes:
          Name: "Imported Template Name"
          # Template Type from TemplateService/TemplateTypes
          Type: 2
          # xml string content
          Content: "<SystemConfiguration Model=\"PowerEdge R940\" ServiceTag=\"SVCTAG1\"
          TimeStamp=\"Tue Sep 24 09:20:57.872551 2019\">\n<Component FQDD=\"AHCI.Slot.6-1\">\n<Attribute
          Name=\"RAIDresetConfig\">True</Attribute>\n<Attribute Name=\"RAIDforeignConfig\">Clear</Attribute>\n
          </Component>\n<Component FQDD=\"Disk.Direct.0-0:AHCI.Slot.6-1\">\n<Attribute Name=\"RAIDPDState\">Ready
          </Attribute>\n<Attribute Name=\"RAIDHotSpareStatus\">No</Attribute>\n</Component>\n
          <Component FQDD=\"Disk.Direct.1-1:AHCI.Slot.6-1\">\n<Attribute Name=\"RAIDPDState\">Ready</Attribute>\n
          <Attribute Name=\"RAIDHotSpareStatus\">No</Attribute>\n</Component>\n</SystemConfiguration>\n"

    - name: Import template from local XML file
      dellemc.openmanage.ome_template:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        command: "import"
        attributes:
          Name: "Imported Template Name"
          Type: 2
          Content: "{{ lookup('ansible.builtin.file', '/path/to/xmlfile') }}"

    - name: "Deploy template and Operating System (OS) on multiple devices."
      dellemc.openmanage.ome_template:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        command: "deploy"
        template_id: 12
        device_id:
          - 12765
        device_service_tag:
          - 'SVTG123'
        attributes:
          # Include this to install OS on the devices.
          # This section is optional
          NetworkBootIsoModel:
            BootToNetwork: true
            ShareType: "CIFS"
            IsoTimeout: 1 # allowable values(1,2,4,8,16) in hours
            IsoPath: "/home/iso_path/filename.iso"
            ShareDetail:
              IpAddress: "192.168.0.2"
              ShareName: "sharename"
              User: "share_user"
              Password: "share_password"
          Options:
            EndHostPowerState: 1
            ShutdownType: 0
            TimeToWaitBeforeShutdown: 300
          Schedule:
            RunLater: true
            RunNow: false

    - name: Create a compliance template from reference device
      dellemc.openmanage.ome_template:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        command: "create"
        device_service_tag:
          - "SVTG123"
        template_view_type: "Compliance"
        attributes:
          Name: "Configuration Compliance"
          Description: "Configuration Compliance Template"
          Fqdds: "BIOS"

    - name: Import a compliance template from XML file
      dellemc.openmanage.ome_template:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        command: "import"
        template_view_type: "Compliance"
        attributes:
          Name: "Configuration Compliance"
          Content: "{{ lookup('ansible.builtin.file', './test.xml') }}"
          Type: 2

    - name: Create a template from a reference device with Job wait as false
      dellemc.openmanage.ome_template:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        device_id: 25123
        attributes:
          Name: "New Template"
          Description: "New Template description"
          Fqdds: iDRAC,BIOS,
        job_wait: false




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
        <div class="ansibleOptionAnchor" id="return-Content"></div>

      .. _ansible_collections.dellemc.openmanage.ome_template_module__return-content:

      .. rst-class:: ansible-option-title

      **Content**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-Content" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      XML content of the exported template. This content can be written to a xml file.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` success, when \ :emphasis:`command`\  is \ :literal:`export`\ 

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`"\<SystemConfiguration Model=\\"PowerEdge R940\\" ServiceTag=\\"DEFG123\\" TimeStamp=\\"Tue Sep 24 09:20:57.872551 2019\\"\>\\n\<Component FQDD=\\"AHCI.Slot.6-1\\"\>\\n\<Attribute Name=\\"RAIDresetConfig\\"\>True\</Attribute\>\\n\<Attribute Name=\\"RAIDforeignConfig\\"\>Clear\</Attribute\>\\n\</Component\>\\n\<Component FQDD=\\"Disk.Direct.0-0:AHCI.Slot.6-1\\"\> \\n\<Attribute Name=\\"RAIDPDState\\"\>Ready\</Attribute\>\\n\<Attribute Name=\\"RAIDHotSpareStatus\\"\>No\</Attribute\> \\n\</Component\>\\n\<Component FQDD=\\"Disk.Direct.1-1:AHCI.Slot.6-1\\"\>\\n\<Attribute Name=\\"RAIDPDState\\"\>Ready \</Attribute\>\\n\<Attribute Name=\\"RAIDHotSpareStatus\\"\>No\</Attribute\>\\n\</Component\>\\n\</SystemConfiguration\>"`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-devices_assigned"></div>

      .. _ansible_collections.dellemc.openmanage.ome_template_module__return-devices_assigned:

      .. rst-class:: ansible-option-title

      **devices_assigned**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-devices_assigned" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Mapping of devices with the templates already deployed on them.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` \ :emphasis:`command`\  is \ :literal:`deploy`\ 

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"10312": 23, "10362": 28}`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-error_info"></div>

      .. _ansible_collections.dellemc.openmanage.ome_template_module__return-error_info:

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

      .. _ansible_collections.dellemc.openmanage.ome_template_module__return-msg:

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

      Overall status of the template operation.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` always

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`"Successfully created a template with ID 23"`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-return_id"></div>

      .. _ansible_collections.dellemc.openmanage.ome_template_module__return-return_id:

      .. rst-class:: ansible-option-title

      **return_id**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-return_id" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      ID of the template for \ :literal:`create`\ , \ :literal:`modify`\ , \ :literal:`import`\  and \ :literal:`clone`\  or task created in case of \ :literal:`deploy`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` success, when \ :emphasis:`command`\  is \ :literal:`create`\ , \ :literal:`modify`\ , \ :literal:`import`\ , \ :literal:`clone`\  and \ :literal:`deploy`\ 

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`12`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-TemplateId"></div>

      .. _ansible_collections.dellemc.openmanage.ome_template_module__return-templateid:

      .. rst-class:: ansible-option-title

      **TemplateId**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-TemplateId" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      ID of the template for \ :literal:`export`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` success, when \ :emphasis:`command`\  is \ :literal:`export`\ 

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`13`


      .. raw:: html

        </div>



..  Status (Presently only deprecated)


.. Authors

Authors
~~~~~~~

- Jagadeesh N V (@jagadeeshnv)
- Husniya Hameed (@husniya_hameed)
- Kritika Bhateja (@Kritika-Bhateja)



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

