


.. _plugins_in_dellemc.openmanage:

Dellemc.Openmanage
==================

Collection version 8.5.0

.. contents::
   :local:
   :depth: 1

Description
-----------

Dell OpenManage Ansible Modules allows data center and IT administrators to use RedHat Ansible to automate and orchestrate the configuration, deployment, and update of Dell PowerEdge Servers and modular infrastructure by leveraging the management automation capabilities in-built into the Integrated Dell Remote Access Controller (iDRAC), OpenManage Enterprise and OpenManage Enterprise Modular.

**Authors:**

* Jagadeesh N V <Jagadeesh.N.V@Dell.com>
* Felix Stephen <Felix.S@Dell.com>
* Sachin Apagundi <Sachin.Apagundi@Dell.com>
* Husniya Hameed <Husniya.Hameed@Dellteam.com>
* Abhishek Sinha <Abhishek.Sinha10@Dell.com>
* Kritika Bhateja <Kritika.Bhateja@Dell.com>
* Shivam Sharma <Shivam.Sharma3@Dell.com>
* Rajshekar P <Rajshekar.P@Dell.com>
* Jennifer John <Jennifer.John@Dell.com>
* Lovepreet Singh <Lovepreet.Singh1@dell.com>

**Supported ansible-core versions:**

* 2.14.0 or newer

.. raw:: html

  <p class="ansible-links">
    <a href="https://github.com/dell/dellemc-openmanage-ansible-modules/issues" aria-role="button" target="_blank" rel="noopener external">Issue Tracker</a>
    <a href="https://github.com/dell/dellemc-openmanage-ansible-modules" aria-role="button" target="_blank" rel="noopener external">Homepage</a>
    <a href="https://github.com/dell/dellemc-openmanage-ansible-modules/tree/collections" aria-role="button" target="_blank" rel="noopener external">Repository (Sources)</a>
  </p>



.. toctree::
    :maxdepth: 1


Plugin Index
------------

These are the plugins in the dellemc.openmanage collection:


Modules
~~~~~~~

* :ref:`dellemc_configure_idrac_eventing module <ansible_collections.dellemc.openmanage.dellemc_configure_idrac_eventing_module>` -- Configures the iDRAC eventing related attributes
* :ref:`dellemc_configure_idrac_services module <ansible_collections.dellemc.openmanage.dellemc_configure_idrac_services_module>` -- Configures the iDRAC services related attributes
* :ref:`dellemc_idrac_lc_attributes module <ansible_collections.dellemc.openmanage.dellemc_idrac_lc_attributes_module>` -- Enable or disable Collect System Inventory on Restart (CSIOR) property for all iDRAC/LC jobs
* :ref:`dellemc_idrac_storage_volume module <ansible_collections.dellemc.openmanage.dellemc_idrac_storage_volume_module>` -- Configures the RAID configuration attributes
* :ref:`dellemc_system_lockdown_mode module <ansible_collections.dellemc.openmanage.dellemc_system_lockdown_mode_module>` -- Configures system lockdown mode for iDRAC
* :ref:`idrac_attributes module <ansible_collections.dellemc.openmanage.idrac_attributes_module>` -- Configure the iDRAC attributes.
* :ref:`idrac_bios module <ansible_collections.dellemc.openmanage.idrac_bios_module>` -- Modify and clear BIOS attributes, reset BIOS settings and configure boot sources
* :ref:`idrac_boot module <ansible_collections.dellemc.openmanage.idrac_boot_module>` -- Configure the boot order settings.
* :ref:`idrac_certificates module <ansible_collections.dellemc.openmanage.idrac_certificates_module>` -- Configure certificates for iDRAC
* :ref:`idrac_firmware module <ansible_collections.dellemc.openmanage.idrac_firmware_module>` -- Firmware update from a repository on a network share (CIFS, NFS, HTTP, HTTPS, FTP)
* :ref:`idrac_firmware_info module <ansible_collections.dellemc.openmanage.idrac_firmware_info_module>` -- Get Firmware Inventory
* :ref:`idrac_lifecycle_controller_job_status_info module <ansible_collections.dellemc.openmanage.idrac_lifecycle_controller_job_status_info_module>` -- Get the status of a Lifecycle Controller job
* :ref:`idrac_lifecycle_controller_jobs module <ansible_collections.dellemc.openmanage.idrac_lifecycle_controller_jobs_module>` -- Delete the Lifecycle Controller Jobs
* :ref:`idrac_lifecycle_controller_logs module <ansible_collections.dellemc.openmanage.idrac_lifecycle_controller_logs_module>` -- Export Lifecycle Controller logs to a network share or local path.
* :ref:`idrac_lifecycle_controller_status_info module <ansible_collections.dellemc.openmanage.idrac_lifecycle_controller_status_info_module>` -- Get the status of the Lifecycle Controller
* :ref:`idrac_network module <ansible_collections.dellemc.openmanage.idrac_network_module>` -- Configures the iDRAC network attributes
* :ref:`idrac_network_attributes module <ansible_collections.dellemc.openmanage.idrac_network_attributes_module>` -- Configures the iDRAC network attributes
* :ref:`idrac_os_deployment module <ansible_collections.dellemc.openmanage.idrac_os_deployment_module>` -- Boot to a network ISO image
* :ref:`idrac_redfish_storage_controller module <ansible_collections.dellemc.openmanage.idrac_redfish_storage_controller_module>` -- Configures the physical disk, virtual disk, and storage controller settings
* :ref:`idrac_reset module <ansible_collections.dellemc.openmanage.idrac_reset_module>` -- Reset iDRAC
* :ref:`idrac_server_config_profile module <ansible_collections.dellemc.openmanage.idrac_server_config_profile_module>` -- Export or Import iDRAC Server Configuration Profile (SCP)
* :ref:`idrac_syslog module <ansible_collections.dellemc.openmanage.idrac_syslog_module>` -- Enable or disable the syslog on iDRAC
* :ref:`idrac_system_info module <ansible_collections.dellemc.openmanage.idrac_system_info_module>` -- Get the PowerEdge Server System Inventory
* :ref:`idrac_timezone_ntp module <ansible_collections.dellemc.openmanage.idrac_timezone_ntp_module>` -- Configures time zone and NTP on iDRAC
* :ref:`idrac_user module <ansible_collections.dellemc.openmanage.idrac_user_module>` -- Configure settings for user accounts
* :ref:`idrac_user_info module <ansible_collections.dellemc.openmanage.idrac_user_info_module>` -- Retrieve details of all users or a specific user on iDRAC.
* :ref:`idrac_virtual_media module <ansible_collections.dellemc.openmanage.idrac_virtual_media_module>` -- Configure the Remote File Share settings.
* :ref:`ome_active_directory module <ansible_collections.dellemc.openmanage.ome_active_directory_module>` -- Configure Active Directory groups to be used with Directory Services
* :ref:`ome_alert_policies module <ansible_collections.dellemc.openmanage.ome_alert_policies_module>` -- Manage OME alert policies.
* :ref:`ome_alert_policies_actions_info module <ansible_collections.dellemc.openmanage.ome_alert_policies_actions_info_module>` -- Get information on actions of alert policies.
* :ref:`ome_alert_policies_category_info module <ansible_collections.dellemc.openmanage.ome_alert_policies_category_info_module>` -- Retrieves information of all OME alert policy categories.
* :ref:`ome_alert_policies_info module <ansible_collections.dellemc.openmanage.ome_alert_policies_info_module>` -- Retrieves information of one or more OME alert policies.
* :ref:`ome_alert_policies_message_id_info module <ansible_collections.dellemc.openmanage.ome_alert_policies_message_id_info_module>` -- Get message ID information of alert policies.
* :ref:`ome_application_alerts_smtp module <ansible_collections.dellemc.openmanage.ome_application_alerts_smtp_module>` -- This module allows to configure SMTP or email configurations
* :ref:`ome_application_alerts_syslog module <ansible_collections.dellemc.openmanage.ome_application_alerts_syslog_module>` -- Configure syslog forwarding settings on OpenManage Enterprise and OpenManage Enterprise Modular
* :ref:`ome_application_certificate module <ansible_collections.dellemc.openmanage.ome_application_certificate_module>` -- This module allows to generate a CSR and upload the certificate
* :ref:`ome_application_console_preferences module <ansible_collections.dellemc.openmanage.ome_application_console_preferences_module>` -- Configure console preferences on OpenManage Enterprise.
* :ref:`ome_application_network_address module <ansible_collections.dellemc.openmanage.ome_application_network_address_module>` -- Updates the network configuration on OpenManage Enterprise
* :ref:`ome_application_network_proxy module <ansible_collections.dellemc.openmanage.ome_application_network_proxy_module>` -- Updates the proxy configuration on OpenManage Enterprise
* :ref:`ome_application_network_settings module <ansible_collections.dellemc.openmanage.ome_application_network_settings_module>` -- This module allows you to configure the session inactivity timeout settings
* :ref:`ome_application_network_time module <ansible_collections.dellemc.openmanage.ome_application_network_time_module>` -- Updates the network time on OpenManage Enterprise
* :ref:`ome_application_network_webserver module <ansible_collections.dellemc.openmanage.ome_application_network_webserver_module>` -- Updates the Web server configuration on OpenManage Enterprise
* :ref:`ome_application_security_settings module <ansible_collections.dellemc.openmanage.ome_application_security_settings_module>` -- Configure the login security properties
* :ref:`ome_chassis_slots module <ansible_collections.dellemc.openmanage.ome_chassis_slots_module>` -- Rename sled slots on OpenManage Enterprise Modular
* :ref:`ome_configuration_compliance_baseline module <ansible_collections.dellemc.openmanage.ome_configuration_compliance_baseline_module>` -- Create, modify, and delete a configuration compliance baseline and remediate non-compliant devices on OpenManage Enterprise
* :ref:`ome_configuration_compliance_info module <ansible_collections.dellemc.openmanage.ome_configuration_compliance_info_module>` -- Device compliance report for devices managed in OpenManage Enterprise
* :ref:`ome_device_group module <ansible_collections.dellemc.openmanage.ome_device_group_module>` -- Add or remove device(s) from a static device group on OpenManage Enterprise
* :ref:`ome_device_info module <ansible_collections.dellemc.openmanage.ome_device_info_module>` -- Retrieves the information of devices inventoried by OpenManage Enterprise
* :ref:`ome_device_local_access_configuration module <ansible_collections.dellemc.openmanage.ome_device_local_access_configuration_module>` -- Configure local access settings on OpenManage Enterprise Modular.
* :ref:`ome_device_location module <ansible_collections.dellemc.openmanage.ome_device_location_module>` -- Configure device location settings on OpenManage Enterprise Modular
* :ref:`ome_device_mgmt_network module <ansible_collections.dellemc.openmanage.ome_device_mgmt_network_module>` -- Configure network settings of devices on OpenManage Enterprise Modular
* :ref:`ome_device_network_services module <ansible_collections.dellemc.openmanage.ome_device_network_services_module>` -- Configure chassis network services settings on OpenManage Enterprise Modular
* :ref:`ome_device_power_settings module <ansible_collections.dellemc.openmanage.ome_device_power_settings_module>` -- Configure chassis power settings on OpenManage Enterprise Modular
* :ref:`ome_device_quick_deploy module <ansible_collections.dellemc.openmanage.ome_device_quick_deploy_module>` -- Configure Quick Deploy settings on OpenManage Enterprise Modular.
* :ref:`ome_devices module <ansible_collections.dellemc.openmanage.ome_devices_module>` -- Perform device-specific operations on target devices
* :ref:`ome_diagnostics module <ansible_collections.dellemc.openmanage.ome_diagnostics_module>` -- Export technical support logs(TSR) to network share location
* :ref:`ome_discovery module <ansible_collections.dellemc.openmanage.ome_discovery_module>` -- Create, modify, or delete a discovery job on OpenManage Enterprise
* :ref:`ome_domain_user_groups module <ansible_collections.dellemc.openmanage.ome_domain_user_groups_module>` -- Create, modify, or delete an Active Directory/LDAP user group on OpenManage Enterprise and OpenManage Enterprise Modular
* :ref:`ome_firmware module <ansible_collections.dellemc.openmanage.ome_firmware_module>` -- Update firmware on PowerEdge devices and its components through OpenManage Enterprise
* :ref:`ome_firmware_baseline module <ansible_collections.dellemc.openmanage.ome_firmware_baseline_module>` -- Create, modify, or delete a firmware baseline on OpenManage Enterprise or OpenManage Enterprise Modular
* :ref:`ome_firmware_baseline_compliance_info module <ansible_collections.dellemc.openmanage.ome_firmware_baseline_compliance_info_module>` -- Retrieves baseline compliance details on OpenManage Enterprise
* :ref:`ome_firmware_baseline_info module <ansible_collections.dellemc.openmanage.ome_firmware_baseline_info_module>` -- Retrieves baseline details from OpenManage Enterprise
* :ref:`ome_firmware_catalog module <ansible_collections.dellemc.openmanage.ome_firmware_catalog_module>` -- Create, modify, or delete a firmware catalog on OpenManage Enterprise or OpenManage Enterprise Modular
* :ref:`ome_groups module <ansible_collections.dellemc.openmanage.ome_groups_module>` -- Manages static device groups on OpenManage Enterprise
* :ref:`ome_identity_pool module <ansible_collections.dellemc.openmanage.ome_identity_pool_module>` -- Manages identity pool settings on OpenManage Enterprise
* :ref:`ome_job_info module <ansible_collections.dellemc.openmanage.ome_job_info_module>` -- Get job details for a given job ID or an entire job queue on OpenMange Enterprise
* :ref:`ome_network_port_breakout module <ansible_collections.dellemc.openmanage.ome_network_port_breakout_module>` -- This module allows to automate the port portioning or port breakout to logical sub ports
* :ref:`ome_network_vlan module <ansible_collections.dellemc.openmanage.ome_network_vlan_module>` -- Create, modify & delete a VLAN
* :ref:`ome_network_vlan_info module <ansible_collections.dellemc.openmanage.ome_network_vlan_info_module>` -- Retrieves the information about networks VLAN(s) present in OpenManage Enterprise
* :ref:`ome_powerstate module <ansible_collections.dellemc.openmanage.ome_powerstate_module>` -- Performs the power management operations on OpenManage Enterprise
* :ref:`ome_profile module <ansible_collections.dellemc.openmanage.ome_profile_module>` -- Create, modify, delete, assign, unassign and migrate a profile on OpenManage Enterprise
* :ref:`ome_profile_info module <ansible_collections.dellemc.openmanage.ome_profile_info_module>` -- Retrieve profiles with attribute details
* :ref:`ome_server_interface_profile_info module <ansible_collections.dellemc.openmanage.ome_server_interface_profile_info_module>` -- Retrieves the information of server interface profile on OpenManage Enterprise Modular.
* :ref:`ome_server_interface_profiles module <ansible_collections.dellemc.openmanage.ome_server_interface_profiles_module>` -- Configure server interface profiles
* :ref:`ome_smart_fabric module <ansible_collections.dellemc.openmanage.ome_smart_fabric_module>` -- Create, modify or delete a fabric on OpenManage Enterprise Modular
* :ref:`ome_smart_fabric_info module <ansible_collections.dellemc.openmanage.ome_smart_fabric_info_module>` -- Retrieves the information of smart fabrics inventoried by OpenManage Enterprise Modular
* :ref:`ome_smart_fabric_uplink module <ansible_collections.dellemc.openmanage.ome_smart_fabric_uplink_module>` -- Create, modify or delete a uplink for a fabric on OpenManage Enterprise Modular
* :ref:`ome_smart_fabric_uplink_info module <ansible_collections.dellemc.openmanage.ome_smart_fabric_uplink_info_module>` -- Retrieve details of fabric uplink on OpenManage Enterprise Modular.
* :ref:`ome_template module <ansible_collections.dellemc.openmanage.ome_template_module>` -- Create, modify, deploy, delete, export, import and clone a template on OpenManage Enterprise
* :ref:`ome_template_identity_pool module <ansible_collections.dellemc.openmanage.ome_template_identity_pool_module>` -- Attach or detach an identity pool to a requested template on OpenManage Enterprise
* :ref:`ome_template_info module <ansible_collections.dellemc.openmanage.ome_template_info_module>` -- Retrieves template details from OpenManage Enterprise
* :ref:`ome_template_network_vlan module <ansible_collections.dellemc.openmanage.ome_template_network_vlan_module>` -- Set tagged and untagged vlans to native network card supported by a template on OpenManage Enterprise
* :ref:`ome_template_network_vlan_info module <ansible_collections.dellemc.openmanage.ome_template_network_vlan_info_module>` -- Retrieves network configuration of template.
* :ref:`ome_user module <ansible_collections.dellemc.openmanage.ome_user_module>` -- Create, modify or delete a user on OpenManage Enterprise
* :ref:`ome_user_info module <ansible_collections.dellemc.openmanage.ome_user_info_module>` -- Retrieves details of all accounts or a specific account on OpenManage Enterprise
* :ref:`redfish_event_subscription module <ansible_collections.dellemc.openmanage.redfish_event_subscription_module>` -- Manage Redfish Subscriptions
* :ref:`redfish_firmware module <ansible_collections.dellemc.openmanage.redfish_firmware_module>` -- To perform a component firmware update using the image file available on the local or remote system
* :ref:`redfish_firmware_rollback module <ansible_collections.dellemc.openmanage.redfish_firmware_rollback_module>` -- To perform a component firmware rollback using component name
* :ref:`redfish_powerstate module <ansible_collections.dellemc.openmanage.redfish_powerstate_module>` -- Manage device power state
* :ref:`redfish_storage_volume module <ansible_collections.dellemc.openmanage.redfish_storage_volume_module>` -- Manages the storage volume configuration

.. toctree::
    :maxdepth: 1
    :hidden:

    dellemc_configure_idrac_eventing_module
    dellemc_configure_idrac_services_module
    dellemc_idrac_lc_attributes_module
    dellemc_idrac_storage_volume_module
    dellemc_system_lockdown_mode_module
    idrac_attributes_module
    idrac_bios_module
    idrac_boot_module
    idrac_certificates_module
    idrac_firmware_module
    idrac_firmware_info_module
    idrac_lifecycle_controller_job_status_info_module
    idrac_lifecycle_controller_jobs_module
    idrac_lifecycle_controller_logs_module
    idrac_lifecycle_controller_status_info_module
    idrac_network_module
    idrac_network_attributes_module
    idrac_os_deployment_module
    idrac_redfish_storage_controller_module
    idrac_reset_module
    idrac_server_config_profile_module
    idrac_syslog_module
    idrac_system_info_module
    idrac_timezone_ntp_module
    idrac_user_module
    idrac_user_info_module
    idrac_virtual_media_module
    ome_active_directory_module
    ome_alert_policies_module
    ome_alert_policies_actions_info_module
    ome_alert_policies_category_info_module
    ome_alert_policies_info_module
    ome_alert_policies_message_id_info_module
    ome_application_alerts_smtp_module
    ome_application_alerts_syslog_module
    ome_application_certificate_module
    ome_application_console_preferences_module
    ome_application_network_address_module
    ome_application_network_proxy_module
    ome_application_network_settings_module
    ome_application_network_time_module
    ome_application_network_webserver_module
    ome_application_security_settings_module
    ome_chassis_slots_module
    ome_configuration_compliance_baseline_module
    ome_configuration_compliance_info_module
    ome_device_group_module
    ome_device_info_module
    ome_device_local_access_configuration_module
    ome_device_location_module
    ome_device_mgmt_network_module
    ome_device_network_services_module
    ome_device_power_settings_module
    ome_device_quick_deploy_module
    ome_devices_module
    ome_diagnostics_module
    ome_discovery_module
    ome_domain_user_groups_module
    ome_firmware_module
    ome_firmware_baseline_module
    ome_firmware_baseline_compliance_info_module
    ome_firmware_baseline_info_module
    ome_firmware_catalog_module
    ome_groups_module
    ome_identity_pool_module
    ome_job_info_module
    ome_network_port_breakout_module
    ome_network_vlan_module
    ome_network_vlan_info_module
    ome_powerstate_module
    ome_profile_module
    ome_profile_info_module
    ome_server_interface_profile_info_module
    ome_server_interface_profiles_module
    ome_smart_fabric_module
    ome_smart_fabric_info_module
    ome_smart_fabric_uplink_module
    ome_smart_fabric_uplink_info_module
    ome_template_module
    ome_template_identity_pool_module
    ome_template_info_module
    ome_template_network_vlan_module
    ome_template_network_vlan_info_module
    ome_user_module
    ome_user_info_module
    redfish_event_subscription_module
    redfish_firmware_module
    redfish_firmware_rollback_module
    redfish_powerstate_module
    redfish_storage_volume_module


Inventory Plugins
~~~~~~~~~~~~~~~~~

* :ref:`ome_inventory inventory <ansible_collections.dellemc.openmanage.ome_inventory_inventory>` -- Group inventory plugin on OpenManage Enterprise.

.. toctree::
    :maxdepth: 1
    :hidden:

    ome_inventory_inventory


Role Index
----------

These are the roles in the dellemc.openmanage collection:

* :ref:`idrac_attributes role <ansible_collections.dellemc.openmanage.idrac_attributes_role>` -- Role to configure the iDRAC attribute
* :ref:`idrac_bios role <ansible_collections.dellemc.openmanage.idrac_bios_role>` -- Modify and clear BIOS attributes, and reset BIOS settings
* :ref:`idrac_boot role <ansible_collections.dellemc.openmanage.idrac_boot_role>` -- Configure the boot order settings
* :ref:`idrac_certificate role <ansible_collections.dellemc.openmanage.idrac_certificate_role>` -- This role allows to generate certificate signing request, import, and export certificates on iDRAC
* :ref:`idrac_export_server_config_profile role <ansible_collections.dellemc.openmanage.idrac_export_server_config_profile_role>` -- Role to export iDRAC Server Configuration Profile (SCP)
* :ref:`idrac_firmware role <ansible_collections.dellemc.openmanage.idrac_firmware_role>` -- Firmware update from a repository on a network share (CIFS, NFS, HTTP, HTTPS, FTP)
* :ref:`idrac_gather_facts role <ansible_collections.dellemc.openmanage.idrac_gather_facts_role>` -- Role to get the facts from the iDRAC Server
* :ref:`idrac_import_server_config_profile role <ansible_collections.dellemc.openmanage.idrac_import_server_config_profile_role>` -- Import iDRAC Server Configuration Profile (SCP)
* :ref:`idrac_job_queue role <ansible_collections.dellemc.openmanage.idrac_job_queue_role>` -- Role to manage the iDRAC lifecycle controller job queue.
* :ref:`idrac_os_deployment role <ansible_collections.dellemc.openmanage.idrac_os_deployment_role>` -- Role to deploy operating system on the iDRAC servers
* :ref:`idrac_reset role <ansible_collections.dellemc.openmanage.idrac_reset_role>` -- Role to reset and restart iDRAC
* :ref:`idrac_server_powerstate role <ansible_collections.dellemc.openmanage.idrac_server_powerstate_role>` -- Role to manage the different power states of the specified device
* :ref:`idrac_storage_controller role <ansible_collections.dellemc.openmanage.idrac_storage_controller_role>` -- Configures the physical disk, virtual disk, and storage controller settings
* :ref:`redfish_firmware role <ansible_collections.dellemc.openmanage.redfish_firmware_role>` -- Update a component firmware using the image file available on the local or remote system
* :ref:`redfish_storage_volume role <ansible_collections.dellemc.openmanage.redfish_storage_volume_role>` -- Role to manage the storage volume configuration

.. toctree::
    :maxdepth: 1
    :hidden:

    idrac_attributes_role
    idrac_bios_role
    idrac_boot_role
    idrac_certificate_role
    idrac_export_server_config_profile_role
    idrac_firmware_role
    idrac_gather_facts_role
    idrac_import_server_config_profile_role
    idrac_job_queue_role
    idrac_os_deployment_role
    idrac_reset_role
    idrac_server_powerstate_role
    idrac_storage_controller_role
    redfish_firmware_role
    redfish_storage_volume_role


.. seealso::

    List of :ref:`collections <list_of_collections>` with docs hosted here.
