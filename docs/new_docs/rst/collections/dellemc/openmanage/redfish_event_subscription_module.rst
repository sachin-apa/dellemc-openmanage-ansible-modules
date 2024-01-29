
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

.. _ansible_collections.dellemc.openmanage.redfish_event_subscription_module:

.. Anchors: short name for ansible.builtin

.. Anchors: aliases



.. Title

dellemc.openmanage.redfish_event_subscription module -- Manage Redfish Subscriptions
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. Collection note

.. note::
    This module is part of the `dellemc.openmanage collection <https://galaxy.ansible.com/dellemc/openmanage>`_ (version 8.5.0).

    To install it, use: :code:`ansible-galaxy collection install dellemc.openmanage`.
    You need further requirements to be able to use this module,
    see :ref:`Requirements <ansible_collections.dellemc.openmanage.redfish_event_subscription_module_requirements>` for details.

    To use it in a playbook, specify: :code:`dellemc.openmanage.redfish_event_subscription`.

.. version_added

.. rst-class:: ansible-version-added

New in dellemc.openmanage 4.1.0

.. contents::
   :local:
   :depth: 1

.. Deprecated


Synopsis
--------

.. Description

- This module allows to add or delete Redfish Event subscriptions.


.. Aliases


.. Requirements

.. _ansible_collections.dellemc.openmanage.redfish_event_subscription_module_requirements:

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

      .. _ansible_collections.dellemc.openmanage.redfish_event_subscription_module__parameter-baseuri:

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

      .. _ansible_collections.dellemc.openmanage.redfish_event_subscription_module__parameter-ca_path:

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
        <div class="ansibleOptionAnchor" id="parameter-destination"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_event_subscription_module__parameter-destination:

      .. rst-class:: ansible-option-title

      **destination**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-destination" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string` / :ansible-option-required:`required`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      The HTTPS URI of the destination to send events.

      HTTPS is required.


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-event_format_type"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_event_subscription_module__parameter-event_format_type:

      .. rst-class:: ansible-option-title

      **event_format_type**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-event_format_type" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Specifies the format type of the event to be subscribed.

      \ :literal:`Event`\  used to subscribe for Event format type.

      \ :literal:`MetricReport`\  used to subscribe for the metrics report format type.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`"Event"` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`"MetricReport"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-event_type"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_event_subscription_module__parameter-event_type:

      .. rst-class:: ansible-option-title

      **event_type**

      .. raw:: html

        <a class="ansibleOptionLink" href="#parameter-event_type" title="Permalink to this option"></a>

      .. rst-class:: ansible-option-type-line

      :ansible-option-type:`string`

      .. raw:: html

        </div>

    - .. raw:: html

        <div class="ansible-option-cell">

      Specifies the event type to be subscribed.

      \ :literal:`Alert`\  used to subscribe for alert.

      \ :literal:`MetricReport`\  used to subscribe for the metrics report.


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`"Alert"` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`"MetricReport"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-password"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_event_subscription_module__parameter-password:

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
        <div class="ansibleOptionAnchor" id="parameter-state"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_event_subscription_module__parameter-state:

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

      \ :literal:`present`\  adds new event subscription.

      \ :literal:`absent`\  deletes event subscription with the specified \ :emphasis:`destination`\ .


      .. rst-class:: ansible-option-line

      :ansible-option-choices:`Choices:`

      - :ansible-option-choices-entry-default:`"present"` :ansible-option-choices-default-mark:`← (default)`
      - :ansible-option-choices-entry:`"absent"`


      .. raw:: html

        </div>

  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="parameter-timeout"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_event_subscription_module__parameter-timeout:

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

      .. _ansible_collections.dellemc.openmanage.redfish_event_subscription_module__parameter-username:

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

      .. _ansible_collections.dellemc.openmanage.redfish_event_subscription_module__parameter-validate_certs:

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
   - \ :emphasis:`event\_type`\  needs to be \ :literal:`MetricReport`\  and \ :emphasis:`event\_format\_type`\  needs to be \ :literal:`MetricReport`\  for metrics subscription.
   - \ :emphasis:`event\_type`\  needs to be \ :literal:`Alert`\  and \ :emphasis:`event\_format\_type`\  needs to be \ :literal:`Event`\  for event subscription.
   - Modifying a subscription is not supported.
   - Context is always set to RedfishEvent.
   - This module supports \ :literal:`check\_mode`\ .

.. Seealso


.. Examples

Examples
--------

.. code-block:: yaml+jinja

    
    ---
    - name: Add Redfish metric subscription
      redfish_event_subscription:
        baseuri: "192.168.0.1"
        username: "user_name"
        password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        destination: "https://192.168.1.100:8188"
        event_type: MetricReport
        event_format_type: MetricReport
        state: present

    - name: Add Redfish alert subscription
      redfish_event_subscription:
        baseuri: "192.168.0.1"
        username: "user_name"
        password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        destination: "https://server01.example.com:8188"
        event_type: Alert
        event_format_type: Event
        state: present

    - name: Delete Redfish subscription with a specified destination
      redfish_event_subscription:
        baseuri: "192.168.0.1"
        username: "user_name"
        password: "user_password"
        ca_path: "/path/to/ca_cert.pem"
        destination: "https://server01.example.com:8188"
        state: absent




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

      .. _ansible_collections.dellemc.openmanage.redfish_event_subscription_module__return-error_info:

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

      Details of http error.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` on http error

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"error": {"@Message.ExtendedInfo": [{"Message": "Unable to complete the operation because the JSON data format entered is invalid.", "Resolution": "Do the following and the retry the operation: 1) Enter the correct JSON data format and retry the operation. 2) Make sure that no syntax error is present in JSON data format. 3) Make sure that a duplicate key is not present in JSON data format.", "Severity": "Critical"}, {"Message": "The request body submitted was malformed JSON and could not be parsed by the receiving service.", "Resolution": "Ensure that the request body is valid JSON and resubmit the request.", "Severity": "Critical"}], "code": "Base.1.2.GeneralError", "message": "A general error has occurred. See ExtendedInfo for more information."}}`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-msg"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_event_subscription_module__return-msg:

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

      Overall status of the task.


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` always

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`"Successfully added the subscription."`


      .. raw:: html

        </div>


  * - .. raw:: html

        <div class="ansible-option-cell">
        <div class="ansibleOptionAnchor" id="return-status"></div>

      .. _ansible_collections.dellemc.openmanage.redfish_event_subscription_module__return-status:

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

      Returns subscription object created


      .. rst-class:: ansible-option-line

      :ansible-option-returned-bold:`Returned:` on adding subscription successfully

      .. rst-class:: ansible-option-line
      .. rst-class:: ansible-option-sample

      :ansible-option-sample-bold:`Sample:` :ansible-rv-sample-value:`{"@Message.ExtendedInfo": [{"Message": "The resource has been created successfully", "MessageArgs": [], "MessageArgs@odata.count": 0, "MessageId": "Base.1.7.Created", "RelatedProperties": [], "RelatedProperties@odata.count": 0, "Resolution": "None", "Severity": "OK"}, {"Message": "A new resource is successfully created.", "MessageArgs": [], "MessageArgs@odata.count": 0, "MessageId": "IDRAC.2.2.SYS414", "RelatedProperties": [], "RelatedProperties@odata.count": 0, "Resolution": "No response action is required.", "Severity": "Informational"}], "Actions": {"#EventDestination.ResumeSubscription": {"target": "/redfish/v1/EventService/Subscriptions/5d432f36-81f4-11eb-9dc0-2cea7ff7ff9a/Actions/EventDestination.ResumeSubscription"}}, "Context": "RedfishEvent", "DeliveryRetryPolicy": "RetryForever", "Description": "Event Subscription Details", "Destination": "https://192.168.1.100:8188", "EventFormatType": "Event", "EventTypes": ["Alert"], "EventTypes@odata.count": 1, "HttpHeaders": [], "HttpHeaders@odata.count": 0, "Id": "5d432f36-81f4-11eb-9dc0-2cea7ff7ff9a", "MetricReportDefinitions": [], "MetricReportDefinitions@odata.count": 0, "Name": "EventSubscription 5d432f36-81f4-11eb-9dc0-2cea7ff7ff9a", "OriginResources": [], "OriginResources@odata.count": 0, "Protocol": "Redfish", "Status": {"Health": "OK", "HealthRollup": "OK", "State": "Enabled"}, "SubscriptionType": "RedfishEvent"}`


      .. raw:: html

        </div>



..  Status (Presently only deprecated)


.. Authors

Authors
~~~~~~~

- Trevor Squillario (@TrevorSquillario)
- Sachin Apagundi (@sachin-apa)



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

