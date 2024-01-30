
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

.. _ansible_collections.dellemc.openmanage.ome_alert_policies_module:

.. Anchors: short name for ansible.builtin

.. Anchors: aliases



.. Title

dellemc.openmanage.ome_alert_policies module -- Manage OME alert policies.
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. Collection note

.. note::
    This module is part of the `dellemc.openmanage collection <https://galaxy.ansible.com/dellemc/openmanage>`_ (version 8.5.0).

    To install it, use: :code:`ansible-galaxy collection install dellemc.openmanage`.
    You need further requirements to be able to use this module,
    see :ref:`Requirements <ansible_collections.dellemc.openmanage.ome_alert_policies_module_requirements>` for details.

    To use it in a playbook, specify: :code:`dellemc.openmanage.ome_alert_policies`.

.. version_added

.. rst-class:: ansible-version-added

New in dellemc.openmanage 8.3.0

.. contents::
   :local:
   :depth: 1

.. Deprecated


Synopsis
--------

.. Description

- This module allows you to create, modify, or delete alert policies on OpenManage Enterprise or OpenManage Enterprise Modular.


.. Aliases


.. Requirements

.. _ansible_collections.dellemc.openmanage.ome_alert_policies_module_requirements:

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
        <div class="ansibleOptionAnchor" id="parameter-actions"></div>

      .. _ansible_collections.dellemc.openmanage.ome_alert_policies_module__parameter-actions:

      .. rst-class:: ansible-option-title

      **actions**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-actions" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Actions to be triggered for the alert policy.

      This parameter is case-sensitive.

      This is mandatory for creating a policy and optional for updating a policy.

      This is applicable only when \ :emphasis:`state`\  is \ :literal:`present`\ 


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-actions/action_name"></div>

      .. _ansible_collections.dellemc.openmanage.ome_alert_policies_module__parameter-actions/action_name:

      .. rst-class:: ansible-option-title

      **action_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-actions/action_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Name of the action.

      This is fetched from the \ :ref:`dellemc.openmanage.ome\_alert\_policies\_action\_info <ansible_collections.dellemc.openmanage.ome_alert_policies_action_info_module>`\ .

      This is mandatory for creating a policy and optional for updating a policy.

      This parameter is case-sensitive.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-actions/parameters"></div>

      .. _ansible_collections.dellemc.openmanage.ome_alert_policies_module__parameter-actions/parameters:

      .. rst-class:: ansible-option-title

      **parameters**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-actions/parameters" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Predefined parameters required to set for \ :emphasis:`action\_name`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-default-bold:`Default:` :ansible-option-default:`[]`

      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-actions/parameters/name"></div>

      .. _ansible_collections.dellemc.openmanage.ome_alert_policies_module__parameter-actions/parameters/name:

      .. rst-class:: ansible-option-title

      **name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-actions/parameters/name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Name of the predefined parameter.

      This is fetched from the \ :ref:`dellemc.openmanage.ome\_alert\_policies\_action\_info <ansible_collections.dellemc.openmanage.ome_alert_policies_action_info_module>`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-actions/parameters/value"></div>

      .. _ansible_collections.dellemc.openmanage.ome_alert_policies_module__parameter-actions/parameters/value:

      .. rst-class:: ansible-option-title

      **value**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-actions/parameters/value" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Value of the predefined parameter.

      These values will not be validated.


      .. raw:: html

        </div>



  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-all_devices"></div>

      .. _ansible_collections.dellemc.openmanage.ome_alert_policies_module__parameter-all_devices:

      .. rst-class:: ansible-option-title

      **all_devices**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-all_devices" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      This option indicates whether the alert policy is applicable to all the discovered and undiscovered devices or not.

      This option is mutually exclusive with \ :emphasis:`device\_service\_tag`\ , \ :emphasis:`specific\_undiscovered\_devices`\ , \ :emphasis:`any\_undiscovered\_devices`\  and \ :emphasis:`device\_group`\ .

      This is applicable only when \ :emphasis:`state`\  is \ :literal:`present`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-any_undiscovered_devices"></div>

      .. _ansible_collections.dellemc.openmanage.ome_alert_policies_module__parameter-any_undiscovered_devices:

      .. rst-class:: ansible-option-title

      **any_undiscovered_devices**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-any_undiscovered_devices" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      This option indicates whether the alert policy is applicable to any undiscovered devices or not.

      This option is mutually exclusive with \ :emphasis:`device\_service\_tag`\ , \ :emphasis:`specific\_undiscovered\_devices`\ , \ :emphasis:`device\_group`\  and \ :emphasis:`all\_devices`\ .

      This is applicable only when \ :emphasis:`state`\  is \ :literal:`present`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-ca_path"></div>

      .. _ansible_collections.dellemc.openmanage.ome_alert_policies_module__parameter-ca_path:

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
        <div class="ansibleOptionAnchor" id="parameter-category"></div>

      .. _ansible_collections.dellemc.openmanage.ome_alert_policies_module__parameter-category:

      .. rst-class:: ansible-option-title

      **category**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-category" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Category of the alerts received.

      This is mutually exclusive with the \ :emphasis:`message\_ids`\ , \ :emphasis:`message\_file`\ .

      This is fetched from the \ :ref:`dellemc.openmanage.ome\_alert\_policies\_category\_info <ansible_collections.dellemc.openmanage.ome_alert_policies_category_info_module>`\ .

      This is applicable only when \ :emphasis:`state`\  is \ :literal:`present`\ .


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-category/catalog_category"></div>

      .. _ansible_collections.dellemc.openmanage.ome_alert_policies_module__parameter-category/catalog_category:

      .. rst-class:: ansible-option-title

      **catalog_category**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-category/catalog_category" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Category of the catalog.


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-category/catalog_category/category_name"></div>

      .. _ansible_collections.dellemc.openmanage.ome_alert_policies_module__parameter-category/catalog_category/category_name:

      .. rst-class:: ansible-option-title

      **category_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-category/catalog_category/category_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Name of the category.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-category/catalog_category/sub_category_names"></div>

      .. _ansible_collections.dellemc.openmanage.ome_alert_policies_module__parameter-category/catalog_category/sub_category_names:

      .. rst-class:: ansible-option-title

      **sub_category_names**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-category/catalog_category/sub_category_names" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      List of sub-categories.


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-category/catalog_name"></div>

      .. _ansible_collections.dellemc.openmanage.ome_alert_policies_module__parameter-category/catalog_name:

      .. rst-class:: ansible-option-title

      **catalog_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-category/catalog_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Name of the catalog.


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-date_and_time"></div>

      .. _ansible_collections.dellemc.openmanage.ome_alert_policies_module__parameter-date_and_time:

      .. rst-class:: ansible-option-title

      **date_and_time**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-date_and_time" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Specifies the schedule for when the alert policy is applicable.

      \ :emphasis:`date\_and\_time`\  is mandatory for creating a policy and optional when updating a policy.

      This is applicable only when \ :emphasis:`state`\  is \ :literal:`present`\ .


      .. raw:: html

        </div>
    
  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-date_and_time/date_from"></div>

      .. _ansible_collections.dellemc.openmanage.ome_alert_policies_module__parameter-date_and_time/date_from:

      .. rst-class:: ansible-option-title

      **date_from**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-date_and_time/date_from" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Start date in the format YYYY-MM-DD.

      This parameter to be provided in quotes.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-date_and_time/date_to"></div>

      .. _ansible_collections.dellemc.openmanage.ome_alert_policies_module__parameter-date_and_time/date_to:

      .. rst-class:: ansible-option-title

      **date_to**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-date_and_time/date_to" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      End date in the format YYYY-MM-DD.

      This parameter to be provided in quotes.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-date_and_time/days"></div>

      .. _ansible_collections.dellemc.openmanage.ome_alert_policies_module__parameter-date_and_time/days:

      .. rst-class:: ansible-option-title

      **days**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-date_and_time/days" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Required days of the week on which alert policy operation must be scheduled.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"monday"`
      - :ansible-option-choices-entry:`"tuesday"`
      - :ansible-option-choices-entry:`"wednesday"`
      - :ansible-option-choices-entry:`"thursday"`
      - :ansible-option-choices-entry:`"friday"`
      - :ansible-option-choices-entry:`"saturday"`
      - :ansible-option-choices-entry:`"sunday"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-date_and_time/time_from"></div>

      .. _ansible_collections.dellemc.openmanage.ome_alert_policies_module__parameter-date_and_time/time_from:

      .. rst-class:: ansible-option-title

      **time_from**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-date_and_time/time_from" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Interval start time in the format HH:MM

      This parameter to be provided in quotes.

      This is mandatory when \ :emphasis:`time\_interval`\  is \ :literal:`true`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-date_and_time/time_interval"></div>

      .. _ansible_collections.dellemc.openmanage.ome_alert_policies_module__parameter-date_and_time/time_interval:

      .. rst-class:: ansible-option-title

      **time_interval**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-date_and_time/time_interval" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Enable the time interval for which alert policy must be scheduled.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-indent"></div><div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-date_and_time/time_to"></div>

      .. _ansible_collections.dellemc.openmanage.ome_alert_policies_module__parameter-date_and_time/time_to:

      .. rst-class:: ansible-option-title

      **time_to**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-date_and_time/time_to" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-indent-desc"></div><div class="ansible-option-cell">

      Interval end time in the format HH:MM

      This parameter to be provided in quotes.

      This is mandatory when \ :emphasis:`time\_interval`\  is \ :literal:`true`\ 


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-description"></div>

      .. _ansible_collections.dellemc.openmanage.ome_alert_policies_module__parameter-description:

      .. rst-class:: ansible-option-title

      **description**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-description" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Description for the alert policy.

      This is applicable only when \ :emphasis:`state`\  is \ :literal:`present`\ 


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-device_group"></div>

      .. _ansible_collections.dellemc.openmanage.ome_alert_policies_module__parameter-device_group:

      .. rst-class:: ansible-option-title

      **device_group**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-device_group" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      List of device group names on which the alert policy is applicable.

      This option is mutually exclusive with \ :emphasis:`device\_service\_tag`\ , \ :emphasis:`specific\_undiscovered\_devices`\ , \ :emphasis:`any\_undiscovered\_devices`\  and \ :emphasis:`all\_devices`\  .

      This is applicable only when \ :emphasis:`state`\  is \ :literal:`present`\ 


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-device_service_tag"></div>

      .. _ansible_collections.dellemc.openmanage.ome_alert_policies_module__parameter-device_service_tag:

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

      List of device service tags on which the alert policy will be applicable.

      This option is mutually exclusive with \ :emphasis:`device\_group`\ , \ :emphasis:`specific\_undiscovered\_devices`\ , \ :emphasis:`any\_undiscovered\_devices`\  and \ :emphasis:`all\_devices`\ .

      This is applicable only when \ :emphasis:`state`\  is \ :literal:`present`\ 


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-enable"></div>

      .. _ansible_collections.dellemc.openmanage.ome_alert_policies_module__parameter-enable:

      .. rst-class:: ansible-option-title

      **enable**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-enable" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`boolean`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      \ :literal:`true`\  allows you to enable an alert policy.

      \ :literal:`false`\  allows you to disable an alert policy.

      This is applicable only when \ :emphasis:`state`\  is \ :literal:`present`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`false`
      - :ansible-option-choices-entry:`true`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-hostname"></div>

      .. _ansible_collections.dellemc.openmanage.ome_alert_policies_module__parameter-hostname:

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
        <div class="ansibleOptionAnchor" id="parameter-message_file"></div>

      .. _ansible_collections.dellemc.openmanage.ome_alert_policies_module__parameter-message_file:

      .. rst-class:: ansible-option-title

      **message_file**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-message_file" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`path`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Local path of a CSV formatted file with message IDs

      This is mutually exclusive with the \ :emphasis:`category`\ , \ :emphasis:`message\_ids`\ 

      This is applicable only when \ :emphasis:`state`\  is \ :literal:`present`\ 

      This is fetched from the \ :ref:`dellemc.openmanage.ome\_alert\_policies\_message\_id\_info <ansible_collections.dellemc.openmanage.ome_alert_policies_message_id_info_module>`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-message_ids"></div>

      .. _ansible_collections.dellemc.openmanage.ome_alert_policies_module__parameter-message_ids:

      .. rst-class:: ansible-option-title

      **message_ids**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-message_ids" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      List of Message ids

      This is mutually exclusive with the \ :emphasis:`category`\ , \ :emphasis:`message\_file`\ 

      This is applicable only when \ :emphasis:`state`\  is \ :literal:`present`\ 

      This is fetched from the \ :ref:`dellemc.openmanage.ome\_alert\_policies\_message\_id\_info <ansible_collections.dellemc.openmanage.ome_alert_policies_message_id_info_module>`\ .


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-name"></div>

      .. _ansible_collections.dellemc.openmanage.ome_alert_policies_module__parameter-name:

      .. rst-class:: ansible-option-title

      **name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Name of an alert policy or a list of alert policies.

      More than one policy name is applicable when \ :emphasis:`state`\  is \ :literal:`absent`\  and \ :emphasis:`state`\  is \ :literal:`present`\  with only \ :emphasis:`enable`\  provided.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-new_name"></div>

      .. _ansible_collections.dellemc.openmanage.ome_alert_policies_module__parameter-new_name:

      .. rst-class:: ansible-option-title

      **new_name**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-new_name" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      New name for the alert policy.

      This is applicable only when \ :emphasis:`state`\  is \ :literal:`present`\ , and an alert policy exists.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-password"></div>

      .. _ansible_collections.dellemc.openmanage.ome_alert_policies_module__parameter-password:

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

      .. _ansible_collections.dellemc.openmanage.ome_alert_policies_module__parameter-port:

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
        <div class="ansibleOptionAnchor" id="parameter-severity"></div>

      .. _ansible_collections.dellemc.openmanage.ome_alert_policies_module__parameter-severity:

      .. rst-class:: ansible-option-title

      **severity**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-severity" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Severity of the alert policy.

      This is mandatory for creating a policy and optional for updating a policy.

      This is applicable only when \ :emphasis:`state`\  is \ :literal:`present`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry:`"all"`
      - :ansible-option-choices-entry:`"unknown"`
      - :ansible-option-choices-entry:`"info"`
      - :ansible-option-choices-entry:`"normal"`
      - :ansible-option-choices-entry:`"warning"`
      - :ansible-option-choices-entry:`"critical"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-specific_undiscovered_devices"></div>

      .. _ansible_collections.dellemc.openmanage.ome_alert_policies_module__parameter-specific_undiscovered_devices:

      .. rst-class:: ansible-option-title

      **specific_undiscovered_devices**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-specific_undiscovered_devices" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`list` / :ansible-option-elements:`elements=string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      List of undiscovered IPs, hostnames, or range of IPs of devices on which the alert policy is applicable.

      This option is mutually exclusive with \ :emphasis:`device\_service\_tag`\ , \ :emphasis:`device\_group`\ , \ :emphasis:`any\_undiscovered\_devices`\  and \ :emphasis:`all\_devices`\  .

      This is applicable only when \ :emphasis:`state`\  is \ :literal:`present`\ 

      Examples of valid IP range format:

           10.35.0.0

           10.36.0.0-10.36.0.255

           10.37.0.0/24

           2607:f2b1:f083:135::5500/118

           2607:f2b1:f083:135::a500-2607:f2b1:f083:135::a600

           hostname.domain.com

      Examples of invalid IP range format:

           10.35.0.\*

           10.36.0.0-255

           10.35.0.0/255.255.255.0

      These values will not be validated.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-state"></div>

      .. _ansible_collections.dellemc.openmanage.ome_alert_policies_module__parameter-state:

      .. rst-class:: ansible-option-title

      **state**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-state" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      \ :literal:`present`\  allows you to create an alert policy or update if the policy name already exists.

      \ :literal:`absent`\  allows you to delete an alert policy.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`"present"` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`"absent"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-timeout"></div>

      .. _ansible_collections.dellemc.openmanage.ome_alert_policies_module__parameter-timeout:

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

      .. _ansible_collections.dellemc.openmanage.ome_alert_policies_module__parameter-username:

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

      .. _ansible_collections.dellemc.openmanage.ome_alert_policies_module__parameter-validate_certs:

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
   - Run this module from a system that has direct access to Dell OpenManage Enterprise or OpenManage Enterprise Modular.
   - This module supports IPv4 and IPv6 addresses.
   - This module supports \ :literal:`check\_mode`\ .

.. Seealso


.. Examples

Examples
--------

.. code-block:: yaml+jinja

    
    ---
    - name: "Create an alert policy"
      dellemc.openamanage.ome_alert_policies:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        name: "Alert Policy One"
        device_service_tag:
          - ABCD123
          - SVC7845
        category:
          - catalog_name: Application
            catalog_category:
              - category_name: Audit
                sub_category_names:
                  - Generic
                  - Devices
          - catalog_name: iDRAC
            catalog_category:
              - category_name: Audit
                sub_category_names:
                  - BIOS Management
                  - iDRAC Service Module
        date_and_time:
          date_from: "2023-10-10"
          date_to: "2023-10-11"
          time_from: "11:00"
          time_to: "12:00"
        severity:
          - unknown
          - critical
        actions:
          - action_name: Trap
            parameters:
              - name: "192.1.2.3:162"
                value: true
              - name: "traphostname.domain.com:162"
                value: true
      tags: create_alert_policy

    - name: "Update an alert Policy"
      dellemc.openamanage.ome_alert_policies:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        new_name: "Update Policy Name"
        device_group: "Group Name"
        message_ids:
          - AMP400
          - CTL201
          - BIOS101
        date_and_time:
          date_from: "2023-10-10"
          date_to: "2023-10-11"
          time_from: "11:00"
          time_to: "12:00"
          time_interval: true
        actions:
          - action_name: Trap
            parameters:
              - name: "192.1.2.3:162"
                value: true
      tags: update_alert_policy

    - name: "Enable an alert policy"
      dellemc.openamanage.ome_alert_policies:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        name: "Policy Name"
        enable: true
      tags: enable_alert_policy

    - name: "Disable multiple alert policies"
      dellemc.openamanage.ome_alert_policies:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        name:
          - "Policy Name 1"
          - "Policy Name 2"
        enable: false
      tags: disable_alert_policy

    - name: "Delete an alert policy"
      dellemc.openamanage.ome_alert_policies:
        hostname: "192.168.0.1"
        username: "username"
        password: "password"
        ca_path: "/path/to/ca_cert.pem"
        name:
          - "Policy Name"
        state: absent
      tags: delete_alert_policy




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

      .. _ansible_collections.dellemc.openmanage.ome_alert_policies_module__return-error_info:

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

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"error": {"@Message.ExtendedInfo": [{"Message": "Unable to create or modify the alert policy because an invalid value [To Email] is entered for the action Email.", "MessageArgs": ["[To Email]", "Email"], "MessageId": "CMON7011", "RelatedProperties": [], "Resolution": "Enter a valid value for the action identified in the message and retry the operation.", "Severity": "Warning"}], "code": "Base.1.0.GeneralError", "message": "A general error has occurred. See ExtendedInfo for more information."}}`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-msg"></div>

      .. _ansible_collections.dellemc.openmanage.ome_alert_policies_module__return-msg:

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

      Status of the alert policies operation.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` always

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`"Successfully created the alert policy."`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-status"></div>

      .. _ansible_collections.dellemc.openmanage.ome_alert_policies_module__return-status:

      .. rst-class:: ansible-option-title

      **status**

      .. raw:: html

        <a class="ansibleOptionLink" href="#return-status" title="Permalink to this return value"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`dictionary`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The policy which was created or modified.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` when state is present

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"DefaultPolicy": false, "Description": "Details of the Policy", "Editable": true, "Enabled": true, "Id": 12345, "Name": "Policy", "PolicyData": {"Actions": [{"Id": 8, "Name": "Email", "ParameterDetails": [{"Id": 1, "Name": "subject", "Type": "string", "TypeParams": [{"Name": "maxLength", "Value": "255"}], "Value": "Device Name: $name,  Device IP Address: $ip,  Severity: $severity"}, {"Id": 1, "Name": "to", "Type": "string", "TypeParams": [{"Name": "maxLength", "Value": "255"}], "Value": "test@org.com"}, {"Id": 1, "Name": "from", "Type": "string", "TypeParams": [{"Name": "maxLength", "Value": "255"}], "Value": "abc@corp.com"}, {"Id": 1, "Name": "message", "Type": "string", "TypeParams": [{"Name": "maxLength", "Value": "255"}], "Value": "Event occurred for Device Name: $name, Device IP Address: $ip"}]}], "Catalogs": [{"CatalogName": "iDRAC", "Categories": [4], "SubCategories": [41]}, {"CatalogName": "Application", "Categories": [0], "SubCategories": [0]}], "DeviceTypes": [1000, 2000], "Devices": [10086, 10088], "Groups": [], "Owner": 10069, "Schedule": {"CronString": "\* \* \* ? \* \* \*", "EndTime": "2023-06-06 18:02:46.000", "StartTime": "2023-06-06 15:02:46.000"}, "Severities": [16, 1, 2, 4, 8], "State": true, "UndiscoveredTargets": []}, "Visible": true}`


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

