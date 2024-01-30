
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

.. _ansible_collections.dellemc.openmanage.idrac_os_deployment_role:

.. Anchors: aliases


.. Title

dellemc.openmanage.idrac_os_deployment role -- Role to deploy operating system on the iDRAC servers
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. Collection note

.. note::
    This role is part of the `dellemc.openmanage collection <https://galaxy.ansible.com/dellemc/openmanage>`_ (version 8.5.0).

    To install it use: :code:`ansible-galaxy collection install dellemc.openmanage`.

    To use it in a playbook, specify: :code:`dellemc.openmanage.idrac_os_deployment`.

.. contents::
   :local:
   :depth: 2


.. Entry point title

Entry point ``main`` -- Role to deploy operating system on the iDRAC servers
----------------------------------------------------------------------------

.. version_added

.. rst-class:: ansible-version-added

New in dellemc.openmanage 7.5.0

.. Deprecated


Synopsis
^^^^^^^^

.. Description

- Role to generate the custom iso using the kickstart configuration file and deploy operating system on the idrac servers.

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

      .. _ansible_collections.dellemc.openmanage.idrac_os_deployment_role__parameter-main__ca_path:

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
        <div class="ansibleOptionAnchor" id="parameter-main--delete_custom_iso"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_os_deployment_role__parameter-main__delete_custom_iso:

      .. rst-class:: ansible-option-title

      **delete_custom_iso**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--delete_custom_iso" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Deletes the Custom iso after the OS deployment is finshed.

      ISO will be delete if \ :emphasis:`delete\_custom\_iso`\  is \ :literal:`true`\  and \ :emphasis:`wait\_for\_os\_deployment`\  is \ :literal:`true`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry-default:`true` :ansible-option-choices-default-mark:`← (default)`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--destination"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_os_deployment_role__parameter-main__destination:

      .. rst-class:: ansible-option-title

      **destination**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--destination" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Share path to mount the ISO to iDRAC.

      Share needs to have a write permission to copy the generated ISO.

      CIFS, NFS, HTTP and HTTPS shares are supported.

      \ :emphasis:`destination`\  is ignored when \ :emphasis:`is\_custom\_iso`\  is \ :literal:`true`\ 

      When the protocol is of \ :literal:`http`\ , \ :literal:`https`\  custom iso is copied into a destination location/folder where the web server content is served.

      When the protocol is of \ :literal:`cifs`\ , c(nfs) custom iso is copied into the locally mounted nfs or cifs location location.


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--destination/hostname"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_os_deployment_role__parameter-main__destination/hostname:

      .. rst-class:: ansible-option-title

      **hostname**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--destination/hostname" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Target machine address/hostname where the custom iso will be copied.

      Address/hostname used to mount the iso as a virtual media.

      \ :emphasis:`hostname`\  is applicable to copy iso using ssh when \ :emphasis:`protocol`\  is \ :literal:`http`\  or \ :literal:`https`\ .

      \ :emphasis:`hostname`\  will be defaulted to localhost to copy iso when \ :emphasis:`protocol`\  is \ :literal:`nfs`\ , \ :literal:`cifs`\ .

      \ :emphasis:`hostname`\  will be used to mount the virtual media in idrac when \ :emphasis:`protocol`\  is \ :literal:`http`\ , \ :literal:`https`\ , \ :literal:`nfs`\  or \ :literal:`cifs`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--destination/iso_name"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_os_deployment_role__parameter-main__destination/iso_name:

      .. rst-class:: ansible-option-title

      **iso_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--destination/iso_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Custom iso file name. If not specified defaulted to \ :literal:`hostname-source.iso\_name`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--destination/iso_path"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_os_deployment_role__parameter-main__destination/iso_path:

      .. rst-class:: ansible-option-title

      **iso_path**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--destination/iso_path" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`path` / :ansible-option-required:`required`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Custom iso absolute path to be used to mount as a virtual media in idrac.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--destination/mountpoint"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_os_deployment_role__parameter-main__destination/mountpoint:

      .. rst-class:: ansible-option-title

      **mountpoint**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--destination/mountpoint" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`path` / :ansible-option-required:`required`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Target machine absolute path where the custom iso will be copied.

      \ :emphasis:`mountpoint`\  will be path where http/https is served from when \ :emphasis:`protocol`\  is \ :literal:`http`\ , \ :literal:`https`\ .

      \ :emphasis:`mountpoint`\  will be local folder mounted with nfs/cifs share when \ :emphasis:`protocol`\  is \ :literal:`nfs`\  \ :literal:`cifs`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--destination/os_type"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_os_deployment_role__parameter-main__destination/os_type:

      .. rst-class:: ansible-option-title

      **os_type**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--destination/os_type" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      HTTP/HTTPS share based on linux/Windows.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`"linux"` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`"windows"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--destination/password"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_os_deployment_role__parameter-main__destination/password:

      .. rst-class:: ansible-option-title

      **password**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--destination/password" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Password of the http/https/cifs share where customized ISO is used to mount as a virtual media.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--destination/protocol"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_os_deployment_role__parameter-main__destination/protocol:

      .. rst-class:: ansible-option-title

      **protocol**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--destination/protocol" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Type of the the transfer protocol used to mount the virtual media on to idrac.

      \ :literal:`https`\  uses the ssh protocol to copy the custom iso to the \ :emphasis:`mountpoint`\  and uses https protocol to the mount the virtual media.

      \ :literal:`http`\  uses the ssh protocol to copy the custom iso to the \ :emphasis:`mountpoint`\  and uses https protocol to the mount the virtual media.

      \ :literal:`nfs`\  copies the the custom iso to the \ :emphasis:`mountpoint`\  mounted localy and uses nfs protocol to the mount the virtual media.

      \ :literal:`cifs`\  copies the the custom iso to the \ :emphasis:`mountpoint`\  mounted localy and uses cifs protocol to the mount the virtual media.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"https"`
      - :ansible-option-choices-entry:`"http"`
      - :ansible-option-choices-entry:`"nfs"`
      - :ansible-option-choices-entry:`"cifs"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--destination/username"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_os_deployment_role__parameter-main__destination/username:

      .. rst-class:: ansible-option-title

      **username**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--destination/username" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Username of the http/https/cifs share where customized ISO is used to mount as a virtual media.


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--eject_iso"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_os_deployment_role__parameter-main__eject_iso:

      .. rst-class:: ansible-option-title

      **eject_iso**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--eject_iso" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Eject the virtual media (ISO) after the tracking of OS deployment is finished.

      ISO will be ejected if \ :emphasis:`eject\_iso`\  is \ :literal:`true`\  and \ :emphasis:`wait\_for\_os\_deployment`\  is \ :literal:`true`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry-default:`true` :ansible-option-choices-default-mark:`← (default)`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--hostname"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_os_deployment_role__parameter-main__hostname:

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
        <div class="ansibleOptionAnchor" id="parameter-main--https_port"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_os_deployment_role__parameter-main__https_port:

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

      .. _ansible_collections.dellemc.openmanage.idrac_os_deployment_role__parameter-main__https_timeout:

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
        <div class="ansibleOptionAnchor" id="parameter-main--os_deployment_timeout"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_os_deployment_role__parameter-main__os_deployment_timeout:

      .. rst-class:: ansible-option-title

      **os_deployment_timeout**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--os_deployment_timeout" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`integer`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Time in minutes to wait for the OS deployment to finish.


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`30`

      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--os_name"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_os_deployment_role__parameter-main__os_name:

      .. rst-class:: ansible-option-title

      **os_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--os_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The operating system name to match the jinja template of the kickstart file.

      Supported os name is versions for RHEL and ESXI.

      Jinja template file should exists in the format \<os\_name\_upper\>\_\<os\_version\_major\>.j2

      This is required when \ :emphasis:`is\_custom\_iso`\  is \ :literal:`false`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--os_version"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_os_deployment_role__parameter-main__os_version:

      .. rst-class:: ansible-option-title

      **os_version**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--os_version" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The operating system version to match the jinja template of the kickstart file.

      Supported versions for RHEL are 9.x and 8.x and for ESXi is 8.x.

      Jinja template file should exists in the format \<os\_name\_upper\>\_\<os\_version\_major\>.j2

      This is required when \ :emphasis:`is\_custom\_iso`\  is \ :literal:`false`\ 


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--password"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_os_deployment_role__parameter-main__password:

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
        <div class="ansibleOptionAnchor" id="parameter-main--source"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_os_deployment_role__parameter-main__source:

      .. rst-class:: ansible-option-title

      **source**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--source" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary` / :ansible-option-required:`required`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      HTTP/HTTPS share or local path of the ISO.


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--source/hostname"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_os_deployment_role__parameter-main__source/hostname:

      .. rst-class:: ansible-option-title

      **hostname**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--source/hostname" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      HTTP/HTTPS address to download the ISO.

      Hostname of the http/https/cifs and nfs to mount the custom iso to virtual media.

      \ :emphasis:`hostname`\  is applicable to download iso only when \ :emphasis:`protocol`\  is \ :literal:`http`\  or \ :literal:`https`\  and \ :emphasis:`is\_custom\_iso`\  is \ :literal:`false`\ .

      \ :emphasis:`hostname`\  is ignored to download the iso when \ :emphasis:`protocol`\  is \ :literal:`local`\ , \ :literal:`nfs`\  or \ :literal:`cifs`\  and \ :emphasis:`is\_custom\_iso`\  is \ :literal:`false`\ .

      \ :emphasis:`hostname`\  will be used to attach the virtual media when \ :emphasis:`is\_custom\_iso`\  is \ :literal:`true`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--source/is_custom_iso"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_os_deployment_role__parameter-main__source/is_custom_iso:

      .. rst-class:: ansible-option-title

      **is_custom_iso**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--source/is_custom_iso" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Specifies the source iso is a custom iso.

      \ :literal:`true`\  uses the custom iso and skips the kickstart file generation and custom iso compilation.

      when \ :literal:`true`\ , \ :emphasis:`destination`\  is ignored and uses the \ :emphasis:`iso\_path`\  to mount the virtual media on idrac.

      \ :literal:`false`\  runs the the kickstart file generation and custom iso compilation


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`false` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--source/iso_name"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_os_deployment_role__parameter-main__source/iso_name:

      .. rst-class:: ansible-option-title

      **iso_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--source/iso_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Name of the iso file.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--source/iso_path"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_os_deployment_role__parameter-main__source/iso_path:

      .. rst-class:: ansible-option-title

      **iso_path**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--source/iso_path" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`path` / :ansible-option-required:`required`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Absolute local path or http/https share path of the iso.

      when \ :emphasis:`custom\_iso`\  true \ :emphasis:`iso\_path`\  should be http, https, nfs or cifs path.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--source/ks_path"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_os_deployment_role__parameter-main__source/ks_path:

      .. rst-class:: ansible-option-title

      **ks_path**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--source/ks_path" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`path`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Absolute local path or http/https share path kickstart file.

      When \ :emphasis:`ks\_path`\  is provided role skips the generation of kickstart file and uses the one provided in the input.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--source/password"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_os_deployment_role__parameter-main__source/password:

      .. rst-class:: ansible-option-title

      **password**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--source/password" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Password of the http, https and cifs share.

      \ :emphasis:`password`\  is applicable only when \ :emphasis:`protocol`\  is \ :literal:`http`\  , \ :literal:`https`\  to download the iso file.

      \ :emphasis:`password`\  is applicable to mount the custom iso as a virtual media in idrac when \ :emphasis:`protocol`\  is \ :literal:`http`\  , \ :literal:`https`\ , c(cifs) and \ :emphasis:`is\_custom\_iso`\  is \ :literal:`true`\ .

      \ :emphasis:`password`\  is ignored when \ :emphasis:`protocol`\  is \ :literal:`local`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--source/protocol"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_os_deployment_role__parameter-main__source/protocol:

      .. rst-class:: ansible-option-title

      **protocol**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--source/protocol" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Type of the the transfer protocol used to download the iso.

      \ :literal:`https`\  uses the https protocol to download the iso.

      \ :literal:`http`\  uses the http protocol to download the iso.

      \ :literal:`nfs`\  uses the locally mounted nfs folder path to download the iso.

      \ :literal:`cifs`\  uses the locally mounted cifs folder path to download the iso.

      \ :literal:`local`\  uses the local folder path to download the iso.

      If \ :emphasis:`custom\_iso\_true`\  is \ :literal:`true`\  this will be used to mount the custom iso to virtual media.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"https"`
      - :ansible-option-choices-entry:`"http"`
      - :ansible-option-choices-entry:`"local"`
      - :ansible-option-choices-entry:`"cifs"`
      - :ansible-option-choices-entry:`"nfs"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--source/username"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_os_deployment_role__parameter-main__source/username:

      .. rst-class:: ansible-option-title

      **username**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--source/username" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Username of the http, https and cifs share.

      \ :emphasis:`username`\  is applicable only when \ :emphasis:`protocol`\  is \ :literal:`http`\  , \ :literal:`https`\  to download the iso file.

      \ :emphasis:`username`\  is applicable to mount the custom iso as a virtual media in idrac when \ :emphasis:`protocol`\  is \ :literal:`http`\  , \ :literal:`https`\ , c(cifs) and \ :emphasis:`is\_custom\_iso`\  is \ :literal:`true`\ .

      \ :emphasis:`username`\  is ignored when \ :emphasis:`protocol`\  is \ :literal:`local`\ .


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--username"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_os_deployment_role__parameter-main__username:

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

      iDRAC username with admin privilages.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--validate_certs"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_os_deployment_role__parameter-main__validate_certs:

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

      If \ :literal:`False`\ , the SSL certificates will not be validated.

      Configure \ :literal:`False`\  only on personally controlled sites where self-signed certificates are used.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry-default:`true` :ansible-option-choices-default-mark:`← (default)`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-main--wait_for_os_deployment"></div>

      .. _ansible_collections.dellemc.openmanage.idrac_os_deployment_role__parameter-main__wait_for_os_deployment:

      .. rst-class:: ansible-option-title

      **wait_for_os_deployment**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-main--wait_for_os_deployment" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`




      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Wait for the OS deployment to finish.


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

