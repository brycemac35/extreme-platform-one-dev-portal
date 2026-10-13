---
source: https://developer.extremeplatformone.com/api-reference/xiq
spec: https://developer.extremeplatformone.com/api/spec/xiq
title: "ExtremeCloud IQ API"
---

# ExtremeCloud IQ API

**XIQ** · Applications. ExtremeCloud IQ.

ExtremeCloud IQ RESTful API for external and internal applications.

Version: `25.14.1-4`

## Servers

- `https://cloudapi.extremecloudiq.com/xiq/v1` — ExtremeCloud IQ REST API Server

Full OpenAPI document: [`specs/xiq.json`](../../specs/xiq.json)

## Endpoints

693 operations.

| Method | Path | Summary |
| --- | --- | --- |
| PUT | `/v1/account/viq/default-device-password` | Update the default device password in the account (with validation) |
| PUT | `/usergroups/{id}` | Update user group |
| DELETE | `/usergroups/{id}` | Delete user group by ID |
| GET | `/user-profiles/{id}` | Get user profile by ID |
| PUT | `/user-profiles/{id}` | Update user profile |
| DELETE | `/user-profiles/{id}` | Delete an user profile by ID |
| GET | `/tunnel-concentrators/{id}` | Get Tunnel Concentrator by ID |
| PUT | `/tunnel-concentrators/{id}` | Update TunnelConcentrator by ID |
| DELETE | `/tunnel-concentrators/{id}` | Delete TunnelConcentrator by ID |
| GET | `/third-party-api-connection` | List third party api connections |
| PUT | `/third-party-api-connection` | Update a third party api connection |
| DELETE | `/third-party-api-connection` | Delete a third party api connection |
| GET | `/tcap-profiles/{id}` | getTcap |
| PUT | `/tcap-profiles/{id}` | updateTcap |
| DELETE | `/tcap-profiles/{id}` | deleteTcap |
| PUT | `/subscriptions/webhook/{id}` | Update webhook subscription |
| PUT | `/ssids/{id}/psk/password` | Change the SSID PSK password |
| PUT | `/ssids/{id}/mode/wep` | Change the SSID mode to WEP |
| PUT | `/ssids/{id}/mode/psk` | Change the SSID mode to PSK |
| PUT | `/ssids/{id}/mode/ppsk` | Change the SSID mode to PPSK |
| PUT | `/ssids/{id}/mode/open` | Change the SSID mode to open access |
| PUT | `/ssids/{id}/mode/dot1x` | Change the SSID mode to 802.1x |
| GET | `/ssids/advanced-settings/{id}` | Get SSID advanced settings |
| PUT | `/ssids/advanced-settings/{id}` | Update SSID advanced settings |
| GET | `/site/afc/schedule` | getSiteAfcSchedule |
| POST | `/site/afc/schedule` | createSiteAfcSchedule |
| PUT | `/site/afc/schedule` | updateSiteAfcSchedule |
| GET | `/radsec-proxies/{id}` | Get the RADSEC proxy configuration |
| PUT | `/radsec-proxies/{id}` | Update RADSEC proxy configuration |
| DELETE | `/radsec-proxies/{id}` | Delete the RADSEC proxy configuration |
| GET | `/radius-servers/internal/{id}` | Get internal RADIUS server by ID |
| PUT | `/radius-servers/internal/{id}` | Update internal RADIUS server configuration |
| DELETE | `/radius-servers/internal/{id}` | Delete internal RADIUS server configuration |
| GET | `/radius-servers/external/{id}` | Get external RADIUS server by ID |
| PUT | `/radius-servers/external/{id}` | Update external RADIUS server configuration |
| DELETE | `/radius-servers/external/{id}` | Delete external RADIUS server configuration |
| GET | `/radius-proxies/{id}` | Get the RADIUS proxy configuration |
| PUT | `/radius-proxies/{id}` | Update RADIUS proxy configuration |
| DELETE | `/radius-proxies/{id}` | Delete the RADIUS proxy configuration |
| GET | `/radius-client-objects/{id}` | Get RADIUS client object by ID |
| PUT | `/radius-client-objects/{id}` | Update RADIUS client object configuration |
| DELETE | `/radius-client-objects/{id}` | Delete a RADIUS client object configuration |
| GET | `/radio-profiles/{id}` | Get radio profile by ID |
| PUT | `/radio-profiles/{id}` | Update radio profile by ID |
| DELETE | `/radio-profiles/{id}` | Delete radio profile by ID |
| GET | `/radio-profiles/wmm-qos/{id}` | Get Wmm QoS settings |
| PUT | `/radio-profiles/wmm-qos/{id}` | Update Wmm QoS settings |
| GET | `/radio-profiles/sensor-scan/{id}` | Get sensor scan settings |
| PUT | `/radio-profiles/sensor-scan/{id}` | Update sensor scan settings |
| GET | `/radio-profiles/radio-usage-opt/{id}` | Get radio usage optimization settings |
| PUT | `/radio-profiles/radio-usage-opt/{id}` | Update radio usage optimization settings |
| GET | `/radio-profiles/neighborhood-analysis/{id}` | Get neighborhood analysis settings |
| PUT | `/radio-profiles/neighborhood-analysis/{id}` | Update neighborhood analysis settings |
| GET | `/radio-profiles/miscellaneous/{id}` | Get radio miscellaneous settings |
| PUT | `/radio-profiles/miscellaneous/{id}` | Update radio miscellaneous settings |
| GET | `/radio-profiles/mac-ouis/{id}` | Get MAC OUI profile |
| PUT | `/radio-profiles/mac-ouis/{id}` | Update MAC OUI profile |
| DELETE | `/radio-profiles/mac-ouis/{id}` | Delete MAC OUI profile |
| GET | `/radio-profiles/channel-selection/{id}` | Get channel selection settings |
| PUT | `/radio-profiles/channel-selection/{id}` | Update channel selection settings |
| GET | `/pcgs/key-based/network-policy-{policyId}/users` | Get users for a PCG-enabled network policy |
| POST | `/pcgs/key-based/network-policy-{policyId}/users` | [LRO] Add users to a PCG-enabled network policy |
| PUT | `/pcgs/key-based/network-policy-{policyId}/users` | Replace all users in a PCG-enabled network policy |
| DELETE | `/pcgs/key-based/network-policy-{policyId}/users` | Delete users from a PCG-enabled network policy |
| GET | `/ng-reports/scheduled/{reportId}/recipients` | Get Recipients for Report |
| POST | `/ng-reports/scheduled/{reportId}/recipients` | Delete Recipients from Report |
| PUT | `/ng-reports/scheduled/{reportId}/recipients` | Add Recipients to Report |
| GET | `/ng-reports/scheduled/custom/{reportId}` | Get a custom report schedule |
| PUT | `/ng-reports/scheduled/custom/{reportId}` | Update a scheduled custom report |
| GET | `/network-policies/{id}` | Get the network policy |
| PUT | `/network-policies/{id}` | Update the network policy |
| DELETE | `/network-policies/{id}` | Delete the network policy |
| GET | `/mac-object-profiles/{id}` | Get MAC Object by ID |
| PUT | `/mac-object-profiles/{id}` | Update MAC Object by ID |
| DELETE | `/mac-object-profiles/{id}` | Delete a MAC object by ID |
| GET | `/mac-firewall-policies/{id}` | Get MAC Firewall Policy by ID |
| PUT | `/mac-firewall-policies/{id}` | Update MAC Firewall policy by ID |
| DELETE | `/mac-firewall-policies/{id}` | Delete MAC Firewall policy by ID |
| PUT | `/locations/{id}` | Update a location |
| DELETE | `/locations/{id}` | Delete a location by ID |
| PUT | `/locations/wall/type/{id}` | Update a wall type |
| DELETE | `/locations/wall/type/{id}` | Delete a wall type |
| GET | `/locations/site/{id}` | Get a site by ID |
| PUT | `/locations/site/{id}` | Update a site by ID |
| DELETE | `/locations/site/{id}` | Delete a site by ID |
| POST | `/locations/folder/zones` | Create a zone |
| PUT | `/locations/folder/zones` | Update zones in folder |
| GET | `/locations/floor/{id}` | Get a floor by ID |
| PUT | `/locations/floor/{id}` | Update a floor |
| DELETE | `/locations/floor/{id}` | Delete a floor by ID |
| GET | `/locations/floor/{floorId}/walls` | List all walls on a floor |
| PUT | `/locations/floor/{floorId}/walls` | Save walls on a floor |
| GET | `/locations/floor/{floorId}/label` | Find all floor map labels referencing the floor |
| POST | `/locations/floor/{floorId}/label` | Creates one floor map label. |
| PUT | `/locations/floor/{floorId}/label` | Updates one floor map label. |
| PUT | `/locations/floor/bulk/label` | Updates one ore more floor map labels. |
| GET | `/locations/building/{id}` | Get a building by ID |
| PUT | `/locations/building/{id}` | Update a building |
| DELETE | `/locations/building/{id}` | Delete a building by ID |
| GET | `/ldap-servers/{id}` | Get LDAP server by ID |
| PUT | `/ldap-servers/{id}` | Update LDAP server configuration |
| DELETE | `/ldap-servers/{id}` | Delete a LDAP server |
| GET | `/l3-address-profiles/{id}` | Get a L3 address profile by ID |
| PUT | `/l3-address-profiles/{id}` | Update a L3 address profile |
| DELETE | `/l3-address-profiles/{id}` | Delete a L3 address profile by ID |
| GET | `/ip-firewall-policies/{id}` | Get IP Firewall Policy by ID |
| PUT | `/ip-firewall-policies/{id}` | Update IP Firewall policy by ID |
| DELETE | `/ip-firewall-policies/{id}` | Delete IP Firewall policy by ID |
| GET | `/iot-profiles/{id}` | Get IoT profile by ID |
| PUT | `/iot-profiles/{id}` | Update IoT profile by ID |
| DELETE | `/iot-profiles/{id}` | Delete IoT profile by ID |
| GET | `/hotspot-service-provider-profiles/{id}` | Get Hotspot Service Provider profile by ID |
| PUT | `/hotspot-service-provider-profiles/{id}` | Update Hotspot Service Provider profile by ID |
| DELETE | `/hotspot-service-provider-profiles/{id}` | Delete Hotspot Service Provider profile by ID |
| GET | `/hotspot-profiles/{id}` | Get Hotspot profile by ID |
| PUT | `/hotspot-profiles/{id}` | Update Hotspot profile by ID |
| DELETE | `/hotspot-profiles/{id}` | Delete Hotspot profile by ID |
| GET | `/hiq/context` | Get HIQ context |
| PUT | `/hiq/context` | Set HIQ context |
| GET | `/hiq/context/reading` | Get organizations for reading data |
| PUT | `/hiq/context/reading` | Set organizations for reading data |
| GET | `/hiq/context/creating` | Get organization for creating new data |
| PUT | `/hiq/context/creating` | Set organization for creating new data |
| GET | `/floor/afc/details` | AFC Related Floor Height and Accuracy data |
| POST | `/floor/afc/details` | AFC Related Floor and AP Height and Accuracy data |
| PUT | `/floor/afc/details` | AFC Related Floor and AP Height and Accuracy data |
| PUT | `/endusers/{id}` | Update an end user |
| DELETE | `/endusers/{id}` | Delete end user by ID |
| PUT | `/devices/{id}/visible` | Update the visible status of a device in a floor |
| GET | `/devices/{id}/radio-operating-mode` | Get the device radio operating mode |
| PUT | `/devices/{id}/radio-operating-mode` | Configure radio operating mode of a device |
| GET | `/devices/{id}/network-policy` | Get network policy for a device |
| PUT | `/devices/{id}/network-policy` | Assign network policy to a device |
| DELETE | `/devices/{id}/network-policy` | Revoke network policy for a device |
| PUT | `/devices/{id}/mobileapp/gps` | Update AP GPS settings |
| GET | `/devices/{id}/location` | Get location for a device |
| PUT | `/devices/{id}/location` | Assign location to a device |
| DELETE | `/devices/{id}/location` | Revoke location for a device |
| PUT | `/devices/{id}/hostname` | Change hostname for a device |
| GET | `/devices/{id}/ftm-settings` | Get FTM Settings by device ID |
| PUT | `/devices/{id}/ftm-settings` | Configure (create / update) device FTM Settings |
| DELETE | `/devices/{id}/ftm-settings` | Delete FTM Settings by device ID |
| PUT | `/devices/{id}/description` | Change description for a device |
| GET | `/devices/{id}/client-monitor` | Get client monitor setting for a device |
| PUT | `/devices/{id}/client-monitor` | Assign client monitor setting to a device |
| DELETE | `/devices/{id}/client-monitor` | Revoke client monitor setting for a device |
| PUT | `/devices/radius-proxy/:assign` | Assign RADIUS proxy to devices |
| PUT | `/devices/ibeacon` | Change iBeacon settings for devices |
| GET | `/deployments/{deploymentId}` | Get deployment details by Id |
| PUT | `/deployments/{deploymentId}` | Update schedule with deployment ID |
| DELETE | `/deployments/{deploymentId}` | Delete the deployment schedule by ID |
| PUT | `/credential-distribution-groups/{id}` | Update Credential Distribution Group by ID |
| PUT | `/copilot/anomalies/update-device-action` | [LRO] Update Anomalies and Devices |
| PUT | `/copilot/anomalies/update-action` | updateAnomalyAction |
| PUT | `/copilot/anomalies/devices/update-action` | updateAnomalyDeviceAction |
| PUT | `/copilot/anomalies/devices/feedback` | updateAnomaliesFeedback |
| PUT | `/clients/alias` | Set the aliases for multiple clients |
| GET | `/client-monitor-profiles/{id}` | Get client monitor profile by ID |
| PUT | `/client-monitor-profiles/{id}` | Update client monitor profile |
| DELETE | `/client-monitor-profiles/{id}` | Delete an client monitor profile by ID |
| GET | `/classification-rules/{id}` | Get a classification rule by ID |
| PUT | `/classification-rules/{id}` | Update classification rule |
| DELETE | `/classification-rules/{id}` | Delete classification rule by ID |
| GET | `/certificate-bundles/{id}` | Get Certificate Bundle by ID |
| PUT | `/certificate-bundles/{id}` | Update Certificate Bundle by ID |
| DELETE | `/certificate-bundles/{id}` | Delete Certificate Bundle by ID |
| GET | `/ccgs/{id}` | Get a cloud config group |
| PUT | `/ccgs/{id}` | Update cloud config group information |
| DELETE | `/ccgs/{id}` | Delete a cloud config group |
| GET | `/alert-subscriptions/webhooks/{id}` | Get alert webhook subscription |
| PUT | `/alert-subscriptions/webhooks/{id}` | Update alert webhook subscription |
| DELETE | `/alert-subscriptions/webhooks/{id}` | Delete alert webhook subscription |
| GET | `/alert-subscriptions/servicenow/{id}` | Get a specific ServiceNow subscription |
| PUT | `/alert-subscriptions/servicenow/{id}` | Update ServiceNow subscription |
| PATCH | `/alert-subscriptions/servicenow/{id}` | Partial or full update ServiceNow subscription |
| GET | `/alert-subscriptions/emails/{id}` | Get alert email subscription |
| PUT | `/alert-subscriptions/emails/{id}` | Update alert email subscription |
| DELETE | `/alert-subscriptions/emails/{id}` | Delete alert email subscription |
| GET | `/alert-policies/{policyId}/rules/{ruleId}` | Get details of an alert rule |
| PUT | `/alert-policies/{policyId}/rules/{ruleId}` | Update an alert rule |
| GET | `/alert-policies/{id}` | Get details of an alert policy |
| PUT | `/alert-policies/{id}` | Update a site-based alert policy |
| DELETE | `/alert-policies/{id}` | Delete a site-based alert policy |
| GET | `/account/viq/default-device-password` | Get the default device password in the account |
| PUT | `/account/viq/default-device-password` | Update the default device password in the account |
| PUT | `/account/vhm/setting/{id}` | Update Vhm Setting |
| GET | `/vlan-profiles` | List VLAN profiles |
| POST | `/vlan-profiles` | Create VLAN profile |
| POST | `/vlan-profiles/:delete` | [LRO] Delete VLAN profiles |
| GET | `/users` | List all users |
| POST | `/users` | Create new user |
| POST | `/users/type-distribution` | Get user type distribution |
| POST | `/users/grid` | List Users |
| POST | `/users/grid-export` | Export the Users grid data |
| POST | `/users/filter-metadata` | List user grid filter metadata |
| GET | `/users/external` | List external access users |
| POST | `/users/external` | Grant external access |
| POST | `/users/data-usage` | Get user data usage |
| GET | `/usergroups` | List user groups |
| POST | `/usergroups` | Create user group |
| GET | `/user-profiles` | List user profiles |
| POST | `/user-profiles` | Create a user profile |
| POST | `/user-profiles/{id}/mac-firewall-policies/:detach` | Detach MAC Firewall Policy from an User Profile |
| POST | `/user-profiles/{id}/mac-firewall-policies/:attach` | Attach MAC Firewall Policy to an User Profile |
| POST | `/user-profiles/{id}/ip-firewall-policies/:detach` | Detach IP Firewall Policy from an User Profile |
| POST | `/user-profiles/{id}/ip-firewall-policies/:attach` | Attach IP Firewall Policy to an User Profile |
| GET | `/user-profile-assignments` | List user profile assignments |
| POST | `/user-profile-assignments` | Create a user profile assignment |
| POST | `/user-folder-preferences/{folderId}` | Save user folder preferences values. |
| GET | `/tunnel-concentrators` | List Tunnel Concentrators |
| POST | `/tunnel-concentrators` | Create a Tunnel Concentrator |
| POST | `/tunnel-concentrators/{id}/license/upload` | Upload Tunnel Concentrator license |
| GET | `/tcap-profiles` | List TCAPs |
| POST | `/tcap-profiles` | createTcap |
| POST | `/switch-inspector/diagnostics` | Switch Inspector Panel Diagnostics |
| GET | `/subscriptions/webhook` | List webhook subscriptions |
| POST | `/subscriptions/webhook` | Create webhook subscriptions |
| POST | `/ssids/{id}/user-profile/:attach` | Attach user profile to an SSID |
| POST | `/ssids/{id}/user-profile-assignment/:attach` | Attach user profile assignment to an SSID |
| POST | `/ssids/{id}/radius-server-group/:attach` | Attach radius server group to an SSID |
| POST | `/ssids/{id}/radius-client-profile/:attach` | Attach RADIUS client profile to an SSID |
| POST | `/ssids/{id}/cwp/:enable` | Enable and attach the CWP on the SSID |
| POST | `/ssids/{id}/cwp/:disable` | Disable the CWP on the SSID |
| POST | `/ssids/{id}/cwp/:attach` | Attach CWP to an SSID |
| POST | `/ssids/{id}/client-monitor-profile/:attach` | Attach client monitor profile to an SSID |
| POST | `/ssids/{id}/:rename` | Rename SSID (Wireless name) |
| POST | `/site/spectrum` | getAfcSpectrumPerSite |
| POST | `/rtts` | Create |
| POST | `/rtts/supported-devices` | List RTTS supported devices |
| GET | `/radsec-proxies` | List RADSEC proxies |
| POST | `/radsec-proxies` | Create RADSEC proxy configuration |
| GET | `/radius-servers/internal` | List all internal RADIUS servers |
| POST | `/radius-servers/internal` | Create internal RADIUS server configuration |
| DELETE | `/radius-servers/internal` | [LRO] Delete internal RADIUS server configuration |
| GET | `/radius-servers/external` | List external RADIUS servers |
| POST | `/radius-servers/external` | Create external RADIUS server configuration |
| GET | `/radius-proxies` | List RADIUS proxies |
| POST | `/radius-proxies` | Create RADIUS proxy configuration |
| GET | `/radius-client-objects` | List RADIUS client objects |
| POST | `/radius-client-objects` | Create RADIUS client object configuration |
| GET | `/radio-profiles` | List radio profiles |
| POST | `/radio-profiles` | Create a radio profile |
| GET | `/radio-profiles/mac-ouis` | List MAC OUI profiles |
| POST | `/radio-profiles/mac-ouis` | Create a MAC OUI profile |
| GET | `/pcgs/key-based` | List Key-based Private Client Groups |
| POST | `/pcgs/key-based` | [LRO] Create a Key-based Private Client Group |
| GET | `/pcgs/key-based/network-policy-{policyId}/port-assignments` | Get device port assignments in network policy |
| POST | `/pcgs/key-based/network-policy-{policyId}/port-assignments` | Assign ports to devices in network policy |
| POST | `/pcgs/key-based/network-policy-{policyId}/keys/:generate` | Generate shared keys for users in network policy |
| POST | `/pcgs/key-based/network-policy-{policyId}/keys/:email` | Send keys to users in network policy via Email |
| POST | `/pcgs/key-based/network-policy-{policyId}/:onboard` | [LRO] Onboard Key-based PCG in network policy |
| GET | `/packetcaptures` | List packet capture sessions |
| POST | `/packetcaptures` | Create a new packet capture session |
| DELETE | `/packetcaptures` | Delete packet capture sessions |
| POST | `/packetcaptures/{id}/:upload` | Upload a packet capture session's capture files |
| POST | `/packetcaptures/{id}/:stop` | Stop a packet capture session |
| POST | `/operations/{operationId}/:cancel` | Cancel Long-Running Operation (LRO) |
| POST | `/ng-reports/timeseries` | Get QoE Diagnostics Time Series Data |
| POST | `/ng-reports/tabledata` | Get QoE Diagnostics Table Data |
| GET | `/ng-reports/scheduled/custom` | List Custom Report Schedules |
| POST | `/ng-reports/scheduled/custom` | Create a scheduled custom report |
| DELETE | `/ng-reports/scheduled/custom` | Delete scheduled custom reports |
| POST | `/ng-reports/metadata/user` | List of Users for filtering |
| POST | `/ng-reports/metadata/ssids` | List of SSIDs for filtering |
| POST | `/ng-reports/metadata/os` | List of OS for filtering |
| POST | `/ng-reports/metadata/device` | List of Devices for filtering |
| POST | `/ng-reports/metadata/client` | List of Clients for filtering |
| POST | `/ng-reports/metadata/bands` | List of Band for filtering |
| POST | `/ng-reports/metadata/application` | List of Applications for filtering |
| POST | `/ng-reports/downloads/reports` | Download the Reports |
| GET | `/network-services` | List Network Services |
| POST | `/network-services` | Create Network Services |
| GET | `/network-policies` | List network policies |
| POST | `/network-policies` | Create network policy |
| POST | `/network-policies/{id}/ssids/:remove` | Removes SSIDs from the network policy |
| POST | `/network-policies/{id}/ssids/:add` | Add SSIDs to a network policy |
| GET | `/mac-object-profiles` | List mac object profiles |
| POST | `/mac-object-profiles` | Create a mac object |
| GET | `/mac-firewall-policies` | List MAC Firewall policies |
| POST | `/mac-firewall-policies` | Create MAC Firewall policy |
| POST | `/mac-firewall-policies/{id}/mac-firewall-rule/:detach` | Detach MAC Firewall Rule from MAC Firewall policy |
| POST | `/mac-firewall-policies/{id}/mac-firewall-rule/:attach` | Attach MAC Firewall Rule to MAC Firewall policy |
| POST | `/logs/audit/reports` | [LRO] Create audit logs report |
| POST | `/logout` | User logout (Revoke the current access token) |
| POST | `/login` | User login with username and password |
| POST | `/locations` | Create a location |
| GET | `/locations/wall/type` | Get wall types |
| POST | `/locations/wall/type` | Create a wall type |
| GET | `/locations/site` | List sites |
| POST | `/locations/site` | Create a site |
| POST | `/locations/import/ekahau` | [LRO] Import one or more floors from an Ekahau archive |
| POST | `/locations/floorplan` | Upload floorplan |
| GET | `/locations/floor` | List floors |
| POST | `/locations/floor` | Create a floor |
| GET | `/locations/building` | List buildings |
| POST | `/locations/building` | Create a building |
| POST | `/locations/:init` | Initialize organization location |
| GET | `/ldap-servers` | List LDAP servers |
| POST | `/ldap-servers` | Create LDAP server |
| GET | `/l3-address-profiles` | List L3 address profiles |
| POST | `/l3-address-profiles` | Create a L3 address profile |
| GET | `/ip-firewall-policies` | List IP Firewall policies |
| POST | `/ip-firewall-policies` | Create IP Firewall policy |
| POST | `/ip-firewall-policies/{id}/ip-firewall-rule/:detach` | Detach IP Firewall Rule from IP Firewall policy |
| POST | `/ip-firewall-policies/{id}/ip-firewall-rule/:attach` | Attach IP Firewall Rule to IP Firewall policy |
| GET | `/iot-profiles` | List IoT profiles |
| POST | `/iot-profiles` | Create a IoT profile |
| GET | `/hotspot-service-provider-profiles` | List Hotspot Service Provider profiles |
| POST | `/hotspot-service-provider-profiles` | Create a Hotspot Service Provider profile |
| GET | `/hotspot-profiles` | List Hotspot profiles |
| POST | `/hotspot-profiles` | Create a Hotspot profile |
| GET | `/hiq/organizations` | List all organizations |
| POST | `/hiq/organizations` | Create a new organization |
| POST | `/hiq/organizations/{id}/:rename` | Rename an existing organization |
| GET | `/endusers` | List end users |
| POST | `/endusers` | Create an end user |
| POST | `/endusers/{id}/:regenerate-password` | Regenerate a new password for the end user |
| POST | `/endusers/client/unlock` | Unlock locked clients |
| POST | `/devices/{id}/thread/commissioner/:stop` | Stop Thread Commissioner |
| POST | `/devices/{id}/thread/commissioner/:start` | Start Thread Commissioner |
| POST | `/devices/{id}/ssid/status/:change` | Enable or disable SSID for a device |
| POST | `/devices/{id}/ssid/:override` | Override SSID for a device |
| POST | `/devices/{id}/monitor/:refresh` | Monitor refresh a device |
| POST | `/devices/{id}/iot/:enable` | Enable IoT Wireless Interface settings on device |
| POST | `/devices/{id}/iot/:disable` | Disable IoT Wireless Interface settings on device |
| POST | `/devices/{id}/bounce-port` | Bounce port of a device (EXOS, VOSS and SR Switches |
| POST | `/devices/{id}/:unmanage` | Change admin state to 'Unmanaged' for a device |
| POST | `/devices/{id}/:reset` | [LRO] Reset a device to factory default |
| POST | `/devices/{id}/:reboot` | Reboot a device |
| POST | `/devices/{id}/:manage` | Change admin state to 'Managed' for a device |
| POST | `/devices/{id}/:cli` | Send CLI to a device |
| POST | `/devices/validate-device-action` | validate device action metadata |
| POST | `/devices/thread/commissioner/stop` | Stop Thread Commissioner by Buildings |
| POST | `/devices/thread/commissioner/start` | Start Thread Commissioner by Buildings |
| POST | `/devices/rm-devices-page` | [LRO] RM Device Page |
| POST | `/devices/rm-devices-page/export` | [LRO] Export RM devices data to CSV |
| POST | `/devices/rm-devices-metadata` | Get Device List Metadata |
| POST | `/devices/rm-devices-connection-status` | Get Device Connection Status |
| POST | `/devices/os/:change` | Change device OS mode |
| POST | `/devices/network-policy/:revoke` | Revoke network policy for multiple devices |
| POST | `/devices/network-policy/:query` | Query network policy for multiple devices |
| POST | `/devices/network-policy/:assign` | Assign network policy to multiple devices |
| POST | `/devices/location/:revoke` | Revoke location for multiple devices |
| POST | `/devices/location/:query` | Query location for multiple devices |
| POST | `/devices/location/:assign` | Assign location to multiple devices |
| POST | `/devices/country-code/:assign` | Assign a country code to devices |
| POST | `/devices/client-monitor/:revoke` | Revoke client monitor setting for multiple devices |
| POST | `/devices/client-monitor/:query` | Query client monitor setting for multiple devices |
| POST | `/devices/client-monitor/:assign` | Assign client monitor setting to multiple devices |
| POST | `/devices/anchor/revoke` | Revoke Anchor capability for multiple devices |
| POST | `/devices/anchor/assign` | Assign AP5050 devices as Anchor devices |
| POST | `/devices/actions-support-metadata` | Get Actions Support metadata |
| POST | `/devices/:unmanage` | Change status to Unmanaged |
| POST | `/devices/:ssh-active-sessions` | List SSH active sessions |
| POST | `/devices/:reset` | [LRO] Reset devices to factory default |
| POST | `/devices/:reboot` | Reboot devices |
| POST | `/devices/:onboard` | Onboard Devices |
| POST | `/devices/:manage` | Change status to Managed |
| POST | `/devices/:delete` | Delete devices |
| POST | `/devices/:cli` | [LRO] Send CLI to devices |
| POST | `/devices/:check-ownership` | Check caller is allowed to access the device |
| POST | `/devices/:advanced-onboard` | [LRO] Advanced Onboard Devices |
| GET | `/deployments` | Get list of deployments |
| POST | `/deployments` | [LRO] Push configuration and upgrade firmware |
| POST | `/deployments/firmware-metadatas` | Get device firmware metadatas |
| POST | `/dashboard/wireless/usage-capacity/grid` | Wireless usage & capacity grid |
| POST | `/dashboard/wireless/usage-capacity/export` | Export all Wireless Usage Capacity Data to CSV |
| POST | `/dashboard/wireless/usage-capacity/excessive-utilization` | Count of APs with excessive utilization |
| POST | `/dashboard/wireless/usage-capacity/excessive-retries` | Count of APs with excessive retries |
| POST | `/dashboard/wireless/usage-capacity/excessive-packet-loss` | Count of APs with excessive packet loss |
| POST | `/dashboard/wireless/device-health/summary` | Device health summary for wireless devices |
| POST | `/dashboard/wireless/device-health/issues/poe-usage-issues` | PoE usage issues for wireless devices |
| POST | `/dashboard/wireless/device-health/issues/memory-usage-issues` | Memory usage issues for wireless devices |
| POST | `/dashboard/wireless/device-health/issues/cpu-usage-issues` | CPU usage issues for wireless devices |
| POST | `/dashboard/wireless/device-health/grid` | Wireless device health grid |
| POST | `/dashboard/wireless/device-health/export` | Export all Wireless Device Health Data to CSV |
| GET | `/dashboard/wireless/dashboard/criteria` | Criteria for Wireless Diagnostics Dashboard |
| POST | `/dashboard/wireless/client-health/roaming-issues` | Wireless clients count with roaming issues |
| POST | `/dashboard/wireless/client-health/issue/roaming` | Roaming issue for wireless client |
| POST | `/dashboard/wireless/client-health/issue/ipaddress` | Ip Address issue for Wireless client |
| POST | `/dashboard/wireless/client-health/issue/authentication` | Authentication issue for wireless client |
| POST | `/dashboard/wireless/client-health/issue/association` | Association issue for wireless client |
| POST | `/dashboard/wireless/client-health/grid` | Wireless client health grid |
| POST | `/dashboard/wireless/client-health/frequency-distribution` | Wireless clients count with frequency distribution |
| POST | `/dashboard/wireless/client-health/filter-metadata` | Filter Metadata for Wireless Client Health Grid |
| POST | `/dashboard/wireless/client-health/export` | Export all Client Health Data to CSV |
| POST | `/dashboard/wireless/client-health/connectivity-issues` | Wireless clients count with connectivity issues |
| POST | `/dashboard/wired/usage-capacity/wired-throughput` | Wired devices throughput |
| POST | `/dashboard/wired/usage-capacity/wired-congestion` | Wired devices congestion |
| POST | `/dashboard/wired/usage-capacity/usage-utilization` | Wired devices total utilized bandwidth |
| POST | `/dashboard/wired/usage-capacity/grid` | Wired Usage and Capacity grid |
| POST | `/dashboard/wired/device-health/temperature-status` | Wired Device Health Temperature Status |
| POST | `/dashboard/wired/device-health/temperature-issues` | Wired Device Health Temperature Issues |
| POST | `/dashboard/wired/device-health/summary` | Wired Device Health Summary |
| POST | `/dashboard/wired/device-health/psu-status` | Wired Device Health PSU Status |
| POST | `/dashboard/wired/device-health/psu-issues` | Wired Device Health PSU Issues |
| POST | `/dashboard/wired/device-health/poe-usage-status` | Wired Device Health PoE Usage Status |
| POST | `/dashboard/wired/device-health/poe-usage-issues` | Wired Device Health PoE Usage Issues |
| POST | `/dashboard/wired/device-health/memory-usage-issues` | Wired Device Health Memory Usage Issues |
| POST | `/dashboard/wired/device-health/grid` | Wired Device Health Grid |
| POST | `/dashboard/wired/device-health/fan-status` | Wired Device Health Fan Status |
| POST | `/dashboard/wired/device-health/fan-issues` | Wired Device Health Fan Issues |
| POST | `/dashboard/wired/device-health/cpu-usage-issues` | Wired Device Health CPU Usage Issues |
| POST | `/dashboard/wired/client-health/traffic-anomalies` | Wired clients count with traffic anomalies |
| POST | `/dashboard/wired/client-health/port-errors` | Wired clients count with port errors |
| POST | `/dashboard/wired/client-health/port-congestion` | Wired clients count with port congestion issues |
| POST | `/dashboard/wired/client-health/ip-connectivity-issues` | Wired clients count with IP connectivity issues |
| POST | `/dashboard/wired/client-health/grid` | Wired client health grid |
| POST | `/dashboard/usage-capacity` | Usage & capacity statistics |
| POST | `/dashboard/sites-with-issues` | Sites with issues |
| POST | `/dashboard/export` | Export all dashboard data to CSV |
| POST | `/dashboard/devices` | Device health statistics |
| POST | `/dashboard/clients` | Client health statistics |
| POST | `/dashboard/assets` | Asset statistics |
| POST | `/dashboard/alerts` | Alert statistics |
| POST | `/d360/wireless/surrounding-aps` | Get a list of SurroundingAps |
| POST | `/d360/client/grid` | Get Client Grid |
| POST | `/d360/client/graph` | List a list of connected clients for Device 360 API |
| GET | `/credential-distribution-groups` | List Credential Distribution Groups |
| POST | `/credential-distribution-groups` | Create a Credential Distribution Group |
| DELETE | `/credential-distribution-groups` | Delete Credential Distribution Group by ID |
| POST | `/copilot/anomalies/exclude-vlans` | updateMissingVlanExcludedVlanList |
| POST | `/copilot/anomalies/exclude-vlans-csv` | updateMissingVlanExcludedVlanCsv |
| POST | `/clients/disconnect` | Disconnect the clients |
| GET | `/client-monitor-profiles` | List client monitor profiles |
| POST | `/client-monitor-profiles` | Create a client monitor profile |
| GET | `/classification-rules` | List classification rules |
| POST | `/classification-rules` | Create classification rule |
| POST | `/certificates/import` | Import Certificate |
| GET | `/certificate-bundles` | List Certificate Bundles |
| POST | `/certificate-bundles` | Create a Certificate Bundle |
| GET | `/ccgs` | [LRO] List clould config groups |
| POST | `/ccgs` | Create new cloud config group |
| POST | `/backup/history/:restore` | Backup History Restore |
| POST | `/auth/permissions/:check` | Check permissions |
| POST | `/auth/apitoken` | Generate new API token |
| POST | `/auth/apitoken/:validate` | Validate API token |
| POST | `/aps/afc/update` | Manual Spectrum request for device(s) |
| GET | `/aps/afc/query` | Get AFC APs Summary Data |
| POST | `/aps/afc/query` | Get AFC APs Summary Data |
| POST | `/applications/usage/summary` | List the application usage summary |
| POST | `/applications/usage/summary/export` | Export the application usage summary |
| POST | `/ap/spectrum` | getAfcSpectrumPerAp |
| POST | `/alerts/reports` | [LRO] Create the alerts report |
| POST | `/alerts/:acknowledge` | Acknowledge the alerts |
| GET | `/alert-subscriptions/webhooks` | List alert webhook subscriptions |
| POST | `/alert-subscriptions/webhooks` | Create alert webhook subscription |
| POST | `/alert-subscriptions/webhooks/:delete` | Delete alert webhook subscription in bulk |
| GET | `/alert-subscriptions/servicenow` | List ServiceNow subscriptions |
| POST | `/alert-subscriptions/servicenow` | Create ServiceNow subscription |
| POST | `/alert-subscriptions/servicenow/:delete` | Delete alert ServiceNow subscription in bulk |
| GET | `/alert-subscriptions/emails` | List alert email subscriptions |
| POST | `/alert-subscriptions/emails` | Create alert email subscription |
| POST | `/alert-subscriptions/emails/{id}/:verify` | Email Verification |
| POST | `/alert-subscriptions/emails/:delete` | Delete alert email subscription in bulk |
| GET | `/alert-policies` | List all alert policies |
| POST | `/alert-policies` | Create a site based alert policy |
| POST | `/alert-policies/{policyId}/rules/{ruleId}/:enable` | Enable a rule from an alert policy |
| POST | `/alert-policies/{policyId}/rules/{ruleId}/:disable` | Disable a rule from an alert policy |
| POST | `/airrm/ap/radioInfo/` | Get Devices Radio Information |
| POST | `/afc/rm-devices-page` | [LRO] RM AFC Device Page |
| POST | `/afc/recalculateSite/{id}` | recalculateSite |
| POST | `/afc/mobileapp/apcandidates` | List of AP candidates that may be used as anchors |
| POST | `/afc/filter-metadata` | RM AFC Device Metadata Page |
| POST | `/afc/export` | [LRO] RM AFC Device export |
| POST | `/afc/aps/reportFtm` | requestAfcFtmData |
| GET | `/acct-api-token` | List API Access tokens |
| POST | `/acct-api-token` | Create an API Access token |
| POST | `/account/viq/import` | [LRO] Import VIQ data |
| POST | `/account/viq/export` | [LRO] Export VIQ data |
| POST | `/account/viq/:reset` | Reset VIQ |
| POST | `/account/viq/:backup` | Backup VIQ |
| POST | `/account/:switch` | Switch to another ExtremeCloud IQ account |
| GET | `/vlan-profiles/{id}` | Get a VLAN profile |
| PATCH | `/vlan-profiles/{id}` | Update a VLAN profile |
| DELETE | `/vlan-profiles/{id}` | Delete a VLAN profile |
| GET | `/users/{id}` | Get user info by ID |
| PATCH | `/users/{id}` | Update user info |
| DELETE | `/users/{id}` | Delete user by ID |
| GET | `/users/external/{id}` | Get external access info |
| PATCH | `/users/external/{id}` | Update external access info |
| DELETE | `/users/external/{id}` | Revoke external access |
| PATCH | `/ng-reports/scheduled/{reportScheduleId}` | Enable or Disable Report Schedule |
| PATCH | `/acct-api-token/{id}` | Update API Access token by ID |
| DELETE | `/acct-api-token/{id}` | Delete API Access token by ID |
| GET | `/users/reports/{id}` | Download the report |
| GET | `/users/me` | Get current user info |
| GET | `/usergroups/:unique` | List unique user group names |
| GET | `/user-profile-assignments/{id}` | Get user profile assignment by ID |
| DELETE | `/user-profile-assignments/{id}` | Delete an user profile assignment by ID |
| GET | `/user-folder-preferences` | Query user folder preferences |
| GET | `/ucp/{id}/engines/installed` | Get UCP Engines by ID |
| GET | `/tunnel-concentrators/{id}/license` | Get Tunnel Concentrator license status |
| GET | `/thread/topology` | Get thread network topology |
| GET | `/thread/routers` | List thread routers |
| GET | `/thread/networks` | Get active thread networks |
| GET | `/subscriptions/webhook/export` | Export all webhook subscriptions to CSV |
| GET | `/ssids` | List SSIDs |
| GET | `/sms-templates` | List SMS templates |
| GET | `/radius-servers/internal/devices` | List all internal RADIUS devices |
| GET | `/radius-proxies/devices` | List Radius proxy devices |
| GET | `/radio-operating-modes/{productType}` | Get Radio Operating Modes by product type |
| GET | `/packetcaptures/{id}` | Get a packet capture session |
| DELETE | `/packetcaptures/{id}` | Delete a packet capture session |
| GET | `/packetcaptures/files` | Get an AP packet capture file |
| GET | `/operations/{operationId}` | Get Long-Running Operation (LRO) status and result |
| DELETE | `/operations/{operationId}` | Delete Long-Running Operation (LRO) |
| GET | `/ng-reports/scheduled/runs/{reportRunId}/recipients` | Get Recipients for Report Run |
| GET | `/ng-reports/scheduled/reports/download` | Download or Preview Scheduled Report File |
| GET | `/ng-reports/scheduled/pci-compliance` | Get PCI Compliance Reports |
| GET | `/ng-reports/scheduled/network-summary` | Get Network Summary Reports |
| GET | `/ng-reports/scheduled/custom/{reportScheduleId}/runs` | Get report runs for a schedule |
| GET | `/ng-reports/information` | Information about QoE-Diagnostics Metrics |
| GET | `/ng-reports/information/{metrics}` | Information about QoE-Diagnostics Metrics |
| GET | `/ng-reports/download/reports/{id}` | Download the Reports by ID |
| GET | `/network-scorecard/wifiHealth/{locationId}` | Get the overall wifi health score |
| GET | `/network-scorecard/servicesHealth/{locationId}` | Get the overall services health score |
| GET | `/network-scorecard/networkHealth/{locationId}` | Get the overall network health score |
| GET | `/network-scorecard/deviceHealth/{locationId}` | Get the overall device health score |
| GET | `/network-scorecard/clientHealth/{locationId}` | Get the overall client health score |
| GET | `/network-policies/{id}/ssids` | List SSIDs for a network policy |
| GET | `/logs/sms` | List SMS logs |
| GET | `/logs/email` | List Email logs |
| GET | `/logs/credential` | List credential logs |
| GET | `/logs/auth` | List auth logs |
| GET | `/logs/audit` | List audit logs |
| GET | `/logs/audit/reports/{id}` | Download audit logs |
| GET | `/logs/audit/full-descriptions/{id}` | Get audit log full descriptions |
| GET | `/logs/accounting` | List accounting logs |
| GET | `/locations/wall/type/references/{id}` | Find references of a wall type |
| GET | `/locations/tree` | Get location tree |
| GET | `/locations/tree/maps` | Get maps on the location hierarchy. |
| GET | `/locations/tree/devices` | Get devices on the location hierarchy. |
| GET | `/locations/folder/{folderId}/zones` | Get all zones in folder |
| GET | `/hiq/status` | Get HIQ status |
| GET | `/geo-view` | Get GeoView Data |
| GET | `/essentials/eloc/clients/{clientMac}/last-known-location` | Get the last known location of the client |
| GET | `/essentials/eloc/clients/location/path-in-interval-on-floor` | Get the path of the client in the specified interval |
| GET | `/essentials/eloc/clients/location/last-known-location-in-interval-on-floor` | Get the last known location of the client in the specified interval |
| GET | `/essentials/eloc/clients/location/density-map-data` | Get the client density map data |
| GET | `/essentials/eloc/clients/location/current-on-floor` | Get the current location of the client |
| GET | `/essentials/eloc/clients/location/current-of-all-on-floor` | Get all connected clients on a floor |
| GET | `/endusers/client/locked-list` | List locked clients |
| GET | `/email-templates` | List Email templates |
| GET | `/devices` | [LRO] List devices |
| GET | `/devices/{id}` | Get device info for a specific device |
| DELETE | `/devices/{id}` | Delete a device |
| GET | `/devices/{id}/ssid/status` | Get SSID status for a device |
| GET | `/devices/{id}/monitor/refresh/status` | Monitor refresh a device status |
| GET | `/devices/{id}/iot` | Get the device IoT Wireless Interface settings |
| GET | `/devices/{id}/interfaces/wifi` | Get the device WiFi interfaces stats |
| GET | `/devices/{id}/installation-report` | Get device installation report |
| GET | `/devices/{id}/ibeacon` | Get the device iBeacon setting |
| GET | `/devices/{id}/history/cpu-mem` | Get device CPU/memory usage history |
| GET | `/devices/{id}/geolocation` | Get Geolocation for a device |
| GET | `/devices/{id}/gallery-image` | Download device gallery image. |
| GET | `/devices/{id}/alarms` | List alarms for a device |
| GET | `/devices/stats` | Get device stats |
| GET | `/devices/rm-devices-stack/{stackId}` | Get Stack Member Info for a given stack id |
| GET | `/devices/reports/{id}` | Download the Export CSV file |
| GET | `/devices/radio-information` | Get Devices Radio Information |
| GET | `/devices/network-policy/{policyId}` | List assigned devices for network policy |
| GET | `/devices/digital-twin` | List Digital Twin product information. |
| GET | `/deployments/{deploymentId}/status` | [LRO] Get firmware deployment status by ID |
| GET | `/deployments/status` | Get configuration deployment status |
| GET | `/deployments/overview` | Get configuration deployment overview |
| GET | `/dashboard/wireless/usage-capacity/reports/{id}` | Download the report |
| GET | `/dashboard/wireless/device-health/reports/{id}` | Download the report |
| GET | `/dashboard/wireless/device-health/reboot/summary` | Device reboot summary for wireless device |
| GET | `/dashboard/wireless/client-health/reports/{id}` | Download the report |
| GET | `/dashboard/reports/{id}` | Download the report |
| GET | `/dashboard/device-types` | Get all diagnostics device types |
| GET | `/d360/wireless/interfaces-stats` | Get Wifi Information |
| GET | `/d360/wireless/interfaces-graph` | Get Wireless Interface Graph |
| GET | `/d360/wired/queue-grid` | Wired QOS queue grid |
| GET | `/d360/ssid-metadata` | Get SSID Metadata |
| GET | `/d360/overview/devices-summary` | List the summary of device details |
| GET | `/d360/event/graph` | Get Client Grid Filter Metadata |
| GET | `/d360/device/tunnel-status` | Get Device Tunnel Status |
| GET | `/d360/device/stats` | Get Device Stats |
| GET | `/d360/device/metadata` | Get Device MetaData |
| GET | `/d360/device/issues` | Get Device Issues |
| GET | `/d360/device/interfaces` | Get Wifi Interfaces Per Device Information |
| GET | `/d360/client/stats` | Get Client Stats Information |
| GET | `/d360/client/grid/metadata` | Get Client Grid Filter Metadata |
| GET | `/cwps` | List captive web portals |
| GET | `/countries` | Get country list |
| GET | `/countries/{countryCode}/:validate` | Validate country code |
| GET | `/countries/{countryAlpha2Code}/states` | Get state list by country code |
| GET | `/copilot/connectivity/wireless/views` | getWirelessViews |
| GET | `/copilot/connectivity/wireless/time-to-connect` | getWirelessTimeToConnect |
| GET | `/copilot/connectivity/wireless/quality-index` | getWirelessQualityIndex |
| GET | `/copilot/connectivity/wireless/performance` | getWirelessPerformance |
| GET | `/copilot/connectivity/wireless/locations/time-to-connect` | getWirelessTimeToConnectByLocation |
| GET | `/copilot/connectivity/wireless/locations/quality-index` | getWirelessQualityIndexByLocation |
| GET | `/copilot/connectivity/wireless/locations/performance` | getWirelessPerformanceByLocation |
| GET | `/copilot/connectivity/wireless/locations/events` | getWirelessEventsByLocation |
| GET | `/copilot/connectivity/wireless/experience` | getWirelessConnectivityExperience |
| GET | `/copilot/connectivity/wireless/events` | getWirelessEvents |
| GET | `/copilot/connectivity/wireless/apps` | getWirelessApps |
| GET | `/copilot/connectivity/wired/quality-index` | getWiredQualityIndex |
| GET | `/copilot/connectivity/wired/locations/hardware` | getWiredHardwareByLocation |
| GET | `/copilot/connectivity/wired/hardware` | getWiredHardware |
| GET | `/copilot/connectivity/wired/experience` | getWiredConnectivityExperience |
| GET | `/copilot/connectivity/wired/events` | getWiredEvents |
| GET | `/copilot/connectivity/locations` | getConnectivityDetailsByLocations |
| GET | `/copilot/connectivity/client-type` | getConnectivityDetailsByClientType |
| GET | `/copilot/assurance-scans/overview` | getAssuranceScansOverviewData |
| GET | `/copilot/anomalies/wifi-efficiency/stats` | getWifiEfficiencyStats |
| GET | `/copilot/anomalies/wifi-efficiency/client-list` | getWifiEfficiencyClientList |
| GET | `/copilot/anomalies/wifi-capacity/stats` | getWifiCapacityStats |
| GET | `/copilot/anomalies/wifi-capacity/client-list` | getWifiCapacityClientList |
| GET | `/copilot/anomalies/report` | getAnomaliesReport |
| GET | `/copilot/anomalies/port-efficiency/stats` | getPortEfficiencyStats |
| GET | `/copilot/anomalies/port-efficiency/speed-duplex-stats` | getPortEfficiencySpeedDuplexStats |
| GET | `/copilot/anomalies/poeflapping/trends` | getPoeFlappingTrends |
| GET | `/copilot/anomalies/poeflapping/stats` | getPoeFlappingStats |
| GET | `/copilot/anomalies/poeflapping/lldp-cdp-info` | getLldpCdpInfo |
| GET | `/copilot/anomalies/notifications` | getAnomaliesNotifications |
| GET | `/copilot/anomalies/missing-vlan/count` | getMissingVlanAnomaliesCount |
| GET | `/copilot/anomalies/locations` | listAnomalyLocations |
| GET | `/copilot/anomalies/hardware-health/stats` | getHardwareHealthStats |
| GET | `/copilot/anomalies/hardware-health/cpu-mem-stats` | getHardwareHealthCpuMemStats |
| GET | `/copilot/anomalies/hardware-health/client-list` | getHardwareHealthClientList |
| GET | `/copilot/anomalies/excluded-vlans-list` | getMissingVlanExcludedVlanList |
| GET | `/copilot/anomalies/dfs-recurrence/count-stats` | getDfsRecurrenceCountStats |
| GET | `/copilot/anomalies/dfs-recurrence/channel-stats` | getDfsRecurrenceChannelStats |
| GET | `/copilot/anomalies/devices-with-locations` | getCopilotDevicesWithLocations |
| GET | `/copilot/anomalies/devices-by-location` | getDevicesByLocation |
| GET | `/copilot/anomalies/anomalies-by-category` | getCopilotAnomaliesbyCategory |
| GET | `/copilot/anomalies/adverse-traffic/packet-counts` | getAtpPacketCounts |
| GET | `/copilot/anomalies/adverse-traffic/device-stats` | getAtpDeviceStats |
| GET | `/clients/{id}` | Get client info |
| GET | `/clients/usage` | Get usage per client |
| GET | `/clients/summary` | Get client summary metrics |
| GET | `/clients/byMac/{clientMac}` | Get client info by mac |
| DELETE | `/clients/byMac/{clientMac}` | Disconnect the client |
| GET | `/clients/active` | List active clients |
| GET | `/clients/active/count` | Get active clients count |
| GET | `/client-details/topology/client-trail/{macAddress}` | getConnectionTrail |
| GET | `/client-details/overview/info/{clientId}` | Get Client Details Info |
| GET | `/client-details/overview/chart-data/{clientId}` | Get Client chart data |
| GET | `/client-details/client-trail/roaming-trail/grid/{clientId}` | Get roaming trail grid |
| GET | `/client-details/client-trail/roaming-trail/count/{clientId}` | Get roaming trail count |
| GET | `/client-details/client-trail/connectivity-experience/{clientId}` | Get connectivity experience grid |
| GET | `/certificates` | List certificates |
| GET | `/backup/history/grid` | List backup history grid |
| GET | `/auth/permissions` | Get permissions for current login user |
| GET | `/auth/apitoken/info` | Get current API token details |
| GET | `/applications` | List the applications |
| GET | `/applications/{id}/clients/top{n}` | List the TopN clients for a application |
| GET | `/applications/usage/summary/meta-data` | Application usage summary meta data |
| GET | `/applications/top{n}` | List the TopN applications |
| GET | `/applications/reports/{id}` | Download the Export CSV file |
| GET | `/ap/afc/v2/floorReport/{deviceId}` | getRmAfcGeolocaitonFloorReport |
| GET | `/ap/afc/interface/details/{sn}` | Get Afc Summary Data |
| GET | `/ap/afc/floorReport/{deviceId}` | getAfcGeolocaitonFloorReport |
| GET | `/ap/afc/diagnostics/{id}` | getApsAfcDiagnostics |
| GET | `/alerts` | List the alerts |
| GET | `/alerts/reports/{id}` | Download the alerts report |
| GET | `/alerts/count-by-{group}` | Count the alerts by different grouping |
| GET | `/alert-policies/available-sites` | The list of current owner's available sites |
| GET | `/airrm/site/{airrmId}` | Get Site Device Regulatory Config and AFC Spectrum |
| GET | `/airrm/radio/apInfo/{radioMac}` | Get Device AP Information |
| GET | `/airrm/device/{serialNumber}` | Get Device Regulatory Config and AFC Spectrum |
| GET | `/afcserver` | Get Afc Server list and their status |
| GET | `/afcserver/{server_id}` | Get Afc Server data |
| GET | `/afcserver/statistics/{server_id}` | Get AFC server Statistics |
| GET | `/afc/reports/{id}` | Download the report |
| GET | `/ad-servers` | List active directory servers |
| GET | `/acct-api-token/export` | Export all API access tokens to CSV |
| GET | `/account/viq` | Get VIQ Info |
| GET | `/account/viq/export-import-status` | Get running export/import status |
| GET | `/account/viq/download` | Download VIQ data file and logs |
| GET | `/account/viq/backup/status` | Get VIQ Backup Status |
| GET | `/account/vhm/status` | Get Vhm Status |
| GET | `/account/vhm/setting` | Get Vhm Setting |
| GET | `/account/third-party-applications` | List Third Party Applications |
| GET | `/account/home` | Get home ExtremeCloud IQ account info |
| GET | `/account/external` | List accessible external guest accounts |
| DELETE | `/subscriptions/webhook/:delete` | Delete webhook subscription |
| DELETE | `/rtts/{id}` | DeleteRttsSession |
| DELETE | `/pcgs/key-based/network-policy-{policyId}` | Delete Private Client Group from a network policy |
| DELETE | `/ng-reports/scheduled/runs` | Delete report runs |
| DELETE | `/network-services/{id}` | Delete Network Services |
| DELETE | `/locations/folder/zone/{id}` | Delete a zone by ID |
| DELETE | `/locations/floor/{floorId}/label/{labelId}` | Deletes one floor map label |
| DELETE | `/hiq/organizations/{id}` | Delete an existing organization |
| DELETE | `/floor/afc/details/{id}` | deleteFloorAfcDetails |
| DELETE | `/devices/radius-proxy/:revoke` | Revoke RADIUS proxy from multiple devices |
| DELETE | `/certificates/{id}` | Delete Certificate by ID |
| DELETE | `/backup/history/delete` | Backup History Delete |
| DELETE | `/acct-api-token/:delete` | Bulk Delete API Access token by ID |

## PUT `/v1/account/viq/default-device-password`

Operation: `updateDefaultDevicePasswordWithValidation`

Update the default device password in the account (with validation)

Update the default device password in the global setting for accessing the console/shell of the devices.

Tags: `Account`

Request body:

- `application/json` — string

Responses:

- `200` — OK

## PUT `/usergroups/{id}`

Operation: `updateUserGroup`

Update user group

Update existing user group information.

Tags: `Configuration - User Management`

Parameters:

- `id` path, required (integer) — The user group ID.

Request body:

- `application/json` — XiqUpdateUserGroupRequest

Responses:

- `200` — OK

## DELETE `/usergroups/{id}`

Operation: `deleteUserGroup`

Delete user group by ID

Delete the user-group for the specified ID.

Tags: `Configuration - User Management`

Parameters:

- `id` path, required (integer) — The user group ID

Responses:

- `200` — OK

## GET `/user-profiles/{id}`

Operation: `getUserProfile`

Get user profile by ID

Get user profile details for the specified ID.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The user profile ID

Responses:

- `200` — OK

## PUT `/user-profiles/{id}`

Operation: `updateCoUserProfile`

Update user profile

Update an existing user profile.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The user profile ID.

Request body:

- `application/json` — XiqUpdateUserProfileRequest

Responses:

- `200` — OK

## DELETE `/user-profiles/{id}`

Operation: `deleteCoUserProfile`

Delete an user profile by ID

Delete an existing user profile by ID.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The user profile ID

Responses:

- `200` — OK

## GET `/tunnel-concentrators/{id}`

Operation: `getTunnelConcentrator`

Get Tunnel Concentrator by ID

Get Tunnel Concentrator details for the specified ID.

Tags: `Configuration - Network`

Parameters:

- `id` path, required (integer) — The Tunnel Concentrator ID

Responses:

- `200` — OK

## PUT `/tunnel-concentrators/{id}`

Operation: `updateTunnelConcentrator`

Update TunnelConcentrator by ID

Update the existing Tunnel Concentrator by ID.

Tags: `Configuration - Network`

Parameters:

- `id` path, required (integer) — The Tunnel Concentrator ID.

Request body:

- `application/json` — XiqTunnelConcentratorRequest

Responses:

- `200` — OK

## DELETE `/tunnel-concentrators/{id}`

Operation: `deleteTunnelConcentrator`

Delete TunnelConcentrator by ID

Delete the existing TunnelConcentrator by the profile ID.

Tags: `Configuration - Network`

Parameters:

- `id` path, required (integer) — The TunnelConcentrator ID

Responses:

- `200` — OK

## GET `/third-party-api-connection`

Operation: `listThirdPartyApiConnections`

List third party api connections

List a page of third party api connections.

Tags: `Administration`

Responses:

- `200` — OK

## PUT `/third-party-api-connection`

Operation: `updateThirdPartyApiConnection`

Update a third party api connection

The payload to update 3rd party API connection.

Tags: `Administration`

Request body:

- `application/json` — XiqUpdateThirdPartyApiConnectionRequest

Responses:

- `200` — OK

## DELETE `/third-party-api-connection`

Operation: `deleteThirdPartyApiConnection`

Delete a third party api connection

Delete 3rd party API connection.

Tags: `Administration`

Responses:

- `200` — OK

## GET `/tcap-profiles/{id}`

Operation: `getTcap`

Tags: `Configuration - Network`

Parameters:

- `id` path, required (integer) — TCAP ID

Responses:

- `200` — OK

## PUT `/tcap-profiles/{id}`

Operation: `updateTcap`

Tags: `Configuration - Network`

Parameters:

- `id` path, required (integer) — TCAP ID

Request body:

- `application/json` — XiqTunnelConcentratorAddressPoolRequest

Responses:

- `200` — OK

## DELETE `/tcap-profiles/{id}`

Operation: `deleteTcap`

Tags: `Configuration - Network`

Parameters:

- `id` path, required (integer) — TCAP ID

Responses:

- `200` — OK

## PUT `/subscriptions/webhook/{id}`

Operation: `updateWebhookSubscription`

Update webhook subscription

Update webhook subscription by ID.

Tags: `Notification`

Parameters:

- `id` path, required (integer) — The webhook subscription ID

Request body:

- `application/json` — XiqUpdateWebhookSubscriptionRequest

Responses:

- `200` — OK

## PUT `/ssids/{id}/psk/password`

Operation: `changePskPassword`

Change the SSID PSK password

Change the SSID PSK password.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The SSID ID

Request body:

- `application/json` — string

Responses:

- `200` — OK

## PUT `/ssids/{id}/mode/wep`

Operation: `setSsidModeWep`

Change the SSID mode to WEP

Change the SSID mode to WEP.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The SSID ID

Request body:

- `application/json` — XiqSetSsidModeWepRequest

Responses:

- `200` — OK

## PUT `/ssids/{id}/mode/psk`

Operation: `setSsidModePsk`

Change the SSID mode to PSK

Change the SSID mode to PSK.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The SSID ID

Request body:

- `application/json` — XiqSetSsidModePskRequest

Responses:

- `200` — OK

## PUT `/ssids/{id}/mode/ppsk`

Operation: `setSsidModePpsk`

Change the SSID mode to PPSK

Change the SSID mode to PPSK.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The SSID ID

Request body:

- `application/json` — XiqSetSsidModePpskRequest

Responses:

- `200` — OK

## PUT `/ssids/{id}/mode/open`

Operation: `setSsidModeOpen`

Change the SSID mode to open access

Change the SSID mode to open access.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The SSID ID

Responses:

- `200` — OK

## PUT `/ssids/{id}/mode/dot1x`

Operation: `setSsidModeDot1x`

Change the SSID mode to 802.1x

Change the SSID mode to 802.1x.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The SSID ID

Request body:

- `application/json` — XiqSetSsidModeDot1xRequest

Responses:

- `200` — OK

## GET `/ssids/advanced-settings/{id}`

Operation: `getSsidAdvancedSettings`

Get SSID advanced settings

Get the advanced settings belonging to the SSID.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The SSID's advanced settings ID

Responses:

- `200` — OK

## PUT `/ssids/advanced-settings/{id}`

Operation: `updateSsidAdvancedSettings`

Update SSID advanced settings

Update the advanced settings belonging to the SSID.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The SSID advanced settings ID.

Request body:

- `application/json` — XiqUpdateSsidAdvancedSettingsRequest

Responses:

- `200` — OK

## GET `/site/afc/schedule`

Operation: `getSiteAfcSchedule`

Tags: `AFC`

Parameters:

- `ownerId` query, required (integer) — Owner Id
- `folderId` query, required (integer) — Folder Id

Responses:

- `200` — OK

## POST `/site/afc/schedule`

Operation: `createSiteAfcSchedule`

Tags: `AFC`

Request body:

- `application/json` — XiqSiteAfcSchedule

Responses:

- `200` — OK

## PUT `/site/afc/schedule`

Operation: `updateSiteAfcSchedule`

Tags: `AFC`

Request body:

- `application/json` — XiqSiteAfcSchedule

Responses:

- `200` — OK

## GET `/radsec-proxies/{id}`

Operation: `getRadsecProxy`

Get the RADSEC proxy configuration

Get an existing RADSEC proxy configuration by ID.

Tags: `Configuration - Authentication`

Parameters:

- `id` path, required (integer) — The RADSEC proxy ID

Responses:

- `200` — OK

## PUT `/radsec-proxies/{id}`

Operation: `updateRadsecProxy`

Update RADSEC proxy configuration

Update RADSEC proxy configuration by ID.

Tags: `Configuration - Authentication`

Parameters:

- `id` path, required (integer) — The RADSEC proxy ID

Request body:

- `application/json` — XiqUpdateRadsecProxyRequest

Responses:

- `200` — OK

## DELETE `/radsec-proxies/{id}`

Operation: `deleteRadsecProxy`

Delete the RADSEC proxy configuration

Delete an existing RADSEC proxy configuration by ID.

Tags: `Configuration - Authentication`

Parameters:

- `id` path, required (integer) — The RADSEC proxy ID

Responses:

- `200` — OK

## GET `/radius-servers/internal/{id}`

Operation: `getInternalRadiusServer`

Get internal RADIUS server by ID

Get detailed configuration for internal RADIUS server by ID.

Tags: `Configuration - Authentication`

Parameters:

- `id` path, required (integer) — The ID for internal RADIUS server

Responses:

- `200` — OK

## PUT `/radius-servers/internal/{id}`

Operation: `updateInternalRadiusServer`

Update internal RADIUS server configuration

Update internal RADIUS server configuration by ID.

Tags: `Configuration - Authentication`

Parameters:

- `id` path, required (integer) — The internal RADIUS server ID

Request body:

- `application/json` — XiqUpdateInternalRadiusServerRequest

Responses:

- `200` — OK

## DELETE `/radius-servers/internal/{id}`

Operation: `deleteInternalRadiusServer`

Delete internal RADIUS server configuration

Delete an existing internal RADIUS server configuration by ID.

Tags: `Configuration - Authentication`

Parameters:

- `id` path, required (integer) — The internal RADIUS server ID

Responses:

- `200` — OK

## GET `/radius-servers/external/{id}`

Operation: `getExternalRadiusServer`

Get external RADIUS server by ID

Get detailed configuration for a specific external RADIUS server.

Tags: `Configuration - Authentication`

Parameters:

- `id` path, required (integer) — The ID for external RADIUS server

Responses:

- `200` — OK

## PUT `/radius-servers/external/{id}`

Operation: `updateExternalRadiusServer`

Update external RADIUS server configuration

Update external RADIUS server configuration by ID.

Tags: `Configuration - Authentication`

Parameters:

- `id` path, required (integer) — The external RADIUS server ID.

Request body:

- `application/json` — XiqUpdateExternalRadiusServerRequest

Responses:

- `200` — OK

## DELETE `/radius-servers/external/{id}`

Operation: `deleteExternalRadiusServer`

Delete external RADIUS server configuration

Delete an existing external RADIUS server configuration by ID.

Tags: `Configuration - Authentication`

Parameters:

- `id` path, required (integer) — The external RADIUS server ID

Responses:

- `200` — OK

## GET `/radius-proxies/{id}`

Operation: `getRadiusProxy`

Get the RADIUS proxy configuration

Get an existing RADIUS proxy configuration by ID.

Tags: `Configuration - Authentication`

Parameters:

- `id` path, required (integer) — The RADIUS proxy ID

Responses:

- `200` — OK

## PUT `/radius-proxies/{id}`

Operation: `updateRadiusProxy`

Update RADIUS proxy configuration

Update RADIUS proxy configuration by ID.

Tags: `Configuration - Authentication`

Parameters:

- `id` path, required (integer) — The RADIUS proxy ID

Request body:

- `application/json` — XiqUpdateRadiusProxyRequest

Responses:

- `200` — OK

## DELETE `/radius-proxies/{id}`

Operation: `deleteRadiusProxy`

Delete the RADIUS proxy configuration

Delete an existing RADIUS proxy configuration by ID.

Tags: `Configuration - Authentication`

Parameters:

- `id` path, required (integer) — The RADIUS proxy ID

Responses:

- `200` — OK

## GET `/radius-client-objects/{id}`

Operation: `getRadiusClientObject`

Get RADIUS client object by ID

Get detailed configuration for a specific RADIUS client object.

Tags: `Configuration - Authentication`

Parameters:

- `id` path, required (integer) — The ID of RADIUS client object

Responses:

- `200` — OK

## PUT `/radius-client-objects/{id}`

Operation: `updateRadiusClientObject`

Update RADIUS client object configuration

Update RADIUS client object configuration by ID.

Tags: `Configuration - Authentication`

Parameters:

- `id` path, required (integer) — The RADIUS client object ID.

Request body:

- `application/json` — XiqUpdateRadiusClientObjectRequest

Responses:

- `200` — OK

## DELETE `/radius-client-objects/{id}`

Operation: `deleteRadiusClientObject`

Delete a RADIUS client object configuration

Delete an existing RADIUS client object configuration by ID.

Tags: `Configuration - Authentication`

Parameters:

- `id` path, required (integer) — The RADIUS client object ID

Responses:

- `200` — OK

## GET `/radio-profiles/{id}`

Operation: `getRadioProfile`

Get radio profile by ID

Get radio profile details for the specified ID.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The radio profile ID

Responses:

- `200` — OK

## PUT `/radio-profiles/{id}`

Operation: `updateRadioProfile`

Update radio profile by ID

Update the existing radio profile by the profile ID.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The radio profile ID.

Request body:

- `application/json` — XiqUpdateRadioProfileRequest

Responses:

- `200` — OK

## DELETE `/radio-profiles/{id}`

Operation: `deleteRadioProfile`

Delete radio profile by ID

Delete the existing radio profile by the profile ID.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The radio profile ID

Responses:

- `200` — OK

## GET `/radio-profiles/wmm-qos/{id}`

Operation: `getRpWmmQosSettings`

Get Wmm QoS settings

Get the Wi-Fi Multimedia (WMM) QoS settings belonging to a radio profile.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The radio QoS settings ID

Responses:

- `200` — OK

## PUT `/radio-profiles/wmm-qos/{id}`

Operation: `updateRpWmmQosSettings`

Update Wmm QoS settings

Update the Wi-Fi Multimedia (WMM) QoS settings belonging to a radio profile.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The Wmm QoS settings ID.

Request body:

- `application/json` — XiqUpdateRpWmmQosSettingsRequest

Responses:

- `200` — OK

## GET `/radio-profiles/sensor-scan/{id}`

Operation: `getRpSensorScanSettings`

Get sensor scan settings

Get the sensor scan settings belonging to a radio profile.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The sensor scan settings ID

Responses:

- `200` — OK

## PUT `/radio-profiles/sensor-scan/{id}`

Operation: `updateRpSensorScanSettings`

Update sensor scan settings

Update the sensor scan settings belonging to a radio profile.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The sensor scan settings ID.

Request body:

- `application/json` — XiqUpdateRpSensorScanSettingsRequest

Responses:

- `200` — OK

## GET `/radio-profiles/radio-usage-opt/{id}`

Operation: `getRpRadioUsageOptimization`

Get radio usage optimization settings

Get the radio usage optimization settings belonging to a radio profile.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The radio usage optimization settings ID

Responses:

- `200` — OK

## PUT `/radio-profiles/radio-usage-opt/{id}`

Operation: `updateRpRadioUsageOptimization`

Update radio usage optimization settings

Update the radio usage optimization settings belonging to a radio profile.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The radio usage optimization settings ID.

Request body:

- `application/json` — XiqUpdateRpRadioUsageOptimizationRequest

Responses:

- `200` — OK

## GET `/radio-profiles/neighborhood-analysis/{id}`

Operation: `getNeighborhoodAnalysis`

Get neighborhood analysis settings

Get the neighborhood analysis settings belonging to a radio profile.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The neighborhood analysis settings ID

Responses:

- `200` — OK

## PUT `/radio-profiles/neighborhood-analysis/{id}`

Operation: `updateNeighborhoodAnalysis`

Update neighborhood analysis settings

Update the neighborhood analysis settings belonging to a radio profile.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The neighborhood analysis settings ID.

Request body:

- `application/json` — XiqUpdateRpNeighborhoodAnalysisRequest

Responses:

- `200` — OK

## GET `/radio-profiles/miscellaneous/{id}`

Operation: `getRpMiscellaneousSettings`

Get radio miscellaneous settings

Get the radio miscellaneous settings belonging to a radio profile.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The radio miscellaneous settings ID

Responses:

- `200` — OK

## PUT `/radio-profiles/miscellaneous/{id}`

Operation: `updateRpMiscellaneousSettings`

Update radio miscellaneous settings

Update the radio miscellaneous settings belonging to a radio profile.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The radio miscellaneous settings ID.

Request body:

- `application/json` — XiqUpdateRpMiscellaneousSettingsRequest

Responses:

- `200` — OK

## GET `/radio-profiles/mac-ouis/{id}`

Operation: `getRpMacOuiProfile`

Get MAC OUI profile

Get the MAC OUI profile belonging the radio optimization settings.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The MAC OUI profile ID

Responses:

- `200` — OK

## PUT `/radio-profiles/mac-ouis/{id}`

Operation: `updateRpMacOuiProfile`

Update MAC OUI profile

Update the existing MAC OUI profile for radio usage optimization.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The MAC OUI profile ID.

Request body:

- `application/json` — XiqUpdateRpMacOuiProfileRequest

Responses:

- `200` — OK

## DELETE `/radio-profiles/mac-ouis/{id}`

Operation: `deleteRpMacOuiProfile`

Delete MAC OUI profile

Delete the existing MAC OUI profile for radio usage optimization.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The MAC OUI profile ID

Responses:

- `200` — OK

## GET `/radio-profiles/channel-selection/{id}`

Operation: `getRpChannelSelection`

Get channel selection settings

Get the channel selection settings belonging to a radio profile.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The channel selection settings ID

Responses:

- `200` — OK

## PUT `/radio-profiles/channel-selection/{id}`

Operation: `updateRpChannelSelection`

Update channel selection settings

Update the channel selection settings belonging to a radio profile.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The channel selection settings ID.

Request body:

- `application/json` — XiqUpdateRpChannelSelectionRequest

Responses:

- `200` — OK

## GET `/pcgs/key-based/network-policy-{policyId}/users`

Operation: `getKeyBasedPcgUsers`

Get users for a PCG-enabled network policy

Get users for a specific PCG-enabled network policy.

Tags: `Configuration - User Management`

Parameters:

- `policyId` path, required (integer) — The network policy ID
- `page` query, optional (integer) — Page number
- `limit` query, optional (integer) — Page Size

Responses:

- `200` — OK

## POST `/pcgs/key-based/network-policy-{policyId}/users`

Operation: `addKeyBasedPcgUsers`

[LRO] Add users to a PCG-enabled network policy

Add users to a PCG-enabled network policy.

Tags: `Configuration - User Management`

Parameters:

- `policyId` path, required (integer) — The network policy ID
- `async` query, optional (boolean) — Whether to enable async mode

Request body:

- `application/json` — XiqCreateKeyBasedPcgUsersRequest

Responses:

- `200` — OK

## PUT `/pcgs/key-based/network-policy-{policyId}/users`

Operation: `updateKeyBasedPcgUsers`

Replace all users in a PCG-enabled network policy

Replace all users in a specific PCG-enabled network policy.

Tags: `Configuration - User Management`

Parameters:

- `policyId` path, required (integer) — The network policy ID

Request body:

- `application/json` — XiqUpdateKeyBasedPcgUsersRequest

Responses:

- `202` — Accepted

## DELETE `/pcgs/key-based/network-policy-{policyId}/users`

Operation: `deleteKeyBasedPcgUsers`

Delete users from a PCG-enabled network policy

Delete users from a PCG-enabled network policy.

Tags: `Configuration - User Management`

Parameters:

- `policyId` path, required (integer) — The network policy ID

Request body:

- `application/json` — XiqDeleteKeyBasedPcgUsersRequest

Responses:

- `202` — Accepted

## GET `/ng-reports/scheduled/{reportId}/recipients`

Operation: `getRecipientsForReport`

Get Recipients for Report

Retrieves all recipients for a given report.

Tags: `NG Reports (Scheduled)`

Parameters:

- `reportId` path, required (integer) — The report ID
- `keyword` query, optional (string) — The keyword to search

Responses:

- `200` — OK

## POST `/ng-reports/scheduled/{reportId}/recipients`

Operation: `deleteRecipientsFromReport`

Delete Recipients from Report

Deletes a list of recipient emails from the specified report.

Tags: `NG Reports (Scheduled)`

Parameters:

- `reportId` path, required (integer) — The report ID

Request body:

- `application/json` — XiqRecipientIdsRequest

Responses:

- `200` — OK

## PUT `/ng-reports/scheduled/{reportId}/recipients`

Operation: `addRecipientsToReport`

Add Recipients to Report

Adds a list of recipient emails to the specified report.

Tags: `NG Reports (Scheduled)`

Parameters:

- `reportId` path, required (integer) — The report ID

Request body:

- `application/json` — array

Responses:

- `200` — OK

## GET `/ng-reports/scheduled/custom/{reportId}`

Operation: `getCustomReportSchedule`

Get a custom report schedule

Fetch details of a scheduled custom report by its ID.

Tags: `NG Reports (Scheduled)`

Parameters:

- `reportId` path, required (integer) — The report ID

Responses:

- `200` — OK

## PUT `/ng-reports/scheduled/custom/{reportId}`

Operation: `updateScheduledCustomReport`

Update a scheduled custom report

Update an existing scheduled custom report identified by reportScheduleId.

Tags: `NG Reports (Scheduled)`

Parameters:

- `reportId` path, required (integer) — The report ID

Request body:

- `application/json` — XiqUpdateCustomReportRequest

Responses:

- `200` — OK

## GET `/network-policies/{id}`

Operation: `getNetworkPolicy`

Get the network policy

Get an existing network policy by ID.

Tags: `Network Policy`

Parameters:

- `id` path, required (integer) — The network policy ID

Responses:

- `200` — OK

## PUT `/network-policies/{id}`

Operation: `updateNetworkPolicy`

Update the network policy

Update network policy by ID.

Tags: `Network Policy`

Parameters:

- `id` path, required (integer) — The network policy ID

Request body:

- `application/json` — XiqUpdateNetworkPolicyRequest

Responses:

- `200` — OK

## DELETE `/network-policies/{id}`

Operation: `deleteNetworkPolicy`

Delete the network policy

Delete an existing network policy by ID.

Tags: `Network Policy`

Parameters:

- `id` path, required (integer) — The network policy ID

Responses:

- `200` — OK

## GET `/mac-object-profiles/{id}`

Operation: `getMacObject`

Get MAC Object by ID

Get an existing MAC object by the specified ID.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The MAC Object ID

Responses:

- `200` — OK

## PUT `/mac-object-profiles/{id}`

Operation: `updateMacObject`

Update MAC Object by ID

Update an existing MAC object by the specified ID.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The MAC Object ID.

Request body:

- `application/json` — XiqUpdateMacObjectRequest

Responses:

- `200` — OK

## DELETE `/mac-object-profiles/{id}`

Operation: `deleteMacObjectProfiles`

Delete a MAC object by ID

Delete an existing MAC object by the specified ID.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The Mac object ID

Responses:

- `200` — OK

## GET `/mac-firewall-policies/{id}`

Operation: `getMacFirewallPolicy`

Get MAC Firewall Policy by ID

Get an existing MAC Firewall policy by the specified ID.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The MAC firewall policy ID

Responses:

- `200` — OK

## PUT `/mac-firewall-policies/{id}`

Operation: `updateMacFirewallPolicy`

Update MAC Firewall policy by ID

Update an existing MAC Firewall policy by the specified ID.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The MAC Firewall Policy ID.

Request body:

- `application/json` — XiqMacFirewallPolicyRequest

Responses:

- `200` — OK

## DELETE `/mac-firewall-policies/{id}`

Operation: `deleteMacFirewallPolicy`

Delete MAC Firewall policy by ID

Delete an existing MAC Firewall policy by the specified ID.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The MAC Firewall Policy ID

Responses:

- `200` — OK

## PUT `/locations/{id}`

Operation: `updateLocation`

Update a location

Update a location information with the specified location ID.

Tags: `Location`

Parameters:

- `id` path, required (integer) — The location ID

Request body:

- `application/json` — XiqUpdateLocationRequest

Responses:

- `200` — OK

## DELETE `/locations/{id}`

Operation: `deleteLocation`

Delete a location by ID

Delete a location for the specified ID.

Tags: `Location`

Parameters:

- `id` path, required (integer) — The location ID
- `force_delete` query, optional (boolean) — Force deletion of this location and its descendants recursively

Responses:

- `200` — OK

## PUT `/locations/wall/type/{id}`

Operation: `updateWallType`

Update a wall type

Update the custom wall type with the specified ID.

Tags: `Location`

Parameters:

- `id` path, required (integer) — The Wall Type ID

Request body:

- `application/json` — XiqUpdateTypeRequest

Responses:

- `200` — OK

## DELETE `/locations/wall/type/{id}`

Operation: `deleteWallType`

Delete a wall type

Delete a wall type for the specified ID.

Tags: `Location`

Parameters:

- `id` path, required (integer) — The Wall Type ID

Responses:

- `204` — No Content

## GET `/locations/site/{id}`

Operation: `getSite`

Get a site by ID

Get a site for the specified ID.

Tags: `Location`

Parameters:

- `id` path, required (integer) — The site ID

Responses:

- `200` — OK

## PUT `/locations/site/{id}`

Operation: `updateSite`

Update a site by ID

Update a site for the specified ID.

Tags: `Location`

Parameters:

- `id` path, required (integer) — The site ID

Request body:

- `application/json` — XiqUpdateSiteRequest

Responses:

- `200` — OK

## DELETE `/locations/site/{id}`

Operation: `deleteSite`

Delete a site by ID

Delete a site for the specified ID.

Tags: `Location`

Parameters:

- `id` path, required (integer) — The site ID
- `force_delete` query, optional (boolean) — Force deletion of this site and its descendants recursively

Responses:

- `200` — OK

## POST `/locations/folder/zones`

Operation: `createZone`

Create a zone

Create a zone.

Tags: `Location`

Request body:

- `application/json` — XiqCreateZoneRequest

Responses:

- `201` — Created

## PUT `/locations/folder/zones`

Operation: `updateZones`

Update zones in folder

Update zones for the specified folder ID.

Tags: `Location`

Request body:

- `application/json` — XiqUpdateZonesRequest

Responses:

- `200` — OK

## GET `/locations/floor/{id}`

Operation: `getFloor`

Get a floor by ID

Get the floor for the specified ID.

Tags: `Location`

Parameters:

- `id` path, required (integer) — The floor ID

Responses:

- `200` — OK

## PUT `/locations/floor/{id}`

Operation: `updateFloor`

Update a floor

Update a floor information with the floor ID.

Tags: `Location`

Parameters:

- `id` path, required (integer) — The floor ID.

Request body:

- `application/json` — XiqUpdateFloorRequest

Responses:

- `200` — OK

## DELETE `/locations/floor/{id}`

Operation: `deleteFloor`

Delete a floor by ID

Delete a floor for the specified ID.

Tags: `Location`

Parameters:

- `id` path, required (integer) — The floor ID

Responses:

- `200` — OK

## GET `/locations/floor/{floorId}/walls`

Operation: `getWalls`

List all walls on a floor

Returns all wall segments belonging to the specified floor

Tags: `Location`

Parameters:

- `floorId` path, required (integer) — The floor ID

Responses:

- `200` — OK

## PUT `/locations/floor/{floorId}/walls`

Operation: `saveWalls`

Save walls on a floor

Replaces the complete set of walls on the specified floor with the provided list. This is the only wall-write XAPI exposed for plan imports.

Tags: `Location`

Parameters:

- `floorId` path, required (integer) — The floor ID

Request body:

- `application/json` — XiqSaveFloorWallsRequest

Responses:

- `200` — OK

## GET `/locations/floor/{floorId}/label`

Operation: `getFloorMapLabels`

Find all floor map labels referencing the floor

Finds all labels referencing the floor given by its id.

Tags: `Location`

Parameters:

- `floorId` path, required (integer) — The Floor ID

Responses:

- `200` — OK

## POST `/locations/floor/{floorId}/label`

Operation: `createFloorMapLabel`

Creates one floor map label.

Creates one floor map label which references the floor given by its id.

Tags: `Location`

Parameters:

- `floorId` path, required (integer) — The Floor ID

Request body:

- `application/json` — XiqFloorMapLabel

Responses:

- `200` — OK

## PUT `/locations/floor/{floorId}/label`

Operation: `updateFloorMapLabel`

Updates one floor map label.

Updates one floor map label which references the floor given by its id.

Tags: `Location`

Parameters:

- `floorId` path, required (integer) — The Floor ID

Request body:

- `application/json` — XiqFloorMapLabel

Responses:

- `200` — OK

## PUT `/locations/floor/bulk/label`

Operation: `bulkUpdateFloorMapLabels`

Updates one ore more floor map labels.

Updates one or more floor map labels.

Tags: `Location`

Request body:

- `application/json` — array

Responses:

- `200` — OK

## GET `/locations/building/{id}`

Operation: `getBuilding`

Get a building by ID

Get the building for the specified ID.

Tags: `Location`

Parameters:

- `id` path, required (integer) — The building ID

Responses:

- `200` — OK

## PUT `/locations/building/{id}`

Operation: `updateBuilding`

Update a building

Update a building information with the building ID.

Tags: `Location`

Parameters:

- `id` path, required (integer) — The building ID

Request body:

- `application/json` — XiqUpdateBuildingRequest

Responses:

- `200` — OK

## DELETE `/locations/building/{id}`

Operation: `deleteBuilding`

Delete a building by ID

Delete a building for the specified ID.

Tags: `Location`

Parameters:

- `id` path, required (integer) — The building ID
- `force_delete` query, optional (boolean) — Force deletion of this building and its descendants recursively

Responses:

- `200` — OK

## GET `/ldap-servers/{id}`

Operation: `getLdapServer`

Get LDAP server by ID

Get a specific LDAP server by ID.

Tags: `Configuration - Authentication`

Parameters:

- `id` path, required (integer) — The LDAP server

Responses:

- `200` — OK

## PUT `/ldap-servers/{id}`

Operation: `updateLdapServer`

Update LDAP server configuration

Update configuration for a specific LDAP server.

Tags: `Configuration - Authentication`

Parameters:

- `id` path, required (integer) — The LDAP server ID.

Request body:

- `application/json` — XiqUpdateLdapServerRequest

Responses:

- `200` — OK

## DELETE `/ldap-servers/{id}`

Operation: `deleteLdapServer`

Delete a LDAP server

Delete a specific LDAP server by ID.

Tags: `Configuration - Authentication`

Parameters:

- `id` path, required (integer) — The LDAP server ID

Responses:

- `200` — OK

## GET `/l3-address-profiles/{id}`

Operation: `getL3AddressProfile`

Get a L3 address profile by ID

Get L3 address profile details for the specified ID.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The L3 address profile ID

Responses:

- `200` — OK

## PUT `/l3-address-profiles/{id}`

Operation: `updateL3AddressProfile`

Update a L3 address profile

Update an existing address profile.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The L3 address profile ID.

Request body:

- `application/json` — XiqUpdateL3AddressProfileRequest

Responses:

- `200` — OK

## DELETE `/l3-address-profiles/{id}`

Operation: `deleteL3AddressProfile`

Delete a L3 address profile by ID

Delete an existing L3 address profile by ID.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The L3 address profile ID

Responses:

- `200` — OK

## GET `/ip-firewall-policies/{id}`

Operation: `getIpFirewallPolicy`

Get IP Firewall Policy by ID

Get an existing IP Firewall policy by the specified ID.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The ip firewall policy ID

Responses:

- `200` — OK

## PUT `/ip-firewall-policies/{id}`

Operation: `updateIpPolicyRequest`

Update IP Firewall policy by ID

Update an existing IP Firewall policy by the specified ID.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The Ip Firewall Policy ID.

Request body:

- `application/json` — XiqIpFirewallPolicyRequest

Responses:

- `200` — OK

## DELETE `/ip-firewall-policies/{id}`

Operation: `deleteIpFirewallPolicy`

Delete IP Firewall policy by ID

Delete an existing IP Firewall policy by the specified ID.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The Ip Firewall Policy ID

Responses:

- `200` — OK

## GET `/iot-profiles/{id}`

Operation: `getIotProfile`

Get IoT profile by ID

Get IoT profile details for the specified ID.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The IoT profile ID

Responses:

- `200` — OK

## PUT `/iot-profiles/{id}`

Operation: `updateIotProfile`

Update IoT profile by ID

Update the existing IoT profile by the profile ID.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The IoT profile ID.

Request body:

- `application/json` — XiqIotProfileRequest

Responses:

- `200` — OK

## DELETE `/iot-profiles/{id}`

Operation: `deleteIotProfile`

Delete IoT profile by ID

Delete the existing IoT profile by the profile ID.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The IoT profile ID

Responses:

- `200` — OK

## GET `/hotspot-service-provider-profiles/{id}`

Operation: `getHotspotServiceProviderProfile`

Get Hotspot Service Provider profile by ID

Get Hotspot Service Provider profile details for the specified ID.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The Hotspot Service Provider profile ID

Responses:

- `200` — OK

## PUT `/hotspot-service-provider-profiles/{id}`

Operation: `updateHotspotServiceProviderProfile`

Update Hotspot Service Provider profile by ID

Update the existing Hotspot Service Provider profile by the profile ID.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The Hotspot Service Provider profile ID.

Request body:

- `application/json` — XiqHotspotServiceProviderProfileRequest

Responses:

- `200` — OK

## DELETE `/hotspot-service-provider-profiles/{id}`

Operation: `deleteHotspotServiceProviderProfile`

Delete Hotspot Service Provider profile by ID

Delete the existing Hotspot Service Provider profile by the profile ID.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The Hotspot Service Provider profile ID

Responses:

- `200` — OK

## GET `/hotspot-profiles/{id}`

Operation: `getHotspotProfile`

Get Hotspot profile by ID

Get Hotspot profile details for the specified ID.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The Hotspot profile ID

Responses:

- `200` — OK

## PUT `/hotspot-profiles/{id}`

Operation: `updateHotspotProfile`

Update Hotspot profile by ID

Update the existing Hotspot profile by the profile ID.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The Hotspot profile ID.

Request body:

- `application/json` — XiqHotspotProfileRequest

Responses:

- `200` — OK

## DELETE `/hotspot-profiles/{id}`

Operation: `deleteHotspotProfile`

Delete Hotspot profile by ID

Delete the existing Hotspot profile by the profile ID.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The Hotspot profile ID

Responses:

- `200` — OK

## GET `/hiq/context`

Operation: `getHiqContext`

Get HIQ context

Get the current effective HIQ context for reading or creating data in organizations. Appliable when HIQ is enabled.

Tags: `HIQ`

Responses:

- `200` — OK

## PUT `/hiq/context`

Operation: `setHiqContext`

Set HIQ context

Set the current effective HIQ context for reading or creating data in organizations. Only HIQ Admin can performance this operation when HIQ is enabled.

Tags: `HIQ`

Request body:

- `application/json` — XiqHiqContext

Responses:

- `200` — OK

## GET `/hiq/context/reading`

Operation: `getReadingOrgIds`

Get organizations for reading data

Get organizations for reading data (Empty list means reading data from all organizations in the HIQ). Appliable when HIQ is enabled.

Tags: `HIQ`

Responses:

- `200` — OK

## PUT `/hiq/context/reading`

Operation: `setReadingOrgIds`

Set organizations for reading data

Set organization for reading data (Empty list means reading data from all organizations in the HIQ). Only HIQ Admin can performance this operation.

Tags: `HIQ`

Request body:

- `application/json` — array

Responses:

- `200` — OK

## GET `/hiq/context/creating`

Operation: `getCreatingOrgId`

Get organization for creating new data

Get organization for creating new data (Only one organization is active for creating new data). Appliable when HIQ is enabled.

Tags: `HIQ`

Responses:

- `200` — OK

## PUT `/hiq/context/creating`

Operation: `setCreatingOrgId`

Set organization for creating new data

Set organization for creating new data (Only one organization is active for creating new data). Only HIQ Admin can performance this operation when HIQ is enabled.

Tags: `HIQ`

Request body:

- `application/json` — integer

Responses:

- `200` — OK

## GET `/floor/afc/details`

Operation: `getFloorAfcProperties`

AFC Related Floor Height and Accuracy data

Tags: `AFC`

Parameters:

- `ownerId` query, required (integer) — Owner Id
- `floorId` query, required (integer) — The Id of the floor

Responses:

- `200` — OK

## POST `/floor/afc/details`

Operation: `addFloorAfcProperties`

AFC Related Floor and AP Height and Accuracy data

Tags: `AFC`

Request body:

- `application/json` — XiqAfcFloorDetailsCreateRequest

Responses:

- `200` — OK

## PUT `/floor/afc/details`

Operation: `updateFloorAfcProperties`

AFC Related Floor and AP Height and Accuracy data

Tags: `AFC`

Request body:

- `application/json` — XiqAfcFloorDetails

Responses:

- `200` — OK

## PUT `/endusers/{id}`

Operation: `updateEndUser`

Update an end user

Update a specific end user.

Tags: `Configuration - User Management`

Parameters:

- `id` path, required (integer) — The end user ID

Request body:

- `application/json` — XiqUpdateEndUserRequest

Responses:

- `200` — OK

## DELETE `/endusers/{id}`

Operation: `deleteSsidUser`

Delete end user by ID

Delete a specific end user.

Tags: `Configuration - User Management`

Parameters:

- `id` path, required (integer) — The end user ID

Responses:

- `200` — OK

## PUT `/devices/{id}/visible`

Operation: `updateDeviceVisible`

Update the visible status of a device in a floor

Tags: `Device`

Parameters:

- `id` path, required (integer) — The device ID
- `visible` query, required (boolean) — The new visible status of a device in a floor

Responses:

- `200` — OK

## GET `/devices/{id}/radio-operating-mode`

Operation: `getDeviceRadioOperatingMode`

Get the device radio operating mode

Get the device radio operating mode by device ID.

Tags: `Device`

Parameters:

- `id` path, required (integer) — The device ID

Responses:

- `200` — OK

## PUT `/devices/{id}/radio-operating-mode`

Operation: `configureDeviceRadioOperatingMode`

Configure radio operating mode of a device

Configure the device-specific radio operating mode settings at device level

Tags: `Device`

Parameters:

- `id` path, required (integer) — The device ID

Request body:

- `application/json` — XiqDeviceRadioOperatingMode

Responses:

- `200` — OK

## GET `/devices/{id}/network-policy`

Operation: `getDeviceNetworkPolicy`

Get network policy for a device

Get the network policy for a specific device.

Tags: `Device`

Parameters:

- `id` path, required (integer) — The device ID

Responses:

- `200` — The network policy assigned to the device.
- `204` — The device exists but has no network policy assigned.
- `400` — The request was malformed.
- `401` — The caller is not authenticated.
- `403` — The caller may not read this device.
- `404` — No device exists with the given identifier.
- `500` — Unexpected server error.

## PUT `/devices/{id}/network-policy`

Operation: `assignDeviceNetworkPolicy`

Assign network policy to a device

Assign a network policy to a specific device.

Tags: `Device`

Parameters:

- `id` path, required (integer) — The device ID
- `networkPolicyId` query, required (integer) — The network policy ID to assign

Responses:

- `200` — OK

## DELETE `/devices/{id}/network-policy`

Operation: `revokeDeviceNetworkPolicy`

Revoke network policy for a device

Revoke the assigned network policy for a specific device.

Tags: `Device`

Parameters:

- `id` path, required (integer) — The device ID

Responses:

- `200` — OK

## PUT `/devices/{id}/mobileapp/gps`

Operation: `mobileappGpsSettings`

Update AP GPS settings

Tags: `Device`

Parameters:

- `id` path, required (integer) — The device ID

Request body:

- `application/json` — XiqMobileappGpsSettingsRequest

Responses:

- `200` — OK

## GET `/devices/{id}/location`

Operation: `getDeviceLocation`

Get location for a device

Get the location info for a specific device.

Tags: `Device`

Parameters:

- `id` path, required (integer) — The device ID

Responses:

- `200` — OK

## PUT `/devices/{id}/location`

Operation: `assignDeviceLocation`

Assign location to a device

Assign a location to a specific device with extra map and geographical properties.

Tags: `Device`

Parameters:

- `id` path, required (integer) — The device ID

Request body:

- `application/json` — XiqDeviceLocationAssignment

Responses:

- `200` — OK

## DELETE `/devices/{id}/location`

Operation: `revokeDeviceLocation`

Revoke location for a device

Revoke the assigned location for a specific device.

Tags: `Device`

Parameters:

- `id` path, required (integer) — The device ID

Responses:

- `200` — OK

## PUT `/devices/{id}/hostname`

Operation: `changeHostname`

Change hostname for a device

Change hostname for a specific device.

Tags: `Device`

Parameters:

- `id` path, required (integer) — The device ID
- `hostname` query, required (string) — The new hostname

Responses:

- `200` — OK

## GET `/devices/{id}/ftm-settings`

Operation: `getFtmSettings`

Get FTM Settings by device ID

Get FTM Settings for the specified device ID.

Tags: `Device`

Parameters:

- `id` path, required (integer) — The device ID

Responses:

- `200` — OK

## PUT `/devices/{id}/ftm-settings`

Operation: `configureFtmSettings`

Configure (create / update) device FTM Settings

Configure (create / update) device FTM Settings.

Tags: `Device`

Parameters:

- `id` path, required (integer) — The device ID

Request body:

- `application/json` — XiqFtmSettingsRequest

Responses:

- `200` — OK

## DELETE `/devices/{id}/ftm-settings`

Operation: `deleteFtmSettings`

Delete FTM Settings by device ID

Delete FTM Settings by device ID.

Tags: `Device`

Parameters:

- `id` path, required (integer) — The device ID

Responses:

- `200` — OK

## PUT `/devices/{id}/description`

Operation: `changeDeviceDescription`

Change description for a device

Change description for a specific device.

Tags: `Device`

Parameters:

- `id` path, required (integer) — The device ID

Request body:

- `text/plain` — string

Responses:

- `200` — OK

## GET `/devices/{id}/client-monitor`

Operation: `getDeviceClientMonitor`

Get client monitor setting for a device

Get the client monitor info for a specific device.

Tags: `Device`

Parameters:

- `id` path, required (integer) — The device ID

Responses:

- `200` — OK

## PUT `/devices/{id}/client-monitor`

Operation: `assignDeviceClientMonitor`

Assign client monitor setting to a device

Assign a client monitor to a specific device with extra map and geographical properties.

Tags: `Device`

Parameters:

- `id` path, required (integer) — The device ID

Request body:

- `application/json` — XiqDeviceClientMonitor

Responses:

- `200` — OK

## DELETE `/devices/{id}/client-monitor`

Operation: `revokeDeviceClientMonitor`

Revoke client monitor setting for a device

Revoke the assigned client monitor for a specific device.

Tags: `Device`

Parameters:

- `id` path, required (integer) — The device ID

Responses:

- `200` — OK

## PUT `/devices/radius-proxy/:assign`

Operation: `assignDevicesRadiusProxy`

Assign RADIUS proxy to devices

Assign a RADIUS proxy to multiple devices.

Tags: `Device`

Parameters:

- `ids` query, required (array) — The device IDs
- `radiusProxyId` query, required (integer) — The RADIUS proxy ID to assign

Responses:

- `200` — OK

## PUT `/devices/ibeacon`

Operation: `changeDevicesIbeacon`

Change iBeacon settings for devices

Update the existing or create new iBeacon settings for multiple devices.

Tags: `Device`

Request body:

- `application/json` — XiqChangeDevicesIbeaconRequest

Responses:

- `200` — OK

## GET `/deployments/{deploymentId}`

Operation: `getDeploymentDetailsById`

Get deployment details by Id

Get deployment schedule across multiple sites

Tags: `Configuration - Deployment`

Parameters:

- `deploymentId` path, required (integer) — The deployment ID

Responses:

- `200` — OK

## PUT `/deployments/{deploymentId}`

Operation: `updateFirmwareUpgradeSchedule`

Update schedule with deployment ID

Update deployment configuration across multiple sites

Tags: `Configuration - Deployment`

Parameters:

- `deploymentId` path, required (integer) — The deployment ID

Request body:

- `application/json` — XiqUpdateFirmwareUpgradeRequest

Responses:

- `200` — OK

## DELETE `/deployments/{deploymentId}`

Operation: `deleteFirmwareUpgradeSchedule`

Delete the deployment schedule by ID

Delete firmware and deployment configuration upgrade schedule.

Tags: `Configuration - Deployment`

Parameters:

- `deploymentId` path, required (integer) — The deployment ID

Responses:

- `200` — OK

## PUT `/credential-distribution-groups/{id}`

Operation: `updateCredentialDistributionGroup`

Update Credential Distribution Group by ID

Update an existing Credential Distribution Group by the specified ID.

Tags: `Administration`

Parameters:

- `id` path, required (integer) — The Credential Distribution Group ID.

Request body:

- `application/json` — XiqCredentialDistributionGroupUpdateRequest

Responses:

- `200` — OK

## PUT `/copilot/anomalies/update-device-action`

Operation: `updateCopilotAnomaliesDevicesAction`

[LRO] Update Anomalies and Devices

Update Anomalies and Devices.

Tags: `Copilot - Anomalies`

Parameters:

- `async` query, optional (boolean) — Whether to enable async mode

Request body:

- `application/json` — XiqUpdateAnomaliesAndDevicesRequest

Responses:

- `200` — OK

## PUT `/copilot/anomalies/update-action`

Operation: `updateAnomalyAction`

Tags: `Copilot - Anomalies`

Request body:

- `application/json` — XiqAnomaliesUpdateActionRequest

Responses:

- `200` — OK

## PUT `/copilot/anomalies/devices/update-action`

Operation: `updateAnomalyDeviceAction`

Tags: `Copilot - Anomalies`

Request body:

- `application/json` — XiqAnomaliesDeviceUpdateActionRequest

Responses:

- `200` — OK

## PUT `/copilot/anomalies/devices/feedback`

Operation: `updateAnomaliesFeedback`

Tags: `Copilot - Anomalies`

Request body:

- `application/json` — XiqAnomaliesFeedbackRequest

Responses:

- `200` — OK

## PUT `/clients/alias`

Operation: `setClientsAliases`

Set the aliases for multiple clients

Bulk update the aliases for multiple clients based on the mac addresses. Empty or null alias value deletes the previous client alias.

Tags: `Client`

Request body:

- `application/json` — array

Responses:

- `200` — OK

## GET `/client-monitor-profiles/{id}`

Operation: `getClientMonitorProfile`

Get client monitor profile by ID

Get client monitor profile details for the specified ID.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The client monitor profile ID

Responses:

- `200` — OK

## PUT `/client-monitor-profiles/{id}`

Operation: `updateClientMonitorProfile`

Update client monitor profile

Update an existing client monitor profile.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The client monitor profile ID.

Request body:

- `application/json` — XiqUpdateClientMonitorProfileRequest

Responses:

- `200` — OK

## DELETE `/client-monitor-profiles/{id}`

Operation: `deleteClientMonitorProfile`

Delete an client monitor profile by ID

Delete an existing client monitor profile by ID.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The client monitor profile ID

Responses:

- `200` — OK

## GET `/classification-rules/{id}`

Operation: `getClassificationRule`

Get a classification rule by ID

Get a specific classification rule.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The classification Rule ID

Responses:

- `200` — OK

## PUT `/classification-rules/{id}`

Operation: `updateClassificationRule`

Update classification rule

Update the exist classification rule.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The classification rule ID

Request body:

- `application/json` — XiqUpdateClassificationRuleRequest

Responses:

- `200` — OK

## DELETE `/classification-rules/{id}`

Operation: `deleteClassificationRule`

Delete classification rule by ID

Delete an existing classification rule by ID.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The classification rule ID

Responses:

- `200` — OK

## GET `/certificate-bundles/{id}`

Operation: `getCertificateBundle`

Get Certificate Bundle by ID

Get Certificate Bundle for the specified ID.

Tags: `Configuration - Certificate`

Parameters:

- `id` path, required (integer) — The Certificate Bundle ID

Responses:

- `200` — OK

## PUT `/certificate-bundles/{id}`

Operation: `updateCertificateBundle`

Update Certificate Bundle by ID

Update the existing Certificate Bundle by the profile ID.

Tags: `Configuration - Certificate`

Parameters:

- `id` path, required (integer) — The Certificate Bundle ID.

Request body:

- `application/json` — XiqUpdateCertificateBundleRequest

Responses:

- `200` — OK

## DELETE `/certificate-bundles/{id}`

Operation: `deleteCertificateBundle`

Delete Certificate Bundle by ID

Delete the existing Certificate Bundle by the ID.

Tags: `Configuration - Certificate`

Parameters:

- `id` path, required (integer) — The Certificate Bundle ID

Responses:

- `200` — OK

## GET `/ccgs/{id}`

Operation: `getCloudConfigGroup`

Get a cloud config group

Get cloud config group info for the specified ID.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The cloud config group ID

Responses:

- `200` — OK

## PUT `/ccgs/{id}`

Operation: `updateCloudConfigGroup`

Update cloud config group information

Update the cloud config group details having the specified ID.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The cloud config group ID

Request body:

- `application/json` — XiqUpdateCloudConfigGroupRequest

Responses:

- `200` — OK

## DELETE `/ccgs/{id}`

Operation: `deleteCloudConfigGroup`

Delete a cloud config group

Delete a specific cloud config group by ID.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The cloud config group ID

Responses:

- `200` — OK

## GET `/alert-subscriptions/webhooks/{id}`

Operation: `getAlertWebhookSubscription`

Get alert webhook subscription

Get an exist alert webhook subscription.

Tags: `Alert`

Parameters:

- `id` path, required (integer) — The alert webhook subscription ID

Responses:

- `200` — OK

## PUT `/alert-subscriptions/webhooks/{id}`

Operation: `updateAlertWebhookSubscription`

Update alert webhook subscription

Update alert webhook subscription.

Tags: `Alert`

Parameters:

- `id` path, required (integer) — The alert webhook subscription ID

Request body:

- `application/json` — XiqUpdateAlertWebhookSubscriptionRequest

Responses:

- `200` — OK

## DELETE `/alert-subscriptions/webhooks/{id}`

Operation: `deleteAlertWebhookSubscription`

Delete alert webhook subscription

Delete an exist alert webhook subscription.

Tags: `Alert`

Parameters:

- `id` path, required (integer) — The alert webhook subscription ID

Responses:

- `200` — OK

## GET `/alert-subscriptions/servicenow/{id}`

Operation: `getServiceNowSubscription`

Get a specific ServiceNow subscription

Get ServiceNow subscription info for a specific ServiceNow account.

Tags: `Alert`

Parameters:

- `id` path, required (integer) — The unique identifier

Responses:

- `200` — OK

## PUT `/alert-subscriptions/servicenow/{id}`

Operation: `updateServiceNowSubscription`

Update ServiceNow subscription

Update ServiceNow subscription.

Tags: `Alert`

Parameters:

- `id` path, required (integer) — The unique identifier

Request body:

- `application/json` — XiqUpdateAlertServiceNowSubscriptionRequest

Responses:

- `200` — OK

## PATCH `/alert-subscriptions/servicenow/{id}`

Operation: `patchServiceNowSubscription`

Partial or full update ServiceNow subscription

Partial or full update ServiceNow subscription.

Tags: `Alert`

Parameters:

- `id` path, required (integer) — The unique identifier

Request body:

- `application/json` — XiqPatchAlertServiceNowSubscriptionRequest

Responses:

- `200` — OK

## GET `/alert-subscriptions/emails/{id}`

Operation: `getAlertEmailSubscription`

Get alert email subscription

Get an exist alert email subscription.

Tags: `Alert`

Parameters:

- `id` path, required (integer) — The alert email subscription ID

Responses:

- `200` — OK

## PUT `/alert-subscriptions/emails/{id}`

Operation: `updateAlertEmailSubscription`

Update alert email subscription

Update alert email subscription.

Tags: `Alert`

Parameters:

- `id` path, required (integer) — The alert email subscription ID

Request body:

- `application/json` — XiqUpdateAlertEmailSubscriptionRequest

Responses:

- `200` — OK

## DELETE `/alert-subscriptions/emails/{id}`

Operation: `deleteAlertEmailSubscription`

Delete alert email subscription

Delete an exist alert email subscription.

Tags: `Alert`

Parameters:

- `id` path, required (integer) — The alert email subscription ID

Responses:

- `200` — OK

## GET `/alert-policies/{policyId}/rules/{ruleId}`

Operation: `getAlertRule`

Get details of an alert rule

Get the full details of an alert rule's state. Users can obtain a rule ID by calling #_get_alert_policy first.The returned rule ID might be different from a predefined rule ID provided as a path parameter when the user overrides the predefined rule

Tags: `Alert`

Parameters:

- `policyId` path, required (integer) — The policy ID
- `ruleId` path, required (integer) — The rule ID

Responses:

- `200` — OK

## PUT `/alert-policies/{policyId}/rules/{ruleId}`

Operation: `updateAlertRule`

Update an alert rule

Update the state of an alert rule. Users can obtain a rule ID by calling #_get_alert_policy first.If all changes adhere to a predetermined rule, a new rule will be duplicated from the predefined one, and all changes will be applied to the newly cloned rule. As a result, users might receive a new rule ID that differs from the one provided as a path parameter.

Tags: `Alert`

Parameters:

- `policyId` path, required (integer) — The policy ID
- `ruleId` path, required (integer) — The rule ID

Request body:

- `application/json` — XiqUpdateAlertRuleRequest

Responses:

- `200` — OK

## GET `/alert-policies/{id}`

Operation: `getAlertPolicy`

Get details of an alert policy

Get the details related to a specific alert policy, given the policy's identifier.

Tags: `Alert`

Parameters:

- `id` path, required (integer) — The policy ID

Responses:

- `200` — OK

## PUT `/alert-policies/{id}`

Operation: `updateAlertPolicy`

Update a site-based alert policy

Delete an alert policy. All the associated alert rules will be deleted as well. The global policy cannot be deleted.

Tags: `Alert`

Parameters:

- `id` path, required (integer) — The policy ID

Request body:

- `application/json` — XiqAlertPolicyFilter

Responses:

- `200` — OK

## DELETE `/alert-policies/{id}`

Operation: `deleteAlertPolicy`

Delete a site-based alert policy

Modify a site-based alert policy's details, including the policy name and sites. The global policy cannot be updated. The sites can be obtained from the alerts/sites API.

Tags: `Alert`

Parameters:

- `id` path, required (integer) — The policy ID

Responses:

- `200` — OK

## GET `/account/viq/default-device-password`

Operation: `getDefaultDevicePassword`

Get the default device password in the account

Get the default device password in the account.

Tags: `Account`

Responses:

- `200` — OK

## PUT `/account/viq/default-device-password`

Operation: `updateDefaultDevicePassword`

Update the default device password in the account

Update the default device password in the global setting for accessing the console/shell of the devices.

Tags: `Account`

Request body:

- `application/json` — string

Responses:

- `200` — OK

## PUT `/account/vhm/setting/{id}`

Operation: `updateVhmSetting`

Update Vhm Setting

Update an existing Vhm Setting.

Tags: `Account`

Parameters:

- `id` path, required (integer) — The Vhm Setting ID.

Request body:

- `application/json` — XiqUpdateVhmSettingRequest

Responses:

- `200` — OK

## GET `/vlan-profiles`

Operation: `listVlanProfiles`

List VLAN profiles

Get a page of VLAN profiles.

Tags: `Configuration - Basic`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100

Responses:

- `200` — OK

## POST `/vlan-profiles`

Operation: `createVlanProfile`

Create VLAN profile

Create a new VLAN profile.

Tags: `Configuration - Basic`

Request body:

- `application/json` — XiqCreateVlanProfileRequest

Responses:

- `201` — Created

## POST `/vlan-profiles/:delete`

Operation: `deleteVlanProfiles`

[LRO] Delete VLAN profiles

Delete VLAN profiles.

Tags: `Configuration - Basic`

Parameters:

- `async` query, optional (boolean) — Whether to enable async mode

Request body:

- `application/json` — XiqVlanProfileFilter

Responses:

- `200` — OK

## GET `/users`

Operation: `listUsers`

List all users

List users with pagination.

Tags: `User`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100

Responses:

- `200` — OK

## POST `/users`

Operation: `createUser`

Create new user

Create a new user to access.

Tags: `User`

Request body:

- `application/json` — XiqCreateUserRequest

Responses:

- `201` — Created

## POST `/users/type-distribution`

Operation: `getUserTypeDistribution`

Get user type distribution

User type distribution and total connected users

Tags: `User`

Parameters:

- `startTime` query, required (integer)
- `endTime` query, required (integer)

Request body:

- `application/json` — RmUserFilterRequest

Responses:

- `200` — OK

## POST `/users/grid`

Operation: `listUsersGrid`

List Users

Returns a paginated list of users with support for search, filter, and sort.

Tags: `User`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 500
- `search` query, optional (string) — The search string
- `startTime` query, required (integer)
- `endTime` query, required (integer)

Request body:

- `application/json` — RmUserGridRequest

Responses:

- `200` — OK

## POST `/users/grid-export`

Operation: `exportToCsv`

Export the Users grid data

Export the Users grid data as a CSV file.

Tags: `User`

Parameters:

- `search` query, optional (string) — The search string
- `startTime` query, required (integer)
- `endTime` query, required (integer)
- `timezoneOffset` query, optional (integer) — timezone offset

Request body:

- `application/json` — RmUserGridRequest

Responses:

- `200` — OK

## POST `/users/filter-metadata`

Operation: `listUserGridFilterMetadata`

List user grid filter metadata

Lists of values for user grid filters

Tags: `User`

Parameters:

- `startTime` query, required (integer)
- `endTime` query, required (integer)

Request body:

- `application/json` — RmUserFilterRequest

Responses:

- `200` — OK

## GET `/users/external`

Operation: `listExternalUsers`

List external access users

List a page of external access users.

Tags: `User`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100

Responses:

- `200` — OK

## POST `/users/external`

Operation: `grantExternalUser`

Grant external access

Grant external access to a specific user.

Tags: `User`

Request body:

- `application/json` — XiqGrantExternalUserRequest

Responses:

- `200` — OK

## POST `/users/data-usage`

Operation: `getUserDataUsage`

Get user data usage

Returns data usage in bytes for each user.

Tags: `User`

Parameters:

- `startTime` query, required (integer)
- `endTime` query, required (integer)

Request body:

- `application/json` — RmUserFilterRequest

Responses:

- `200` — OK

## GET `/usergroups`

Operation: `listUserGroups`

List user groups

List a page of user groups.

Tags: `Configuration - User Management`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `password_db_location` query, optional (XiqPasswordDbLocation) — The password DB location
- `password_type` query, optional (XiqPasswordType) — The password type

Responses:

- `200` — OK

## POST `/usergroups`

Operation: `createUserGroup`

Create user group

Create a new user group.

Tags: `Configuration - User Management`

Request body:

- `application/json` — XiqCreateUserGroupRequest

Responses:

- `200` — OK

## GET `/user-profiles`

Operation: `listUserProfiles`

List user profiles

List a page of user profiles.

Tags: `Configuration - Policy`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100

Responses:

- `200` — OK

## POST `/user-profiles`

Operation: `createUserProfile`

Create a user profile

Create a new user profile.

Tags: `Configuration - Policy`

Request body:

- `application/json` — XiqCreateUserProfileRequest

Responses:

- `201` — Created

## POST `/user-profiles/{id}/mac-firewall-policies/:detach`

Operation: `detachMacFirewallPolicyFromUserProfile`

Detach MAC Firewall Policy from an User Profile

Detach MAC Firewall from an User Profile.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The User Profile ID

Request body:

- `application/json` — XiqAttachMacFirewallPolicyToUserProfileRequest

Responses:

- `200` — OK

## POST `/user-profiles/{id}/mac-firewall-policies/:attach`

Operation: `attachMacFirewallPolicyToUserProfile`

Attach MAC Firewall Policy to an User Profile

Attach MAC Firewall to an User Profile.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The User Profile ID

Request body:

- `application/json` — XiqAttachMacFirewallPolicyToUserProfileRequest

Responses:

- `200` — OK

## POST `/user-profiles/{id}/ip-firewall-policies/:detach`

Operation: `detachIpFirewallPolicyFromUserProfile`

Detach IP Firewall Policy from an User Profile

Detach IP Firewall from an User Profile.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The User Profile ID

Request body:

- `application/json` — XiqAttachIpFirewallPolicyToUserProfileRequest

Responses:

- `200` — OK

## POST `/user-profiles/{id}/ip-firewall-policies/:attach`

Operation: `attachIpFirewallPolicyToUserProfile`

Attach IP Firewall Policy to an User Profile

Attach IP Firewall to an User Profile.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The User Profile ID

Request body:

- `application/json` — XiqAttachIpFirewallPolicyToUserProfileRequest

Responses:

- `200` — OK

## GET `/user-profile-assignments`

Operation: `listUserProfileAssignments`

List user profile assignments

List a page of user profile assignments.

Tags: `Configuration - Policy`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100

Responses:

- `200` — OK

## POST `/user-profile-assignments`

Operation: `createUserProfileAssignment`

Create a user profile assignment

Create a new user profile assignment.

Tags: `Configuration - Policy`

Request body:

- `application/json` — XiqCreateUserProfileAssignmentRequest

Responses:

- `201` — Created

## POST `/user-folder-preferences/{folderId}`

Operation: `saveUserFolderPreferences`

Save user folder preferences values.

Persists given preferences values.

Tags: `Use Folder Preferences`

Parameters:

- `folderId` path, required (integer) — The id of the folder

Request body:

- `application/json`

Responses:

- `200` — OK

## GET `/tunnel-concentrators`

Operation: `listTunnelConcentrators`

List Tunnel Concentrators

List a page of Tunnel Concentrators.

Tags: `Configuration - Network`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100

Responses:

- `200` — OK

## POST `/tunnel-concentrators`

Operation: `createTunnelConcentrator`

Create a Tunnel Concentrator

Create a new Tunnel Concentrator.

Tags: `Configuration - Network`

Request body:

- `application/json` — XiqTunnelConcentratorRequest

Responses:

- `201` — Created

## POST `/tunnel-concentrators/{id}/license/upload`

Operation: `uploadTunnelConcentratorLicense`

Upload Tunnel Concentrator license

Upload a license file for the specified Tunnel Concentrator device.

Tags: `Configuration - Network`

Parameters:

- `id` path, required (integer) — The Tunnel Concentrator device ID

Request body:

- `application/json` — XiqTunnelConcentratorLicenseUploadRequest

Responses:

- `200` — OK

## GET `/tcap-profiles`

Operation: `listTcap`

List TCAPs

List a page of TCAPS.

Tags: `Configuration - Network`

Responses:

- `200` — OK

## POST `/tcap-profiles`

Operation: `createTcap`

Tags: `Configuration - Network`

Request body:

- `application/json` — XiqTunnelConcentratorAddressPoolRequest

Responses:

- `201` — Created

## POST `/switch-inspector/diagnostics`

Operation: `getDiagnostics`

Switch Inspector Panel Diagnostics

Returns the switch inspector panel diagnostics widget data (Device Health, Usage and Capacity and Client Health issue counts)

Tags: `Switch Inspector Panel`

Parameters:

- `deviceId` query, required (integer) — The ID of the device

Responses:

- `200` — OK

## GET `/subscriptions/webhook`

Operation: `list`

List webhook subscriptions

List all webhook subscriptions.

Tags: `Notification`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `order` query, optional (XiqSortOrder) — The sort order (descending by default)
- `keyword` query, optional (string) — The keyword - url

Responses:

- `200` — OK

## POST `/subscriptions/webhook`

Operation: `createSubscriptions`

Create webhook subscriptions

Create multiple webhook subscriptions.

Tags: `Notification`

Request body:

- `application/json` — array

Responses:

- `202` — Accepted

## POST `/ssids/{id}/user-profile/:attach`

Operation: `attachUserProfileToSsid`

Attach user profile to an SSID

Attach user profile to an SSID.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The SSID ID

Request body:

- `application/json` — integer

Responses:

- `200` — OK

## POST `/ssids/{id}/user-profile-assignment/:attach`

Operation: `attachUserProfileAssignmentToSsid`

Attach user profile assignment to an SSID

Attach user profile assignment to an SSID.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The SSID ID

Request body:

- `application/json` — XiqAttachUPAssignmentRequest

Responses:

- `200` — OK

## POST `/ssids/{id}/radius-server-group/:attach`

Operation: `attachRadiusServerGroupToSsid`

Attach radius server group to an SSID

Attach radius server group to an SSID.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The SSID ID

Request body:

- `application/json` — integer

Responses:

- `200` — OK

## POST `/ssids/{id}/radius-client-profile/:attach`

Operation: `attachRadiusClientProfileToSsid`

Attach RADIUS client profile to an SSID

Attach RADIUS client profile to an SSID.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The SSID ID

Request body:

- `application/json` — integer

Responses:

- `200` — OK

## POST `/ssids/{id}/cwp/:enable`

Operation: `enableSsidCwp`

Enable and attach the CWP on the SSID

Enable and attach the CWP on the SSID.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The SSID ID

Request body:

- `application/json` — integer

Responses:

- `200` — OK

## POST `/ssids/{id}/cwp/:disable`

Operation: `disableSsidCwp`

Disable the CWP on the SSID

Disable the CWP on the SSID.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The SSID ID

Responses:

- `200` — OK

## POST `/ssids/{id}/cwp/:attach`

Operation: `attachCwpToSsid`

Attach CWP to an SSID

Attach CWP to an SSID.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The SSID ID

Request body:

- `application/json` — integer

Responses:

- `200` — OK

## POST `/ssids/{id}/client-monitor-profile/:attach`

Operation: `attachClientMonitorProfileToSsid`

Attach client monitor profile to an SSID

Attach client monitor profile to an SSID.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The SSID ID

Request body:

- `application/json` — XiqAttachClientMonitorProfileRequest

Responses:

- `200` — OK

## POST `/ssids/{id}/:rename`

Operation: `renameSsid`

Rename SSID (Wireless name)

Change SSID broadcast name (Wireless name).

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The SSID ID

Request body:

- `application/json` — string

Responses:

- `200` — OK

## POST `/site/spectrum`

Operation: `getAfcSpectrumPerSite`

Tags: `AFC`

Parameters:

- `IsEmptyList` query, required (boolean)

Request body:

- `application/json` — XiqGetAfcSpectrumForSiteApsRequest

Responses:

- `200` — OK

## POST `/rtts`

Operation: `createRttsSession`

Create

Tags: `rtts-endpoint`

Parameters:

- `ownerId` query, required (integer) — Owner Id

Request body:

- `application/json` — RttsSessionDevices

Responses:

- `200` — OK

## POST `/rtts/supported-devices`

Operation: `listRttsSupportedDevices`

List RTTS supported devices

List RTTS supported devices for the specified location filter.

Tags: `rtts-endpoint`

Request body:

- `application/json` — RttsSupportedDevicesRequest

Responses:

- `200` — OK

## GET `/radsec-proxies`

Operation: `listRadsecProxies`

List RADSEC proxies

List a page of RADSEC proxy configurations.

Tags: `Configuration - Authentication`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100

Responses:

- `200` — OK

## POST `/radsec-proxies`

Operation: `createRadsecProxy`

Create RADSEC proxy configuration

Create a new RADSEC proxy configuration.

Tags: `Configuration - Authentication`

Request body:

- `application/json` — XiqCreateRadsecProxyRequest

Responses:

- `201` — Created

## GET `/radius-servers/internal`

Operation: `listInternalRadiusServers`

List all internal RADIUS servers

List all internal RADIUS servers configurations.

Tags: `Configuration - Authentication`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100

Responses:

- `200` — OK

## POST `/radius-servers/internal`

Operation: `createInternalRadiusServer`

Create internal RADIUS server configuration

Create a new internal RADIUS server configuration.

Tags: `Configuration - Authentication`

Request body:

- `application/json` — XiqCreateInternalRadiusServerRequest

Responses:

- `201` — Created

## DELETE `/radius-servers/internal`

Operation: `deleteBulkInternalRadiusServer`

[LRO] Delete internal RADIUS server configuration

Delete an existing internal RADIUS server configuration by ID.

Tags: `Configuration - Authentication`

Parameters:

- `ids` query, required (array) — The internal RADIUS server IDs to be delete, min = 1 ID, max = 100 IDs
- `async` query, optional (boolean) — Whether to enable async mode

Responses:

- `200` — OK

## GET `/radius-servers/external`

Operation: `listExternalRadiusServers`

List external RADIUS servers

List a page of external RADIUS server configurations.

Tags: `Configuration - Authentication`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `accessType` query, optional (XiqRadiusAccessType) — The access type: STANDARD, SECURE

Responses:

- `200` — OK

## POST `/radius-servers/external`

Operation: `createExternalRadiusServer`

Create external RADIUS server configuration

Create a new external RADIUS server configuration.

Tags: `Configuration - Authentication`

Request body:

- `application/json` — XiqCreateExternalRadiusServerRequest

Responses:

- `201` — Created

## GET `/radius-proxies`

Operation: `listRadiusProxies`

List RADIUS proxies

List a page of RADIUS proxy configurations.

Tags: `Configuration - Authentication`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100

Responses:

- `200` — OK

## POST `/radius-proxies`

Operation: `createRadiusProxy`

Create RADIUS proxy configuration

Create a new RADIUS proxy configuration.

Tags: `Configuration - Authentication`

Request body:

- `application/json` — XiqCreateRadiusProxyRequest

Responses:

- `201` — Created

## GET `/radius-client-objects`

Operation: `listRadiusClientObjects`

List RADIUS client objects

List a page of RADIUS client object configurations.

Tags: `Configuration - Authentication`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100

Responses:

- `200` — OK

## POST `/radius-client-objects`

Operation: `createRadiusClientObject`

Create RADIUS client object configuration

Create a new RADIUS client object configuration.

Tags: `Configuration - Authentication`

Request body:

- `application/json` — XiqCreateRadiusClientObjectRequest

Responses:

- `201` — Created

## GET `/radio-profiles`

Operation: `listRadioProfiles`

List radio profiles

List a page of radio profiles.

Tags: `Configuration - Policy`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100

Responses:

- `200` — OK

## POST `/radio-profiles`

Operation: `createRadioProfile`

Create a radio profile

Create a new radio profile.

Tags: `Configuration - Policy`

Request body:

- `application/json` — XiqCreateRadioProfileRequest

Responses:

- `201` — Created

## GET `/radio-profiles/mac-ouis`

Operation: `listRpMacOuiProfiles`

List MAC OUI profiles

List a page of MAC OUI profiles.

Tags: `Configuration - Policy`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100

Responses:

- `200` — OK

## POST `/radio-profiles/mac-ouis`

Operation: `createMacOuiProfile`

Create a MAC OUI profile

Create a new MAC OUI profile for radio usage optimization.

Tags: `Configuration - Policy`

Request body:

- `application/json` — XiqCreateRpMacOuiProfileRequest

Responses:

- `201` — Created

## GET `/pcgs/key-based`

Operation: `listKeyBasedPrivateClientGroups`

List Key-based Private Client Groups

List all Key-based Private Client Groups.

Tags: `Configuration - User Management`

Responses:

- `200` — OK

## POST `/pcgs/key-based`

Operation: `createKeyBasedPcgNetworkPolicy`

[LRO] Create a Key-based Private Client Group

Create a Key-based Private Client Group, including network policy, user, user group, SSID, etc.

Tags: `Configuration - User Management`

Parameters:

- `async` query, optional (boolean) — Whether to enable async mode

Request body:

- `application/json` — XiqInitKeyBasedPcgNetworkPolicyRequest

Responses:

- `200` — OK

## GET `/pcgs/key-based/network-policy-{policyId}/port-assignments`

Operation: `getPortAssignments`

Get device port assignments in network policy

Get port assignments for devices (currently support for AP150W & AP302W) in a network policy.

Tags: `Configuration - User Management`

Parameters:

- `policyId` path, required (integer) — The network policy ID

Responses:

- `200` — OK

## POST `/pcgs/key-based/network-policy-{policyId}/port-assignments`

Operation: `assignPorts`

Assign ports to devices in network policy

Assign ports for devices (currently support for AP150W & AP302W) in a network policy.

Tags: `Configuration - User Management`

Parameters:

- `policyId` path, required (integer) — The network policy ID

Request body:

- `application/json` — XiqPcgAssignPortsRequest

Responses:

- `200` — OK

## POST `/pcgs/key-based/network-policy-{policyId}/keys/:generate`

Operation: `generateKeys`

Generate shared keys for users in network policy

Generate/regenerate shared keys for specified users in a specific PCG-enable network policy.

Tags: `Configuration - User Management`

Parameters:

- `policyId` path, required (integer) — The network policy ID
- `userIds` query, required (array) — The user IDs

Responses:

- `202` — Accepted

## POST `/pcgs/key-based/network-policy-{policyId}/keys/:email`

Operation: `emailKeys`

Send keys to users in network policy via Email

Send keys to specified users in PCG-enabled network policy via Email.

Tags: `Configuration - User Management`

Parameters:

- `policyId` path, required (integer) — The network policy ID
- `userIds` query, required (array) — The user IDs

Responses:

- `202` — Accepted

## POST `/pcgs/key-based/network-policy-{policyId}/:onboard`

Operation: `onboardKeyBasedPrivateClientGroup`

[LRO] Onboard Key-based PCG in network policy

Onboard a Key-based Private Client Group for a specific network policy.

Tags: `Configuration - User Management`

Parameters:

- `policyId` path, required (integer) — The network policy ID
- `async` query, optional (boolean) — Whether to enable async mode

Request body:

- `application/json` — XiqOnboardKeyBasedPcgRequest

Responses:

- `200` — OK

## GET `/packetcaptures`

Operation: `listPacketCaptures`

List packet capture sessions

List packet captures with filters and pagination.

Tags: `Packet Capture`

Parameters:

- `searchString` query, optional (string) — The string to be searched in capture session name, interface name and device host name
- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 500
- `sortField` query, optional (XiqPacketCaptureSortField) — Sort field. Available values - NAME, START_TIME and STATUS
- `order` query, optional (XiqSortOrder) — Sort order (ascending by default)
- `fields` query, optional (array) — The packet capture fields to return

Responses:

- `200` — OK

## POST `/packetcaptures`

Operation: `createPacketCapture`

Create a new packet capture session

Create and start a new packet capture session with requested capture location and filter criteria.

Tags: `Packet Capture`

Request body:

- `application/json` — XiqPacketCapture

Responses:

- `200` — OK

## DELETE `/packetcaptures`

Operation: `deletePacketCaptures`

Delete packet capture sessions

Delete existing packet capture sessions and capture files by ID.

Tags: `Packet Capture`

Parameters:

- `ids` query, required (array) — The packet capture IDs

Responses:

- `200` — OK

## POST `/packetcaptures/{id}/:upload`

Operation: `uploadPacketCaptureFiles`

Upload a packet capture session's capture files

Upload the capture files from a packet capture session, if files previously failed to be uploaded to XIQ cloud.

Tags: `Packet Capture`

Parameters:

- `id` path, required (integer) — The packet capture ID

Responses:

- `200` — OK

## POST `/packetcaptures/{id}/:stop`

Operation: `stopPacketCapture`

Stop a packet capture session

Stop an active packet capture session.

Tags: `Packet Capture`

Parameters:

- `id` path, required (integer) — The packet capture ID

Request body:

- `application/json` — XiqCaptureStopRequest

Responses:

- `200` — OK

## POST `/operations/{operationId}/:cancel`

Operation: `cancelOperation`

Cancel Long-Running Operation (LRO)

When the cancelable is true in operation metadata the clients are allowed to send a cancel request to ask the backend to cancel the operation. The server makes its best effort to cancel the operation, but success is not guaranteed.

Tags: `Operation`

Parameters:

- `operationId` path, required (string) — The operation ID

Responses:

- `200` — OK

## POST `/ng-reports/timeseries`

Operation: `qoeDiagnosticsTimeSeriesData`

Get QoE Diagnostics Time Series Data

Retrieve QoE diagnostics time-series data for the selected metric using applicable filters

Tags: `NG Reports (Ondemand)`

Request body:

- `application/json` — XiqQoeDiagnosticsTimeSeriesFilters

Responses:

- `200` — OK

## POST `/ng-reports/tabledata`

Operation: `qoeDiagnosticsTableData`

Get QoE Diagnostics Table Data

Retrieve QoE diagnostics table data for the selected metric using applicable filters

Tags: `NG Reports (Ondemand)`

Request body:

- `application/json` — XiqQoeDiagnosticsTableDataFilters

Responses:

- `200` — OK

## GET `/ng-reports/scheduled/custom`

Operation: `listScheduledCustomReports`

List Custom Report Schedules

List custom report schedules with filters and pagination.

Tags: `NG Reports (Scheduled)`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 500
- `frequency` query, optional (array) — The frequency of the scheduled report (e.g., DAILY, WEEKLY, MONTHLY)
- `keyword` query, optional (string) — The keyword to search in the report name

Responses:

- `200` — OK

## POST `/ng-reports/scheduled/custom`

Operation: `createScheduledCustomReport`

Create a scheduled custom report

Create a new scheduled custom report with the provided details.

Tags: `NG Reports (Scheduled)`

Request body:

- `application/json` — XiqCustomReportRequest

Responses:

- `200` — OK

## DELETE `/ng-reports/scheduled/custom`

Operation: `deleteScheduledCustomReports`

Delete scheduled custom reports

Bulk delete scheduled custom reports by IDs.

Tags: `NG Reports (Scheduled)`

Parameters:

- `reportScheduleIds` query, required (array) — List of scheduled report IDs to delete

Responses:

- `200` — OK

## POST `/ng-reports/metadata/user`

Operation: `getUsersListForFilter`

List of Users for filtering

Gives List of Users for filtering

Tags: `NG Reports (Ondemand)`

Request body:

- `application/json` — XiqQoeMetadataUsersFilter

Responses:

- `200` — OK

## POST `/ng-reports/metadata/ssids`

Operation: `getSsisMetadata`

List of SSIDs for filtering

Please note: if you need to fetch all SSIDs configured in VIQ, send fetchAll as true; otherwise, send with start time and end time

Tags: `NG Reports (Ondemand)`

Parameters:

- `fetchAll` query, optional (boolean) — fetch all ssid

Request body:

- `application/json` — XiqQoeDiagnosticsSsidMetadataFilter

Responses:

- `200` — OK

## POST `/ng-reports/metadata/os`

Operation: `getOsFilterMetadata`

List of OS for filtering

Gives List of OS for filtering

Tags: `NG Reports (Ondemand)`

Request body:

- `application/json` — XiqQoeDiagnosticsChannelMetadataFilter

Responses:

- `200` — OK

## POST `/ng-reports/metadata/device`

Operation: `getDeviceListForFilter`

List of Devices for filtering

Gives List of Devices for filtering

Tags: `NG Reports (Ondemand)`

Request body:

- `application/json` — XiqQoeMetadataDeviceFilter

Responses:

- `200` — OK

## POST `/ng-reports/metadata/client`

Operation: `getClientListForFilter`

List of Clients for filtering

Gives List of Clients for filtering

Tags: `NG Reports (Ondemand)`

Request body:

- `application/json` — XiqQoeMetadataClientFilter

Responses:

- `200` — OK

## POST `/ng-reports/metadata/bands`

Operation: `getBandMetadata`

List of Band for filtering

Gives List of Band for filtering, please note there is no validation for start time and end time

Tags: `NG Reports (Ondemand)`

Request body:

- `application/json` — XiqQoeDiagnosticsBandMetadataFilter

Responses:

- `200` — OK

## POST `/ng-reports/metadata/application`

Operation: `getApplicationListForFilter`

List of Applications for filtering

Gives List of Applications for filtering

Tags: `NG Reports (Ondemand)`

Request body:

- `application/json` — XiqQoeMetadataApplicationFilter

Responses:

- `200` — OK

## POST `/ng-reports/downloads/reports`

Operation: `qoeDiagnosticsXlsxData`

Download the Reports

Download reports of Metrics

Tags: `NG Reports (Ondemand)`

Request body:

- `application/json` — XiqXlsxNgReportsDataFilters

Responses:

- `200` — OK

## GET `/network-services`

Operation: `listNetworkServices`

List Network Services

List a page of Network Services.

Tags: `Configuration - Network`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `name` query, optional (string) — Network Service name.
- `ipProtocol` query, optional (XiqNetworkIpProtocol) — IP Protocol, only for custom Application.
- `algType` query, optional (XiqNetworkAlgType) — Application Layer Gateway (ALG) type, only for custom Application.

Responses:

- `200` — OK

## POST `/network-services`

Operation: `createNetworkServices`

Create Network Services

Create a new Network Services.

Tags: `Configuration - Network`

Request body:

- `application/json` — XiqNetworkServiceRequest

Responses:

- `201` — Created

## GET `/network-policies`

Operation: `listNetworkPolices`

List network policies

List a page of network policies.

Tags: `Network Policy`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 2000
- `policyNames` query, optional (array) — The list of full network policy names to filter the query
- `keyword` query, optional (string) — The keyword to partial search by network policy name
- `fields` query, optional (array) — The network policy fields to return
- `view` query, optional (XiqNetworkPolicyView) — The views to return network policy fields (Check fields for each view at XiqNetworkPolicyView schema)

Responses:

- `200` — OK

## POST `/network-policies`

Operation: `createNetworkPolicy`

Create network policy

Create a new network policy.

Tags: `Network Policy`

Request body:

- `application/json` — XiqCreateNetworkPolicyRequest

Responses:

- `201` — Created

## POST `/network-policies/{id}/ssids/:remove`

Operation: `deleteSsidsFromNetworkPolicy`

Removes SSIDs from the network policy

Removing multiple SSIDs from the network policy.

Tags: `Network Policy`

Parameters:

- `id` path, required (integer) — The network policy ID

Request body:

- `application/json` — array

Responses:

- `200` — OK

## POST `/network-policies/{id}/ssids/:add`

Operation: `addSsidsToNetworkPolicy`

Add SSIDs to a network policy

Add SSIDs to a specific network policy.

Tags: `Network Policy`

Parameters:

- `id` path, required (integer) — The network policy ID

Request body:

- `application/json` — array

Responses:

- `200` — OK

## GET `/mac-object-profiles`

Operation: `listMacObjectProfiles`

List mac object profiles

List a page of mac object profiles.

Tags: `Configuration - Policy`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100

Responses:

- `200` — OK

## POST `/mac-object-profiles`

Operation: `createMacObject`

Create a mac object

Create a new mac object

Tags: `Configuration - Policy`

Request body:

- `application/json` — XiqCreateMacObjectRequest

Responses:

- `201` — Created

## GET `/mac-firewall-policies`

Operation: `listMacFirewallPolicies`

List MAC Firewall policies

List a page of MAC Firewall policies.

Tags: `Configuration - Policy`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100

Responses:

- `200` — OK

## POST `/mac-firewall-policies`

Operation: `createMacFirewallPolicy`

Create MAC Firewall policy

Create a new MAC Firewall policy.

Tags: `Configuration - Policy`

Request body:

- `application/json` — XiqMacFirewallPolicyRequest

Responses:

- `201` — Created

## POST `/mac-firewall-policies/{id}/mac-firewall-rule/:detach`

Operation: `detachServiceToMacFirewallPolicy`

Detach MAC Firewall Rule from MAC Firewall policy

Detach MAC Firewall Rule from MAC Firewall policy.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The MAC Firewall Policy ID

Request body:

- `application/json` — integer

Responses:

- `200` — OK

## POST `/mac-firewall-policies/{id}/mac-firewall-rule/:attach`

Operation: `attachServiceToMacFirewallPolicy`

Attach MAC Firewall Rule to MAC Firewall policy

Attach MAC Firewall Rule to MAC Firewall policy.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The MAC Firewall Policy ID

Request body:

- `application/json` — XiqMacFirewallRuleRequest

Responses:

- `200` — OK

## POST `/logs/audit/reports`

Operation: `auditLogsReport`

[LRO] Create audit logs report

Creates a report page of audit logs.

Tags: `Log`

Parameters:

- `sortField` query, optional (XiqAuditLogSortField) — The field for sorting
- `sortOrder` query, optional (XiqSortOrder) — The sorting order
- `categories` query, optional (array) — Audit category
- `username` query, optional (string) — The user login name
- `startTime` query, optional (integer) — The start time to query, epoch time in milliseconds since 1/1/1970, default is 0 if not specified or is negative
- `endTime` query, optional (integer) — The end time to query, epoch time in milliseconds since 1/1/1970, default is now if not specified or is negative, endTime - startTime must be no greater than 2592000000 (30 days)
- `timeZoneOffset` query, optional (integer) — The time zone off set
- `keyword` query, optional (string) — The case-insensitive keyword to search in description
- `async` query, optional (boolean) — Whether to enable async mode

Responses:

- `200` — OK

## POST `/logout`

Operation: `logout`

User logout (Revoke the current access token)

User logout, the current access token will be revoked and the following access with the same token will be immediately denied.

Tags: `Authentication`

Responses:

- `200` — OK

## POST `/login`

Operation: `login`

User login with username and password

Get access token via username and password authentication. The client must present Bearer token to access the protected API endpoints.The Bearer token should be present in the "Authorization" request header field and use the "Bearer" HTTP authentication scheme to transmit the access token.

Tags: `Authentication`

Request body:

- `application/json` — XiqLoginRequest

Responses:

- `200` — Successful operation
- `400` — Bad request
- `401` — UNAUTHORIZED

## POST `/locations`

Operation: `createLocation`

Create a location

Create a new location under the parent location.

Tags: `Location`

Request body:

- `application/json` — XiqCreateLocationRequest

Responses:

- `200` — OK

## GET `/locations/wall/type`

Operation: `getWallType`

Get wall types

Retrieve the list of wall types, including both predefined and custom ones.

Tags: `Location`

Responses:

- `200` — OK

## POST `/locations/wall/type`

Operation: `createWallType`

Create a wall type

Create a custom wall type.

Tags: `Location`

Request body:

- `application/json` — XiqCreateTypeRequest

Responses:

- `201` — Created

## GET `/locations/site`

Operation: `listSites`

List sites

List a page of sites by filter.

Tags: `Location`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `order` query, optional (XiqSortOrder) — The sort order by name (ascending by default)
- `name` query, optional (string) — List sites by name (case insensitive)
- `ids` query, optional (array) — List sites by IDs

Responses:

- `200` — OK

## POST `/locations/site`

Operation: `createSite`

Create a site

Create a new site under the site group.

Tags: `Location`

Request body:

- `application/json` — XiqCreateSiteRequest

Responses:

- `200` — OK

## POST `/locations/import/ekahau`

Operation: `startEkahauImport`

[LRO] Import one or more floors from an Ekahau archive

Import the specified Ekahau floor(s) from the provided archive.

Tags: `Location`

Parameters:

- `async` query, optional (boolean) — Whether to enable async mode.
- `floorAssociations` query, required (array) — Describes how Ekahau floors are imported into XIQ as floors in buildings.
- `outdoorSiteAssociations` query, required (array) — Describes how Ekahau floors are Imported into XIQ as outdoor sites in site groups.
- `importCustomApConfigurations` query, optional (boolean) — Whether to also import or not the custom AP configurations such as: Hostname, TX Power & Channel.

Request body:

- `multipart/form-data` — file

Responses:

- `200` — OK

## POST `/locations/floorplan`

Operation: `uploadFloorplan`

Upload floorplan

Upload the floorplan map for the VIQ.

Tags: `Location`

Request body:

- `multipart/form-data` — file

Responses:

- `200` — OK

## GET `/locations/floor`

Operation: `listFloors`

List floors

List a page of floors by filter.

Tags: `Location`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `order` query, optional (XiqSortOrder) — The sort order by name (ascending by default)
- `name` query, optional (string) — List floors by name (case insensitive)
- `ids` query, optional (array) — List floors by IDs

Responses:

- `200` — OK

## POST `/locations/floor`

Operation: `createFloor`

Create a floor

Create a new floor under the parent building.

Tags: `Location`

Request body:

- `application/json` — XiqCreateFloorRequest

Responses:

- `200` — OK

## GET `/locations/building`

Operation: `listBuildings`

List buildings

List a page of buildings by filter.

Tags: `Location`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `order` query, optional (XiqSortOrder) — The sort order by name (ascending by default)
- `name` query, optional (string) — List buildings by name (case insensitive)
- `ids` query, optional (array) — List buildings by IDs

Responses:

- `200` — OK

## POST `/locations/building`

Operation: `createBuilding`

Create a building

Create a new building under the parent site.

Tags: `Location`

Request body:

- `application/json` — XiqCreateBuildingRequest

Responses:

- `200` — OK

## POST `/locations/:init`

Operation: `initializeLocation`

Initialize organization location

Initialize the organization location hierarchy tree.

Tags: `Location`

Request body:

- `application/json` — XiqInitializeLocationRequest

Responses:

- `200` — OK

## GET `/ldap-servers`

Operation: `listLdapServers`

List LDAP servers

List a page of LDAP servers.

Tags: `Configuration - Authentication`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100

Responses:

- `200` — OK

## POST `/ldap-servers`

Operation: `createLdapServer`

Create LDAP server

Create a new LDAP server.

Tags: `Configuration - Authentication`

Request body:

- `application/json` — XiqCreateLdapServerRequest

Responses:

- `201` — Created

## GET `/l3-address-profiles`

Operation: `listL3AddressProfiles`

List L3 address profiles

List all L3 Address Profiles.

Tags: `Configuration - Policy`

Parameters:

- `addressType` query, required (string) — The address type

Responses:

- `200` — OK

## POST `/l3-address-profiles`

Operation: `createL3AddressProfile`

Create a L3 address profile

Create a new L3 address profile.

Tags: `Configuration - Policy`

Request body:

- `application/json` — XiqCreateL3AddressProfileRequest

Responses:

- `201` — Created

## GET `/ip-firewall-policies`

Operation: `listIpFirewallPolicies`

List IP Firewall policies

List a page of IP Firewall policies.

Tags: `Configuration - Policy`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100

Responses:

- `200` — OK

## POST `/ip-firewall-policies`

Operation: `createIpFirewallPolicy`

Create IP Firewall policy

Create a new IP Firewall policy.

Tags: `Configuration - Policy`

Request body:

- `application/json` — XiqIpFirewallPolicyRequest

Responses:

- `201` — Created

## POST `/ip-firewall-policies/{id}/ip-firewall-rule/:detach`

Operation: `detachServiceToIpFirewallPolicy`

Detach IP Firewall Rule from IP Firewall policy

Detach IP Firewall Rule from IP Firewall policy.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The IP Firewall Policy ID

Request body:

- `application/json` — integer

Responses:

- `200` — OK

## POST `/ip-firewall-policies/{id}/ip-firewall-rule/:attach`

Operation: `attachServiceToIpFirewallPolicy`

Attach IP Firewall Rule to IP Firewall policy

Attach IP Firewall Rule to IP Firewall policy.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The IP Firewall Policy ID

Request body:

- `application/json` — XiqIpFirewallRuleRequest

Responses:

- `200` — OK

## GET `/iot-profiles`

Operation: `listIotProfiles`

List IoT profiles

List a page of IoT profiles.

Tags: `Configuration - Policy`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `appId` query, optional (XiqIotApplicationId) — Application ID, e.g. THREAD_GATEWAY
- `appSupported` query, optional (XiqIotApplicationSupported) — Application Supported, e.g. SINGLE or MULTI

Responses:

- `200` — OK

## POST `/iot-profiles`

Operation: `createIotProfile`

Create a IoT profile

Create a new IoT profile.

Tags: `Configuration - Policy`

Request body:

- `application/json` — XiqIotProfileRequest

Responses:

- `201` — Created

## GET `/hotspot-service-provider-profiles`

Operation: `listHotspotServiceProviderProfiles`

List Hotspot Service Provider profiles

List a page of Hotspot Service Provider profiles.

Tags: `Configuration - Policy`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 500

Responses:

- `200` — OK

## POST `/hotspot-service-provider-profiles`

Operation: `createHotspotServiceProviderProfile`

Create a Hotspot Service Provider profile

Create a new Hotspot Service Provider profile.

Tags: `Configuration - Policy`

Request body:

- `application/json` — XiqHotspotServiceProviderProfileRequest

Responses:

- `201` — Created

## GET `/hotspot-profiles`

Operation: `listHotspotProfiles`

List Hotspot profiles

List a page of Hotspot profiles.

Tags: `Configuration - Policy`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 500

Responses:

- `200` — OK

## POST `/hotspot-profiles`

Operation: `createHotspotProfile`

Create a Hotspot profile

Create a new Hotspot profile.

Tags: `Configuration - Policy`

Request body:

- `application/json` — XiqHotspotProfileRequest

Responses:

- `201` — Created

## GET `/hiq/organizations`

Operation: `listOrganizations`

List all organizations

List all organizations in current HIQ (Available when HIQ is enabled).

Tags: `HIQ`

Responses:

- `200` — OK

## POST `/hiq/organizations`

Operation: `createOrganization`

Create a new organization

Create a new organization in current HIQ (Available when HIQ is enabled).

Tags: `HIQ`

Request body:

- `application/json` — XiqCreateOrganizationRequest

Responses:

- `201` — Created

## POST `/hiq/organizations/{id}/:rename`

Operation: `renameOrganization`

Rename an existing organization

Rename an existing organization (Available when HIQ is enabled).

Tags: `HIQ`

Parameters:

- `id` path, required (integer) — Organization ID to rename

Request body:

- `application/json` — string

Responses:

- `204` — No Content

## GET `/endusers`

Operation: `listEndUsers`

List end users

List a page of end users.

Tags: `Configuration - User Management`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `user_group_ids` query, optional (array) — The user group IDs
- `usernames` query, optional (array) — The list of username

Responses:

- `200` — OK

## POST `/endusers`

Operation: `createEndUser`

Create an end user

Create a new end user.

Tags: `Configuration - User Management`

Request body:

- `application/json` — XiqCreateEndUserRequest

Responses:

- `200` — OK

## POST `/endusers/{id}/:regenerate-password`

Operation: `regenerateEndUserPassword`

Regenerate a new password for the end user

Update the user's password with a system generated password.

Tags: `Configuration - User Management`

Parameters:

- `id` path, required (integer) — The enduser's ID

Responses:

- `200` — OK

## POST `/endusers/client/unlock`

Operation: `unlockClients`

Unlock locked clients

Unlock one or more locked clients by MAC address.

Tags: `Configuration - User Management`

Request body:

- `application/json` — XiqUnlockClientsRequest

Responses:

- `200` — OK

## POST `/devices/{id}/thread/commissioner/:stop`

Operation: `stopThreadCommissioner`

Stop Thread Commissioner

Stop the thread commissioner on the device.

Tags: `Device`

Parameters:

- `id` path, required (integer)

Request body:

- `application/json` — XiqThreadStopCommissionerRequest

Responses:

- `200` — OK

## POST `/devices/{id}/thread/commissioner/:start`

Operation: `startThreadCommissioner`

Start Thread Commissioner

Start the thread commissioner on the device.

Tags: `Device`

Parameters:

- `id` path, required (integer)

Request body:

- `application/json` — XiqThreadStartCommissionerRequest

Responses:

- `200` — OK

## POST `/devices/{id}/ssid/status/:change`

Operation: `changeDeviceLevelSsidStatus`

Enable or disable SSID for a device

Enable or disable SSIDs on the given wifi interfaces for a specific device.

Tags: `Device`

Parameters:

- `id` path, required (integer) — The device ID

Request body:

- `application/json` — XiqUpdateDeviceLevelSsidStatus

Responses:

- `200` — OK

## POST `/devices/{id}/ssid/:override`

Operation: `overrideDeviceLevelSsid`

Override SSID for a device

Override SSID broadcast name/passphrase for a specific device.

Tags: `Device`

Parameters:

- `id` path, required (integer) — The device ID

Request body:

- `application/json` — XiqDeviceLevelSsid

Responses:

- `200` — OK

## POST `/devices/{id}/monitor/:refresh`

Operation: `monitorRefreshDevice`

Monitor refresh a device

Monitor refresh a specific device.

Tags: `Device`

Parameters:

- `id` path, required (integer) — The device ID
- `function` query, optional (string) — Monitor refresh function

Responses:

- `200` — OK

## POST `/devices/{id}/iot/:enable`

Operation: `enableIotOnDevice`

Enable IoT Wireless Interface settings on device

Enable and attach IoT profile Wireless Interface settings by device ID and IoT profile ID.

Tags: `Device`

Parameters:

- `id` path, required (integer) — The device ID

Request body:

- `application/json` — integer

Responses:

- `200` — OK

## POST `/devices/{id}/iot/:disable`

Operation: `disableIotOnDevice`

Disable IoT Wireless Interface settings on device

Disable and detach IoT profile Wireless Interface settings by device ID and IoT profile ID.

Tags: `Device`

Parameters:

- `id` path, required (integer) — The device ID

Responses:

- `200` — OK

## POST `/devices/{id}/bounce-port`

Operation: `bounceDevicePort`

Bounce port of a device (EXOS, VOSS and SR Switches

Bounce port for the given device id.

Tags: `Device`

Parameters:

- `id` path, required (integer) — The device id

Request body:

- `application/json` — XiqBounceDevicePortRequest

Responses:

- `200` — OK

## POST `/devices/{id}/:unmanage`

Operation: `changeDeviceStatusToUnmanage`

Change admin state to 'Unmanaged' for a device

Change device admin state to 'Unmanaged' for a specific device.

Tags: `Device`

Parameters:

- `id` path, required (integer) — The device ID

Responses:

- `200` — OK

## POST `/devices/{id}/:reset`

Operation: `resetDevice`

[LRO] Reset a device to factory default

Reset a device to factory default settings.

Tags: `Device`

Parameters:

- `id` path, required (integer) — The device ID
- `async` query, optional (boolean) — Whether to enable async mode

Responses:

- `200` — OK

## POST `/devices/{id}/:reboot`

Operation: `rebootDevice`

Reboot a device

Reboot a specific device.

Tags: `Device`

Parameters:

- `id` path, required (integer) — The device ID

Responses:

- `200` — OK

## POST `/devices/{id}/:manage`

Operation: `changeDeviceStatusToManage`

Change admin state to 'Managed' for a device

Change device management status to Managed for a specific device.

Tags: `Device`

Parameters:

- `id` path, required (integer) — The device ID

Responses:

- `200` — OK

## POST `/devices/{id}/:cli`

Operation: `sendCliToDevice`

Send CLI to a device

Send CLI commands to a specific device.

Tags: `Device`

Parameters:

- `id` path, required (integer) — The device ID

Request body:

- `application/json` — array

Responses:

- `200` — OK

## POST `/devices/validate-device-action`

Operation: `validateDeviceAction`

validate device action metadata

validate metadata information of actions supported for devices

Tags: `Device`

Request body:

- `application/json` — XiqRmDeviceActionValidationRequest

Responses:

- `200` — OK

## POST `/devices/thread/commissioner/stop`

Operation: `stopThreadCommissionerByBuildings`

Stop Thread Commissioner by Buildings

Stop the thread commissioner on the devices located in the buildings.

Tags: `Device`

Request body:

- `application/json` — XiqThreadStopCommissionerByBuildingsRequest

Responses:

- `200` — OK

## POST `/devices/thread/commissioner/start`

Operation: `startThreadCommissionerByBuildings`

Start Thread Commissioner by Buildings

Start the thread commissioner on the devices located in the buildings.

Tags: `Device`

Request body:

- `application/json` — XiqThreadStartCommissionerByBuildingsRequest

Responses:

- `200` — OK

## POST `/devices/rm-devices-page`

Operation: `rmDeviceList`

[LRO] RM Device Page

Device List with pagination.

Tags: `Device`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `keyword` query, optional (string) — The keyword to search
- `connected` query, optional (boolean) — The device connect status
- `adminStates` query, optional (array) — The device admin states to filter
- `deviceCategory` query, optional (XiqRmDeviceCategoryRequest) — The device category - Wired, Wireless, TPME, Appliances
- `sortField` query, optional (XiqRmDeviceSortField) — The sort field
- `order` query, optional (XiqSortOrder) — The sort order (ascending by default)
- `deviceTypes` query, optional (array) — The device types to return
- `configMismatch` query, optional (boolean) — Config audit status(MATCHED(false) or UNMATCHED(true))
- `async` query, optional (boolean) — Whether to enable async mode
- `includeUnassigned` query, optional (boolean) — Whether to include unassigned devices
- `stacked_view` query, optional (boolean) — Whether to include only virtual stack (stacked_view = true) or also the stack members (stacked_view = false)
- `copilotLicenseStatuses` query, optional (array) — The copilot license status to filter

Request body:

- `application/json` — XiqRmDeviceListRequest

Responses:

- `200` — OK

## POST `/devices/rm-devices-page/export`

Operation: `exportRmDevicesToCsv`

[LRO] Export RM devices data to CSV

Export RM devices data to a CSV file.

Tags: `Device`

Parameters:

- `keyword` query, optional (string) — The keyword to search
- `connected` query, optional (boolean) — The device connect status
- `adminStates` query, optional (array) — The device admin states
- `deviceCategory` query, optional (XiqDeviceCategory) — The device category - wired, wireless
- `sortField` query, optional (XiqRmDeviceSortField) — The sort field
- `sortOrder` query, optional (XiqSortOrder) — Sort order (ASC, DESC)
- `deviceTypes` query, optional (array) — The device types to return
- `configMismatch` query, optional (boolean) — Config audit status(MATCHED(false) or UNMATCHED(true))
- `timezoneOffset` query, optional (integer) — timezone offset
- `async` query, optional (boolean) — Param to include additional columns data corresponding to 'Show Additional Data' option on the Network Devices page
- `includeUnassigned` query, optional (boolean) — Whether to include unassigned devices
- `copilotLicenseStatuses` query, optional (array) — Copilot license status to filter devices

Request body:

- `application/json` — XiqRmDeviceListRequest

Responses:

- `200` — OK

## POST `/devices/rm-devices-metadata`

Operation: `getDeviceListMetadata`

Get Device List Metadata

Retrieve metadata information about devices.

Tags: `Device`

Parameters:

- `deviceCategory` query, optional (XiqRmDeviceCategoryRequest) — The device category - Wired, Wireless, TPME, Appliances
- `adminStates` query, optional (array) — The device admin states to filter
- `deviceTypes` query, optional (array) — The device types to return
- `includeUnassigned` query, optional (boolean) — Whether to include unassigned devices

Request body:

- `application/json` — XiqRmSiteIdsRequest

Responses:

- `200` — OK

## POST `/devices/rm-devices-connection-status`

Operation: `getDeviceConnectionStatus`

Get Device Connection Status

Retrieve the connection status of devices for given site IDs.

Tags: `Device`

Parameters:

- `deviceCategory` query, optional (XiqRmDeviceCategoryRequest) — The device category - Wired, Wireless, TPME, Appliances
- `deviceTypes` query, optional (array) — The device types to return
- `includeUnassigned` query, optional (boolean) — Whether to include unassigned devices

Request body:

- `application/json` — XiqRmSiteIdsRequest

Responses:

- `200` — OK

## POST `/devices/os/:change`

Operation: `changeDevicesOsMode`

Change device OS mode

Change OS mode for AP or Switch.

Tags: `Device`

Request body:

- `application/json` — XiqChangeDevicesOsModeRequest

Responses:

- `200` — OK

## POST `/devices/network-policy/:revoke`

Operation: `revokeDevicesNetworkPolicy`

Revoke network policy for multiple devices

Revoke the network policy from the target devices.

Tags: `Device`

Request body:

- `application/json` — XiqDeviceFilter

Responses:

- `200` — OK

## POST `/devices/network-policy/:query`

Operation: `queryDevicesNetworkPolicy`

Query network policy for multiple devices

Query the network policy for the target devices.

Tags: `Device`

Request body:

- `application/json` — XiqDeviceFilter

Responses:

- `200` — OK

## POST `/devices/network-policy/:assign`

Operation: `assignDevicesNetworkPolicy`

Assign network policy to multiple devices

Assign the network policy to the target devices.

Tags: `Device`

Request body:

- `application/json` — XiqAssignDevicesNetworkPolicyRequest

Responses:

- `200` — OK

## POST `/devices/location/:revoke`

Operation: `revokeDevicesLocation`

Revoke location for multiple devices

Revoke the location from the target devices.

Tags: `Device`

Request body:

- `application/json` — XiqDeviceFilter

Responses:

- `200` — OK

## POST `/devices/location/:query`

Operation: `queryDevicesLocation`

Query location for multiple devices

Query the location for the target devices.

Tags: `Device`

Request body:

- `application/json` — XiqDeviceFilter

Responses:

- `200` — OK

## POST `/devices/location/:assign`

Operation: `assignDevicesLocation`

Assign location to multiple devices

Assign the location to the target devices.

Tags: `Device`

Request body:

- `application/json` — XiqAssignDevicesLocationRequest

Responses:

- `200` — OK

## POST `/devices/country-code/:assign`

Operation: `assignDevicesCountryCode`

Assign a country code to devices

Assign the country code to one or more devices.

Tags: `Device`

Request body:

- `application/json` — XiqAssignDevicesCountryCodeRequest

Responses:

- `200` — OK

## POST `/devices/client-monitor/:revoke`

Operation: `revokeDevicesClientMonitor`

Revoke client monitor setting for multiple devices

Revoke the client monitor setting from the target devices.

Tags: `Device`

Request body:

- `application/json` — XiqDeviceFilter

Responses:

- `200` — OK

## POST `/devices/client-monitor/:query`

Operation: `queryDevicesClientMonitor`

Query client monitor setting for multiple devices

Query the client monitor setting for the target devices.

Tags: `Device`

Request body:

- `application/json` — XiqDeviceFilter

Responses:

- `200` — OK

## POST `/devices/client-monitor/:assign`

Operation: `assignDevicesClientMonitor`

Assign client monitor setting to multiple devices

Assign the client monitor setting to the target devices.

Tags: `Device`

Request body:

- `application/json` — XiqAssignDevicesClientMonitorRequest

Responses:

- `200` — OK

## POST `/devices/anchor/revoke`

Operation: `revokeDevicesAsAnchor`

Revoke Anchor capability for multiple devices

Revoke Anchor capability from the target devices.

Tags: `Device`

Parameters:

- `ids` query, required (array) — The device IDs

Responses:

- `200` — OK

## POST `/devices/anchor/assign`

Operation: `assignDevicesAsAnchor`

Assign AP5050 devices as Anchor devices

Assign multiple AP5050 devices as Anchor.

Tags: `Device`

Parameters:

- `ids` query, required (array) — The device IDs

Responses:

- `200` — OK

## POST `/devices/actions-support-metadata`

Operation: `getDeviceActionSupportMetadata`

Get Actions Support metadata

Get metadata information of actions supported for devices

Tags: `Device`

Parameters:

- `deviceActions` query, optional (array) — Request body for device model properties

Request body:

- `application/json` — XiqRmDeviceActionSupportMetadataRequest

Responses:

- `200` — OK

## POST `/devices/:unmanage`

Operation: `changeStatusToUnmanage`

Change status to Unmanaged

Change device management status to Unmanaged for the target devices.

Tags: `Device`

Request body:

- `application/json` — XiqDeviceFilter

Responses:

- `200` — OK

## POST `/devices/:ssh-active-sessions`

Operation: `listSshActiveSessions`

List SSH active sessions

List active SSH sessions for devices.

Tags: `Device`

Request body:

- `application/json` — XiqSshActiveSessionsRequest

Responses:

- `200` — OK

## POST `/devices/:reset`

Operation: `resetDevices`

[LRO] Reset devices to factory default

Reset multiple devices to factory default settings.

Tags: `Device`

Parameters:

- `async` query, optional (boolean) — Whether to enable async mode

Request body:

- `application/json` — XiqDevicesResetToDefaultRequest

Responses:

- `200` — OK

## POST `/devices/:reboot`

Operation: `rebootDevices`

Reboot devices

Reboot the target devices.

Tags: `Device`

Request body:

- `application/json` — XiqDeviceFilter

Responses:

- `200` — OK

## POST `/devices/:onboard`

Operation: `onboardDevices`

Onboard Devices

Onboard devices for all devices, such as Extreme/Aerohive, EXOS, VOSS, WiNG, Dell, and Digital Twin. This is asynchronized operation to support massive device onboarding.

Tags: `Device`

Request body:

- `application/json` — XiqOnboardDeviceRequest

Responses:

- `200` — OK

## POST `/devices/:manage`

Operation: `changeStatusToManage`

Change status to Managed

Change device management status to Managed for the target devices.

Tags: `Device`

Request body:

- `application/json` — XiqDeviceFilter

Responses:

- `200` — OK

## POST `/devices/:delete`

Operation: `deleteDevices`

Delete devices

Bulk delete the devices matching the filter criteria.

Tags: `Device`

Parameters:

- `force_delete` query, optional (boolean) — Force deletion of devices

Request body:

- `application/json` — XiqDeviceFilter

Responses:

- `200` — OK

## POST `/devices/:cli`

Operation: `sendCliToDevices`

[LRO] Send CLI to devices

Send CLI commands to the target devices. This API can be run at async mode, please follow the Long-Running Operation (LRO) guide to track the progress and the result.

Tags: `Device`

Parameters:

- `async` query, optional (boolean) — Whether to enable async mode

Request body:

- `application/json` — XiqSendCliRequest

Responses:

- `200` — OK

## POST `/devices/:check-ownership`

Operation: `checkDeviceOwnership`

Check caller is allowed to access the device

Check caller is allowed to access the device.

Tags: `Device`

Request body:

- `application/json` — string

Responses:

- `200` — OK

## POST `/devices/:advanced-onboard`

Operation: `advancedOnboardDevices`

[LRO] Advanced Onboard Devices

Advanced onboard devices for all devices, such as Extreme/Aerohive, EXOS, VOSS, WiNG, Dell, and Digital Twin. Advanced onboard devices will allow the user to set the device hostname, attach the device location, associate network policy, etc. in a single API request. To avoid API timeout when onboarding a large number of devices, please make sure to enable async mode (set async=true in query parameter) and use long-running operation API to query the result.

Tags: `Device`

Parameters:

- `async` query, optional (boolean) — Whether to enable async mode

Request body:

- `application/json` — XiqAdvancedOnboardDeviceRequest

Responses:

- `200` — OK

## GET `/deployments`

Operation: `getListOfDeployments`

Get list of deployments

Get deployment details across multiple sites.

Tags: `Configuration - Deployment`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100

Responses:

- `200` — OK

## POST `/deployments`

Operation: `deployConfig`

[LRO] Push configuration and upgrade firmware

Push configuration and upgrade firmware to the target devices. To avoid API timeout with large number of devices, please make sure to enable async mode (set async=true in query parameter) and use long-running operation API to query the result.

Tags: `Configuration - Deployment`

Parameters:

- `async` query, optional (boolean) — Whether to enable async mode

Request body:

- `application/json` — XiqDeploymentRequest

Responses:

- `200` — OK

## POST `/deployments/firmware-metadatas`

Operation: `getDeviceFirmwareMetadatas`

Get device firmware metadatas

Get the compatible firmware metadatas for the devices.

Tags: `Configuration - Deployment`

Request body:

- `application/json` — XiqFirmwareMetadatasRequest

Responses:

- `200` — OK

## POST `/dashboard/wireless/usage-capacity/grid`

Operation: `getUsageCapacityGrid`

Wireless usage & capacity grid

Returns the usage & capacity grid of wireless devices based on the provided filters. You can filter the results by sites.

Tags: `Dashboard Wireless Usage and Capacity`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `keyword` query, optional (string) — The keyword to search - site name, device hostname, device MAC
- `sortField` query, optional (string) — The sort field
- `sortOrder` query, optional (XiqSortOrder) — The sort order (descending by default)
- `includeUnassigned` query, optional (boolean) — Whether to include unassigned devices

Request body:

- `application/json` — XiqUsageAndCapacityGridFilter

Responses:

- `200` — OK

## POST `/dashboard/wireless/usage-capacity/export`

Operation: `exportToCsv_1`

Export all Wireless Usage Capacity Data to CSV

Export all Wireless Usage Capacity Data to a CSV file.

Tags: `Dashboard Wireless Usage and Capacity`

Parameters:

- `keyword` query, optional (string) — The keyword to search - site name, device hostname, device MAC
- `sortField` query, optional (string) — The sort field
- `sortOrder` query, optional (XiqSortOrder) — The sort order (descending by default)
- `includeUnassigned` query, optional (boolean) — Whether to include unassigned devices

Request body:

- `application/json` — XiqUsageAndCapacityGridFilter

Responses:

- `200` — OK

## POST `/dashboard/wireless/usage-capacity/excessive-utilization`

Operation: `getWirelessUsageCapacityExcessiveUtilization`

Count of APs with excessive utilization

Returns the count of wireless devices having excessive channel utilization based on the provided filters. You can filter the results by sites, device types, and a specific timestamp.

Tags: `Dashboard Wireless Usage and Capacity`

Parameters:

- `includeUnassigned` query, optional (boolean) — Whether to include unassigned devices

Request body:

- `application/json` — XiqDashboardFilter

Responses:

- `200` — OK

## POST `/dashboard/wireless/usage-capacity/excessive-retries`

Operation: `getCountExcessiveRetries`

Count of APs with excessive retries

Returns the count of wireless devices having excessive retries based on the provided filters. You can filter the results by sites.

Tags: `Dashboard Wireless Usage and Capacity`

Parameters:

- `includeUnassigned` query, optional (boolean) — Whether to include unassigned devices

Request body:

- `application/json` — XiqDashboardFilter

Responses:

- `200` — OK

## POST `/dashboard/wireless/usage-capacity/excessive-packet-loss`

Operation: `getPacketLossExcessiveResponse`

Count of APs with excessive packet loss

Returns the count of wireless devices having excessive packet loss based on the provided filters. You can filter the results by sites

Tags: `Dashboard Wireless Usage and Capacity`

Parameters:

- `includeUnassigned` query, optional (boolean) — Whether to include unassigned devices

Request body:

- `application/json` — XiqDashboardFilter

Responses:

- `200` — OK

## POST `/dashboard/wireless/device-health/summary`

Operation: `getDeviceSummary`

Device health summary for wireless devices

Returns the count of total wireless devices and total devices with health issues based on the provided filters. You can filter the results by sites.

Tags: `Dashboard Wireless Device Health`

Parameters:

- `includeUnassigned` query, optional (boolean) — Whether to include unassigned devices

Request body:

- `application/json` — XiqDashboardFilter

Responses:

- `200` — OK

## POST `/dashboard/wireless/device-health/issues/poe-usage-issues`

Operation: `getDevicePoeUsageIssuesCount`

PoE usage issues for wireless devices

Returns the count of wireless devices having PoE usage issues (Non-adequate power) based on the provided filters. You can filter the results by sites.

Tags: `Dashboard Wireless Device Health`

Parameters:

- `includeUnassigned` query, optional (boolean) — Whether to include unassigned devices

Request body:

- `application/json` — XiqDashboardFilter

Responses:

- `200` — OK

## POST `/dashboard/wireless/device-health/issues/memory-usage-issues`

Operation: `getDeviceMemoryUsageIssueCount`

Memory usage issues for wireless devices

Returns the count of wireless devices having Memory usage issues based on the provided filters. You can filter the results by sites.

Tags: `Dashboard Wireless Device Health`

Parameters:

- `includeUnassigned` query, optional (boolean) — Whether to include unassigned devices

Request body:

- `application/json` — XiqDashboardFilter

Responses:

- `200` — OK

## POST `/dashboard/wireless/device-health/issues/cpu-usage-issues`

Operation: `getDeviceCpuUsageIssueCount`

CPU usage issues for wireless devices

Returns the count of wireless devices having CPU usage issues (CPU usage >= 95%) based on the provided filters. You can filter the results by sites.

Tags: `Dashboard Wireless Device Health`

Parameters:

- `includeUnassigned` query, optional (boolean) — Whether to include unassigned devices

Request body:

- `application/json` — XiqDashboardFilter

Responses:

- `200` — OK

## POST `/dashboard/wireless/device-health/grid`

Operation: `getDeviceHealthGrid`

Wireless device health grid

Returns the device health grid of wireless devices based on the provided filters. The results can be filtered by sites.

Tags: `Dashboard Wireless Device Health`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `keyword` query, optional (string) — The keyword to search - site name, device hostname, device MAC, device IP
- `sortField` query, optional (XiqWirelessDeviceHealthSortField) — The sort field
- `sortOrder` query, optional (XiqSortOrder) — The sort order (descending by default)
- `includeUnassigned` query, optional (boolean) — Whether to include unassigned devices

Request body:

- `application/json` — XiqWirelessDeviceHealthGridFilter

Responses:

- `200` — OK

## POST `/dashboard/wireless/device-health/export`

Operation: `exportToCsv_2`

Export all Wireless Device Health Data to CSV

Export all Wireless Device Health Data to a CSV file.

Tags: `Dashboard Wireless Device Health`

Parameters:

- `keyword` query, optional (string) — The keyword to search - site name, device hostname, device MAC, device IP
- `sortField` query, optional (XiqWirelessDeviceHealthSortField) — The sort field
- `sortOrder` query, optional (XiqSortOrder) — The sort order (descending by default)
- `includeUnassigned` query, optional (boolean) — Whether to include unassigned devices

Request body:

- `application/json` — XiqWirelessDeviceHealthGridFilter

Responses:

- `200` — OK

## GET `/dashboard/wireless/dashboard/criteria`

Operation: `getWirelessDiagnosticsDashboardCriteriaParam`

Criteria for Wireless Diagnostics Dashboard

Returns the criteria for wireless diagnostics dashboard, including client health, device health, and usage and capacity issues.

Tags: `Dashboard`

Responses:

- `200` — OK

## POST `/dashboard/wireless/client-health/roaming-issues`

Operation: `getClientHealthRoamingIssues`

Wireless clients count with roaming issues

Returns the wireless clients with roaming issues based on the provided filters. You can filter the results by sites.

Tags: `Dashboard Wireless Client Health`

Parameters:

- `includeUnassigned` query, optional (boolean) — Whether to include unassigned devices
- `connectionStatus` query, optional (XiqClientConnectionStatus) — Connection Status

Request body:

- `application/json` — XiqDashboardFilter

Responses:

- `200` — OK

## POST `/dashboard/wireless/client-health/issue/roaming`

Operation: `getClientRoamingIssues`

Roaming issue for wireless client

Returns roaming issue for wireless client based on the provided filters. You can filter the results by sites and mac address.

Tags: `Dashboard Wireless Client Health`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `macAddress` query, required (string) — macAddress
- `includeUnassigned` query, optional (boolean) — Whether to include unassigned devices

Request body:

- `application/json` — XiqDashboardFilter

Responses:

- `200` — OK

## POST `/dashboard/wireless/client-health/issue/ipaddress`

Operation: `getClientIpAddressIssues`

Ip Address issue for Wireless client

Returns ip address issue for wireless client based on the provided filters. You can filter the results by sites and mac address.

Tags: `Dashboard Wireless Client Health`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `macAddress` query, required (string) — The MAC address in format 'AABBCCDDEEFF' without separators. Accepted formats: (1) OUI only — first 6 hex characters (e.g., 'AABBCC'), (2) Full MAC address — 12 hex characters (e.g., 'AABBCCDDEEFF').
- `includeUnassigned` query, optional (boolean) — Whether to include unassigned devices

Request body:

- `application/json` — XiqDashboardFilter

Responses:

- `200` — OK

## POST `/dashboard/wireless/client-health/issue/authentication`

Operation: `getClientAuthIssues`

Authentication issue for wireless client

Returns authentication issue list for wireless client based on the provided filters. You can filter the results by sites and mac address.

Tags: `Dashboard Wireless Client Health`

Parameters:

- `macAddress` query, required (string) — The MAC address in format 'AABBCCDDEEFF' without separators. Accepted formats: (1) OUI only — first 6 hex characters (e.g., 'AABBCC'), (2) Full MAC address — 12 hex characters (e.g., 'AABBCCDDEEFF').
- `includeUnassigned` query, optional (boolean) — Whether to include unassigned devices

Request body:

- `application/json` — XiqDashboardFilter

Responses:

- `200` — OK

## POST `/dashboard/wireless/client-health/issue/association`

Operation: `getClientAssociationIssues`

Association issue for wireless client

Returns association issue list for wireless client based on the provided filters. You can filter the results by sites and macAddress.

Tags: `Dashboard Wireless Client Health`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `macAddress` query, required (string) — The MAC address in format 'AABBCCDDEEFF' without separators. Accepted formats: (1) OUI only — first 6 hex characters (e.g., 'AABBCC'), (2) Full MAC address — 12 hex characters (e.g., 'AABBCCDDEEFF').
- `includeUnassigned` query, optional (boolean) — Whether to include unassigned devices

Request body:

- `application/json` — XiqDashboardFilter

Responses:

- `200` — OK

## POST `/dashboard/wireless/client-health/grid`

Operation: `getClientHealthGrid`

Wireless client health grid

Returns the client health grid of wireless devices based on the provided filters. You can filter the results by sites.

Tags: `Dashboard Wireless Client Health`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `keyword` query, optional (string) — The keyword to search
- `connectionStatus` query, optional (XiqClientConnectionStatus) — Connection Status
- `sortField` query, optional (XiqClientHealthSortField) — Sort Field
- `sortOrder` query, optional (XiqSortOrder) — Sort Order
- `includeUnassigned` query, optional (boolean) — Whether to include unassigned devices

Request body:

- `application/json` — XiqClientGridFilter

Responses:

- `200` — OK

## POST `/dashboard/wireless/client-health/frequency-distribution`

Operation: `getClientFrequencyDistribution`

Wireless clients count with frequency distribution

Returns the wireless clients with different frequency distribution based on the provided filters. You can filter the results by sites.

Tags: `Dashboard Wireless Client Health`

Parameters:

- `includeUnassigned` query, optional (boolean) — Whether to include unassigned devices
- `connectionStatus` query, optional (XiqClientConnectionStatus) — Connection Status

Request body:

- `application/json` — XiqDashboardFilter

Responses:

- `200` — OK

## POST `/dashboard/wireless/client-health/filter-metadata`

Operation: `getClientHealthGridFilterMetadata`

Filter Metadata for Wireless Client Health Grid

Filter Metadata for Wireless Client Health Grid based on the provided filters. You can filter the results by sites.

Tags: `Dashboard Wireless Client Health`

Parameters:

- `includeUnassigned` query, optional (boolean) — Whether to include unassigned devices

Request body:

- `application/json` — XiqDashboardFilter

Responses:

- `200` — OK

## POST `/dashboard/wireless/client-health/export`

Operation: `exportToCsv_3`

Export all Client Health Data to CSV

Export all Client Health Data to a CSV file.

Tags: `Dashboard Wireless Client Health`

Parameters:

- `keyword` query, optional (string) — The keyword to search
- `connectionStatus` query, optional (XiqClientConnectionStatus) — Connection Status
- `sortField` query, optional (XiqClientHealthSortField) — Sort Field
- `sortOrder` query, optional (XiqSortOrder) — Sort Order
- `includeUnassigned` query, optional (boolean) — Whether to include unassigned devices

Request body:

- `application/json` — XiqClientGridFilter

Responses:

- `200` — OK

## POST `/dashboard/wireless/client-health/connectivity-issues`

Operation: `getClientHealthConnectivityIssues`

Wireless clients count with connectivity issues

Returns the wireless clients with connectivity issues based on the provided filters. You can filter the results by sites.

Tags: `Dashboard Wireless Client Health`

Parameters:

- `includeUnassigned` query, optional (boolean) — Whether to include unassigned devices
- `connectionStatus` query, optional (XiqClientConnectionStatus) — Connection Status

Request body:

- `application/json` — XiqDashboardFilter

Responses:

- `200` — OK

## POST `/dashboard/wired/usage-capacity/wired-throughput`

Operation: `getWiredUsageCapacityThroughput`

Wired devices throughput

Returns the throughput for wired devices based on the provided filters. The result can be filtered by sites.

Tags: `Dashboard Wired Usage and Capacity`

Request body:

- `application/json` — XiqWiredUsageCapacityThroughputRequest

Responses:

- `200` — OK

## POST `/dashboard/wired/usage-capacity/wired-congestion`

Operation: `getWiredUsageCapacityCongestion`

Wired devices congestion

Returns the congestion for wired devices based on the provided filters. The result can be filtered by sites.

Tags: `Dashboard Wired Usage and Capacity`

Request body:

- `application/json` — XiqWiredUsageCapacityThroughputRequest

Responses:

- `200` — OK

## POST `/dashboard/wired/usage-capacity/usage-utilization`

Operation: `getWiredUsageCapacityUsageUtilization`

Wired devices total utilized bandwidth

Returns total bandwidth utilized by wired devices based on the provided filters. The result can be filtered by sites.

Tags: `Dashboard Wired Usage and Capacity`

Request body:

- `application/json` — XiqWiredUsageCapacityUsageUtilizationRequest

Responses:

- `200` — OK

## POST `/dashboard/wired/usage-capacity/grid`

Operation: `getWiredUsageCapacityGrid`

Wired Usage and Capacity grid

Returns information related to usage and capacity for wired devices based on the provided filters. The result can be filtered by sites.

Tags: `Dashboard Wired Usage and Capacity`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `keyword` query, optional (string) — The keyword to search
- `sortField` query, optional (XiqWiredUsageAndCapacitySortField) — The field used for sorting
- `sortOrder` query, optional (XiqSortOrder) — The sort order

Request body:

- `application/json` — XiqWiredUsageCapacityGridRequest

Responses:

- `200` — OK

## POST `/dashboard/wired/device-health/temperature-status`

Operation: `getWiredDeviceHealthTempStatus`

Wired Device Health Temperature Status

Returns the temperature status of the device

Tags: `Dashboard Wired Device Health`

Parameters:

- `deviceId` query, required (integer) — The ID of the device

Responses:

- `200` — OK

## POST `/dashboard/wired/device-health/temperature-issues`

Operation: `getWiredDeviceHealthTemp`

Wired Device Health Temperature Issues

Returns the total number of wired devices with temperature issues based on the provided filters. The results can be filtered by sites.

Tags: `Dashboard Wired Device Health`

Request body:

- `application/json` — XiqWiredDeviceHealthTempRequest

Responses:

- `200` — OK

## POST `/dashboard/wired/device-health/summary`

Operation: `getWiredDeviceHealthSummary`

Wired Device Health Summary

Returns the total number of wired devices and the total number of wired devices with health issues based on the provided filters. The results can be filtered by sites.

Tags: `Dashboard Wired Device Health`

Request body:

- `application/json` — XiqWiredDeviceHealthSummaryRequest

Responses:

- `200` — OK

## POST `/dashboard/wired/device-health/psu-status`

Operation: `getWiredDeviceHealthPsuStatus`

Wired Device Health PSU Status

Returns the PSU status of the device

Tags: `Dashboard Wired Device Health`

Parameters:

- `deviceId` query, required (integer) — The ID of the device

Responses:

- `200` — OK

## POST `/dashboard/wired/device-health/psu-issues`

Operation: `getWiredDeviceHealthPsu`

Wired Device Health PSU Issues

Returns the total number of wired devices with PSU issues based on the provided filters. The results can be filtered by sites.

Tags: `Dashboard Wired Device Health`

Request body:

- `application/json` — XiqWiredDeviceHealthPsuRequest

Responses:

- `200` — OK

## POST `/dashboard/wired/device-health/poe-usage-status`

Operation: `getWiredDeviceHealthPoeUsageStatus`

Wired Device Health PoE Usage Status

Returns the PoE usage status of the device

Tags: `Dashboard Wired Device Health`

Parameters:

- `deviceId` query, required (integer) — The ID of the device

Responses:

- `200` — OK

## POST `/dashboard/wired/device-health/poe-usage-issues`

Operation: `getWiredDeviceHealthPoe`

Wired Device Health PoE Usage Issues

Returns the total number of wired devices with PoE issues based on the provided filters. The results can be filtered by sites.

Tags: `Dashboard Wired Device Health`

Request body:

- `application/json` — XiqWiredDeviceHealthPoeRequest

Responses:

- `200` — OK

## POST `/dashboard/wired/device-health/memory-usage-issues`

Operation: `getWiredDeviceHealthMem`

Wired Device Health Memory Usage Issues

Returns the total number of wired devices with memory issues based on the provided filters. The results can be filtered by sites.

Tags: `Dashboard Wired Device Health`

Request body:

- `application/json` — XiqWiredDeviceHealthMemRequest

Responses:

- `200` — OK

## POST `/dashboard/wired/device-health/grid`

Operation: `getWiredDeviceHealthGrid`

Wired Device Health Grid

Returns the wired device health grid based on the provided filters. The results can be filtered by sites.

Tags: `Dashboard Wired Device Health`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `keyword` query, optional (string) — The keyword to search
- `sortField` query, optional (XiqWiredDeviceHealthSortField) — The sort field
- `sortOrder` query, optional (XiqSortOrder) — The sort order (descending by default)

Request body:

- `application/json` — XiqWiredDeviceHealthGridRequest

Responses:

- `200` — OK

## POST `/dashboard/wired/device-health/fan-status`

Operation: `getWiredDeviceHealthFanStatus`

Wired Device Health Fan Status

Returns the fan status of the device

Tags: `Dashboard Wired Device Health`

Parameters:

- `deviceId` query, required (integer) — The ID of the device

Responses:

- `200` — OK

## POST `/dashboard/wired/device-health/fan-issues`

Operation: `getWiredDeviceHealthFan`

Wired Device Health Fan Issues

Returns the total number of wired devices with fan issues based on the provided filters. The results can be filtered by sites.

Tags: `Dashboard Wired Device Health`

Request body:

- `application/json` — XiqWiredDeviceHealthFanRequest

Responses:

- `200` — OK

## POST `/dashboard/wired/device-health/cpu-usage-issues`

Operation: `getWiredDeviceHealthCpu`

Wired Device Health CPU Usage Issues

Returns the total number of wired devices with CPU issues based on the provided filters. The results can be filtered by sites.

Tags: `Dashboard Wired Device Health`

Request body:

- `application/json` — XiqWiredDeviceHealthCpuRequest

Responses:

- `200` — OK

## POST `/dashboard/wired/client-health/traffic-anomalies`

Operation: `getTrafficAnomalies`

Wired clients count with traffic anomalies

Returns the wired clients with traffic anomalies based on the provided filters. You can filter the results by sites.

Tags: `Dashboard Wired Client Health`

Request body:

- `application/json` — XiqWiredClientHealthTrafficAnomaliesRequest

Responses:

- `200` — OK

## POST `/dashboard/wired/client-health/port-errors`

Operation: `getPortErrors`

Wired clients count with port errors

Returns the wired clients with port errors based on the provided filters. You can filter the results by sites.

Tags: `Dashboard Wired Client Health`

Request body:

- `application/json` — XiqWiredClientHealthPortErrorsRequest

Responses:

- `200` — OK

## POST `/dashboard/wired/client-health/port-congestion`

Operation: `getPortCongestion`

Wired clients count with port congestion issues

Returns the wired clients with port congestion issues based on the provided filters. You can filter the results by sites.

Tags: `Dashboard Wired Client Health`

Request body:

- `application/json` — XiqWiredClientHealthPortCongestionRequest

Responses:

- `200` — OK

## POST `/dashboard/wired/client-health/ip-connectivity-issues`

Operation: `getIpConnectivityIssues`

Wired clients count with IP connectivity issues

Returns the wired clients with IP connectivity issues based on the provided filters. You can filter the results by sites.

Tags: `Dashboard Wired Client Health`

Request body:

- `application/json` — XiqWiredClientHealthIpConnectivityIssuesRequest

Responses:

- `200` — OK

## POST `/dashboard/wired/client-health/grid`

Operation: `getWiredClientHealthGrid`

Wired client health grid

Returns the client health grid of wired devices based on the provided filters. You can filter the results by sites.

Tags: `Dashboard Wired Client Health`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `keyword` query, optional (string) — The keyword to search
- `sortField` query, optional (XiqWiredClientHealthSortField) — Sort Field
- `sortOrder` query, optional (XiqSortOrder) — Sort Order

Request body:

- `application/json` — XiqWiredClientHealthGridRequest

Responses:

- `200` — OK

## POST `/dashboard/usage-capacity`

Operation: `getUsageAndCapacityDiagnostics`

Usage & capacity statistics

Returns the count of wired, wireless and total usage & capacity issues based on the provided filters. You can filter the results by sites.

Tags: `Dashboard`

Parameters:

- `includeUnassigned` query, optional (boolean) — Whether to include unassigned devices

Request body:

- `application/json` — XiqDashboardFilter

Responses:

- `200` — OK

## POST `/dashboard/sites-with-issues`

Operation: `getSitesWithIssuesDiagnostics`

Sites with issues

Returns the site names along with alerts, usage and capacity, assets, client health, and device health based on the provided filters. You can filter the results by sites.

Tags: `Dashboard`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `sortField` query, optional (string) — Sort Field
- `sortOrder` query, optional (XiqSortOrder) — Sort Order
- `keyword` query, optional (string) — The Site Name Filter
- `includeUnassigned` query, optional (boolean) — Whether to include unassigned devices
- `alertsTimeRange` query, optional (integer) — Alerts Time Range in days (defaults to 1 day)
- `clientConnectionStatus` query, optional (XiqClientConnectionStatus) — Filter by Client Connection Status

Request body:

- `application/json` — XiqDashboardFilter

Responses:

- `200` — OK

## POST `/dashboard/export`

Operation: `exportToCsv_4`

Export all dashboard data to CSV

Export all dashboard data to a CSV file.

Tags: `Dashboard`

Parameters:

- `sortField` query, optional (string) — Sort Field
- `sortOrder` query, optional (XiqSortOrder) — Sort Order
- `keyword` query, optional (string) — The Site Name Filter
- `includeUnassigned` query, optional (boolean) — Whether to include unassigned devices
- `alertsTimeRange` query, optional (integer) — Alerts Time Range in days (defaults to 1 day)

Request body:

- `application/json` — XiqDashboardFilter

Responses:

- `200` — OK

## POST `/dashboard/devices`

Operation: `getDeviceHealthDiagnostics`

Device health statistics

Returns the count of total devices, total unhealthy devices, wired unhealthy devices, and wireless unhealthy devices based on the provided filters. You can filter the results by sites.

Tags: `Dashboard`

Parameters:

- `includeUnassigned` query, optional (boolean) — Whether to include unassigned devices

Request body:

- `application/json` — XiqDashboardFilter

Responses:

- `200` — OK

## POST `/dashboard/clients`

Operation: `getClientHealthDiagnostics`

Client health statistics

Returns the count of total clients, total unhealthy clients, wired unhealthy clients, and wireless unhealthy clients based on the provided filters.You can filter the results by sites.

Tags: `Dashboard`

Parameters:

- `includeUnassigned` query, optional (boolean) — Whether to include unassigned devices
- `connectionStatus` query, optional (XiqClientConnectionStatus) — Connection Status

Request body:

- `application/json` — XiqDashboardFilter

Responses:

- `200` — OK

## POST `/dashboard/assets`

Operation: `getAssetDiagnostics`

Asset statistics

Returns the count of total devices, total offline devices, wired offline devices, and wireless offline devices based on the provided filters. You can filter the results by sites.

Tags: `Dashboard`

Parameters:

- `includeUnassigned` query, optional (boolean) — Whether to include unassigned devices

Request body:

- `application/json` — XiqDashboardFilter

Responses:

- `200` — OK

## POST `/dashboard/alerts`

Operation: `getAlertDiagnostics`

Alert statistics

Returns the count of different types of alerts (critical, warning, information, and total unacknowledged) based on the provided filters. You can filter the results by sites.

Tags: `Dashboard`

Parameters:

- `includeUnassigned` query, optional (boolean) — Whether to include unassigned devices
- `alertsTimeRange` query, optional (integer) — Alerts Time Range in days (defaults to 1 day)

Request body:

- `application/json` — XiqDashboardFilter

Responses:

- `200` — OK

## POST `/d360/wireless/surrounding-aps`

Operation: `getSurroundingAps`

Get a list of SurroundingAps

Returns a list of SurroundingAps

Tags: `D360`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `deviceId` query, required (integer)
- `startTime` query, required (integer)
- `endTime` query, required (integer)
- `selectedTime` query, optional (integer)

Request body:

- `application/json` — XiqD360Filter

Responses:

- `200` — OK

## POST `/d360/client/grid`

Operation: `getClientStatsGrid`

Get Client Grid

List of Client

Tags: `D360`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `keyword` query, optional (string) — The search string
- `deviceId` query, required (integer) — The unique identifier of the wireless device
- `startTime` query, required (integer) — Start time in milliseconds (epoch time)
- `endTime` query, required (integer) — End time in milliseconds (epoch time)
- `clientStatus` query, optional (array)
- `sortField` query, optional (string)
- `sortOrder` query, optional (XiqSortOrder)
- `connectionStatus` query, optional (string)

Request body:

- `application/json` — XiqD360ClientGridFilterRequest

Responses:

- `200` — OK

## POST `/d360/client/graph`

Operation: `getClientGraph`

List a list of connected clients for Device 360 API

List a list of connected clients for Device 360 Api

Tags: `D360`

Parameters:

- `deviceId` query, required (integer) — The device ID
- `startTime` query, required (integer) — The start time to query, epoch time in milliseconds since 1/1/1970
- `endTime` query, required (integer) — The end time to query, epoch time in milliseconds since 1/1/1970
- `filter` query, required (array) — The filter type

Responses:

- `200` — OK

## GET `/credential-distribution-groups`

Operation: `listCredentialDistributionGroups`

List Credential Distribution Groups

List a page of Credential Distribution Groups.

Tags: `Administration`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 500
- `order` query, optional (XiqSortOrder) — The sort order (descending by default)
- `sortField` query, optional (string) — The sort order (descending by default)
- `keyword` query, optional (string) — The keyword to search - Group Name, Member of, User Detail or User Group
- `userGroupIds` query, optional (array) — The User Group ID to filter

Responses:

- `200` — OK

## POST `/credential-distribution-groups`

Operation: `createCredentialDistributionGroup`

Create a Credential Distribution Group

Create a new Credential Distribution Group

Tags: `Administration`

Request body:

- `application/json` — XiqCredentialDistributionGroupCreateRequest

Responses:

- `201` — Created

## DELETE `/credential-distribution-groups`

Operation: `deleteCredentialDistributionGroup`

Delete Credential Distribution Group by ID

Delete an existing Credential Distribution Group by the specified ID.

Tags: `Administration`

Parameters:

- `ids` query, required (array) — The Credential Distribution Group IDs

Responses:

- `200` — OK

## POST `/copilot/anomalies/exclude-vlans`

Operation: `updateMissingVlanExcludedVlanList`

Tags: `Copilot - Anomalies`

Request body:

- `application/json` — XiqMissingVlanExcludedVlanDetailsListRequest

Responses:

- `200` — OK

## POST `/copilot/anomalies/exclude-vlans-csv`

Operation: `updateMissingVlanExcludedVlanCsv`

Tags: `Copilot - Anomalies`

Parameters:

- `action_type` query, required (XiqExcludedVlanActionType)
- `dismiss` query, required (boolean)

Request body:

- `multipart/form-data` — csv_file
- `application/json` — csv_file
- `text/csv` — csv_file

Responses:

- `200` — OK

## POST `/clients/disconnect`

Operation: `disconnectClients`

Disconnect the clients

Disconnect multiple clients by macAddress.

Tags: `Client`

Request body:

- `application/json` — XiqDisconnectClientsByMacRequest

Responses:

- `200` — OK

## GET `/client-monitor-profiles`

Operation: `listClientMonitorProfiles`

List client monitor profiles

List a page of client monitor profiles.

Tags: `Configuration - Policy`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100

Responses:

- `200` — OK

## POST `/client-monitor-profiles`

Operation: `createClientMonitorProfile`

Create a client monitor profile

Create a new client monitor profile.

Tags: `Configuration - Policy`

Request body:

- `application/json` — XiqClientMonitorProfileRequest

Responses:

- `201` — Created

## GET `/classification-rules`

Operation: `listClassificationRules`

List classification rules

List a page of classification rules.

Tags: `Configuration - Policy`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100

Responses:

- `200` — OK

## POST `/classification-rules`

Operation: `createClassificationRule`

Create classification rule

Create a new classification rule.

Tags: `Configuration - Policy`

Request body:

- `application/json` — XiqCreateClassificationRuleRequest

Responses:

- `201` — Created

## POST `/certificates/import`

Operation: `importCertificate`

Import Certificate

Import a new Certificate.

Tags: `Configuration - Certificate`

Parameters:

- `name` query, required (string)
- `certType` query, optional (XiqCertificateType)
- `enableConvertPfx` query, optional (boolean)
- `pfxPassword` query, optional (string)
- `enableConvertDer` query, optional (boolean)
- `convertOptionType` query, optional (XiqConvertOptionType)
- `derPassword` query, optional (string)

Request body:

- `multipart/form-data` — certificate

Responses:

- `201` — Created

## GET `/certificate-bundles`

Operation: `listCertificateBundles`

List Certificate Bundles

List a page of Certificate Bundles.

Tags: `Configuration - Certificate`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `certType` query, optional (string) — The certificate bundle type

Responses:

- `200` — OK

## POST `/certificate-bundles`

Operation: `createCertificateBundle`

Create a Certificate Bundle

Create a new Certificate Bundle.

Tags: `Configuration - Certificate`

Request body:

- `application/json` — XiqCreateCertificateBundleRequest

Responses:

- `201` — Created

## GET `/ccgs`

Operation: `listCloudConfigGroups`

[LRO] List clould config groups

List a papge of cloud config groups.

Tags: `Configuration - Policy`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `sortField` query, optional (XiqCloudConfigGroupSortField) — The Sort field (Name by default)
- `order` query, optional (XiqSortOrder) — The Sort order (ascending by default)
- `async` query, optional (boolean) — Whether to enable async mode

Responses:

- `200` — OK

## POST `/ccgs`

Operation: `createCloudConfigGroup`

Create new cloud config group

Create a new cloud config group.

Tags: `Configuration - Policy`

Request body:

- `application/json` — XiqCreateCloudConfigGroupRequest

Responses:

- `201` — Created

## POST `/backup/history/:restore`

Operation: `restoreBackup`

Backup History Restore

Restore Backup History in ExtremeCloud IQ.

Tags: `Account`

Parameters:

- `backupFile` query, required (string) — The backup file that needs to be restored.

Responses:

- `200` — OK

## POST `/auth/permissions/:check`

Operation: `checkPermissions`

Check permissions

Get required permissions for given HTTP request.

Tags: `Authorization`

Request body:

- `application/json` — XiqCheckPermissionRequest

Responses:

- `200` — Successful operation
- `400` — Bad Request
- `401` — Unauthorized
- `403` — Access Denied

## POST `/auth/apitoken`

Operation: `generateApiToken`

Generate new API token

Generate a new API token with given permissions and expiration time. The available permission list can be found via 'GET /auth/permissions' endpoint.

Tags: `Authorization`

Request body:

- `application/json` — XiqGenerateApiTokenRequest

Responses:

- `200` — OK

## POST `/auth/apitoken/:validate`

Operation: `validateApiToken`

Validate API token

Validate JWT format API token

Tags: `Authorization`

Request body:

- `text/plain` — string

Responses:

- `200` — OK

## POST `/aps/afc/update`

Operation: `postApsManualAfcSpectrum`

Manual Spectrum request for device(s)

Manual Spectrum request for device(s).

Tags: `AFC`

Request body:

- `application/json` — XiqAfcApManualSpectrum

Responses:

- `200` — OK

## GET `/aps/afc/query`

Operation: `getApsAfcSummaryInfo`

Get AFC APs Summary Data

Tags: `AFC`

Parameters:

- `ownerId` query, required (integer) — Owner Id

Responses:

- `200` — OK

## POST `/aps/afc/query`

Operation: `getApsAfcSummaryInfoWithFilter`

Get AFC APs Summary Data

Tags: `AFC`

Parameters:

- `ownerId` query, required (integer) — Owner Id

Request body:

- `application/json` — XiqAfcApsFilterCriteria

Responses:

- `200` — OK

## POST `/applications/usage/summary`

Operation: `listApplicationUsageSummary`

List the application usage summary

List a page of application usage summary by filter.

Tags: `Application`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 500
- `sortField` query, optional (XiqAppUsageSummarySortField) — The sort field
- `order` query, optional (XiqSortOrder) — The sort order (ascending by default)
- `name` query, optional (string) — Application or Category Name
- `async` query, optional (boolean) — Whether to enable async mode

Request body:

- `application/json` — XiqAppUsageSummaryFilter

Responses:

- `200` — OK

## POST `/applications/usage/summary/export`

Operation: `exportApplicationUsageSummary`

Export the application usage summary

Export of application usage summary by filter.

Tags: `Application`

Parameters:

- `sortField` query, optional (XiqAppUsageSummarySortField) — The sort field
- `order` query, optional (XiqSortOrder) — The sort order (ascending by default)
- `name` query, optional (string) — Application or Category Name
- `async` query, optional (boolean) — Whether to enable async mode

Request body:

- `application/json` — XiqAppUsageSummaryFilter

Responses:

- `200` — OK

## POST `/ap/spectrum`

Operation: `getAfcSpectrumPerAp`

Tags: `AFC`

Parameters:

- `IsEmptyList` query, required (boolean)

Request body:

- `application/json` — XiqGetAfcSpectrumForApRequest

Responses:

- `200` — OK

## POST `/alerts/reports`

Operation: `createAlertReport`

[LRO] Create the alerts report

Create the alerts by filter.

Tags: `Alert`

Parameters:

- `startTime` query, required (integer) — The start time for querying alerts in milliseconds
- `endTime` query, required (integer) — The end time for querying alerts in milliseconds
- `severityIds` query, optional (array) — The severity identifier. The currently supported severity IDs are 1 for critical, 2 for warning, and 3 for info.
- `categoryIds` query, optional (array) — The alert category Id to filter
- `messageMetadataIds` query, optional (array) — The alert type to filter
- `acknowledged` query, optional (boolean) — The site to filter, return global data if not specified
- `siteId` query, optional (integer) — The site id to filter
- `timeZoneOffset` query, optional (integer) — The time zone to setup the timestamp
- `keyword` query, optional (string) — The keyword to filter, such as source name or description
- `sortField` query, optional (XiqAlertSortField) — The sort field
- `order` query, optional (XiqSortOrder) — The sort order (ascending by default)
- `async` query, optional (boolean) — Whether to enable async mode

Responses:

- `200` — OK

## POST `/alerts/:acknowledge`

Operation: `acknowledgeAlerts`

Acknowledge the alerts

acknowledge the alerts by alert ids.

Tags: `Alert`

Request body:

- `application/json` — XiqAcknowledgeAlertsRequest

Responses:

- `200` — OK

## GET `/alert-subscriptions/webhooks`

Operation: `listAlertWebhookSubscriptions`

List alert webhook subscriptions

List all alert webhook subscriptions.

Tags: `Alert`

Responses:

- `200` — OK

## POST `/alert-subscriptions/webhooks`

Operation: `createAlertWebhookSubscription`

Create alert webhook subscription

Create alert webhook subscription.

Tags: `Alert`

Request body:

- `application/json` — XiqCreateAlertWebhookSubscriptionRequest

Responses:

- `200` — OK

## POST `/alert-subscriptions/webhooks/:delete`

Operation: `deleteBulkAlertSubscriptionWebhook`

Delete alert webhook subscription in bulk

Delete alert webhook subscription in bulk.

Tags: `Alert`

Parameters:

- `async` query, optional (boolean) — Whether to enable async mode

Request body:

- `application/json` — XiqDeleteBulkAlertSubscriptionRequest

Responses:

- `200` — OK

## GET `/alert-subscriptions/servicenow`

Operation: `listServiceNowSubscriptions`

List ServiceNow subscriptions

List all ServiceNow subscriptions.

Tags: `Alert`

Responses:

- `200` — OK

## POST `/alert-subscriptions/servicenow`

Operation: `createServiceNowSubscription`

Create ServiceNow subscription

Create ServiceNow subscription.

Tags: `Alert`

Request body:

- `application/json` — XiqCreateAlertServiceNowSubscriptionRequest

Responses:

- `200` — OK

## POST `/alert-subscriptions/servicenow/:delete`

Operation: `deleteBulkAlertSubscriptionServiceNow`

Delete alert ServiceNow subscription in bulk

Delete alert ServiceNow subscription by a list of provided IDs.

Tags: `Alert`

Parameters:

- `async` query, optional (boolean) — Whether to enable async mode

Request body:

- `application/json` — XiqDeleteBulkAlertSubscriptionRequest

Responses:

- `200` — OK

## GET `/alert-subscriptions/emails`

Operation: `listAlertEmailSubscriptions`

List alert email subscriptions

List all alert email subscriptions.

Tags: `Alert`

Responses:

- `200` — OK

## POST `/alert-subscriptions/emails`

Operation: `createAlertEmailSubscription`

Create alert email subscription

Create alert email subscription.

Tags: `Alert`

Request body:

- `application/json` — XiqCreateAlertEmailSubscriptionRequest

Responses:

- `200` — OK

## POST `/alert-subscriptions/emails/{id}/:verify`

Operation: `verifySubscriptionEmail`

Email Verification

Send a request to verify an email

Tags: `Alert`

Parameters:

- `id` path, required (integer) — The alert email subscription ID

Responses:

- `200` — OK

## POST `/alert-subscriptions/emails/:delete`

Operation: `deleteBulkAlertSubscriptionEmail`

Delete alert email subscription in bulk

Delete alert email subscription in bulk.

Tags: `Alert`

Parameters:

- `async` query, optional (boolean) — Whether to enable async mode

Request body:

- `application/json` — XiqDeleteBulkAlertSubscriptionRequest

Responses:

- `200` — OK

## GET `/alert-policies`

Operation: `listAlertPolicies`

List all alert policies

Get a list of all alert policies belonging to the current user and an overview of their associated alert rules. The details for the rules is available from the alert policy rules API.

Tags: `Alert`

Parameters:

- `keyword` query, optional (string) — The keyword to filter, such as policy name or site name
- `policyType` query, optional (XiqAlertPolicyType) — The policy type to filter, such as site or global

Responses:

- `200` — OK

## POST `/alert-policies`

Operation: `createAlertPolicy`

Create a site based alert policy

Create a new site-based alert policy. The global policy for each account is created automatically.

Tags: `Alert`

Request body:

- `application/json` — XiqAlertPolicyFilter

Responses:

- `200` — OK

## POST `/alert-policies/{policyId}/rules/{ruleId}/:enable`

Operation: `enableAlertRule`

Enable a rule from an alert policy

Set the status of a rule to enabled. Users can obtain a rule ID by calling #_get_alert_policy first.If the ENABLE operation adheres to a predetermined rule, a new rule will be duplicated from the predefined one, and the ENABLE operation will be applied to the newly cloned rule. As a result, users might receive a new rule ID that differs from the one provided as a path parameter.

Tags: `Alert`

Parameters:

- `policyId` path, required (integer) — The policy ID
- `ruleId` path, required (integer) — The rule ID

Responses:

- `200` — OK

## POST `/alert-policies/{policyId}/rules/{ruleId}/:disable`

Operation: `disableAlertRule`

Disable a rule from an alert policy

Set the status of a rule to disabled. Users can obtain a rule ID by calling #_get_alert_policy first.If the DISABLE operation adheres to a predetermined rule, a new rule will be duplicated from the predefined one, and the DISABLE operation will be applied to the newly cloned rule. As a result, users might receive a new rule ID that differs from the one provided as a path parameter.

Tags: `Alert`

Parameters:

- `policyId` path, required (integer) — The policy ID
- `ruleId` path, required (integer) — The rule ID

Responses:

- `200` — OK

## POST `/airrm/ap/radioInfo/`

Operation: `getDevicesRadioInfo`

Get Devices Radio Information

Get radio information for devices by serial number or AIRRM ID

Tags: `airrm-endpoint`

Request body:

- `application/json` — XiqDeviceRadioInfoRequest

Responses:

- `200` — OK

## POST `/afc/rm-devices-page`

Operation: `rmDeviceList_1`

[LRO] RM AFC Device Page

AFC Device List with pagination.

Tags: `AFC`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `keyword` query, optional (string) — The keyword to search
- `sortField` query, optional (XiqRmDeviceSortField) — The sort field
- `order` query, optional (XiqSortOrder) — The sort order (ascending by default)
- `includeUnassigned` query, optional (boolean) — Whether to include unassigned devices

Request body:

- `application/json` — XiqRmAfcDeviceListRequest

Responses:

- `200` — OK

## POST `/afc/recalculateSite/{id}`

Operation: `recalculateSite`

Tags: `AFC`

Parameters:

- `id` path, required (integer) — The device id for the site

Responses:

- `200` — OK

## POST `/afc/mobileapp/apcandidates`

Operation: `getMobileappApcandidates`

List of AP candidates that may be used as anchors

Tags: `AFC`

Request body:

- `application/json` — XiqAfcMobileappScanInfo

Responses:

- `200` — OK

## POST `/afc/filter-metadata`

Operation: `getAfcGridFilterMetadata`

RM AFC Device Metadata Page

AFC Device metadata api.

Tags: `AFC`

Parameters:

- `includeUnassigned` query, optional (boolean) — Whether to include unassigned devices

Request body:

- `application/json` — XiqDashboardFilter

Responses:

- `200` — OK

## POST `/afc/export`

Operation: `rmDeviceListExport`

[LRO] RM AFC Device export

AFC Device List export.

Tags: `AFC`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `keyword` query, optional (string) — The keyword to search
- `sortField` query, optional (XiqRmDeviceSortField) — The sort field
- `order` query, optional (XiqSortOrder) — The sort order (ascending by default)
- `timezoneOffset` query, optional (integer) — timezone offset
- `includeUnassigned` query, optional (boolean) — Whether to include unassigned devices

Request body:

- `application/json` — XiqRmAfcDeviceListRequest

Responses:

- `200` — OK

## POST `/afc/aps/reportFtm`

Operation: `requestAfcFtmData`

Tags: `AFC`

Request body:

- `application/json` — XiqReportFtmDataRequest

Responses:

- `200` — OK

## GET `/acct-api-token`

Operation: `listApiAccessTokens`

List API Access tokens

List a page of API Access tokens.

Tags: `Administration`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `order` query, optional (XiqSortOrder) — The sort order (descending by default)
- `keyword` query, optional (string) — The keyword - application name or grantor
- `sortField` query, optional (XiqApiAccessTokenSortField) — The sort field

Responses:

- `200` — OK

## POST `/acct-api-token`

Operation: `createApiAccessToken`

Create an API Access token

Create a new API access token

Tags: `Administration`

Parameters:

- `clientId` query, required (string) — The client ID
- `tokenExpireInDay` query, required (integer) — The expire time in days

Responses:

- `201` — Created

## POST `/account/viq/import`

Operation: `importViq`

[LRO] Import VIQ data

This is used import VIQ details from a file

Tags: `Account`

Parameters:

- `timeoutInSeconds` query, optional (integer) — The maximum import duration
- `resendUserNotifications` query, optional (boolean) — Resend Cloud PPSK/RADIUS password through email/SMS

Request body:

- `multipart/form-data` — importFile

Responses:

- `200` — OK

## POST `/account/viq/export`

Operation: `exportViq`

[LRO] Export VIQ data

This is used to Export VIQ data.

Tags: `Account`

Parameters:

- `timeoutInSeconds` query, optional (integer) — The maximum export duration
- `excludeDeviceFirmware` query, optional (boolean) — Whether exclude device firmwares from VIQ export file or not

Responses:

- `200` — OK

## POST `/account/viq/:reset`

Operation: `resetViq`

Reset VIQ

Reset VIQ in ExtremeCloud IQ.

Tags: `Account`

Responses:

- `200` — OK

## POST `/account/viq/:backup`

Operation: `backupViq`

Backup VIQ

Backup VIQ in ExtremeCloud IQ.

Tags: `Account`

Responses:

- `200` — OK

## POST `/account/:switch`

Operation: `switchAccount`

Switch to another ExtremeCloud IQ account

Switch to external ExtremeCloud IQ account or switch back to home ExtremeCloud IQ account.

Tags: `Account`

Parameters:

- `id` query, optional (integer) — The account ID to switch, switch back to home ExtremeCloud IQ account if not provide

Responses:

- `200` — OK

## GET `/vlan-profiles/{id}`

Operation: `getVlanProfile`

Get a VLAN profile

Get a specific VLAN profile by ID.

Tags: `Configuration - Basic`

Parameters:

- `id` path, required (integer) — The VLAN profile ID

Responses:

- `200` — OK

## PATCH `/vlan-profiles/{id}`

Operation: `updateVlanProfile`

Update a VLAN profile

Update a specific VLAN profile.

Tags: `Configuration - Basic`

Parameters:

- `id` path, required (integer) — The VLAN profile ID.

Request body:

- `application/json` — XiqUpdateVlanProfileRequest

Responses:

- `200` — OK

## DELETE `/vlan-profiles/{id}`

Operation: `deleteVlanProfile`

Delete a VLAN profile

Delete a specific VLAN profile by ID.

Tags: `Configuration - Basic`

Parameters:

- `id` path, required (integer) — The VLAN profile ID

Responses:

- `200` — OK

## GET `/users/{id}`

Operation: `getUser`

Get user info by ID

Get user info for a specific user.

Tags: `User`

Parameters:

- `id` path, required (integer) — The user ID

Responses:

- `200` — OK

## PATCH `/users/{id}`

Operation: `updateUser`

Update user info

Updates user info for a specific user.

Tags: `User`

Parameters:

- `id` path, required (integer) — The user ID

Request body:

- `application/json` — XiqUpdateUserRequest

Responses:

- `200` — OK

## DELETE `/users/{id}`

Operation: `deleteUser`

Delete user by ID

Delete a specific user.

Tags: `User`

Parameters:

- `id` path, required (integer) — The user ID

Responses:

- `200` — OK

## GET `/users/external/{id}`

Operation: `getExternalUser`

Get external access info

Get external access info for a specific external user.

Tags: `User`

Parameters:

- `id` path, required (integer) — The external user ID

Responses:

- `200` — OK

## PATCH `/users/external/{id}`

Operation: `updateExternalUser`

Update external access info

Updates external access info for a specific user.

Tags: `User`

Parameters:

- `id` path, required (integer) — The external user ID

Request body:

- `application/json` — XiqUpdateExternalUserRequest

Responses:

- `200` — OK

## DELETE `/users/external/{id}`

Operation: `revokeExternalUser`

Revoke external access

Revoke external acccess for a specific user.

Tags: `User`

Parameters:

- `id` path, required (integer) — The external user ID

Responses:

- `200` — OK

## PATCH `/ng-reports/scheduled/{reportScheduleId}`

Operation: `enableDisableReportSchedule`

Enable or Disable Report Schedule

Enables or disables a report schedule based on the provided flag.

Tags: `NG Reports (Scheduled)`

Parameters:

- `reportScheduleId` path, required (integer) — The report schedule ID
- `enableSchedule` query, required (boolean) — Flag to enable or disable the report schedule

Responses:

- `200` — OK

## PATCH `/acct-api-token/{id}`

Operation: `updateApiAccessToken`

Update API Access token by ID

Tags: `Administration`

Parameters:

- `id` path, required (integer) — The API Access Token ID.

Request body:

- `application/json` — XiqUpdateApiAccessTokenRequest

Responses:

- `200` — OK

## DELETE `/acct-api-token/{id}`

Operation: `deleteApiAccessToken`

Delete API Access token by ID

Delete an existing API Access token by the specified ID.

Tags: `Administration`

Parameters:

- `id` path, required (integer) — The API Access token ID

Responses:

- `200` — OK

## GET `/users/reports/{id}`

Operation: `downloadUsersReport`

Download the report

Download report of Users

Tags: `User`

Parameters:

- `id` path, required (string) — The report ID

Responses:

- `200` — OK

## GET `/users/me`

Operation: `getCurrentUser`

Get current user info

Get currently login user info.

Tags: `User`

Responses:

- `200` — OK

## GET `/usergroups/:unique`

Operation: `listUniqueUserGroupNames`

List unique user group names

List unique user group names.

Tags: `Configuration - User Management`

Responses:

- `200` — OK

## GET `/user-profile-assignments/{id}`

Operation: `getUserProfileAssignment`

Get user profile assignment by ID

Get user profile assignment details for the specified ID.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The user profile assignment ID

Responses:

- `200` — OK

## DELETE `/user-profile-assignments/{id}`

Operation: `deleteUserProfileAssignment`

Delete an user profile assignment by ID

Delete an existing user profile assignment by ID.

Tags: `Configuration - Policy`

Parameters:

- `id` path, required (integer) — The user profile ID

Responses:

- `200` — OK

## GET `/user-folder-preferences`

Operation: `queryUserFolderPreferences`

Query user folder preferences

Returns matched preferences.

Tags: `Use Folder Preferences`

Parameters:

- `folderId` query, required (integer) — The folder identifier
- `type` query, required (array) — The types of preferences to retrieve (e.g. FLOOR_THRESHOLDS)

Responses:

- `200` — OK

## GET `/ucp/{id}/engines/installed`

Operation: `getUcpEngines`

Get UCP Engines by ID

Get UCP Engine details for the specified device ID.

Tags: `Universal Compute Platform`

Parameters:

- `id` path, required (integer) — The UCP device ID

Responses:

- `200` — OK

## GET `/tunnel-concentrators/{id}/license`

Operation: `getTunnelConcentratorLicense`

Get Tunnel Concentrator license status

Get the license status for the specified Tunnel Concentrator device.

Tags: `Configuration - Network`

Parameters:

- `id` path, required (integer) — The Tunnel Concentrator device ID

Responses:

- `200` — OK

## GET `/thread/topology`

Operation: `getThreadNetworkTopology`

Get thread network topology

Get thread routers, neighboring routers and end-devices

Tags: `Thread`

Parameters:

- `networkConfigIds` query, required (array) — Thread network config id
- `routerFields` query, optional (array) — The thread router fields to return
- `routerViews` query, optional (array) — The views to return thread router fields
- `clientViews` query, optional (array) — The views to return client fields (Check fields for each view at XiqClientView schema)
- `clientFields` query, optional (array) — The client fields to return

Responses:

- `200` — OK

## GET `/thread/routers`

Operation: `getThreadRouters`

List thread routers

List thread routers with pagination.

Tags: `Thread`

Parameters:

- `ids` query, required (array) — The thread router IDs
- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `sortField` query, optional (string) — The sort field
- `sortOrder` query, optional (XiqSortOrder) — The sort order (ascending by default)
- `views` query, optional (array) — The views to return thread router fields
- `fields` query, optional (array) — The thread router fields to return

Responses:

- `200` — OK

## GET `/thread/networks`

Operation: `getThreadNetworks`

Get active thread networks

Get thread networks with atleast one device

Tags: `Thread`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `folderId` query, required (integer) — Thread network config folder id
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `fields` query, optional (array) — The thread network config fields to return
- `views` query, optional (array) — The views to return thread network config fields

Responses:

- `200` — OK

## GET `/subscriptions/webhook/export`

Operation: `exportToCsv_5`

Export all webhook subscriptions to CSV

Export all webhook subscriptions to a CSV file.

Tags: `Notification`

Parameters:

- `order` query, optional (XiqSortOrder)
- `keyword` query, optional (string)

Responses:

- `200` — OK

## GET `/ssids`

Operation: `listSsids`

List SSIDs

List SSIDs with filter and pagination.

Tags: `Configuration - Policy`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100

Responses:

- `200` — OK

## GET `/sms-templates`

Operation: `listSmsTemplates`

List SMS templates

List all SMS notification templates.

Tags: `Configuration - User Management`

Parameters:

- `passwordType` query, optional (XiqPasswordType) — The password type

Responses:

- `200` — OK

## GET `/radius-servers/internal/devices`

Operation: `listInternalRadiusDevices`

List all internal RADIUS devices

List all internal RADIUS devices fields.

Tags: `Configuration - Authentication`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100

Responses:

- `200` — OK

## GET `/radius-proxies/devices`

Operation: `listRadiusProxyDevices`

List Radius proxy devices

List devices for Radius Proxy.

Tags: `Configuration - Authentication`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100

Responses:

- `200` — OK

## GET `/radio-operating-modes/{productType}`

Operation: `getRadioOperatingModes`

Get Radio Operating Modes by product type

Modern AP hardware types include dual or triple band radios. A limited subset of band combinations are supported. Operating mode defines the supported band combinations per radio. Access Points with fixed band radios use GENERIC operating mode. SERVICE_2_5_6: wifi0-2.4Ghz, wifi1-5Ghz, wifi2-6Ghz SENSOR_SERVICE_5_6: wifi0-Tri-band sensor, wifi1-5Ghz, wifi2-6Ghz SERVICE_5L_5H_6: wifi0-5G Low, wifi1-5G High, wifi2-6Ghz SENSOR_SERVICE_5_2: wifi0-Tri-band sensor, wifi1-5GHz, wifi2-2.4Ghz SERVICE_5L_5H_2: wifi0-5G Low, wifi1-5G High, wifi2-2.4Ghz SERVICE_2_5H_5L: wifi2-2.4Ghz, wifi1-5G High, wifi0-5G Low SERVICE_6L_5_6H: wifi0-6G Low, wifi1-5GHz, wifi2-6Ghz. SERVICE_6H_5_6L: wifi0-6G High, wifi1-5GHz, wifi2-6Ghz Low. SERVICE_2_5: wifi0-2.4Ghz, wifi1-5Ghz. SERVICE_6_5: wifi0-6Ghz, wifi1-5Ghz.

Tags: `Configuration - Policy`

Parameters:

- `productType` path, required (string) — Product Type/Model

Responses:

- `200` — OK

## GET `/packetcaptures/{id}`

Operation: `getPacketCapture`

Get a packet capture session

Get packet capture session by ID.

Tags: `Packet Capture`

Parameters:

- `id` path, required (integer) — The packet capture ID
- `fields` query, optional (array) — The packet capture fields to return

Responses:

- `200` — OK

## DELETE `/packetcaptures/{id}`

Operation: `deletePacketCapture`

Delete a packet capture session

Delete an existing packet capture session and capture files by ID.

Tags: `Packet Capture`

Parameters:

- `id` path, required (integer) — The packet capture ID

Responses:

- `200` — OK

## GET `/packetcaptures/files`

Operation: `getPacketCaptureFile`

Get an AP packet capture file

Get an AP packet capture file from XIQ cloud storage.

Tags: `Packet Capture`

Parameters:

- `cloudFileUrl` query, required (string) — The packet capture file path

Responses:

- `200` — OK

## GET `/operations/{operationId}`

Operation: `getOperation`

Get Long-Running Operation (LRO) status and result

Get the Long-Running Operation (LRO) status and result. The response will include either result or error if the operation is done.

Tags: `Operation`

Parameters:

- `operationId` path, required (string) — The operation ID

Responses:

- `200` — OK

## DELETE `/operations/{operationId}`

Operation: `deleteOperation`

Delete Long-Running Operation (LRO)

The Long-Running Operation (LRO) can be deleted when the operation is done or in PENDING status.

Tags: `Operation`

Parameters:

- `operationId` path, required (string) — The operation ID

Responses:

- `200` — OK

## GET `/ng-reports/scheduled/runs/{reportRunId}/recipients`

Operation: `getRecipientsForReportRun`

Get Recipients for Report Run

Retrieves all recipients for a given report run.

Tags: `NG Reports (Scheduled)`

Parameters:

- `reportRunId` path, required (integer) — The report run ID
- `keyword` query, optional (string) — The keyword to search

Responses:

- `200` — OK

## GET `/ng-reports/scheduled/reports/download`

Operation: `downloadScheduledReportFile`

Download or Preview Scheduled Report File

Downloads or previews a scheduled report file in PDF or XLSX format.

Tags: `NG Reports (Scheduled)`

Parameters:

- `reportRunId` query, required (integer)
- `fileFormat` query, required (XiqReportFileFormat)
- `preview` query, optional (boolean) — Param to view in Preview mode, (supported only when fileFormat = PDF)

Responses:

- `200` — OK

## GET `/ng-reports/scheduled/pci-compliance`

Operation: `getPciComplianceReports`

Get PCI Compliance Reports

Retrieves all PCI compliance reports with optional keyword filtering.

Tags: `NG Reports (Scheduled)`

Parameters:

- `keyword` query, optional (string) — Keyword to search report file name and recipient emails

Responses:

- `200` — OK

## GET `/ng-reports/scheduled/network-summary`

Operation: `getNetworkSummaryReports`

Get Network Summary Reports

Retrieves all network summary reports with optional keyword filtering.

Tags: `NG Reports (Scheduled)`

Parameters:

- `keyword` query, optional (string) — Keyword to search report file name and recipient emails

Responses:

- `200` — OK

## GET `/ng-reports/scheduled/custom/{reportScheduleId}/runs`

Operation: `getReportRunsForSchedule`

Get report runs for a schedule

Fetch all report runs for a specific schedule ID and optional frequencies.

Tags: `NG Reports (Scheduled)`

Parameters:

- `reportScheduleId` path, required (integer) — The report schedule ID
- `frequency` query, optional (array) — Optional list of schedule frequencies to filter by

Responses:

- `200` — OK

## GET `/ng-reports/information`

Operation: `qOeDiagnosticsHelp`

Information about QoE-Diagnostics Metrics

Gives information about metrics, there functionality and applicable filters

Tags: `NG Reports (Ondemand)`

Responses:

- `200` — OK

## GET `/ng-reports/information/{metrics}`

Operation: `qOeDiagnosticsHelp_1`

Information about QoE-Diagnostics Metrics

Gives information about metrics, there functionality and applicable filters

Tags: `NG Reports (Ondemand)`

Parameters:

- `metrics` path, required (XiqQoeDiagnosticsMetrics) — metrics

Responses:

- `200` — OK

## GET `/ng-reports/download/reports/{id}`

Operation: `downloadReport`

Download the Reports by ID

Download reports of Metrics

Tags: `NG Reports (Ondemand)`

Parameters:

- `id` path, required (string) — The report ID

Responses:

- `200` — Report downloaded successfully
- `400` — Invalid Report Id
- `404` — Report not found

## GET `/network-scorecard/wifiHealth/{locationId}`

Operation: `getWifiHealth`

Get the overall wifi health score

Get the wifi health score over the period

Tags: `Network Scorecard`

Parameters:

- `locationId` path, required (integer) — The location folder ID
- `startTime` query, optional (integer) — The start time to query, epoch time in milliseconds since 1/1/1970
- `endTime` query, optional (integer) — The end time to query, epoch time in milliseconds since 1/1/1970

Responses:

- `200` — OK

## GET `/network-scorecard/servicesHealth/{locationId}`

Operation: `getServicesHealth`

Get the overall services health score

Get the health score over the period

Tags: `Network Scorecard`

Parameters:

- `locationId` path, required (integer) — The location folder ID
- `startTime` query, optional (integer) — The start time to query, epoch time in milliseconds since 1/1/1970
- `endTime` query, optional (integer) — The end time to query, epoch time in milliseconds since 1/1/1970

Responses:

- `200` — OK

## GET `/network-scorecard/networkHealth/{locationId}`

Operation: `getNetworkHealth`

Get the overall network health score

Get the network health score over the period

Tags: `Network Scorecard`

Parameters:

- `locationId` path, required (integer) — The location folder ID
- `startTime` query, optional (integer) — The start time to query, epoch time in milliseconds since 1/1/1970
- `endTime` query, optional (integer) — The end time to query, epoch time in milliseconds since 1/1/1970

Responses:

- `200` — OK

## GET `/network-scorecard/deviceHealth/{locationId}`

Operation: `getDeviceHealth`

Get the overall device health score

Get the devices health score over the period

Tags: `Network Scorecard`

Parameters:

- `locationId` path, required (integer) — The location folder ID
- `startTime` query, optional (integer) — The start time to query, epoch time in milliseconds since 1/1/1970
- `endTime` query, optional (integer) — The end time to query, epoch time in milliseconds since 1/1/1970

Responses:

- `200` — OK

## GET `/network-scorecard/clientHealth/{locationId}`

Operation: `getClientHealth`

Get the overall client health score

Get the clients health score over the period

Tags: `Network Scorecard`

Parameters:

- `locationId` path, required (integer) — The location folder ID
- `startTime` query, optional (integer) — The start time to query, epoch time in milliseconds since 1/1/1970
- `endTime` query, optional (integer) — The end time to query, epoch time in milliseconds since 1/1/1970
- `vlans` query, optional (array) — The associate vlan IDs
- `userProfileNames` query, optional (array) — The user profile names
- `ssids` query, optional (array) — The SSIDs

Responses:

- `200` — OK

## GET `/network-policies/{id}/ssids`

Operation: `listSsidsByNetworkPolicy`

List SSIDs for a network policy

List a page of SSIDs for a specific network policy.

Tags: `Network Policy`

Parameters:

- `id` path, required (integer) — The network policy ID
- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100

Responses:

- `200` — OK

## GET `/logs/sms`

Operation: `listSmsLogs`

List SMS logs

List a page of SMS logs.

Tags: `Log`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `phoneNumber` query, optional (string) — The phone number
- `startTime` query, optional (integer) — The start time to query, epoch time in milliseconds since 1/1/1970, default is 0 if not specified or is negative
- `endTime` query, optional (integer) — The end time to query, epoch time in milliseconds since 1/1/1970, default is now if not specified or is negative

Responses:

- `200` — OK

## GET `/logs/email`

Operation: `listEmailLogs`

List Email logs

List a page of Email logs.

Tags: `Log`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `username` query, optional (string) — The user login name
- `startTime` query, optional (integer) — The start time to query, epoch time in milliseconds since 1/1/1970, default is 0 if not specified or is negative
- `endTime` query, optional (integer) — The end time to query, epoch time in milliseconds since 1/1/1970, default is now if not specified or is negative

Responses:

- `200` — OK

## GET `/logs/credential`

Operation: `listCredentialLogs`

List credential logs

List a page of credential logs.

Tags: `Log`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `username` query, optional (string) — The user login name
- `startTime` query, optional (integer) — The start time to query, epoch time in milliseconds since 1/1/1970, default is 0 if not specified or is negative
- `endTime` query, optional (integer) — The end time to query, epoch time in milliseconds since 1/1/1970, default is now if not specified or is negative

Responses:

- `200` — OK

## GET `/logs/auth`

Operation: `listAuthLogs`

List auth logs

List a page of auth logs.

Tags: `Log`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `username` query, optional (string) — The user login name
- `callingStationId` query, optional (string) — The calling station ID
- `startTime` query, optional (integer) — The start time to query, epoch time in milliseconds since 1/1/1970, default is 0 if not specified or is negative
- `endTime` query, optional (integer) — The end time to query, epoch time in milliseconds since 1/1/1970, default is now if not specified or is negative

Responses:

- `200` — OK

## GET `/logs/audit`

Operation: `listAuditLogs`

List audit logs

List a page of audit logs.

Tags: `Log`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 500
- `sortField` query, optional (XiqAuditLogSortField) — The field for sorting
- `sortOrder` query, optional (XiqSortOrder) — The sorting order
- `categories` query, optional (array) — Audit category
- `username` query, optional (string) — The user login name
- `startTime` query, required (integer) — The start time to query, epoch time in milliseconds since 1/1/1970
- `endTime` query, required (integer) — The end time to query, epoch time in milliseconds since 1/1/1970. Note: endTime - startTime must be no greater than 2592000000 (30 days)
- `keyword` query, optional (string) — The case-insensitive keyword to search in description

Responses:

- `200` — OK

## GET `/logs/audit/reports/{id}`

Operation: `downloadAuditLogsReport`

Download audit logs

Download report of audit logs.

Tags: `Log`

Parameters:

- `id` path, required (integer) — The report ID

Responses:

- `200` — OK

## GET `/logs/audit/full-descriptions/{id}`

Operation: `getAuditLogFullDescriptions`

Get audit log full descriptions

Get audit log full descriptions by ID.

Tags: `Log`

Parameters:

- `id` path, required (integer) — The audit log full description ID

Responses:

- `200` — OK

## GET `/logs/accounting`

Operation: `listAccountingLogs`

List accounting logs

List a page of accounting logs.

Tags: `Log`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `username` query, optional (string) — The user login name
- `callingStationId` query, optional (string) — The calling station ID
- `startTime` query, optional (integer) — The start time to query, epoch time in milliseconds since 1/1/1970, default is 0 if not specified or is negative
- `endTime` query, optional (integer) — The end time to query, epoch time in milliseconds since 1/1/1970, default is now if not specified or is negative

Responses:

- `200` — OK

## GET `/locations/wall/type/references/{id}`

Operation: `findWallTypeReferences`

Find references of a wall type

Find all floors a/o sites referencing a wall type by its ID

Tags: `Location`

Parameters:

- `id` path, required (integer) — The Wall Type ID

Responses:

- `200` — OK

## GET `/locations/tree`

Operation: `getLocationTree`

Get location tree

Get location hierarchical tree.

Tags: `Location`

Parameters:

- `parentId` query, optional (integer) — The parent location ID, return root locations if parent is null
- `expandChildren` query, optional (boolean) — Whether to return the child locations recursively, default is true. Set it to false to improve performance when there are a lot of child locations.

Responses:

- `200` — OK

## GET `/locations/tree/maps`

Operation: `getLocationMapsList`

Get maps on the location hierarchy.

Get maps on the location hierarchy with pagination.

Tags: `Location`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `locationId` query, optional (integer) — The location ID, or null for all locations.
- `expandChildren` query, optional (boolean) — Whether to return the child locations recursively, default is true. Set it to false to improve performance when there are a lot of child locations.

Responses:

- `200` — OK

## GET `/locations/tree/devices`

Operation: `getLocationDevicesList`

Get devices on the location hierarchy.

Get devices on the location hierarchy with pagination.

Tags: `Location`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `locationId` query, optional (integer) — The location ID, or null for all locations.
- `expandChildren` query, optional (boolean) — Whether to return the child locations recursively, default is true. Set it to false to improve performance when there are a lot of child locations.

Responses:

- `200` — OK

## GET `/locations/folder/{folderId}/zones`

Operation: `getZonesInFolder`

Get all zones in folder

Retrieve the list of zones in folder by folder ID.

Tags: `Location`

Parameters:

- `folderId` path, required (integer) — The Folder ID

Responses:

- `200` — OK

## GET `/hiq/status`

Operation: `getHiqStatus`

Get HIQ status

Get Hierarchical ExtremeCloud IQ (HIQ) status.

Tags: `HIQ`

Responses:

- `200` — OK

## GET `/geo-view`

Operation: `getGeoViewData`

Get GeoView Data

Tags: `Geo View`

Responses:

- `200` — OK

## GET `/essentials/eloc/clients/{clientMac}/last-known-location`

Operation: `getClientLastLocation`

Get the last known location of the client

Get the last known location of the client on the floor plan.

Tags: `Essentials - ExtremeLocation`

Parameters:

- `clientMac` path, required (string) — The mac address of client
- `floorId` query, required (integer) — Location Id of the floor
- `parentId` query, required (integer) — Location Id of the floor's parent

Responses:

- `200` — OK

## GET `/essentials/eloc/clients/location/path-in-interval-on-floor`

Operation: `getClientPath`

Get the path of the client in the specified interval

Get the path of the client on the floor plan in the specified interval.

Tags: `Essentials - ExtremeLocation`

Parameters:

- `parentId` query, required (integer) — Location Id of the floor's parent
- `floorId` query, required (integer) — Location Id of the floor
- `clientMac` query, required (string) — The mac address of the client
- `startDate` query, required (string) — Start date for the path ('yyyy-MM-dd HH:mm' format)
- `endDate` query, required (string) — End date for the path ('yyyy-MM-dd HH:mm' format)

Responses:

- `200` — OK

## GET `/essentials/eloc/clients/location/last-known-location-in-interval-on-floor`

Operation: `getClientLastKnownLocationInInterval`

Get the last known location of the client in the specified interval

Get the last known location of the client on the floor plan in the specified interval.

Tags: `Essentials - ExtremeLocation`

Parameters:

- `parentId` query, required (integer) — Location Id of the floor's parent
- `floorId` query, required (integer) — Location Id of the floor
- `clientMac` query, required (string) — The mac address of the client
- `interval` query, required (XiqClientLocationSearchInterval) — Interval for the last known location

Responses:

- `200` — OK

## GET `/essentials/eloc/clients/location/density-map-data`

Operation: `getClientDensityMapData`

Get the client density map data

Get the density map of clients on the floor plan for a specific date, structured per hour.

Tags: `Essentials - ExtremeLocation`

Parameters:

- `floorId` query, required (integer) — Location Id of the floor
- `parentId` query, required (integer) — Location Id of the floor's parent
- `date` query, required (string) — Date for the density map ('yyyy-MM-dd' format)

Responses:

- `200` — OK

## GET `/essentials/eloc/clients/location/current-on-floor`

Operation: `getClientCurrentLocation`

Get the current location of the client

Get the current location of the client on the floor plan.

Tags: `Essentials - ExtremeLocation`

Parameters:

- `parentId` query, required (integer) — Location Id of the floor's parent
- `floorId` query, required (integer) — Location Id of the floor
- `clientMac` query, required (string) — The mac address of the client

Responses:

- `200` — OK

## GET `/essentials/eloc/clients/location/current-of-all-on-floor`

Operation: `getCurrentLocationOfAllClientsOnFloor`

Get all connected clients on a floor

Get the locations of all connected clients on a floor.

Tags: `Essentials - ExtremeLocation`

Parameters:

- `parentId` query, required (integer) — Location Id of the floor's parent
- `floorId` query, required (integer) — Location Id of the floor

Responses:

- `200` — OK

## GET `/endusers/client/locked-list`

Operation: `lockedClients`

List locked clients

List a page of clients that are locked due to too many failed authentication attempts.

Tags: `Configuration - User Management`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `sortField` query, optional (XiqLockedClientSortField) — The sort field
- `sortOrder` query, optional (XiqSortOrder) — The sort order (ascending by default)

Responses:

- `200` — OK

## GET `/email-templates`

Operation: `listEmailTemplates`

List Email templates

List all Email notification templates.

Tags: `Configuration - User Management`

Parameters:

- `passwordType` query, optional (XiqPasswordType) — The password type

Responses:

- `200` — OK

## GET `/devices`

Operation: `listDevices`

[LRO] List devices

List devices with filters and pagination.

Tags: `Device`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `locationId` query, optional (integer) — Location Id
- `connected` query, optional (boolean) — The device connect status
- `adminStates` query, optional (array) — The device admin states
- `macAddresses` query, optional (array) — The device mac addresses
- `sns` query, optional (array) — The device serial numbers
- `hostnames` query, optional (array) — The device host names
- `sortField` query, optional (XiqDeviceSortField) — The sort field
- `order` query, optional (XiqSortOrder) — The sort order (ascending by default)
- `views` query, optional (array) — The views to return device fields (Check fields for each view at XiqDeviceView schema)
- `fields` query, optional (array) — The device fields to return
- `deviceTypes` query, optional (array) — The device types to return
- `nullField` query, optional (XiqDeviceNullField) — The device empty field, only returns the selected field that is null
- `locationIds` query, optional (array) — The location IDs
- `async` query, optional (boolean) — Whether to enable async mode
- `configMismatch` query, optional (boolean) — Config audit status(MATCHED(false) or UNMATCHED(true))

Responses:

- `200` — OK

## GET `/devices/{id}`

Operation: `getDevice`

Get device info for a specific device

Get device info for a specific device.

Tags: `Device`

Parameters:

- `id` path, required (integer) — The device ID
- `views` query, optional (array) — The views to return device fields (Check details at XiqDeviceView schema)
- `fields` query, optional (array) — The device fields to return

Responses:

- `200` — OK

## DELETE `/devices/{id}`

Operation: `deleteDevice`

Delete a device

Delete a specific device.

Tags: `Device`

Parameters:

- `id` path, required (integer) — The device ID
- `force_delete` query, optional (boolean) — Force deletion of device

Responses:

- `200` — OK

## GET `/devices/{id}/ssid/status`

Operation: `getDeviceLevelSsidStatus`

Get SSID status for a device

Get the SSIDs status on each wifi interface for a specific device.

Tags: `Device`

Parameters:

- `id` path, required (integer) — The device ID

Responses:

- `200` — OK

## GET `/devices/{id}/monitor/refresh/status`

Operation: `monitorRefreshDeviceStatus`

Monitor refresh a device status

Monitor refresh a specific device status.

Tags: `Device`

Parameters:

- `id` path, required (integer) — The device ID
- `taskKey` query, required (string) — Monitor refresh task key

Responses:

- `200` — OK

## GET `/devices/{id}/iot`

Operation: `getDeviceIot`

Get the device IoT Wireless Interface settings

Get the device IoT profile Wireless Interface settings by device ID.

Tags: `Device`

Parameters:

- `id` path, required (integer) — The device ID

Responses:

- `200` — OK

## GET `/devices/{id}/interfaces/wifi`

Operation: `getDeviceWifiInterface`

Get the device WiFi interfaces stats

Get the device WiFi interfaces stats by device ID.

Tags: `Device`

Parameters:

- `id` path, required (integer) — The device ID
- `startTime` query, required (integer) — The start time for collecting the wifi interfaces stat
- `endTime` query, required (integer) — The end time for collecting the wifi interfaces stat

Responses:

- `200` — OK

## GET `/devices/{id}/installation-report`

Operation: `getXiqDeviceInstallationReport`

Get device installation report

Get device installation report of a specific device.

Tags: `Device`

Parameters:

- `id` path, required (integer) — The device ID

Responses:

- `200` — OK

## GET `/devices/{id}/ibeacon`

Operation: `getDeviceIbeacon`

Get the device iBeacon setting

Get the device iBeacon setting by device ID.

Tags: `Device`

Parameters:

- `id` path, required (integer) — The device ID

Responses:

- `200` — OK

## GET `/devices/{id}/history/cpu-mem`

Operation: `getDeviceCpuMemoryHistory`

Get device CPU/memory usage history

Get average device CPU and memory usage history.

Tags: `Device`

Parameters:

- `id` path, required (integer) — Device ID
- `startTime` query, required (integer) — The start time to query, epoch time in milliseconds since 1/1/1970
- `endTime` query, required (integer) — The end time to query, epoch time in milliseconds since 1/1/1970
- `interval` query, optional (integer) — The aggregate interval in minutes, min = 10

Responses:

- `200` — OK

## GET `/devices/{id}/geolocation`

Operation: `getDeviceGeolocation`

Get Geolocation for a device

Get the Geolocation info for a specific device.

Tags: `Device`

Parameters:

- `id` path, required (integer) — The device ID

Responses:

- `200` — OK

## GET `/devices/{id}/gallery-image`

Operation: `downloadDeviceGalleryImage`

Download device gallery image.

Download the image file from the device media gallery.

Tags: `Device`

Parameters:

- `id` path, required (integer) — The device ID
- `imageName` query, required (string) — The image name

Responses:

- `200` — OK

## GET `/devices/{id}/alarms`

Operation: `listDeviceAlarm`

List alarms for a device

List alarms for a specific device.

Tags: `Device`

Parameters:

- `id` path, required (integer) — Device ID
- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `startTime` query, required (integer) — The start time for query alarm
- `endTime` query, required (integer) — The end time for query alarm

Responses:

- `200` — OK

## GET `/devices/stats`

Operation: `getDeviceStats`

Get device stats

Get device stats, such as total device count, managed device count, connected device count, etc.

Tags: `Device`

Parameters:

- `locationId` query, optional (integer) — The location ID

Responses:

- `200` — OK

## GET `/devices/rm-devices-stack/{stackId}`

Operation: `getStackMemberInfo`

Get Stack Member Info for a given stack id

Retrieve information about stack members.

Tags: `Device`

Parameters:

- `stackId` path, required (integer) — The stack ID

Responses:

- `200` — OK

## GET `/devices/reports/{id}`

Operation: `downloadExportCsvFile`

Download the Export CSV file

Download the Export CSV file for Device Status

Tags: `Device`

Parameters:

- `id` path, required (string) — The report ID

Responses:

- `200` — OK

## GET `/devices/radio-information`

Operation: `listDevicesRadioInformation`

Get Devices Radio Information

Get client radios information of the devices.

Tags: `Device`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Number of Records, min = 1, max = 50
- `deviceIds` query, required (array) — the list of devices
- `includeDisabledRadio` query, optional (boolean) — Include Disabled Radios

Responses:

- `200` — OK

## GET `/devices/network-policy/{policyId}`

Operation: `listDevicesByNetworkPolicy`

List assigned devices for network policy

List assigned devices for the network policy with pagination.

Tags: `Device`

Parameters:

- `policyId` path, required (integer) — The network policy ID
- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100

Responses:

- `200` — OK

## GET `/devices/digital-twin`

Operation: `listDigitalTwinProducts`

List Digital Twin product information.

List of Digital Twin product information with pagination.

Tags: `Device`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `makes` query, optional (array) — List by makes or any with null/empty makes.
- `models` query, optional (array) — List by makes or any with null/empty models.

Responses:

- `200` — OK

## GET `/deployments/{deploymentId}/status`

Operation: `getDeploymentByIdStatus`

[LRO] Get firmware deployment status by ID

Get firmware upgrade schedule status for a site based on deployment ID.

Tags: `Configuration - Deployment`

Parameters:

- `deploymentId` path, required (integer) — The deployment ID
- `async` query, optional (boolean) — Whether to enable async mode

Responses:

- `200` — OK

## GET `/deployments/status`

Operation: `getDeployStatus`

Get configuration deployment status

Get configuration deployment status for the target devices.

Tags: `Configuration - Deployment`

Parameters:

- `deviceIds` query, required (array) — The target device IDs

Responses:

- `200` — OK

## GET `/deployments/overview`

Operation: `getDeployOverview`

Get configuration deployment overview

Get configuration deployment status overview.

Tags: `Configuration - Deployment`

Responses:

- `200` — OK

## GET `/dashboard/wireless/usage-capacity/reports/{id}`

Operation: `downloadUsageAndCapacityReport`

Download the report

Download report of Metrics

Tags: `Dashboard Wireless Usage and Capacity`

Parameters:

- `id` path, required (string) — The report ID

Responses:

- `200` — OK

## GET `/dashboard/wireless/device-health/reports/{id}`

Operation: `downloadDeviceHealthReport`

Download the report

Download report of Metrics

Tags: `Dashboard Wireless Device Health`

Parameters:

- `id` path, required (string) — The report ID

Responses:

- `200` — OK

## GET `/dashboard/wireless/device-health/reboot/summary`

Operation: `getDeviceRebootSummary`

Device reboot summary for wireless device

Returns the device reboot summary of wireless device based on the provided filters.

Tags: `Dashboard Wireless Device Health`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `deviceId` query, optional (integer) — The device Id

Responses:

- `200` — OK

## GET `/dashboard/wireless/client-health/reports/{id}`

Operation: `downloadClientHealthReport`

Download the report

Download report of Metrics

Tags: `Dashboard Wireless Client Health`

Parameters:

- `id` path, required (string) — The report ID

Responses:

- `200` — OK

## GET `/dashboard/reports/{id}`

Operation: `downloadSiteWithIssueReport`

Download the report

Download report of Metrics

Tags: `Dashboard`

Parameters:

- `id` path, required (string) — The report ID

Responses:

- `200` — OK

## GET `/dashboard/device-types`

Operation: `getAllDiagnosticsDeviceTypes`

Get all diagnostics device types

Returns all available diagnostics device types (unspecified, wired, wireless, or all).

Tags: `Dashboard`

Responses:

- `200` — OK

## GET `/d360/wireless/interfaces-stats`

Operation: `getWirelessWifi`

Get Wifi Information

Returns the information related to wifi0, wifi1 and wifi2.

Tags: `D360`

Parameters:

- `deviceId` query, required (integer) — The unique identifier of the wireless device
- `startTime` query, required (integer) — Start time in milliseconds (epoch time)
- `endTime` query, required (integer) — End time in milliseconds (epoch time)
- `selectedTime` query, optional (integer) — Selected time in milliseconds (epoch time). Optional parameter.

Responses:

- `200` — OK

## GET `/d360/wireless/interfaces-graph`

Operation: `getWirelessInterfaceGraph`

Get Wireless Interface Graph

List a list of wireless interfaces metrics for Graphing API.

Tags: `D360`

Parameters:

- `deviceId` query, required (integer) — The device ID
- `startTime` query, required (integer) — The start time
- `endTime` query, required (integer) — The end time
- `channel` query, required (XiqRmChannelFilterType) — The channel utilization type
- `source` query, optional (array) — The source type as channel utilization or connected clients (By default both are shown)

Responses:

- `200` — OK

## GET `/d360/wired/queue-grid`

Operation: `getWiredQueueGrid`

Wired QOS queue grid

Returns all QOS queue statistics for a wired device

Tags: `D360`

Parameters:

- `deviceId` query, required (integer)
- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100

Responses:

- `200` — OK

## GET `/d360/ssid-metadata`

Operation: `getSsidMetadata`

Get SSID Metadata

Returns the SSID metadata for surrounding APs

Tags: `D360`

Parameters:

- `deviceId` query, required (integer)
- `startTime` query, required (integer)
- `endTime` query, required (integer)

Responses:

- `200` — OK

## GET `/d360/overview/devices-summary`

Operation: `getDeviceSummary_1`

List the summary of device details

List the summary of device details.

Tags: `D360`

Parameters:

- `deviceId` query, required (integer) — The device ID

Responses:

- `200` — OK

## GET `/d360/event/graph`

Operation: `getEventsGraph`

Get Client Grid Filter Metadata

Retrieve a time-series graph of event metrics. Each timestamp includes an array of event types with their respective counts. Only selected filters will be included in the response.

Tags: `D360`

Parameters:

- `deviceId` query, required (integer)
- `startTime` query, required (integer)
- `endTime` query, required (integer)
- `filter` query, optional (array) — The Enum for graph filter type

Responses:

- `200` — OK

## GET `/d360/device/tunnel-status`

Operation: `getDeviceTunnelStatus`

Get Device Tunnel Status

Returns the tunnel policy status for a device, including the state of primary, secondary, and tertiary tunnel endpoints. Instead of raw IP addresses, the Tunnel Concentrator Service name is resolved where possible.

Tags: `D360`

Parameters:

- `deviceId` query, required (integer) — The device ID

Responses:

- `200` — OK

## GET `/d360/device/stats`

Operation: `getDeviceStats_1`

Get Device Stats

Gives the device Stats

Tags: `D360`

Parameters:

- `deviceId` query, required (integer) — The device ID
- `startTime` query, required (integer) — The start time
- `endTime` query, required (integer) — The end time

Responses:

- `200` — OK

## GET `/d360/device/metadata`

Operation: `getDeviceMetaData`

Get Device MetaData

Gives the device information along with placement co-ordinates and floor map

Tags: `D360`

Parameters:

- `deviceId` query, required (integer)

Responses:

- `200` — OK

## GET `/d360/device/issues`

Operation: `getDeviceIssues`

Get Device Issues

Returns the information related to device issues

Tags: `D360`

Parameters:

- `deviceId` query, required (integer)
- `startTime` query, required (integer)
- `endTime` query, required (integer)

Responses:

- `200` — OK

## GET `/d360/device/interfaces`

Operation: `getWifiInterfacePerDevice`

Get Wifi Interfaces Per Device Information

Returns the information related to wifi0, wifi1, and wifi2 interfaces available per device model.

Tags: `D360`

Parameters:

- `deviceModel` query, required (string) — The Enum for device model

Responses:

- `200` — OK

## GET `/d360/client/stats`

Operation: `getClientStats`

Get Client Stats Information

Returns the information related to Client Stats.

Tags: `D360`

Parameters:

- `deviceId` query, required (integer)
- `startTime` query, required (integer)
- `endTime` query, required (integer)
- `selectedTime` query, optional (integer)

Responses:

- `200` — OK

## GET `/d360/client/grid/metadata`

Operation: `getClientGridMetadata`

Get Client Grid Filter Metadata

Returns the metadata for the client grid

Tags: `D360`

Parameters:

- `deviceId` query, required (integer)
- `startTime` query, required (integer)
- `endTime` query, required (integer)

Responses:

- `200` — OK

## GET `/cwps`

Operation: `listCaptiveWebPortals`

List captive web portals

List a page of Captive Web Portals.

Tags: `Configuration - Authentication`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100

Responses:

- `200` — OK

## GET `/countries`

Operation: `getCountryList`

Get country list

Get list of countries and country codes.

Tags: `Misc`

Responses:

- `200` — OK

## GET `/countries/{countryCode}/:validate`

Operation: `validateCountryCode`

Validate country code

Validate whether the country code is a valid code or not.

Tags: `Misc`

Parameters:

- `countryCode` path, required (integer) — The country code.

Responses:

- `200` — OK

## GET `/countries/{countryAlpha2Code}/states`

Operation: `getStateListByCountryCode`

Get state list by country code

Get list of states or provinces in a country with country alpha2 code.

Tags: `Misc`

Parameters:

- `countryAlpha2Code` path, required (string)

Responses:

- `200` — OK

## GET `/copilot/connectivity/wireless/views`

Operation: `getWirelessViews`

Tags: `Copilot - Connectivity Experience`

Parameters:

- `viewType` query, required (XiqWirelessViewsListType) — The type of View

Responses:

- `200` — OK

## GET `/copilot/connectivity/wireless/time-to-connect`

Operation: `getWirelessTimeToConnect`

Tags: `Copilot - Connectivity Experience`

Parameters:

- `viewType` query, required (XiqConnectivityExperienceViewType) — The type of View
- `startTime` query, required (integer) — The start time to query, epoch time in milliseconds since 1/1/1970
- `endTime` query, required (integer) — The end time to query, epoch time in milliseconds since 1/1/1970
- `viewId` query, optional (string) — The view type identifier
- `forensicBucket` query, optional (XiqForensicBucket) — The time period bucket detected
- `locationId` query, optional (string) — The location identifier
- `locationType` query, optional (string) — The location type

Responses:

- `200` — OK

## GET `/copilot/connectivity/wireless/quality-index`

Operation: `getWirelessQualityIndex`

Tags: `Copilot - Connectivity Experience`

Parameters:

- `viewType` query, required (XiqConnectivityExperienceViewType) — The type of View
- `startTime` query, required (integer) — The start time to query, epoch time in milliseconds since 1/1/1970
- `endTime` query, required (integer) — The end time to query, epoch time in milliseconds since 1/1/1970
- `viewId` query, optional (string) — The view type identifier
- `forensicBucket` query, optional (XiqForensicBucket) — The time period bucket detected
- `locationId` query, optional (string) — The location identifier
- `locationType` query, optional (string) — The location type

Responses:

- `200` — OK

## GET `/copilot/connectivity/wireless/performance`

Operation: `getWirelessPerformance`

Tags: `Copilot - Connectivity Experience`

Parameters:

- `viewType` query, required (XiqConnectivityExperienceViewType) — The type of View
- `startTime` query, required (integer) — The start time to query, epoch time in milliseconds since 1/1/1970
- `endTime` query, required (integer) — The end time to query, epoch time in milliseconds since 1/1/1970
- `viewId` query, optional (string) — The view type identifier
- `forensicBucket` query, optional (XiqForensicBucket) — The time period bucket detected
- `locationId` query, optional (string) — The location identifier
- `locationType` query, optional (string) — The location type

Responses:

- `200` — OK

## GET `/copilot/connectivity/wireless/locations/time-to-connect`

Operation: `getWirelessTimeToConnectByLocation`

Tags: `Copilot - Connectivity Experience`

Parameters:

- `buildingId` query, required (string) — The location identifier for building
- `ssid` query, optional (string) — The ssid
- `osType` query, optional (string) — The client type
- `startTime` query, required (integer) — The start time to query, epoch time in milliseconds since 1/1/1970
- `endTime` query, required (integer) — The end time to query, epoch time in milliseconds since 1/1/1970
- `forensicBucket` query, optional (XiqForensicBucket) — The time period bucket detected

Responses:

- `200` — OK

## GET `/copilot/connectivity/wireless/locations/quality-index`

Operation: `getWirelessQualityIndexByLocation`

Tags: `Copilot - Connectivity Experience`

Parameters:

- `buildingId` query, required (string) — The location identifier for building
- `ssid` query, optional (string) — The ssid
- `osType` query, optional (string) — The os type
- `startTime` query, required (integer) — The start time to query, epoch time in milliseconds since 1/1/1970
- `endTime` query, required (integer) — The end time to query, epoch time in milliseconds since 1/1/1970
- `forensicBucket` query, optional (XiqForensicBucket) — The time period bucket detected

Responses:

- `200` — OK

## GET `/copilot/connectivity/wireless/locations/performance`

Operation: `getWirelessPerformanceByLocation`

Tags: `Copilot - Connectivity Experience`

Parameters:

- `buildingId` query, required (string) — The location identifier for building
- `ssid` query, optional (string) — The ssid
- `osType` query, optional (string) — The client type
- `startTime` query, required (integer) — The start time to query, epoch time in milliseconds since 1/1/1970
- `endTime` query, required (integer) — The end time to query, epoch time in milliseconds since 1/1/1970
- `forensicBucket` query, optional (XiqForensicBucket) — The time period bucket detected

Responses:

- `200` — OK

## GET `/copilot/connectivity/wireless/locations/events`

Operation: `getWirelessEventsByLocation`

Tags: `Copilot - Connectivity Experience`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Number of Records, min = 1, max = 100
- `startTime` query, required (integer) — The start time to query, epoch time in milliseconds since 1/1/1970
- `endTime` query, required (integer) — The end time to query, epoch time in milliseconds since 1/1/1970
- `sortField` query, optional (XiqCopilotEventsWirelessSortField) — the sort field
- `sortOrder` query, optional (XiqSortOrder) — The sorting order
- `scoreType` query, required (XiqCopilotWirelessEventsScoreType) — The wireless score type
- `forensicBucket` query, optional (XiqForensicBucket) — The time period bucket detected
- `searchKey` query, optional (string) — The search key
- `locationId` query, required (string) — The location identifier
- `timestamp` query, optional (integer) — The timestamp to query, epoch time in milliseconds since 1/1/1970
- `ssid` query, optional (string) — The ssid
- `osType` query, optional (string) — The os type

Responses:

- `200` — OK

## GET `/copilot/connectivity/wireless/experience`

Operation: `getWirelessConnectivityExperience`

Tags: `Copilot - Connectivity Experience`

Parameters:

- `viewType` query, required (XiqConnectivityExperienceViewType) — View by location, ssid or osTypes
- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Number of Records, min = 1, max = 100
- `startTime` query, required (integer) — The start time to query, epoch time in milliseconds since 1/1/1970
- `endTime` query, required (integer) — The end time to query, epoch time in milliseconds since 1/1/1970
- `sortField` query, optional (XiqSortField) — sort by name or quality index
- `sortOrder` query, optional (XiqSortOrder) — The sorting order

Responses:

- `200` — OK

## GET `/copilot/connectivity/wireless/events`

Operation: `getWirelessEvents`

Tags: `Copilot - Connectivity Experience`

Parameters:

- `viewType` query, required (XiqConnectivityExperienceViewType) — View by location, ssid or osTypes
- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Number of Records, min = 1, max = 100
- `startTime` query, required (integer) — The start time to query, epoch time in milliseconds since 1/1/1970
- `endTime` query, required (integer) — The end time to query, epoch time in milliseconds since 1/1/1970
- `sortField` query, optional (XiqCopilotEventsWirelessSortField) — the sort field
- `sortOrder` query, optional (XiqSortOrder) — The sorting order
- `viewId` query, optional (string) — The view type identifier
- `scoreType` query, required (XiqCopilotWirelessEventsScoreType) — The wireless score type
- `forensicBucket` query, optional (XiqForensicBucket) — The time period bucket detected
- `searchKey` query, optional (string) — The search key
- `locationId` query, optional (string) — The location identifier
- `locationType` query, optional (string) — The location type
- `timestamp` query, optional (integer) — The timestamp to query, epoch time in milliseconds since 1/1/1970

Responses:

- `200` — OK

## GET `/copilot/connectivity/wireless/apps`

Operation: `getWirelessApps`

Tags: `Copilot - Connectivity Experience`

Parameters:

- `viewType` query, required (XiqConnectivityExperienceViewType) — The type of View
- `startTime` query, required (integer) — The start time to query, epoch time in milliseconds since 1/1/1970
- `endTime` query, required (integer) — The end time to query, epoch time in milliseconds since 1/1/1970
- `viewId` query, optional (string) — The view type identifier
- `forensicBucket` query, optional (XiqForensicBucket) — The time period bucket detected
- `locationId` query, optional (string) — The location identifier
- `locationType` query, optional (string) — The location type

Responses:

- `200` — OK

## GET `/copilot/connectivity/wired/quality-index`

Operation: `getWiredQualityIndex`

Tags: `Copilot - Connectivity Experience`

Parameters:

- `viewType` query, optional (XiqWiredViewType) — The type of View
- `startTime` query, required (integer) — The start time to query, epoch time in milliseconds since 1/1/1970
- `endTime` query, required (integer) — The end time to query, epoch time in milliseconds since 1/1/1970
- `viewId` query, optional (string) — The view id based on view type
- `forensicBucket` query, optional (XiqForensicBucket) — The selected time bucket

Responses:

- `200` — OK

## GET `/copilot/connectivity/wired/locations/hardware`

Operation: `getWiredHardwareByLocation`

Tags: `Copilot - Connectivity Experience`

Parameters:

- `viewType` query, optional (XiqWiredViewType) — The type of View
- `startTime` query, required (integer) — The start time to query, epoch time in milliseconds since 1/1/1970
- `endTime` query, required (integer) — The end time to query, epoch time in milliseconds since 1/1/1970
- `viewId` query, optional (string) — The view id based on view type
- `forensicBucket` query, required (XiqForensicBucket) — The selected time bucket

Responses:

- `200` — OK

## GET `/copilot/connectivity/wired/hardware`

Operation: `getWiredHardware`

Tags: `Copilot - Connectivity Experience`

Parameters:

- `viewType` query, required (XiqWiredViewType) — The type of View
- `startTime` query, required (integer) — The start time to query, epoch time in milliseconds since 1/1/1970
- `endTime` query, required (integer) — The end time to query, epoch time in milliseconds since 1/1/1970
- `viewId` query, optional (string) — The view id based on view type
- `forensicBucket` query, required (XiqForensicBucket) — The selected time bucket

Responses:

- `200` — OK

## GET `/copilot/connectivity/wired/experience`

Operation: `getWiredConnectivityExperience`

Tags: `Copilot - Connectivity Experience`

Parameters:

- `viewType` query, required (XiqWiredViewType) — The type of View
- `startTime` query, required (integer) — The start time to query, epoch time in milliseconds since 1/1/1970
- `endTime` query, required (integer) — The end time to query, epoch time in milliseconds since 1/1/1970
- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `sortField` query, optional (XiqSortField) — sort by name or quality index
- `sortOrder` query, optional (XiqSortOrder) — The sorting order

Responses:

- `200` — OK

## GET `/copilot/connectivity/wired/events`

Operation: `getWiredEvents`

Tags: `Copilot - Connectivity Experience`

Parameters:

- `viewType` query, required (XiqWiredViewType) — The type of View
- `startTime` query, required (integer) — The start time to query, epoch time in milliseconds since 1/1/1970
- `endTime` query, required (integer) — The end time to query, epoch time in milliseconds since 1/1/1970
- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `sortBy` query, optional (XiqCopilotEventsWiredSortField) — The sort field
- `sortOrder` query, optional (XiqSortOrder) — The sorting order
- `viewId` query, optional (string) — The view id based on view type
- `forensicBucket` query, required (XiqForensicBucket) — The selected time bucket
- `scoreType` query, required (XiqCopilotWiredEventsScoreType) — The selected score type
- `searchKey` query, optional (string) — The selected search key
- `locationType` query, optional (string) — The selected location type
- `locationId` query, optional (string) — The selected location id
- `timestamp` query, optional (integer) — The timestamp to query, epoch time in milliseconds since 1/1/1970

Responses:

- `200` — OK

## GET `/copilot/connectivity/locations`

Operation: `getConnectivityDetailsByLocations`

Tags: `Copilot - Connectivity Experience`

Parameters:

- `startTime` query, required (integer) — The start time to query, epoch time in milliseconds since 1/1/1970
- `endTime` query, required (integer) — The end time to query, epoch time in milliseconds since 1/1/1970
- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `sortField` query, optional (XiqSortField) — sort by name or quality index
- `sortOrder` query, optional (XiqSortOrder) — The sorting order
- `locationId` query, optional (integer) — The location Id
- `searchKey` query, optional (string) — The search value
- `clientType` query, optional (XiqClientType) — The client type
- `forensicBucket` query, optional (XiqForensicBucket) — The time period bucket detected
- `qualityIndex` query, optional (XiqQualityIndex) — The quality index value

Responses:

- `200` — OK

## GET `/copilot/connectivity/client-type`

Operation: `getConnectivityDetailsByClientType`

Tags: `Copilot - Connectivity Experience`

Parameters:

- `startTime` query, required (integer) — The start time to query, epoch time in milliseconds since 1/1/1970
- `endTime` query, required (integer) — The end time to query, epoch time in milliseconds since 1/1/1970
- `locationId` query, optional (integer) — The location Id
- `clientType` query, optional (XiqClientType) — The client type
- `forensicBucket` query, optional (XiqForensicBucket) — The time period bucket detected

Responses:

- `200` — OK

## GET `/copilot/assurance-scans/overview`

Operation: `getAssuranceScansOverviewData`

Tags: `Copilot - Anomalies`

Responses:

- `200` — OK

## GET `/copilot/anomalies/wifi-efficiency/stats`

Operation: `getWifiEfficiencyStats`

Tags: `Copilot - Anomalies`

Parameters:

- `anomalyId` query, required (string) — The anomaly id

Responses:

- `200` — OK

## GET `/copilot/anomalies/wifi-efficiency/client-list`

Operation: `getWifiEfficiencyClientList`

Tags: `Copilot - Anomalies`

Parameters:

- `deviceId` query, required (integer) — The device id
- `channel` query, required (integer) — The channel number
- `timestamp` query, required (integer) — The timestamp

Responses:

- `200` — OK

## GET `/copilot/anomalies/wifi-capacity/stats`

Operation: `getWifiCapacityStats`

Tags: `Copilot - Anomalies`

Parameters:

- `anomalyId` query, required (string) — The anomaly id

Responses:

- `200` — OK

## GET `/copilot/anomalies/wifi-capacity/client-list`

Operation: `getWifiCapacityClientList`

Tags: `Copilot - Anomalies`

Parameters:

- `deviceId` query, required (integer) — The device id
- `channel` query, required (integer) — The channel
- `timestamp` query, required (integer) — The timestamp

Responses:

- `200` — OK

## GET `/copilot/anomalies/report`

Operation: `getAnomaliesReport`

Tags: `Copilot - Anomalies`

Parameters:

- `startTime` query, required (integer) — The start time to query, epoch time in milliseconds since 1/1/1970
- `endTime` query, required (integer) — The end time to query, epoch time in milliseconds since 1/1/1970
- `anomalyType` query, optional (XiqAnomalyType) — The type of anomaly
- `buildingId` query, optional (integer) — The location identifier
- `severity` query, optional (XiqAnomalySeverity) — The severity of anomaly
- `excludeMuted` query, optional (boolean) — Exclude muted anomalies
- `sortField` query, optional (XiqAnomalySortField) — The sorting field
- `sortOrder` query, optional (XiqSortOrder) — The sorting order
- `searchKey` query, optional (string) — The search key
- `fileType` query, optional (string) — The file format
- `offsetTime` query, required (integer) — The offset value

Responses:

- `200` — OK

## GET `/copilot/anomalies/port-efficiency/stats`

Operation: `getPortEfficiencyStats`

Tags: `Copilot - Anomalies`

Parameters:

- `anomalyId` query, required (string) — The anomaly id
- `offsetTime` query, optional (integer) — The offset value

Responses:

- `200` — OK

## GET `/copilot/anomalies/port-efficiency/speed-duplex-stats`

Operation: `getPortEfficiencySpeedDuplexStats`

Tags: `Copilot - Anomalies`

Parameters:

- `anomalyId` query, required (string) — The anomaly id

Responses:

- `200` — OK

## GET `/copilot/anomalies/poeflapping/trends`

Operation: `getPoeFlappingTrends`

Tags: `Copilot - Anomalies`

Parameters:

- `anomalyId` query, required (string) — The anomaly id

Responses:

- `200` — OK

## GET `/copilot/anomalies/poeflapping/stats`

Operation: `getPoeFlappingStats`

Tags: `Copilot - Anomalies`

Parameters:

- `anomalyId` query, required (string) — The anomaly id

Responses:

- `200` — OK

## GET `/copilot/anomalies/poeflapping/lldp-cdp-info`

Operation: `getLldpCdpInfo`

Tags: `Copilot - Anomalies`

Parameters:

- `anomalyType` query, required (XiqAnomalyType) — The anomaly Type
- `anomalyId` query, required (string) — The anomaly ID
- `deviceId` query, required (integer) — The device ID
- `lastDetectedTime` query, required (integer) — The last detected timestamp of anomaly

Responses:

- `200` — OK

## GET `/copilot/anomalies/notifications`

Operation: `getAnomaliesNotifications`

Tags: `Copilot - Anomalies`

Responses:

- `200` — OK

## GET `/copilot/anomalies/missing-vlan/count`

Operation: `getMissingVlanAnomaliesCount`

Tags: `Copilot - Anomalies`

Parameters:

- `startTime` query, required (integer) — The start time to query, epoch time in milliseconds since 1/1/1970
- `endTime` query, required (integer) — The end time to query, epoch time in milliseconds since 1/1/1970
- `vlanIds` query, required (array) — The Vlan ids
- `siteIds` query, required (array) — The Site ids

Responses:

- `200` — OK

## GET `/copilot/anomalies/locations`

Operation: `listAnomalyLocations`

Tags: `Copilot - Anomalies`

Parameters:

- `anomalyType` query, optional (XiqAnomalyType) — Anomaly type
- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Number of Records, min = 1, max = 100
- `sortField` query, optional (XiqAnomalySortField) — sort by field
- `sortOrder` query, optional (XiqSortOrder) — The sorting order
- `excludeMuted` query, optional (boolean) — exclude muted

Responses:

- `200` — OK

## GET `/copilot/anomalies/hardware-health/stats`

Operation: `getHardwareHealthStats`

Tags: `Copilot - Anomalies`

Parameters:

- `anomalyId` query, required (string) — The anomaly id

Responses:

- `200` — OK

## GET `/copilot/anomalies/hardware-health/cpu-mem-stats`

Operation: `getHardwareHealthCpuMemStats`

Tags: `Copilot - Anomalies`

Parameters:

- `deviceId` query, required (integer) — The device id
- `statsField` query, required (XiqAnomalyHhStatsType) — Field selector
- `timestamp` query, required (integer) — The timestamp

Responses:

- `200` — OK

## GET `/copilot/anomalies/hardware-health/client-list`

Operation: `getHardwareHealthClientList`

Tags: `Copilot - Anomalies`

Parameters:

- `deviceId` query, required (integer) — The device id
- `timestamp` query, required (integer) — The timestamp

Responses:

- `200` — OK

## GET `/copilot/anomalies/excluded-vlans-list`

Operation: `getMissingVlanExcludedVlanList`

Tags: `Copilot - Anomalies`

Parameters:

- `page` query, optional (integer) — Page number, min =1
- `limit` query, optional (integer) — Number of Records, min = 1, max = 100

Responses:

- `200` — OK

## GET `/copilot/anomalies/dfs-recurrence/count-stats`

Operation: `getDfsRecurrenceCountStats`

Tags: `Copilot - Anomalies`

Parameters:

- `anomalyId` query, required (string) — The anomaly id

Responses:

- `200` — OK

## GET `/copilot/anomalies/dfs-recurrence/channel-stats`

Operation: `getDfsRecurrenceChannelStats`

Tags: `Copilot - Anomalies`

Parameters:

- `anomalyId` query, required (string) — The anomaly id

Responses:

- `200` — OK

## GET `/copilot/anomalies/devices-with-locations`

Operation: `getCopilotDevicesWithLocations`

Tags: `Copilot - Anomalies`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Number of Records, min = 1, max = 100
- `anomalyType` query, optional (XiqAnomalyType) — The type of anomaly
- `startTime` query, required (integer) — The start time to query, epoch time in milliseconds since 1/1/1970
- `endTime` query, required (integer) — The end time to query, epoch time in milliseconds since 1/1/1970
- `buildingId` query, optional (integer) — The location identifier
- `severity` query, optional (XiqAnomalySeverity) — The severity of anomaly
- `excludeMuted` query, optional (boolean) — Exclude muted anomalies
- `sortField` query, optional (XiqAnomalySortField) — The sorting field
- `sortOrder` query, optional (XiqSortOrder) — The sorting order
- `searchKey` query, optional (string) — The search key

Responses:

- `200` — OK

## GET `/copilot/anomalies/devices-by-location`

Operation: `getDevicesByLocation`

Tags: `Copilot - Anomalies`

Parameters:

- `anomalyType` query, optional (XiqAnomalyType) — Anomaly type
- `locationIds` query, required (array) — The location IDs

Responses:

- `200` — OK

## GET `/copilot/anomalies/anomalies-by-category`

Operation: `getCopilotAnomaliesbyCategory`

Tags: `Copilot - Anomalies`

Parameters:

- `anomalyType` query, optional (XiqAnomalyType) — The type of anomaly
- `startTime` query, required (integer) — The start time to query, epoch time in milliseconds since 1/1/1970
- `endTime` query, required (integer) — The end time to query, epoch time in milliseconds since 1/1/1970
- `buildingId` query, optional (integer) — The location identifier
- `severity` query, optional (XiqAnomalySeverity) — The severity od anomaly
- `excludeMuted` query, optional (boolean) — exclude muted

Responses:

- `200` — OK

## GET `/copilot/anomalies/adverse-traffic/packet-counts`

Operation: `getAtpPacketCounts`

Tags: `Copilot - Anomalies`

Parameters:

- `anomalyId` query, required (string) — The anomaly id

Responses:

- `200` — OK

## GET `/copilot/anomalies/adverse-traffic/device-stats`

Operation: `getAtpDeviceStats`

Tags: `Copilot - Anomalies`

Parameters:

- `anomalyId` query, required (string) — The anomaly id

Responses:

- `200` — OK

## GET `/clients/{id}`

Operation: `getClient`

Get client info

Get client detailed information.

Tags: `Client`

Parameters:

- `id` path, required (integer) — The client ID
- `views` query, optional (array) — The views to return client fields (Check fields for each view at XiqClientView schema)
- `fields` query, optional (array) — The client fields to return

Responses:

- `200` — OK

## GET `/clients/usage`

Operation: `getClientUsage`

Get usage per client

Get the client usage.

Tags: `Client`

Parameters:

- `clientIds` query, required (array) — The client IDs
- `startTime` query, required (integer) — The start time to query, epoch time in milliseconds since 1/1/1970
- `endTime` query, required (integer) — The end time to query, epoch time in milliseconds since 1/1/1970

Responses:

- `200` — OK

## GET `/clients/summary`

Operation: `getClientSummary`

Get client summary metrics

Get number of connected wireless clients and number of detected wired clients.

Tags: `Client`

Parameters:

- `locationIds` query, optional (array) — The location IDs
- `deviceIds` query, optional (array) — The device IDs
- `vlans` query, optional (array) — The associate VLAN IDs
- `userProfileNames` query, optional (array) — The user profile names
- `ssids` query, optional (array) — The SSIDs
- `clientOsNames` query, optional (array) — The client os names
- `clientHealthStatus` query, optional (integer) — The client health status: 1 - HEALTHY, 2 - POOR
- `excludeLocallyManaged` query, optional (boolean) — Return Cloud managed Devices' clients count
- `searchString` query, optional (string) — The search string

Responses:

- `200` — OK

## GET `/clients/byMac/{clientMac}`

Operation: `getClientByMac`

Get client info by mac

Get client detailed information based on clientMac.

Tags: `Client`

Parameters:

- `clientMac` path, required (string) — The client mac address
- `views` query, optional (array) — The views to return client fields (Check fields for each view at XiqClientView schema)
- `fields` query, optional (array) — The client fields to return

Responses:

- `200` — OK

## DELETE `/clients/byMac/{clientMac}`

Operation: `disconnectClient`

Disconnect the client

Disconnect the client by macAddress.

Tags: `Client`

Parameters:

- `clientMac` path, required (string) — The client mac address

Responses:

- `200` — OK

## GET `/clients/active`

Operation: `listActiveClients`

List active clients

List active clients with filters and pagination.

Tags: `Client`

Parameters:

- `locationIds` query, optional (array) — The location IDs
- `deviceIds` query, optional (array) — The device IDs
- `vlans` query, optional (array) — The associate vlan IDs
- `userProfileNames` query, optional (array) — The user profile names
- `ssids` query, optional (array) — The SSIDs
- `clientOsNames` query, optional (array) — The client os names
- `clientConnectionTypes` query, optional (array) — The client connection types: 1 - WIRELESS, 2 - WIRED, -1 - UNDETERMINED
- `clientHealthStatus` query, optional (integer) — The client health status: 1 - HEALTHY, 2 - POOR
- `excludeLocallyManaged` query, optional (boolean) — Return Cloud managed Devices' clients
- `userNames` query, optional (array) — The user names
- `searchString` query, optional (string) — The search string
- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `sortField` query, optional (XiqClientSortField) — Sort field
- `sortOrder` query, optional (XiqSortOrder) — Sort order (ascending by default)
- `views` query, optional (array) — The views to return client fields (Check fields for each view at XiqClientView schema)
- `fields` query, optional (array) — The client fields to return

Responses:

- `200` — OK

## GET `/clients/active/count`

Operation: `getActiveClientsCount`

Get active clients count

Get number of active clients with filters and pagination.

Tags: `Client`

Parameters:

- `locationIds` query, optional (array) — The location IDs
- `deviceIds` query, optional (array) — The device IDs
- `vlans` query, optional (array) — The associate VLAN IDs
- `userProfileNames` query, optional (array) — The user profile names
- `ssids` query, optional (array) — The SSIDs
- `clientOsNames` query, optional (array) — The client os names
- `clientConnectionTypes` query, optional (array) — The client connection types: 1 - WIRELESS, 2 - WIRED, -1 - UNDETERMINED
- `clientHealthStatus` query, optional (integer) — The client health status: 1 - HEALTHY, 2 - POOR
- `excludeLocallyManaged` query, optional (boolean) — Return Cloud managed Devices' clients count
- `searchString` query, optional (string) — The search string

Responses:

- `200` — OK

## GET `/client-details/topology/client-trail/{macAddress}`

Operation: `getConnectionTrail`

Tags: `Client - Details`

Parameters:

- `macAddress` path, required (string)

Responses:

- `200` — OK

## GET `/client-details/overview/info/{clientId}`

Operation: `getClientDetailsInfo`

Get Client Details Info

Tags: `Client - Details`

Parameters:

- `clientId` path, required (integer) — The client ID
- `startTime` query, required (integer) — The start time to query, epoch time in milliseconds since 1/1/1970
- `endTime` query, required (integer) — The end time to query, epoch time in milliseconds since 1/1/1970

Responses:

- `200` — OK

## GET `/client-details/overview/chart-data/{clientId}`

Operation: `getClientChartData`

Get Client chart data

Tags: `Client - Details`

Parameters:

- `clientId` path, required (integer) — The client ID
- `startTime` query, required (integer) — The start time to query, epoch time in milliseconds since 1/1/1970
- `endTime` query, required (integer) — The end time to query, epoch time in milliseconds since 1/1/1970
- `precision` query, optional (integer) — The precision in milliseconds since 1/1/1970

Responses:

- `200` — OK

## GET `/client-details/client-trail/roaming-trail/grid/{clientId}`

Operation: `getRoamingTrail`

Get roaming trail grid

get roaming trail grid

Tags: `Client - Details`

Parameters:

- `clientId` path, required (integer) — The client ID
- `startTime` query, required (integer) — The start time to query, epoch time in milliseconds since 1/1/1970
- `endTime` query, required (integer) — The end time to query, epoch time in milliseconds since 1/1/1970
- `precision` query, optional (integer) — The precision in milliseconds since 1/1/1970

Responses:

- `200` — OK

## GET `/client-details/client-trail/roaming-trail/count/{clientId}`

Operation: `getRoamingCount`

Get roaming trail count

get roaming trail count

Tags: `Client - Details`

Parameters:

- `clientId` path, required (integer) — The client ID
- `startTime` query, required (integer) — The start time to query, epoch time in milliseconds since 1/1/1970
- `endTime` query, required (integer) — The end time to query, epoch time in milliseconds since 1/1/1970
- `precision` query, optional (integer) — The precision in milliseconds since 1/1/1970

Responses:

- `200` — OK

## GET `/client-details/client-trail/connectivity-experience/{clientId}`

Operation: `getConnectivityExperienceGrid`

Get connectivity experience grid

get connectivity experience grid

Tags: `Client - Details`

Parameters:

- `clientId` path, required (integer) — The client ID
- `startTime` query, required (integer) — The start time to query, epoch time in milliseconds since 1/1/1970
- `endTime` query, required (integer) — The end time to query, epoch time in milliseconds since 1/1/1970
- `precision` query, optional (integer) — The precision in milliseconds since 1/1/1970
- `keyword` query, optional (string) — The case-insensitive keyword to search
- `includeWired` query, optional (boolean) — Include Wired client
- `onlyWired` query, optional (boolean) — Return only Wired

Responses:

- `200` — OK

## GET `/certificates`

Operation: `listCertificates`

List certificates

List a page of certificates.

Tags: `Configuration - Certificate`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `certType` query, optional (XiqCertificateType) — The certificate type

Responses:

- `200` — OK

## GET `/backup/history/grid`

Operation: `listBackupHistory`

List backup history grid

Tags: `Account`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 10
- `keyword` query, optional (string) — The keyword to search - Display name
- `order` query, optional (XiqSortOrder) — The sort order (descending by default) - on backup date

Responses:

- `200` — OK

## GET `/auth/permissions`

Operation: `listPermissions`

Get permissions for current login user

Get permissions for current login user, which are allowed for generating new API tokens.

Tags: `Authorization`

Responses:

- `200` — Successful operation
- `400` — Bad request
- `401` — UNAUTHORIZED
- `403` — Access denied

## GET `/auth/apitoken/info`

Operation: `getCurrentApiTokenInfo`

Get current API token details

Introspect current API token and get detail information.

Tags: `Authorization`

Responses:

- `200` — OK

## GET `/applications`

Operation: `listApplications`

List the applications

List a page of applications by filter.

Tags: `Application`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `name` query, optional (string) — Application Name
- `detectionProtocol` query, optional (XiqApplicationDetectionProtocol) — Application Detection Protocol, only for custom Application
- `detectionType` query, optional (XiqApplicationDetectionType) — Application Detection Type, only for custom Application
- `predefined` query, optional (boolean) — Flag to filter predefined or custom Application
- `sortField` query, optional (XiqApplicationSortField) — The sort field
- `order` query, optional (XiqSortOrder) — The sort order (ascending by default)

Responses:

- `200` — OK

## GET `/applications/{id}/clients/top{n}`

Operation: `listApplicationTopClientsUsage`

List the TopN clients for a application

List the TopN clients by usage for a specific application.

Tags: `Application`

Parameters:

- `id` path, required (integer) — The application ID
- `n` path, required (integer) — The TopN number
- `startTime` query, required (integer) — The start time for querying top client usage of application
- `endTime` query, required (integer) — The end time for querying top application usage of application

Responses:

- `200` — OK

## GET `/applications/usage/summary/meta-data`

Operation: `listAppUsageSummaryMetaData`

Application usage summary meta data

List the application usage summary meta data

Tags: `Application`

Responses:

- `200` — OK

## GET `/applications/top{n}`

Operation: `listTopApplicationsUsage`

List the TopN applications

List the TopN applications by usage.

Tags: `Application`

Parameters:

- `n` path, required (integer) — The TopN number
- `startTime` query, required (integer) — The start time for querying top application usage
- `endTime` query, required (integer) — The end time for querying top application usage

Responses:

- `200` — OK

## GET `/applications/reports/{id}`

Operation: `downloadExportCsvFile_1`

Download the Export CSV file

Download the Export CSV file for Application Usage Summary

Tags: `Application`

Parameters:

- `id` path, required (string) — The report ID

Responses:

- `200` — OK

## GET `/ap/afc/v2/floorReport/{deviceId}`

Operation: `getRmAfcGeolocaitonFloorReport`

Tags: `AFC`

Parameters:

- `deviceId` path, required (integer) — device Id

Responses:

- `200` — OK

## GET `/ap/afc/interface/details/{sn}`

Operation: `getApsAfcInfo`

Get Afc Summary Data

Get Afc data per site

Tags: `AFC`

Parameters:

- `sn` path, required (string) — The Serial Number of the AP

Responses:

- `200` — OK

## GET `/ap/afc/floorReport/{deviceId}`

Operation: `getAfcGeolocaitonFloorReport`

Tags: `AFC`

Parameters:

- `deviceId` path, required (integer) — Owner Id

Responses:

- `200` — OK

## GET `/ap/afc/diagnostics/{id}`

Operation: `getApsAfcDiagnostics`

Tags: `AFC`

Parameters:

- `ownerId` query, required (integer) — Owner Id
- `id` path, required (integer) — The device id of the AP

Responses:

- `200` — OK

## GET `/alerts`

Operation: `listAlerts`

List the alerts

List a page of alerts by filter.

Tags: `Alert`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100
- `startTime` query, required (integer) — The start time for querying alerts in milliseconds
- `endTime` query, required (integer) — The end time for querying alerts in milliseconds
- `severityIds` query, optional (array) — The alert severity identifiers to filter. The currently supported severity IDs are 1 for critical, 2 for warning, and 3 for info.
- `categoryIds` query, optional (array) — The alert category ID to filter
- `messageMetadataIds` query, optional (array) — The message metadata ID list to filter
- `acknowledged` query, optional (boolean) — The acknowledged to filter, return global data if not specified
- `siteId` query, optional (integer) — The site id to filter
- `floorId` query, optional (integer) — The floor id to filter
- `buildingId` query, optional (integer) — The building id to filter
- `keyword` query, optional (string) — The keyword to filter, such as summary, severity, source, etc.
- `sortField` query, optional (XiqAlertSortField) — The sort field
- `order` query, optional (XiqSortOrder) — The sort order (descending by default)

Responses:

- `200` — OK

## GET `/alerts/reports/{id}`

Operation: `downloadAlertReport`

Download the alerts report

Download report of alerts.

Tags: `Alert`

Parameters:

- `id` path, required (integer) — The report ID

Responses:

- `200` — OK

## GET `/alerts/count-by-{group}`

Operation: `countAlertsByGroup`

Count the alerts by different grouping

Count the number of alerts and events based on Severity, Category, and Alert Type.

Tags: `Alert`

Parameters:

- `group` path, required (XiqAlertGroupQuery) — The group to count from
- `acknowledged` query, optional (boolean) — The acknowledged to filter, return global data if not specified
- `siteId` query, optional (integer) — The site id for counting the alerts, default to global
- `startTime` query, required (integer) — The start time for counting the alerts
- `endTime` query, required (integer) — The end time for counting the alerts

Responses:

- `200` — OK

## GET `/alert-policies/available-sites`

Operation: `listAvailableSites`

The list of current owner's available sites

List all sites belonging to the current owner. If the site has been configured an site policy, then the site will not be available.

Tags: `Alert`

Responses:

- `200` — OK

## GET `/airrm/site/{airrmId}`

Operation: `getSiteDeviceRegulatoryConfigAfcSpectrum`

Get Site Device Regulatory Config and AFC Spectrum

Get AFC spectrum regulatory configuration for all devices in a site

Tags: `airrm-endpoint`

Parameters:

- `airrmId` path, required (integer) — The AIRRM site ID

Responses:

- `200` — OK

## GET `/airrm/radio/apInfo/{radioMac}`

Operation: `getDeviceApInfo`

Get Device AP Information

Get device AP information by radio MAC address

Tags: `airrm-endpoint`

Parameters:

- `radioMac` path, required (string) — The radio MAC address

Responses:

- `200` — OK

## GET `/airrm/device/{serialNumber}`

Operation: `getDeviceRegulatoryConfigAfcSpectrum`

Get Device Regulatory Config and AFC Spectrum

Get AFC spectrum and regulatory configuration for a specific device

Tags: `airrm-endpoint`

Parameters:

- `serialNumber` path, required (string) — The device serial number

Responses:

- `200` — OK

## GET `/afcserver`

Operation: `listAfcServers`

Get Afc Server list and their status

Get all Afc Servers data

Tags: `AFC`

Parameters:

- `ownerId` query, required (integer) — Owner Id

Responses:

- `200` — OK

## GET `/afcserver/{server_id}`

Operation: `getAfcServer`

Get Afc Server data

Tags: `AFC`

Parameters:

- `server_id` path, required (integer) — The Id of the server

Responses:

- `200` — OK

## GET `/afcserver/statistics/{server_id}`

Operation: `getAfcServerStatistics`

Get AFC server Statistics

Tags: `AFC`

Parameters:

- `server_id` path, required (integer) — The Id of the server
- `startTime` query, required (integer) — Query Start Time
- `endTime` query, required (integer) — Query End Time
- `precision` query, optional (integer) — precision specified in seconds

Responses:

- `200` — OK

## GET `/afc/reports/{id}`

Operation: `downloadHealthReport`

Download the report

Download report of Metrics

Tags: `AFC`

Parameters:

- `id` path, required (string) — The report ID

Responses:

- `200` — OK

## GET `/ad-servers`

Operation: `listActiveDirectoryServers`

List active directory servers

List a page of active directory servers.

Tags: `Configuration - Authentication`

Parameters:

- `page` query, optional (integer) — Page number, min = 1
- `limit` query, optional (integer) — Page Size, min = 1, max = 100

Responses:

- `200` — OK

## GET `/acct-api-token/export`

Operation: `exportToCsv_6`

Export all API access tokens to CSV

Export all API access tokens to a CSV file.

Tags: `Administration`

Parameters:

- `order` query, optional (XiqSortOrder) — The sort order (descending by default)
- `keyword` query, optional (string) — The keyword - application name or grantor
- `sortField` query, optional (XiqApiAccessTokenSortField) — The sort field

Responses:

- `200` — OK

## GET `/account/viq`

Operation: `getViqInfo`

Get VIQ Info

Get account VIQ and license info.

Tags: `Account`

Responses:

- `200` — OK

## GET `/account/viq/export-import-status`

Operation: `exportImportStatus`

Get running export/import status

This is used check the live status of VIQ export or import

Tags: `Account`

Parameters:

- `viqOperationType` query, required (XiqViqOperationType) — Select the type of operation to get status

Responses:

- `200` — OK

## GET `/account/viq/download`

Operation: `downloadViqReport`

Download VIQ data file and logs

This is used to download the VIQ export data or export/import logs

Tags: `Account`

Parameters:

- `reportName` query, required (string) — The report full name

Responses:

- `200` — OK

## GET `/account/viq/backup/status`

Operation: `get_viq_backup_status`

Get VIQ Backup Status

Returns IDLE, IN_PROGRESS, COMPLETED or FAILED. Safe to call during an active backup.

Tags: `Account`

Responses:

- `200` — OK

## GET `/account/vhm/status`

Operation: `getVhmStatus`

Get Vhm Status

Get an existing Vhm Status.

Tags: `Account`

Responses:

- `200` — OK

## GET `/account/vhm/setting`

Operation: `getVhmSetting`

Get Vhm Setting

Get an existing Vhm Settings.

Tags: `Account`

Responses:

- `200` — OK

## GET `/account/third-party-applications`

Operation: `getApiAccessTokens`

List Third Party Applications

List a page of Third Party Applications.

Tags: `Account`

Responses:

- `200` — OK

## GET `/account/home`

Operation: `getHomeAccount`

Get home ExtremeCloud IQ account info

Get home ExtremeCloud IQ account info.

Tags: `Account`

Responses:

- `200` — OK

## GET `/account/external`

Operation: `listExternalAccounts`

List accessible external guest accounts

List accessible external ExtremeCloud IQ accounts.

Tags: `Account`

Responses:

- `200` — OK

## DELETE `/subscriptions/webhook/:delete`

Operation: `deleteSubscription`

Delete webhook subscription

Delete an exist webhook subscription.

Tags: `Notification`

Parameters:

- `ids` query, required (array) — The Webhook subscription IDs

Responses:

- `202` — Accepted

## DELETE `/rtts/{id}`

Operation: `DeleteRttsSession`

Tags: `rtts-endpoint`

Parameters:

- `ownerId` query, required (integer) — Owner Id
- `id` path, required (string) — The session id

Responses:

- `200` — OK

## DELETE `/pcgs/key-based/network-policy-{policyId}`

Operation: `deletePcg`

Delete Private Client Group from a network policy

Delete Private Client Group settings from a network policy.

Tags: `Configuration - User Management`

Parameters:

- `policyId` path, required (integer) — The network policy ID
- `ids` query, required (array) — The IDs of the Key-based PCG entity to be deleted from network policy

Responses:

- `202` — Accepted

## DELETE `/ng-reports/scheduled/runs`

Operation: `deleteReportRuns`

Delete report runs

Bulk delete report runs by IDs.

Tags: `NG Reports (Scheduled)`

Parameters:

- `reportRunsIds` query, required (array) — List of report run IDs to delete

Responses:

- `200` — OK

## DELETE `/network-services/{id}`

Operation: `deleteNetworkService`

Delete Network Services

Delete specific Network Services.

Tags: `Configuration - Network`

Parameters:

- `id` path, required (integer) — The Network Service ID

Responses:

- `200` — OK

## DELETE `/locations/folder/zone/{id}`

Operation: `deleteZone`

Delete a zone by ID

Delete a zone for the specified ID.

Tags: `Location`

Parameters:

- `id` path, required (integer) — The Zone ID

Responses:

- `204` — No Content

## DELETE `/locations/floor/{floorId}/label/{labelId}`

Operation: `deleteFloorMapLabel`

Deletes one floor map label

Deletes one floor map label, given by its id, on condition it references the floor given by its id.

Tags: `Location`

Parameters:

- `floorId` path, required (integer) — The Floor ID
- `labelId` path, required (integer)

Responses:

- `200` — OK

## DELETE `/hiq/organizations/{id}`

Operation: `deleteOrganization`

Delete an existing organization

Delete an existing organization (Available when HIQ is enabled).

Tags: `HIQ`

Parameters:

- `id` path, required (integer) — Organization ID to delete

Responses:

- `204` — No Content

## DELETE `/floor/afc/details/{id}`

Operation: `deleteFloorAfcDetails`

Tags: `AFC`

Parameters:

- `ownerId` query, required (integer) — Owner Id
- `id` path, required (integer)

Responses:

- `200` — OK

## DELETE `/devices/radius-proxy/:revoke`

Operation: `revokeDevicesRadiusProxy`

Revoke RADIUS proxy from multiple devices

Revoke the RADIUS proxy from the target devices.

Tags: `Device`

Parameters:

- `ids` query, required (array) — The device IDs

Responses:

- `200` — OK

## DELETE `/certificates/{id}`

Operation: `deleteCertificate`

Delete Certificate by ID

Delete the existing Certificate by the ID.

Tags: `Configuration - Certificate`

Parameters:

- `id` path, required (integer) — The Certificate ID

Responses:

- `200` — OK

## DELETE `/backup/history/delete`

Operation: `deleteBackup`

Backup History Delete

Delete Backup History by backup files.

Tags: `Account`

Parameters:

- `backupFiles` query, required (string) — The list of backup files (comma-separated) that need to be deleted.

Responses:

- `200` — OK

## DELETE `/acct-api-token/:delete`

Operation: `bulkDeleteApiAccessToken`

Bulk Delete API Access token by ID

Tags: `Administration`

Parameters:

- `ids` query, required (array) — The API Access Token IDs

Responses:

- `200` — OK

