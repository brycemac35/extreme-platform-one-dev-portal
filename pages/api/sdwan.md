---
source: https://developer.extremeplatformone.com/api-reference/sdwan
spec: https://developer.extremeplatformone.com/api/spec/sdwan
title: "ExtremeCloud SD-WAN API"
---

# ExtremeCloud SD-WAN API

**SDWAN** · Applications. ExtremeCloud SD-WAN.

ExtremeCloud SD-WAN API allows customers and partners to configure solutions for the management, monitoring, and provisioning of their SD-WAN environment.

Version: `26.2.0.0`

## Servers

- `https://cloudapi.extremecloudiq.com/sdwan` — ExtremeCloud SD-WAN REST API

Full OpenAPI document: [`specs/sdwan.json`](../../specs/sdwan.json)

## Endpoints

295 operations.

| Method | Path | Summary |
| --- | --- | --- |
| POST | `/login` | User login with username and password |
| POST | `/logout` | User logout (Revoke the current access token) |
| GET | `/locations/site` | List sites |
| POST | `/locations/site` | Create site |
| GET | `/locations/site/{id}` | Get site by ID |
| PUT | `/locations/site/{id}` | Update site by ID |
| DELETE | `/locations/site/{id}` | Delete site by ID |
| GET | `/countries` | Get country list |
| GET | `/alarms/v1/alarms` | Get alarms with their configuration status |
| GET | `/alarms/v1/alarms/active-counts` | Get active alarms count per severity |
| GET | `/alarms/v1/alarms/notification-rules` | Get alarm notification rules |
| POST | `/alarms/v1/alarms/notification-rules` | Create alarm notification rule |
| PUT | `/alarms/v1/alarms/notification-rules/{id}` | Update alarm notification rule |
| DELETE | `/alarms/v1/alarms/notification-rules/{id}` | Delete alarm notification rule |
| GET | `/alarms/v1/alarms/sites` | Sites Summary |
| GET | `/alarms/v1/alarms/filters` | Get alarm filter values |
| GET | `/alarms/v1/alarms/timeline` | Get alarms timeline chart data |
| GET | `/alarms/v1/alarms/notification-rules/filters` | Get alarm notification rules filters |
| GET | `/monitoring/v1/dashboard/sites-summary` | Get Sites Summary |
| GET | `/monitoring/v1/dashboard/appliances-summary` | Get Appliance Summary Information |
| GET | `/monitoring/v1/dashboard/wans-summary` | Get WANs Summary |
| GET | `/monitoring/v1/dashboard/applications-summary` | Get Applications Summary |
| GET | `/monitoring/v1/dashboard/site/status` | Get Site Alarms and Appliances status |
| GET | `/monitoring/v1/dashboard/site/metrics` | Get Site Eqs and Throughput |
| GET | `/monitoring/v1/connections` | Get Connection Details |
| GET | `/monitoring/v1/connections/sites` | Get Connection Sites |
| GET | `/monitoring/v1/connections/appliances/{id}` | Get Appliance Connection Details |
| GET | `/monitoring/v1/connections/underlays` | Get Underlay Connection |
| GET | `/monitoring/v1/connections/filters` | Get Connection Filters |
| GET | `/monitoring/v1/applications/metrics/summary` | Get application overview Summary API |
| GET | `/monitoring/v1/applications/eqs/timeseries` | Get Eqs Evolution API |
| GET | `/monitoring/v1/applications/volume/top` | Get Top 10 Volume API |
| GET | `/monitoring/v1/applications/eqs/worst` | Get worst 10 Eqs API |
| GET | `/monitoring/v1/applications/throughput/timeseries` | Get Throughput Evolution API |
| GET | `/monitoring/v1/saasapplications` | Get Active SaaS Applications API |
| GET | `/monitoring/v1/saasapplications/filters` | Get Active SaaS Applications API filters |
| GET | `/monitoring/v1/dpiapplications` | Get Discovered DPI Applications API |
| GET | `/monitoring/v1/dpiapplications/filters` | Get DPI Applications filters |
| GET | `/monitoring/v1/compression-metrics/stats/applications` | Get Compression Metrics Per Application |
| GET | `/monitoring/v1/compression-metrics/stats/sites` | Get Compression Metrics Per Site |
| GET | `/monitoring/v1/compression-metrics/time-charts` | Get Compression Metrics Time Charts |
| GET | `/monitoring/v1/compression-metrics/stats` | Get Compression Metrics Stats |
| GET | `/monitoring/v1/compression-metrics/filters` | Get Compression Metrics filters |
| GET | `/monitoring/v1/applications/performance/filters` | Get Application Performance filters |
| GET | `/monitoring/v1/applications/overview/filters` | Get Application Overview filters |
| GET | `/monitoring/v1/applications/eqs/worst/timeseries` | Get Eqs Evolution by worst 10 application API |
| GET | `/monitoring/v1/applications/throughput/top/timeseries` | Get Throughput Evolution by Top 10 application API |
| GET | `/monitoring/v1/adrapplications` | Get Discovered Applications API |
| GET | `/monitoring/v1/adrapplications/filters` | Get Applications filters |
| GET | `/monitoring/v1/sites/overview` | Get Sites Overview |
| GET | `/monitoring/v1/sites/{id}/metrics/wans` | Get Wan Services Informations API |
| GET | `/monitoring/v1/sites/{id}/eqs/worst` | Get worst 10 Eqs API |
| GET | `/monitoring/v1/sites/{id}/eqs/worst/timeseries` | Get Eqs Evolution by worst 10 application API |
| GET | `/monitoring/v1/sites/{id}/volume/top` | Get Top 10 Volume API |
| GET | `/monitoring/v1/sites/{id}/metrics/wans/throughput` | Get WAN throughput evolution API |
| GET | `/monitoring/v1/sites/{id}/metrics/wans/eqs` | Get WAN EQS evolution API |
| GET | `/monitoring/v1/metrics/timeseries` | Get Monitoring metrics Evolution API |
| GET | `/monitoring/v1/sites/{id}/throughput/timeseries` | Get Throughput Evolution API |
| GET | `/monitoring/v1/sites/{id}/eqs/timeseries` | Get Eqs Evolution API |
| GET | `/monitoring/v1/sites/{id}/throughput/top/timeseries` | Get Throughput Evolution by Top 10 application API |
| GET | `/monitoring/v1/sites/application-groups` | Get Application Groups |
| GET | `/monitoring/v1/flows` | Get Flows View |
| GET | `/monitoring/v1/flows/filters` | Get Flows Filters |
| GET | `/monitoring/v1/sites/{id}/metrics/summary` | Get Site 360 application overview Summary API |
| GET | `/monitoring/v1/sites/{id}/jitter` | Get jitter evolution for a site |
| GET | `/monitoring/v1/sites/{id}/delay-jitter` | Get TCP delay and jitter evolution for a site |
| GET | `/monitoring/v1/sites/{id}/average-sessions` | Get TCP session evolution for a site |
| GET | `/monitoring/v1/sites/{id}/rtt-srt` | Get TCP RTT and SRT evolution for a site |
| GET | `/monitoring/v1/sites/{id}/throughput` | Get the throughput evolution for a site |
| GET | `/monitoring/v1/sites/{id}/packet-retransmission` | Get TCP packets retransmission |
| GET | `/monitoring/v1/sites/{id}/packet-loss` | Get TCP packets loss evolution for a site |
| GET | `/monitoring/v1/sites/{id}/eqs` | Get the EQS evolution for a site |
| GET | `/monitoring/v1/sites/{id}/delay` | Get TCP delay evolution for a site |
| GET | `/monitoring/v1/sites/{id}/rtt` | Get TCP RTT evolution for a site |
| GET | `/monitoring/v1/sites/{id}/srt` | Get SRT evolution for a site |
| GET | `/monitoring/v1/sites/{id}/appliances-wans` | Get appliances-wans for a site |
| GET | `/monitoring/v1/sites/overview/filters` | Get Site 360 Filters API |
| GET | `/monitoring/v1/sites/performance/filters` | Get Site performance Filters API |
| GET | `/monitoring/v1/metrics/wans/throughput` | Get throughput evolution API |
| GET | `/monitoring/v1/metrics/wans` | Get Wan Services Informations API |
| GET | `/monitoring/v1/metrics/wans/local/availability` | Get local availability and EQS API |
| GET | `/monitoring/v1/metrics/wans/end-end/availability` | Get end to end availabilty and EQS API |
| GET | `/monitoring/v1/metrics/wans/eqs` | Get EQS evolution API |
| GET | `/monitoring/v1/wans/filters` | Get Wan Overview Filters API |
| GET | `/monitoring/v1/appliances/status` | Get Appliance Status List |
| GET | `/monitoring/v1/appliances/{id}/status` | Get Appliance Status |
| GET | `/monitoring/v1/appliances/{id}/cpu-usage` | Get Appliance CPU Usage |
| GET | `/monitoring/v1/appliances/{id}/fabric-peers` | Get Appliance's Fabric Peer Status |
| GET | `/monitoring/v1/appliances/{id}/system-usage` | Get Appliance System Usage |
| GET | `/monitoring/v1/network-analysis/metrics` | Get network analysis metrics |
| GET | `/monitoring/v1/network-analysis/summary` | Get network analysis summary |
| GET | `/monitoring/v1/network-analysis/filters` | Get network analysis filters |
| GET | `/monitoring/v1/network-analysis/ethernet-throughput` | Get ethernet throughput metrics |
| GET | `/monitoring/v1/network-analysis/ip-throughput` | Get IP throughput metrics |
| POST | `/monitoring/v1/flows/live/sessions` | Create Real Time Monitoring Session |
| POST | `/monitoring/v1/flows/live/sessions/create` | Create Real Time Monitoring Session |
| GET | `/monitoring/v1/flows/live/sessions/{id}` | Get Real Time Monitoring data |
| DELETE | `/monitoring/v1/flows/live/sessions/{id}` | Delete Real Time Monitoring Session |
| POST | `/monitoring/v1/rtg/sessions` | Create Real Time Monitoring Session |
| POST | `/monitoring/v1/rtg/sessions/create` | Create Real Time Monitoring Session |
| GET | `/monitoring/v1/rtg/sessions/{id}` | Get Real Time Monitoring data |
| DELETE | `/monitoring/v1/rtg/sessions/{id}` | Delete Real Time Monitoring Session |
| GET | `/configuration/v1/manage/devices` | Get devices with their configuration status |
| GET | `/configuration/v1/manage/devices/{applianceId}` | Get Device by Appliance Id |
| GET | `/configuration/v1/network-policies/{policyId}/vpn-zones` | Get VPN Zones |
| POST | `/configuration/v1/network-policies/{policyId}/vpn-zones` | Add VPN Zones |
| PUT | `/configuration/v1/network-policies/{policyId}/vpn-zones` | Update VPN Zones |
| DELETE | `/configuration/v1/network-policies/{policyId}/vpn-zones` | Delete VPN Zones |
| GET | `/configuration/v1/network-policies/{policyId}/vpn-zones/{id}` | Get a VPN Zone |
| GET | `/configuration/v1/network-policies/{policyId}/overlays` | Get Overlay Configuration |
| DELETE | `/configuration/v1/network-policies/{policyId}/overlays` | Delete Overlay Configuration |
| POST | `/configuration/v1/network-policies/{policyId}/overlays/hub-and-spokes` | Create Hub and Spoke Overlay Configuration |
| PUT | `/configuration/v1/network-policies/{policyId}/overlays/hub-and-spokes` | Update Hub and Spoke Overlay Configuration |
| POST | `/configuration/v1/network-policies/{policyId}/overlays/third-party-vpns` | Create Third Party Vpn Configuration |
| PUT | `/configuration/v1/network-policies/{policyId}/overlays/third-party-vpns` | Update Third Party Vpn Configuration |
| GET | `/configuration/v1/network-policies/{policyId}/overlays/{id}` | Get Overlay Configuration by Id |
| GET | `/configuration/v1/network-policies/{policyId}/overlays/associations` | Get Overlay with Hub/Spoke/WAN Associations |
| GET | `/configuration/v1/network-policies/{policyId}/application-performance/application-groups` | Get application groups |
| POST | `/configuration/v1/network-policies/{policyId}/application-performance/application-groups` | Create application groups |
| PUT | `/configuration/v1/network-policies/{policyId}/application-performance/application-groups` | Update application groups |
| DELETE | `/configuration/v1/network-policies/{policyId}/application-performance/application-groups` | Delete application groups |
| GET | `/configuration/v1/network-policies/{policyId}/application-performance/application-groups/{id}` | Get an application group |
| GET | `/configuration/v1/appliances` | Get Appliances |
| POST | `/configuration/v1/appliances` | Onboard Appliances |
| DELETE | `/configuration/v1/appliances` | Trigger deletion of appliances |
| GET | `/configuration/v1/appliances/{applianceId}` | Get Appliance by Appliance Id |
| PATCH | `/configuration/v1/appliances/{applianceId}` | Patch an appliance's name and serial number |
| POST | `/configuration/v1/appliances-csv` | Onboard Appliances by uploading CSV |
| GET | `/configuration/v1/appliances/serial-number/{serialNumber}` | Get Appliance by Serial Number |
| GET | `/configuration/v1/templates` | Get Appliance Template |
| POST | `/configuration/v1/templates` | Create Appliance Template |
| PUT | `/configuration/v1/templates` | Update Appliance Template |
| DELETE | `/configuration/v1/templates` | Delete Appliance Template |
| GET | `/configuration/v1/templates/{id}` | Get Appliance Template by Id |
| GET | `/configuration/v1/templates/associations` | Get Templates with Associations |
| GET | `/configuration/v1/appliances/{applianceId}/general-settings` | Get general settings of an appliance |
| PUT | `/configuration/v1/appliances/{applianceId}/general-settings` | Update general settings of an appliance |
| POST | `/configuration/v1/appliances/{applianceId}/general-settings/reset-to-template` | Reset general settings to template default |
| GET | `/configuration/v1/appliances/{applianceId}/lan-settings` | Get LAN settings of an appliance |
| PUT | `/configuration/v1/appliances/{applianceId}/lan-settings` | Update LAN settings for an appliance |
| POST | `/configuration/v1/appliances/{applianceId}/lan-settings/reset-to-template` | Reset LAN settings to template default |
| GET | `/configuration/v1/appliances/{applianceId}/wan-settings` | Get all WAN settings of an appliance |
| POST | `/configuration/v1/appliances/{applianceId}/wan-settings/reset-to-template` | Reset WAN settings to template default |
| GET | `/configuration/v1/appliances/{applianceId}/wan-settings/{name}` | Get WAN settings of appliance by interface's name |
| PUT | `/configuration/v1/appliances/{applianceId}/wan-settings/{name}` | Update WAN settings of an appliance WAN settings |
| GET | `/configuration/v1/network-policies` | Get SD-WAN Policy |
| POST | `/configuration/v1/network-policies` | Create SD-WAN Policy |
| PUT | `/configuration/v1/network-policies` | Update SD-WAN Policy |
| GET | `/configuration/v1/network-policies/{id}` | Get Network Policy by Id |
| GET | `/configuration/v1/network-policies/active-policy` | Get Active SD-WAN Policy |
| GET | `/configuration/v1/common-objects/vlans` | Get all VLAN |
| POST | `/configuration/v1/common-objects/vlans` | Add new VLANs |
| PUT | `/configuration/v1/common-objects/vlans` | Update VLAN |
| DELETE | `/configuration/v1/common-objects/vlans` | Delete VLAN |
| GET | `/configuration/v1/common-objects/vlans/{id}` | Get VLAN by Id |
| GET | `/configuration/v1/lans` | Get all LANs |
| POST | `/configuration/v1/lans` | Create new LANs |
| PUT | `/configuration/v1/lans` | Update LANs |
| DELETE | `/configuration/v1/lans` | Delete LANs |
| GET | `/configuration/v1/lans/{id}` | Get LAN by Id |
| GET | `/configuration/v1/network-policies/{policyId}/application-performance/transport-networks` | Get transport networks |
| POST | `/configuration/v1/network-policies/{policyId}/application-performance/transport-networks` | Add transport networks |
| PUT | `/configuration/v1/network-policies/{policyId}/application-performance/transport-networks` | Update transport networks |
| DELETE | `/configuration/v1/network-policies/{policyId}/application-performance/transport-networks` | Delete transport networks |
| GET | `/configuration/v1/network-policies/{policyId}/application-performance/transport-networks/{id}` | Get a transport network |
| GET | `/configuration/v1/wans` | Get WAN Configuration |
| POST | `/configuration/v1/wans` | Create WAN Configuration |
| PUT | `/configuration/v1/wans` | Update WAN Configuration |
| DELETE | `/configuration/v1/wans` | Delete WAN Configuration |
| GET | `/configuration/v1/wans/{id}` | Get WAN Configuration by Id |
| GET | `/configuration/v1/sites` | Get all Sites |
| GET | `/configuration/v1/sites/{siteId}` | Get Site by Site ID |
| POST | `/configuration/v1/sites/assign-appliances` | Assign Appliances to Sites |
| GET | `/configuration/v1/sites/associations` | Get Sites with statistics |
| POST | `/configuration/v1/manage/configuration/validate` | Request current configuration validation |
| GET | `/configuration/v1/manage/configuration/validation-status/{snapshotId}` | Configuration validation status |
| POST | `/configuration/v1/manage/configuration/deploy` | Validate and deploy Configuration |
| POST | `/configuration/v1/manage/configuration/deploy/{id}` | Deploy pre-validated Configuration by ID |
| POST | `/configuration/v1/manage/configuration/async-validation` | Trigger an asynchronous validation |
| GET | `/configuration/v1/manage/configuration/async-validation/{snapshotId}` | Asynchronous configuration validation result |
| GET | `/configuration/v1/network-policies/{policyId}/vpn-policies` | Get VPN Policies |
| PUT | `/configuration/v1/network-policies/{policyId}/vpn-policies` | Update VPN Policies |
| GET | `/configuration/v1/network-policies/{policyId}/vpn-policies/{id}` | Get a VPN Policy |
| GET | `/configuration/v1/network-policies/{policyId}/port-based-application-sets` | Get Port Based Application Sets |
| POST | `/configuration/v1/network-policies/{policyId}/port-based-application-sets` | Create Port Based Application Sets |
| PUT | `/configuration/v1/network-policies/{policyId}/port-based-application-sets` | Port Based Application Sets |
| DELETE | `/configuration/v1/network-policies/{policyId}/port-based-application-sets` | Delete Port Based Application Sets |
| GET | `/configuration/v1/network-policies/{policyId}/port-based-application-sets/{id}` | Get a Port Based Application Set |
| GET | `/configuration/v1/network-policies/{policyId}/internet-access-policies` | Get Internet Access Policies |
| PUT | `/configuration/v1/network-policies/{policyId}/internet-access-policies` | Update Internet Access Policies |
| GET | `/configuration/v1/network-policies/{policyId}/internet-access-policies/{id}` | Get a Internet Access Policy |
| GET | `/configuration/v1/network-policies/{policyId}/saas-application-sets` | Get Saas Application Sets |
| POST | `/configuration/v1/network-policies/{policyId}/saas-application-sets` | Saas Application Sets |
| PUT | `/configuration/v1/network-policies/{policyId}/saas-application-sets` | Saas Application Sets |
| DELETE | `/configuration/v1/network-policies/{policyId}/saas-application-sets` | Delete Saas Application Sets |
| GET | `/configuration/v1/network-policies/{policyId}/saas-application-sets/{id}` | Get a Saas Application Set |
| GET | `/configuration/v1/network-policies/{policyId}/secure-web-gateways` | Get Secure Web Gateway |
| POST | `/configuration/v1/network-policies/{policyId}/secure-web-gateways` | Create Secure Web Gateway |
| PUT | `/configuration/v1/network-policies/{policyId}/secure-web-gateways` | Update Secure Web Gateway |
| DELETE | `/configuration/v1/network-policies/{policyId}/secure-web-gateways` | Delete Secure Web Gateway |
| GET | `/configuration/v1/network-policies/{policyId}/secure-web-gateways/{id}` | Get Secure Web Gateway by secure web gateway id |
| GET | `/configuration/v1/vpn-sites` | Get all User Sites |
| GET | `/configuration/v1/vpn-sites/{siteId}` | Get any User Site by ID |
| GET | `/configuration/v1/network-policies/{policyId}/application-performance/applications` | Get applications |
| POST | `/configuration/v1/network-policies/{policyId}/application-performance/applications` | Add applications |
| PUT | `/configuration/v1/network-policies/{policyId}/application-performance/applications` | Update applications |
| DELETE | `/configuration/v1/network-policies/{policyId}/application-performance/applications` | Delete applications |
| GET | `/configuration/v1/network-policies/{policyId}/application-performance/applications/{id}` | Get an application |
| GET | `/configuration/v1/network-policies/{policyId}/application-performance/applications/inventory` | Get applications inventory |
| GET | `/configuration/v1/network-policies/{policyId}/application-performance/saas-applications` | Get SaaS Applications |
| POST | `/configuration/v1/network-policies/{policyId}/application-performance/saas-applications` | Create SaaS Applications |
| PUT | `/configuration/v1/network-policies/{policyId}/application-performance/saas-applications` | Update SaaS applications |
| DELETE | `/configuration/v1/network-policies/{policyId}/application-performance/saas-applications` | Delete SaaS Applications |
| GET | `/configuration/v1/network-policies/{policyId}/application-performance/saas-applications/{id}` | Get a SaaS Application by ID |
| GET | `/configuration/v1/network-policies/{policyId}/application-performance/qos-profiles` | Get QoS profiles |
| POST | `/configuration/v1/network-policies/{policyId}/application-performance/qos-profiles` | Add QoS profiles |
| PUT | `/configuration/v1/network-policies/{policyId}/application-performance/qos-profiles` | Update QoS profiles |
| DELETE | `/configuration/v1/network-policies/{policyId}/application-performance/qos-profiles` | Delete QoS profiles |
| GET | `/configuration/v1/network-policies/{policyId}/application-performance/qos-profiles/{id}` | Get a QoS profile |
| GET | `/configuration/v1/network-policies/{policyId}/application-performance/dws-policies` | Get DWS policies |
| POST | `/configuration/v1/network-policies/{policyId}/application-performance/dws-policies` | Add DWS policies |
| PUT | `/configuration/v1/network-policies/{policyId}/application-performance/dws-policies` | Update DWS policies |
| DELETE | `/configuration/v1/network-policies/{policyId}/application-performance/dws-policies` | Delete DWS policies |
| GET | `/configuration/v1/network-policies/{policyId}/application-performance/dws-policies/{id}` | Get a DWS policy |
| GET | `/configuration/v1/appliances/fabric-settings` | Get all configured fabric appliances |
| PUT | `/configuration/v1/appliances/fabric-settings` | Configured fabric appliances |
| GET | `/configuration/v1/common-objects/dhcp-services` | Get all DHCP Services |
| POST | `/configuration/v1/common-objects/dhcp-services` | Add DHCP Service |
| PUT | `/configuration/v1/common-objects/dhcp-services` | Update DHCP Services |
| DELETE | `/configuration/v1/common-objects/dhcp-services` | Delete DHCP Services |
| GET | `/configuration/v1/common-objects/dhcp-services/{id}` | Get DHCP Service by Id |
| GET | `/configuration/v1/appliances/{applianceId}/available-bgp-peer-appliances` | Get all BGP peer appliances of an appliance |
| GET | `/configuration/v1/network-policies/{policyId}/application-performance/ihap-profiles` | Get all IHAP Profiles |
| POST | `/configuration/v1/network-policies/{policyId}/application-performance/ihap-profiles` | Add IHAP Profile |
| PUT | `/configuration/v1/network-policies/{policyId}/application-performance/ihap-profiles` | Update IHAP Profiles |
| DELETE | `/configuration/v1/network-policies/{policyId}/application-performance/ihap-profiles` | Delete IHAP Profiles |
| GET | `/configuration/v1/network-policies/{policyId}/application-performance/ihap-profiles/{id}` | Get IHAP Profile by Id |
| GET | `/configuration/v1/network-policies/{policyId}/application-performance/vrrp-profiles` | Get all VRRP Profiles |
| POST | `/configuration/v1/network-policies/{policyId}/application-performance/vrrp-profiles` | Add VRRP Profile |
| PUT | `/configuration/v1/network-policies/{policyId}/application-performance/vrrp-profiles` | Update VRRP Profiles |
| DELETE | `/configuration/v1/network-policies/{policyId}/application-performance/vrrp-profiles` | Delete VRRP Profiles |
| GET | `/configuration/v1/network-policies/{policyId}/application-performance/vrrp-profiles/{id}` | Get VRRP Profile by Id |
| GET | `/configuration/v1/network-policies/{policyId}/application-performance/vrrp-profiles/associations` | Get VRRP Profile Associations |
| GET | `/configuration/v1/appliances/{applianceId}/wan-settings/connections` | Get WAN External Connections |
| GET | `/configuration/v1/appliances/{applianceId}/wan-settings/{name}/connections` | Get WAN External Connections By Wan Name |
| GET | `/configuration/v1/appliances/{applianceId}/wan-settings/{name}/connections/hub-and-spoke-synthesis` | Get WAN Hub and Spoke Connections Synthesis |
| GET | `/configuration/v1/appliances/{applianceId}/wan-settings/{name}/connections/{type}` | Get WAN External Connections By Type |
| GET | `/configuration/v1/appliances/{applianceId}/wan-settings/{name}/available-site-to-site-endpoints` | Get Available Remote Site to Site Endpoints |
| GET | `/configuration/v1/sites/{siteId}/appliances` | Get appliances by Site ID |
| GET | `/configuration/v1/common-objects/protocols` | Get protocols |
| GET | `/configuration/v1/common-objects/protocols/{id}` | Get Protocol by Id |
| GET | `/configuration/v1/network-policies/{policyId}/routing/settings` | Get routing settings |
| PUT | `/configuration/v1/network-policies/{policyId}/routing/settings` | Update routing settings |
| GET | `/configuration/v1/network-policies/{policyId}/routing/settings/{id}` | Get a routing settings |
| GET | `/configuration/v1/policy-advanced-settings` | Get advanced settings |
| POST | `/configuration/v1/policy-advanced-settings` | Create advanced settings |
| PUT | `/configuration/v1/policy-advanced-settings` | Update advanced settings |
| DELETE | `/configuration/v1/policy-advanced-settings` | Delete advanced settings |
| GET | `/configuration/v1/policy-advanced-settings/{id}` | Get an advanced settings |
| GET | `/configuration/v1/rvc-destinations` | Get RVC destinations |
| POST | `/configuration/v1/rvc-destinations` | Add RVC destinations |
| PUT | `/configuration/v1/rvc-destinations` | Update RVC destinations |
| DELETE | `/configuration/v1/rvc-destinations` | Delete RVC Destinations |
| GET | `/configuration/v1/rvc-destinations/{id}` | Get a RVC destination |
| GET | `/configuration/v1/saas-catalog` | Get SaaS catalog |
| GET | `/configuration/v1/saas-catalog/info` | Get SaaS catalog info |
| GET | `/tools/v1/upgrade/catalog` | Firmware catalog |
| POST | `/tools/v1/upgrade/activate` | Activate upgrade |
| GET | `/tools/v1/upgrade/status` | Upgrade status |
| DELETE | `/tools/v1/upgrade/cancel` | Cancel a scheduled upgrade |
| POST | `/tools/v1/troubleshooting/start` | Start Appliance troubleshooting |
| GET | `/tools/v1/troubleshooting/stats` | Appliance troubleshooting stats |
| GET | `/tools/v1/troubleshooting/graph` | Appliance troubleshooting graph |
| POST | `/tools/v1/troubleshooting/stop/{request_id}` | Stop Appliance troubleshooting |
| GET | `/tools/v1/scripts/catalog` | Get scripts catalog |
| POST | `/tools/v1/scripts/execute/{script_name}` | Run a script |
| GET | `/tools/v1/scripts/status` | Get script status |
| GET | `/tools/v1/scripts/result` | Get script result(s) |
| POST | `/tools/v1/scripts/result/delete` | Delete result(s) |
| GET | `/tools/v1/scripts/result/download` | Download script result |
| GET | `/system/v1/audit/records` | Get All Audit Records |
| GET | `/system/v1/audit/records/{id}` | Get Audit Record Details |
| GET | `/system/v1/audit/filters` | Get Audit Record Filters |
| POST | `/reporting/v1/reports/config` | Create report API |
| GET | `/reporting/v1/reports` | Get all report configs with generated report list |
| DELETE | `/reporting/v1/reports` | Delete Report/Reports |
| PUT | `/reporting/v1/reports/{config_id}` | Put update report config API |
| GET | `/reporting/v1/reports/{report_id}/download` | download report |
| GET | `/reporting/v1/reports/components` | Report Widget list API |
| GET | `/reporting/v1/reports/templates` | Template List API |
| POST | `/reporting/v1/reports/templates` | Save template API |
| DELETE | `/reporting/v1/reports/templates` | Template Delete API |
| GET | `/reporting/v1/reports/templates/{template_id}` | Template metadata API |
| PUT | `/reporting/v1/reports/templates/{template_id}` | Update template API |
| POST | `/reporting/v1/reports/templates/clone` | Clone Template |

## POST `/login`

Operation: `login`

User login with username and password

Get access token via username and password authentication. The client must present Bearer token to access the protected API endpoints.The Bearer token should be present in the "Authorization" request header field and use the "Bearer" HTTP authentication scheme to transmit the access token.

Tags: `Authentication`

Request body:

- `application/json` — XiqLoginRequest

Responses:

- `200` — Successfully login

## POST `/logout`

Operation: `logout`

User logout (Revoke the current access token)

User logout, the current access token will be revoked and the following access with the same token will be immediately denied.

Tags: `Authentication`

Responses:

- `200` — OK
- `default`

## GET `/locations/site`

Operation: `clsGetSites`

List sites

List pages of sites by filter.

Tags: `Sites`

Parameters:

- `None` , optional
- `None` , optional
- `name` query, optional (string) — List sites by name (case insensitive)
- `ids` query, optional (array) — List sites by IDs

Responses:

- `200` — OK
- `default`

## POST `/locations/site`

Operation: `clsCreateSite`

Create site

Create a new site under the GENERIC folder.

Tags: `Sites`

Request body:

- `application/json` — ClsCreateSiteRequest

Responses:

- `200` — OK
- `default`

## GET `/locations/site/{id}`

Operation: `xiqLocationGetSiteById`

Get site by ID

Get the site for the specified ID.

Tags: `Sites`

Parameters:

- `None` , optional

Responses:

- `200` — OK
- `default`

## PUT `/locations/site/{id}`

Operation: `updateSite`

Update site by ID

Update the site information with the site ID.

Tags: `Sites`

Parameters:

- `None` , optional

Request body:

- `application/json` — ClsUpdateSiteRequest

Responses:

- `200` — OK
- `default`

## DELETE `/locations/site/{id}`

Operation: `deleteSite`

Delete site by ID

Delete the site for the specified ID.

Tags: `Sites`

Parameters:

- `None` , optional
- `force_delete` query, optional (boolean) — Force deletion of this site and its descendants recursively

Responses:

- `200` — OK
- `default`

## GET `/countries`

Operation: `getCountryList`

Get country list

Get list of countries and country codes.

Tags: `Sites`

Responses:

- `200` — OK
- `default`

## GET `/alarms/v1/alarms`

Operation: `getSdwanAlarms`

Get alarms with their configuration status

Returns manageable SD-WAN alarms.

Tags: `Alarms`

Parameters:

- `page` query, optional (integer) — next page number for navigation for Sites Overview UI page used for pagination. Default value is 1 (used if set value is not an integer > 0).
- `size` query, optional (integer) — current page size for Sites Overview UI page used for pagination. Default value is 20 (used if set value is not an integer > 0).
- `state` query, required (string) — The parameter is used to specify the state to be active. If no value is provided or an invalid value is provided then error message will be thrown.
- `sort` query, optional (string) — The sort field. Sorting can applied on specfied column. Sorting can be applied only on one column at a time. Specified column followed by the sorting direction (ie asc or desc) with the comma separation. Allowed columns are site,…
- `start_time` query, optional (integer) — start_time is epoch time in seconds. It represents the start of the time range (start_time - end_time) for which the metrics data for sites will be fetched. Only a single value is allowed.
- `end_time` query, optional (integer) — end_time is epoch time in seconds. It represents the end of the time range (start_time - end_time) for which the metrics data for sites will be fetched. Only a single value is allowed.
- `severity` query, optional (string) — Severity of the alarm. Supported values are critical, major and minor .
- `layer` query, optional (string) — category. Supported values are overlay, underlay, management, services, resources, eqs
- `alarm_name` query, optional (string) — unique alarm name. Supported alarms are - appliance-disk-failure, appliance-disk-full, appliance-reboot, bad-nw-interface-config-fullduplex, bad-nw-interface-config-halfduplex, cloudmesh-failure, configuration-mismatch,…
- `local_site_id` query, optional (integer) — local site id.
- `remote_site_id` query, optional (integer) — remote site id.
- `local_appliance_id` query, optional (integer) — local appliance id
- `remote_appliance_id` query, optional (integer) — remote appliance id
- `local_appliance_serial_number` query, optional (string) — local appliance serial number. Filter can be applied on multiple values by passing comma-separated values. For example, "?local_appliance_serial_number=A0214J0172,N0815K0319A0,A0518X0005A0" will search for all the three appliances.…
- `remote_appliance_serial_number` query, optional (string) — remote appliance serial number
- `keyword` query, optional (string) — keyword for case-insensitive search across columns having string values. Applicable on columns - alarm_description, details, local_appliance_name, remote_appliance_name, remote_site_name, local_site_name

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/alarms/v1/alarms/active-counts`

Operation: `getSdwanAlarmsActiveCounts`

Get active alarms count per severity

This REST-API can be used to fetch the count of currently active alarms grouped by a specific column. (as of now supported only for severity column) .

Tags: `Alarms`

Parameters:

- `by` query, required (string) — column on which the count of alarms has to be grouped by (as of now supported only for severity column).
- `start_time` query, optional (integer) — start_time is epoch time in seconds. It represents the start of the time range (start_time - end_time) in which the alarm was raised (inclusive). Both start_time and end_time parameters should be provided together.
- `end_time` query, optional (integer) — end_time is epoch time in seconds. It represents the end of the time range (start_time - end_time) in which the alarm was raised (exclusive). Both start_time and end_time parameters should be provided together.

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/alarms/v1/alarms/notification-rules`

Operation: `getNotificationRules`

Get alarm notification rules

This api provides a list of alarm notification rules.

Tags: `Alarm Notification Rules`

Parameters:

- `page` query, optional (integer) — next page number for navigation for alarms notifications page used for pagination. Default value is 1 (used if set value is not an integer > 0).
- `size` query, optional (integer) — current page size for alarms notifications page used for pagination. Default value is 20 (used if set value is not an integer > 0).
- `sort` query, optional (string) — column on which the sort is required and the sort order (ASC, DESC). Sorting can be applied on only name column.

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## POST `/alarms/v1/alarms/notification-rules`

Operation: `createNotificationRules`

Create alarm notification rule

This api allows user to create an alarm notification rule.

Tags: `Alarm Notification Rules`

Request body:

- `application/json` — RulesPostPayload

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## PUT `/alarms/v1/alarms/notification-rules/{id}`

Operation: `updateNotificationRules`

Update alarm notification rule

This api allows user to update an alarm notification rule.

Tags: `Alarm Notification Rules`

Parameters:

- `id` path, required (string) — id of the notification rule

Request body:

- `application/json` — RulesPutPayload

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## DELETE `/alarms/v1/alarms/notification-rules/{id}`

Operation: `deleteNotificationRules`

Delete alarm notification rule

This api allows user to delete an alarm notification rule.

Tags: `Alarm Notification Rules`

Parameters:

- `id` path, required (string) — id of the notification rule

Responses:

- `204` — No Content
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/alarms/v1/alarms/sites`

Operation: `getSdwanAlarmsSites`

Sites Summary

This API provides a list of sites with number of active alarms per severity.

Tags: `Alarms`

Parameters:

- `id` query, optional (string) — Site id. Multiple values are allowed with comma (,) separation
- `is_paginated` query, optional (boolean) — This indicates whether paginated response is required or not. The default value is true. When it is set to false then, the page and size parameter is ignored.
- `page` query, optional (integer) — Next page number for navigation for alarms notifications page used for pagination. Default value is 1 (used if set value is not an integer > 0).
- `size` query, optional (integer) — Current page size for alarms notifications page used for pagination. Default value is 20 (used if set value is not an integer > 0).
- `sort` query, optional (string) — Column on which the sort is required and the sort order (ASC, DESC). Sorting can be applied on only name and id column.

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/alarms/v1/alarms/filters`

Operation: `getAlarmsFilters`

Get alarm filter values

This api provides multiple lists of unique values to populate the filter dropdowns. (This is a private/internal api).

Tags: `Alarms`

Parameters:

- `state` query, required (string) — state=active for alarms that are currently active and state=cleared for alarms that are currently cleared. Only 2 values, active or cleared are supported for this query parameter.

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/alarms/v1/alarms/timeline`

Operation: `getAlarmsTimeline`

Get alarms timeline chart data

This REST-API can be used to get the count of the alarms based on their status (active, raised, cleared) within the time interval (start-end). active_count - count of alarms that were raised before the end time and were active at the end time. raised_count - count of alarms raised within the time interval (start-end) cleared_count - count of alarms cleared within the time interval (start-end) .

Tags: `Alarms`

Parameters:

- `start_time` query, required (integer) — start_time is epoch time in seconds. It represents the start of the time range (start_time - end_time) in which the alarm was raised (inclusive). Both start_time and end_time parameters should be provided together.
- `end_time` query, required (integer) — end_time is epoch time in seconds. It represents the end of the time range (start_time - end_time) in which the alarm was raised (exclusive). Both start_time and end_time parameters should be provided together.

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/alarms/v1/alarms/notification-rules/filters`

Operation: `getAlarmsNotificationRulesFilters`

Get alarm notification rules filters

This api provides a list of alarm notification rules filters.

Tags: `Alarm Notification Rules`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/dashboard/sites-summary`

Operation: `getSdwanSitesSummary`

Get Sites Summary

Get sites summary returns summarised data of all sites.

Tags: `Topology`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/dashboard/appliances-summary`

Operation: `getSdwanApplianceSummary`

Get Appliance Summary Information

Get appliances summary returns summarised data of all the appliances of dashboard.

Tags: `Topology`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/dashboard/wans-summary`

Operation: `getSdwanWansSummary`

Get WANs Summary

Get wans summary returns summarised data of all the wan services.

Tags: `Topology`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/dashboard/applications-summary`

Operation: `applicationsSummary`

Get Applications Summary

Get applications summary returns summarised data of all the applications.

Tags: `Topology`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/dashboard/site/status`

Operation: `sitesAlarms`

Get Site Alarms and Appliances status

Get site alarms and Appliances status returns alarms count grouped by severity and appliance status.

Tags: `Topology`

Parameters:

- `site_id` query, required (integer) — Site Id of the site for which the details will be fetched. Only a single value is allowed.

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/dashboard/site/metrics`

Operation: `dashboardSitesEqs`

Get Site Eqs and Throughput

Get Site Eqs and Throughput API returns eqs grouped by criticality and throughput.

Tags: `Topology`

Parameters:

- `site_id` query, required (integer) — Site Id of the site for which the details will be fetched. Only a single value is allowed.

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/connections`

Operation: `getSdwanConnections`

Get Connection Details

Get connection details API will return information related to all connections.

Tags: `Topology`

Parameters:

- `initiator_appliance_id` query, optional (integer) — The initiator appliance ID.
- `responder_appliance_id` query, optional (integer) — The responder appliance ID.
- `initiator_site_id` query, optional (integer) — The initiator site ID.
- `responder_site_id` query, optional (integer) — The responder site ID.
- `initiator_interface` query, optional (string) — The initiator interface.
- `responder_interface` query, optional (string) — The responder interface.
- `overlay_id` query, optional (integer) — The overlay ID.
- `status` query, optional (string) — The connection status.
- `type` query, optional (RequestParamEnum) — The connection type.
- `keyword` query, optional (string) — The keyword search uses case-insensitive search across fields having string values.
- `is_paginated` query, optional (boolean) — The boolean flag for pagination. Default value will be false, which means no pagination.
- `page` query, optional (integer) — The page field for the pagination. Default value is 1 (used if set value is not an integer > 0).
- `size` query, optional (integer) — The size field for the pagination. Default value is 20 (used if set value is not an integer > 0).
- `sort` query, optional (string) — Sorting can applied on specified column, followed by the sorting direction (ie asc or desc) with the comma separation.

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/connections/sites`

Operation: `getSdwanConnectionsSites`

Get Connection Sites

Get connection sites will return the site details corresponding to connection endpoints.

Tags: `Topology`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/connections/appliances/{id}`

Operation: `connectionApplianceInfo`

Get Appliance Connection Details

Get connection appliance details API will return all connections with the provided appliance ID as either the initiator or the responder.

Tags: `Topology`

Parameters:

- `id` path, required (integer) — ID of the Appliance
- `initiator_appliance_id` query, optional (integer) — The initiator appliance ID.
- `responder_appliance_id` query, optional (integer) — The responder appliance ID.
- `initiator_site_id` query, optional (integer) — The initiator site ID.
- `responder_site_id` query, optional (integer) — The responder site ID.
- `initiator_interface` query, optional (string) — The initiator interface.
- `responder_interface` query, optional (string) — The responder interface.
- `overlay_id` query, optional (integer) — The overlay ID.
- `status` query, optional (string) — The connection status.
- `type` query, optional (RequestParamEnum) — The connection type.
- `is_paginated` query, optional (boolean) — The boolean flag for pagination. Default value will be false, which means no pagination.
- `page` query, optional (QuerryPage) — The page field for the pagination. Default value is 1 (used if set value is not an integer > 0).
- `size` query, optional (QuerryPageSize) — The size field for the pagination. Default value is 20 (used if set value is not an integer > 0).
- `keyword` query, optional (string) — The keyword search uses case-insensitive search across fields having string values.
- `sort` query, optional (string) — Sorting can applied on specified column, followed by the sorting direction (ie asc or desc) with the comma separation.

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/connections/underlays`

Operation: `getUnderlayConnection`

Get Underlay Connection

Get underlay connection returns underlay connectivity of WAN.

Tags: `Topology`

Parameters:

- `appliance_id` query, optional (integer) — Appliance ID.
- `site_id` query, optional (integer) — Site ID.
- `interface_name` query, optional (string) — Interface name.
- `wan_service_id` query, optional (integer) — WAN service ID.
- `status` query, optional (string) — Underlay connection status
- `type` query, optional (string) — Underlay connection type
- `keyword` query, optional (string) — The keyword search uses case-insensitive search across all fields having string values except 'type' & 'status'.
- `is_paginated` query, optional (boolean) — This indicates whether paginated response is required. Default value is true. When it is set to false then, the page and size parameter is ignored.
- `page` query, optional (integer) — Page field for the pagination. Default value is 1 (used if set value is not an integer > 0).
- `size` query, optional (integer) — Size field for the pagination. Default value is 20 (used if set value is not an integer > 0).
- `sort` query, optional (string) — Above example is sorting on Site ID in asc order. Sorting can applied on specified column. Specified column can be site_id, site_name, appliance_id, appliance_name, interface_name, wan_service_id, wan_service_name, lan_to_wan_throughput,…

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/connections/filters`

Operation: `getConnectionsFilters`

Get Connection Filters

Get connection filters API will returns the list of all connections fields required for performing filtering actions in the UI.

Tags: `Topology`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/applications/metrics/summary`

Operation: `getSdwanApplianceMetricsSummary`

Get application overview Summary API

Get Application overview Summary will return Application overview summary data group by application, application group or criticality.

Tags: `Application 360`

Parameters:

- `start_time` query, required (integer) — (required)start time is epoch time in seconds. It represents the start of the time range (start - end) from which the application summary will be fetched.
- `end_time` query, required (integer) — (required)end time is epoch time in seconds. It represents the end of the time range (start - end) upto which the flow data for application summary will be fetched.
- `group_by` query, required (string) — (required) Filter the result of Eqs group by applicationGroup, application or criticality.
- `criticality_id` query, optional (integer) — Filter the data with criticality. Multiple values are allowed with comma (,) separation.
- `application_id` query, optional (integer) — Filter the data with Application. Multiple values are allowed with comma (,) separation.
- `application_group_id` query, optional (integer) — Filter the data with application group. Multiple values are allowed with comma (,) separation.
- `src_site_id` query, optional (integer) — Filter the application overview summary by source site Id. Multiple values are allowed with comma (,) separation.
- `dst_site_id` query, optional (integer) — Filter the application overview summary by destination site Id. Multiple values are allowed with comma (,) separation.
- `src_network_id` query, optional (integer) — Filter the application overview summary by source network Id. Multiple values are allowed with comma (,) separation.
- `dst_network_id` query, optional (integer) — Filter the application overview summary by destination network Id. Multiple values are allowed with comma (,) separation.
- `src_appliance_id` query, optional (integer) — Filter the data with Local Appliance Id. Multiples values are allowed with comma (,) separation.
- `dst_appliance_id` query, optional (integer) — Filter the data with Remote Appliance Id. Multiples values are allowed with comma (,) separation.
- `eqs_gt` query, optional (number) — Filter for EQS greater than the specified value.
- `eqs_lt` query, optional (number) — Filter for EQS less than the specified value.
- `eqs_eq` query, optional (number) — Filter for EQS equals the specified value.
- `eqs_gteq` query, optional (number) — Filter for EQS greater than or equal to the specified value.
- `eqs_lteq` query, optional (number) — Filter for EQS less than or equal to the specified value.
- `keyword` query, optional (string) — keyword for case-insensitive search across columns having string values. Applicable on columns - application and application group.
- `page` query, optional (QuerryPage) — Next page number for navigation for Application Overview summary UI page used for pagination. Default value is 1 (used if set value is not an integer > 0).
- `size` query, optional (QuerryPageSize) — Current page size for Application Overview summary UI page used for pagination. Default value is 20 (used if set value is not an integer > 0).
- `sort` query, optional (string) — The sort field. Sorting can applied on specified column. Sorting can be applied only on one column at a time. Specified column followed by the sorting direction (ie asc or desc) with the comma separation. Allowed columns are application,…

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/applications/eqs/timeseries`

Operation: `eqsInfo`

Get Eqs Evolution API

Get Eqs Evolution API will returns Eqs evolution data grouped by Criticality or Application Group .

Tags: `Application 360`

Parameters:

- `start_time` query, required (integer) — (required)start time is epoch time in seconds. It represents the start of the time range (start - end) from which the flow data for Eqs will be fetched.
- `end_time` query, required (integer) — (required)end time is epoch time in seconds. It represents the end of the time range (start - end) upto which the flow data for Eqs will be fetched.
- `group_by` query, required (string) — (required) Filter the result of Eqs group by applicationGroup or criticality.
- `criticality_id` query, optional (integer) — Filter the data with criticality.Multiples values are allowed with comma (,) separation.
- `application_id` query, optional (integer) — Filter the data with Application.Multiples values are allowed with comma (,) separation.
- `application_group_id` query, optional (integer) — Filter the data with application group.Multiples values are allowed with comma (,) separation.
- `src_site_id` query, optional (integer) — Filter data with Local Site Id.Multiples values are allowed with comma (,) separation.
- `dst_site_id` query, optional (integer) — Filter data with Remote Site Id.Multiples values are allowed with comma (,) separation.
- `src_network_id` query, optional (integer) — Filter data with Local Network Id..Multiples values are allowed with comma (,) separation.
- `dst_network_id` query, optional (integer) — Filter data with Remote Network Id.Multiples values are allowed with comma (,) separation.
- `src_appliance_id` query, optional (integer) — Filter the data with Local Appliance Id. Multiples values are allowed with comma (,) separation.
- `dst_appliance_id` query, optional (integer) — Filter the data with Remote Appliance Id. Multiples values are allowed with comma (,) separation.

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/applications/volume/top`

Operation: `volumeInfo`

Get Top 10 Volume API

Get Top 10 Volume api will return Volume data for top 10 Volume group by application or application group.

Tags: `Application 360`

Parameters:

- `start_time` query, required (integer) — (required)start time is epoch time in seconds. It represents the start of the time range (start - end) from which the flow data for Volume will be fetched.
- `end_time` query, required (integer) — (required)end time is epoch time in seconds. It represents the end of the time range (start - end) upto which the flow data for Volume will be fetched.
- `group_by` query, required (string) — (required) Filter the result of Volume group by applicationGroup or application .
- `criticality_id` query, optional (integer) — Filter the data with criticality.Multiples values are allowed with comma (,) separation.
- `application_id` query, optional (integer) — Filter the data with Application.Multiples values are allowed with comma (,) separation.
- `application_group_id` query, optional (integer) — Filter the data with application group.Multiples values are allowed with comma (,) separation.
- `src_site_id` query, optional (integer) — Filter the data with Local Site Id.Multiples values are allowed with comma (,) separation.
- `dst_site_id` query, optional (integer) — Filter the data with Remote Site Id.Multiples values are allowed with comma (,) separation.
- `src_network_id` query, optional (integer) — Filter the data with Local Network Id.Multiples values are allowed with comma (,) separation.
- `dst_network_id` query, optional (integer) — Filter the data with Remoe Network Id.Multiples values are allowed with comma (,) separation.
- `src_appliance_id` query, optional (integer) — Filter the data with Local Appliance Id. Multiples values are allowed with comma (,) separation.
- `dst_appliance_id` query, optional (integer) — Filter the data with Remote Appliance Id. Multiples values are allowed with comma (,) separation.

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/applications/eqs/worst`

Operation: `worstEqsInfo`

Get worst 10 Eqs API

Get worst 10 Eqs api will return Eqs data for worst 10 Eqs group by application or application group.

Tags: `Application 360`

Parameters:

- `start_time` query, required (integer) — (required)start time is epoch time in seconds. It represents the start of the time range (start - end) from which the flow data for Eqs will be fetched.
- `end_time` query, required (integer) — (required)end time is epoch time in seconds. It represents the end of the time range (start - end) upto which the flow data for Eqs will be fetched.
- `group_by` query, required (string) — (required) Filter the result of Eqs group by applicationGroup or application .
- `criticality_id` query, optional (integer) — Filter the data with criticality.Multiples values are allowed with comma (,) separation.
- `application_id` query, optional (integer) — Filter the data with Application.Multiples values are allowed with comma (,) separation.
- `application_group_id` query, optional (integer) — Filter the data with application group.Multiples values are allowed with comma (,) separation.
- `src_site_id` query, optional (integer) — Filter the data with Local Site Id.Multiples values are allowed with comma (,) separation.
- `dst_site_id` query, optional (integer) — Filter the data with Remote Site Id.Multiples values are allowed with comma (,) separation.
- `src_network_id` query, optional (integer) — Filter the data with Local Network Id.Multiples values are allowed with comma (,) separation.
- `dst_network_id` query, optional (integer) — Filter the data with Remote Network Id.Multiples values are allowed with comma (,) separation.
- `src_appliance_id` query, optional (integer) — Filter the data with Local Appliance Id. Multiples values are allowed with comma (,) separation.
- `dst_appliance_id` query, optional (integer) — Filter the data with Remote Appliance Id. Multiples values are allowed with comma (,) separation.

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/applications/throughput/timeseries`

Operation: `throughputInfo`

Get Throughput Evolution API

Get Throughput Evolution API will returns throughput evolution data grouped by Application Group or Criticality.

Tags: `Application 360`

Parameters:

- `start_time` query, required (integer) — (required)start time is epoch time in seconds. It represents the start of the time range (start - end) from which the flow data for throughput will be fetched.
- `end_time` query, required (integer) — (required)end time is epoch time in seconds. It represents the end of the time range (start - end) upto which the flow data for throughput will be fetched.
- `group_by` query, required (string) — (required) Filter the result of throughput group by applicationGroup or criticality.
- `criticality_id` query, optional (integer) — Filter the data with criticality.Multiples values are allowed with comma (,) separation.
- `application_id` query, optional (integer) — Filter the data with Application.Multiples values are allowed with comma (,) separation.
- `application_group_id` query, optional (integer) — Filter the data with application group.Multiples values are allowed with comma (,) separation.
- `src_site_id` query, optional (integer) — Filter the data with Local Site Id.Multiples values are allowed with comma (,) separation.
- `dst_site_id` query, optional (integer) — Filter the data with Remote Site Id.Multiples values are allowed with comma (,) separation.
- `src_network_id` query, optional (integer) — Filter the data with Local Network Id.Multiples values are allowed with comma (,) separation.
- `dst_network_id` query, optional (integer) — Filter the data with Remote Network Id.Multiples values are allowed with comma (,) separation.
- `src_appliance_id` query, optional (integer) — Filter the data with Local Appliance Id. Multiples values are allowed with comma (,) separation.
- `dst_appliance_id` query, optional (integer) — Filter the data with Remote Appliance Id. Multiples values are allowed with comma (,) separation.

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/saasapplications`

Operation: `saasApplicationsList`

Get Active SaaS Applications API

Get Saas Applications seen on a customer network in a given time range.

Tags: `Application 360`

Parameters:

- `start_time` query, required (integer) — (required) start is epoch time in seconds. It represents the start of the selected time range (start - end).
- `end_time` query, required (integer) — (required) end is epoch time in seconds. It represents the end of the selected time range (start - end).
- `at` query, optional (integer) — epoch time in seconds. It represents the actual timestamp for which we want the values (in the time range start to end).
- `site_id` query, optional (integer) — Site ID.
- `keyword` query, optional (string) — keyword for case-insensitive search across columns having string values. Applicable on columns - application and category.
- `is_paginated` query, optional (boolean) — This indicates whether paginated response is required or not. The default value is true. When it is set to false then, the page and size parameter is ignored.
- `page` query, optional (integer) — The page field for the pagination. Default value is 1 (used if set value is not an integer > 0).
- `size` query, optional (integer) — The size field for the pagination. Default value is 20 (used if set value is not an integer > 0).
- `sort` query, optional (string) — Sorting can applied on specified column, followed by the sorting direction (ie asc or desc) with the comma separation.

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/saasapplications/filters`

Operation: `saasApplicationsFilters`

Get Active SaaS Applications API filters

Get Active SaaS Applications API filters.

Tags: `Application 360`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/dpiapplications`

Operation: `dpiApplicationsList`

Get Discovered DPI Applications API

Get both configured and discovered DPI Applications seen on a customer network for a given time range.

Tags: `Application 360`

Parameters:

- `start_time` query, required (integer) — It is epoch time in seconds. It represents the start of the selected time range.
- `end_time` query, required (integer) — It is epoch time in seconds. It represents the end of the selected time range.
- `at` query, optional (integer) — It is epoch time in seconds. It represents the exact timestamp.
- `site_id` query, optional (integer) — Site ID.
- `keyword` query, optional (string) — keyword for case-insensitive search across columns having string values. Applicable on columns - application, category and protocol.
- `is_paginated` query, optional (boolean) — This indicates whether paginated response is required. Default value is true. When it is set to false then, the page and size parameter is ignored.
- `page` query, optional (integer) — The page field for the pagination. Default value is 1 (used if set value is not an integer > 0).
- `size` query, optional (integer) — The size field for the pagination. Default value is 20 (used if set value is not an integer > 0).
- `sort` query, optional (string) — Sorting is allowed on a specific column only. Sorting order can be given column name followed by the direction (e.g. asc or desc) with a comma separator. Supported columns are id, name, description, protocol_id, protocol_name,…

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/dpiapplications/filters`

Operation: `dpiApplicationsFilters`

Get DPI Applications filters

Get filter list for DPI application API.

Tags: `Application 360`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/compression-metrics/stats/applications`

Operation: `compressionStatsByApplication`

Get Compression Metrics Per Application

Get Compression Metrics Per Application.

Tags: `Application 360`

Parameters:

- `start_time` query, required (integer) — start_time is epoch time in seconds. It represents the start of the time range for which the metrics data for sites will be fetched. Only a single value is allowed.
- `end_time` query, required (integer) — end_time is epoch time in seconds. It represents the end of the time range for which the metrics data for sites will be fetched. Only a single value is allowed.
- `criticality_id` query, optional (integer) — Filter the data with criticality. Multiple values are allowed with comma (,) separation.
- `application_id` query, optional (integer) — Filter the data with application. Multiple values are allowed with comma (,) separation.
- `application_group_id` query, optional (integer) — Filter the data with application group. Multiple values are allowed with comma (,) separation.
- `src_site_id` query, optional (integer) — Filter the data with source site. Multiple values are allowed with comma (,) separation.
- `dst_site_id` query, optional (integer) — Filter the data with destination site. Multiple values are allowed with comma (,) separation.
- `src_wan_service_id` query, optional (integer) — Filter the data with source WAN service. Multiple values are allowed with comma (,) separation.
- `dst_wan_service_id` query, optional (integer) — Filter the data with destination WAN service. Multiple values are allowed with comma (,) separation.
- `keyword` query, optional (string) — The string value of keyword is used to case-insensitive search on application_name field.
- `is_paginated` query, optional (boolean) — This indicates whether paginated response is required. Default value is true. When it is set to false then, the page and size parameter is ignored.
- `page` query, optional (integer) — The page field for next page number to fetch data. Default value is 1 (used if set value is not an integer > 0).
- `size` query, optional (integer) — The number of items in each page. Default value is 20 (used if set value is not an integer > 0).
- `sort` query, optional (string) — Sorting is allowed on a specific column only. Sorting order can be given column name followed by the direction (e.g. asc or desc) with a comma separator. Supported columns are application_id, application_name, compressible, compressed, and…

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/compression-metrics/stats/sites`

Operation: `compressionStatsBySite`

Get Compression Metrics Per Site

Get Compression Metrics Per Site.

Tags: `Application 360`

Parameters:

- `start_time` query, required (integer) — start_time is epoch time in seconds. It represents the start of the time range for which the metrics data for sites will be fetched. Only a single value is allowed.
- `end_time` query, required (integer) — end_time is epoch time in seconds. It represents the end of the time range for which the metrics data for sites will be fetched. Only a single value is allowed.
- `criticality_id` query, optional (integer) — Filter the data with criticality. Multiple values are allowed with comma (,) separation.
- `application_id` query, optional (integer) — Filter the data with application. Multiple values are allowed with comma (,) separation.
- `application_group_id` query, optional (integer) — Filter the data with application group. Multiple values are allowed with comma (,) separation.
- `src_site_id` query, optional (integer) — Filter the data with source site. Multiple values are allowed with comma (,) separation.
- `dst_site_id` query, optional (integer) — Filter the data with destination site. Multiple values are allowed with comma (,) separation.
- `src_wan_service_id` query, optional (integer) — Filter the data with source WAN service. Multiple values are allowed with comma (,) separation.
- `dst_wan_service_id` query, optional (integer) — Filter the data with destination WAN service. Multiple values are allowed with comma (,) separation.
- `keyword` query, optional (string) — The string value of keyword is used to case-insensitive search on site_name field.
- `is_paginated` query, optional (boolean) — This indicates whether paginated response is required. Default value is true. When it is set to false then, the page and size parameter is ignored.
- `page` query, optional (integer) — The page field for next page number to fetch data. Default value is 1 (used if set value is not an integer > 0).
- `size` query, optional (integer) — The number of items in each page. Default value is 20 (used if set value is not an integer > 0).
- `sort` query, optional (string) — Sorting is allowed on a specific column only. Sorting order can be given column name followed by the direction (e.g. asc or desc) with a comma separator. Supported columns are site_id, site_name, direction, compressible, compressed, and…

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/compression-metrics/time-charts`

Operation: `compressionStatsTimeCharts`

Get Compression Metrics Time Charts

Get Compression Metrics Time Charts.

Tags: `Application 360`

Parameters:

- `start_time` query, required (integer) — start_time is epoch time in seconds. It represents the start of the time range for which the metrics data for sites will be fetched. Only a single value is allowed.
- `end_time` query, required (integer) — end_time is epoch time in seconds. It represents the end of the time range for which the metrics data for sites will be fetched. Only a single value is allowed.
- `criticality_id` query, optional (integer) — Filter the data with criticality. Multiple values are allowed with comma (,) separation.
- `application_id` query, optional (integer) — Filter the data with application. Multiple values are allowed with comma (,) separation.
- `application_group_id` query, optional (integer) — Filter the data with application group. Multiple values are allowed with comma (,) separation.
- `src_site_id` query, optional (integer) — Filter the data with source site. Multiple values are allowed with comma (,) separation.
- `dst_site_id` query, optional (integer) — Filter the data with destination site. Multiple values are allowed with comma (,) separation.
- `src_wan_service_id` query, optional (integer) — Filter the data with source WAN service. Multiple values are allowed with comma (,) separation.
- `dst_wan_service_id` query, optional (integer) — Filter the data with destination WAN service. Multiple values are allowed with comma (,) separation.

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/compression-metrics/stats`

Operation: `compressionStats`

Get Compression Metrics Stats

Returns compressible, compressed, incompressible bytes for given time range. These data helps to find compression ratio and compressibility. The formula for compression ratio and compressibility is '((compressible - compressed) / compressible) * 100' and '(compressible / (compressible + incompressible)) * 100' respectively.

Tags: `Application 360`

Parameters:

- `start_time` query, required (integer) — start_time is epoch time in seconds. It represents the start of the time range for which the metrics data for sites will be fetched. Only a single value is allowed.
- `end_time` query, required (integer) — end_time is epoch time in seconds. It represents the end of the time range for which the metrics data for sites will be fetched. Only a single value is allowed.
- `criticality_id` query, optional (integer) — Filter the data with criticality. Multiple values are allowed with comma (,) separation.
- `application_id` query, optional (integer) — Filter the data with application. Multiple values are allowed with comma (,) separation.
- `application_group_id` query, optional (integer) — Filter the data with application group. Multiple values are allowed with comma (,) separation.
- `src_site_id` query, optional (integer) — Filter the data with source site. Multiple values are allowed with comma (,) separation.
- `dst_site_id` query, optional (integer) — Filter the data with destination site. Multiple values are allowed with comma (,) separation.
- `src_wan_service_id` query, optional (integer) — Filter the data with source WAN service. Multiple values are allowed with comma (,) separation.
- `dst_wan_service_id` query, optional (integer) — Filter the data with destination WAN service. Multiple values are allowed with comma (,) separation.

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/compression-metrics/filters`

Operation: `compressionStatsFilters`

Get Compression Metrics filters

Get filter list for compression metrics APIs.

Tags: `Application 360`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/applications/performance/filters`

Operation: `applicationsPerformanceFilters`

Get Application Performance filters

Get filter list for applications performance APIs.

Tags: `Application 360`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/applications/overview/filters`

Operation: `applicationsOverviewFilters`

Get Application Overview filters

Get filter list for applications overview APIs.

Tags: `Application 360`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/applications/eqs/worst/timeseries`

Operation: `worstEqsInfoTimeSeries`

Get Eqs Evolution by worst 10 application API

Get Eqs Worst 10 Application Time series API will return Eqs evolution data grouped by Worst Application.

Tags: `Application 360`

Parameters:

- `start_time` query, required (integer) — (required)start time is epoch time in seconds. It represents the start of the time range (start - end) from which the flow data for Eqs will be fetched.
- `end_time` query, required (integer) — (required)end time is epoch time in seconds. It represents the end of the time range (start - end) upto which the flow data for Eqs will be fetched.
- `criticality_id` query, optional (integer) — Filter the data with criticality.Multiples values are allowed with comma (,) separation.
- `application_id` query, optional (integer) — Filter the data with Application.Multiples values are allowed with comma (,) separation.
- `application_group_id` query, optional (integer) — Filter the data with application group.Multiples values are allowed with comma (,) separation.
- `src_site_id` query, optional (integer) — Filter the data with Local Site Id.Multiples values are allowed with comma (,) separation.
- `dst_site_id` query, optional (integer) — Filter the data with Remote Site Id.Multiples values are allowed with comma (,) separation.
- `src_network_id` query, optional (integer) — Filter the data with Local Network Id.Multiples values are allowed with comma (,) separation.
- `dst_network_id` query, optional (integer) — Filter the data with Remote Network Id.Multiples values are allowed with comma (,) separation.
- `src_appliance_id` query, optional (integer) — Filter the data with Local Appliance Id. Multiples values are allowed with comma (,) separation.
- `dst_appliance_id` query, optional (integer) — Filter the data with Remote Appliance Id. Multiples values are allowed with comma (,) separation.

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/applications/throughput/top/timeseries`

Operation: `application360TopApplicationThroughputInfo`

Get Throughput Evolution by Top 10 application API

Get Throughput Evolution API will returns throughput evolution data grouped by top 10 Applicaion.

Tags: `Application 360`

Parameters:

- `start_time` query, required (integer) — (required)start time is epoch time in seconds. It represents the start of the time range (start - end) from which the flow data for throughput will be fetched.
- `end_time` query, required (integer) — (required)end time is epoch time in seconds. It represents the end of the time range (start - end) upto which the flow data for throughput will be fetched.
- `criticality_id` query, optional (integer) — Filter the data with criticality.Multiples values are allowed with comma (,) separation.
- `application_id` query, optional (integer) — Filter the data with Application.Multiples values are allowed with comma (,) separation.
- `application_group_id` query, optional (integer) — Filter the data with application group.Multiples values are allowed with comma (,) separation.
- `src_site_id` query, optional (integer) — Filter the data with Local Site Id.Multiples values are allowed with comma (,) separation.
- `dst_site_id` query, optional (integer) — Filter the data with Remote Site Id.Multiples values are allowed with comma (,) separation.
- `src_network_id` query, optional (integer) — Filter the data with Local Network Id.Multiples values are allowed with comma (,) separation.
- `dst_network_id` query, optional (integer) — Filter the data with Remote Network Id.Multiples values are allowed with comma (,) separation.
- `src_appliance_id` query, optional (integer) — Filter the data with Local Appliance Id. Multiples values are allowed with comma (,) separation.
- `dst_appliance_id` query, optional (integer) — Filter the data with Remote Appliance Id. Multiples values are allowed with comma (,) separation.

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/adrapplications`

Operation: `applicationsList`

Get Discovered Applications API

Get both configured and discovered Applications seen on a customer network for a given time range.

Tags: `Application 360`

Parameters:

- `start_time` query, required (integer) — It is epoch time in seconds. It represents the start of the selected time range.
- `end_time` query, required (integer) — It is epoch time in seconds. It represents the end of the selected time range.
- `at` query, optional (integer) — It is epoch time in seconds. It represents the exact timestamp.
- `site_id` query, optional (integer) — Site ID.
- `keyword` query, optional (string) — keyword for case-insensitive search across columns having string values. Applicable on columns - application, category and protocol.
- `is_paginated` query, optional (boolean) — This indicates whether paginated response is required. Default value is true. When it is set to false then, the page and size parameter is ignored.
- `page` query, optional (integer) — The page field for the pagination. Default value is 1 (used if set value is not an integer > 0).
- `size` query, optional (integer) — The size field for the pagination. Default value is 20 (used if set value is not an integer > 0).
- `sort` query, optional (string) — Sorting is allowed on a specific column only. Sorting order can be given column name followed by the direction (e.g. asc or desc) with a comma separator. Supported columns are id, name, description, protocol_id, protocol_name,…

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/adrapplications/filters`

Operation: `applicationsFilters`

Get Applications filters

Get filter list for application API.

Tags: `Application 360`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/sites/overview`

Operation: `getSdwanSitesOverview`

Get Sites Overview

Get sites overview will return data related to all the sites.

Tags: `Site 360`

Parameters:

- `start_time` query, required (integer) — start_time is epoch time in seconds. It represents the start of the time range (start_time - end_time) for which the metrics data for sites will be fetched. Only a single value is allowed.
- `end_time` query, required (integer) — end_time is epoch time in seconds. It represents the end of the time range (start_time - end_time) for which the metrics data for sites will be fetched. Only a single value is allowed.
- `flow_direction` query, required (FlowDirection) — The parameter is used to specify the direction of flow data the user wants to view lan_to_wan or wan_to_lan. Allowed values are lan_to_wan and wan_to_lan. If no value is provided or an invalid value is provided then error message will be…
- `page` query, optional (QuerryPage) — next page number for navigation for Sites Overview UI page used for pagination. Default value is 1 (used if set value is not an integer > 0).
- `size` query, optional (QuerryPageSize) — current page size for Sites Overview UI page used for pagination. Default value is 20 (used if set value is not an integer > 0).
- `sort` query, optional (string) — The sort field. Sorting can applied on specified column. Sorting can be applied only on one column at a time. Specified column followed by the sorting direction (ie asc or desc) with the comma separation. Allowed columns are site,…
- `eqs_gt` query, optional (number) — Filter for EQS greater than the specified value.
- `eqs_lt` query, optional (number) — Filter for EQS less than the specified value.
- `eqs_eq` query, optional (number) — Filter for EQS equals the specified value.
- `eqs_gteq` query, optional (number) — Filter for EQS greater than or equal to the specified value.
- `eqs_lteq` query, optional (number) — Filter for EQS less than or equal to the specified value.
- `throughput_gt` query, optional (integer) — Filter for Throughput greater than the specified value.
- `throughput_lt` query, optional (integer) — Filter for Throughput less than the specified value.
- `throughput_eq` query, optional (integer) — Filter for Throughput equals the specified value.
- `throughput_gteq` query, optional (integer) — Filter for Throughput greater than or equal to the specified value.
- `throughput_lteq` query, optional (integer) — Filter for Throughput less than or equal to the specified value.
- `utilization_gt` query, optional (integer) — Filter for Utilization greater than the specified value.
- `utilization_lt` query, optional (integer) — Filter for Utilization less than the specified value.
- `utilization_eq` query, optional (integer) — Filter for Utilization equals the specified value.
- `utilization_gteq` query, optional (integer) — Filter for Utilization greater than or equal to the specified value.
- `utilization_lteq` query, optional (integer) — Filter for Utilization less than or equal to the specified value.
- `capacity_gt` query, optional (integer) — Filter for Capacity greater than the specified value.
- `capacity_lt` query, optional (integer) — Filter for Capacity less than the specified value.
- `capacity_eq` query, optional (integer) — Filter for Capacity equals the specified value.
- `capacity_gteq` query, optional (integer) — Filter for Capacity greater than or equal to the specified value.
- `capacity_lteq` query, optional (integer) — Filter for Capacity less than or equal to the specified value.
- `keyword` query, optional (string) — keyword for case-insensitive search across columns having string values. Applicable on columns - application, application group, site and appliance.

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/sites/{id}/metrics/wans`

Operation: `site360WanServicesInfo`

Get Wan Services Informations API

Get wan services state for a customer in a given time range.

Tags: `Site 360`

Parameters:

- `id` path, required (integer) — the unique id for site.
- `start_time` query, required (integer) — (required) Start is epoch time in seconds. It represents the start of the selected time range (start - end).
- `end_time` query, required (integer) — (required) End is epoch time in seconds. It represents the end of the selected time range (start - end).
- `page` query, optional (QuerryPage) — Next page number used for pagination. Default value is 1 (used if set value is not an integer > 0).
- `size` query, optional (QuerryPageSize) — Current page size used for pagination. Default value is 20 (used if set value is not an integer > 0).
- `sort` query, optional (string) — Sorting column used for column sorting, specified column followed by the sorting direction (ie asc or desc) with the comma separation. Allowed columns are network_name,throughput, eqs,…
- `criticality_id` query, optional (integer) — Filter the data with criticality. Multiples vales are allowed with comma (,) separation.
- `application_id` query, optional (integer) — Filter the data with Application. Multiples vales are allowed with comma (,) separation.
- `application_group_id` query, optional (integer) — Filter the data with application group. Multiples vales are allowed with comma (,) separation.
- `dst_site_id` query, optional (integer) — Filter the data with Remote Site Id. Multiples values are allowed with comma (,) separation.
- `remote_site_id` query, optional (integer) — Filter the data with Remote Site Id. Multiples values are allowed with comma (,) separation.
- `src_network_id` query, optional (integer) — Filter the data with Local Network Id. Multiples values are allowed with comma (,) separation.
- `local_network_id` query, optional (integer) — Filter the data with Local Network Id. Multiples values are allowed with comma (,) separation.
- `dst_network_id` query, optional (integer) — Filter the data with Remote Network Id. Multiples values are allowed with comma (,) separation.
- `remote_network_id` query, optional (integer) — Filter the data with Remote Network Id. Multiples values are allowed with comma (,) separation.
- `local_appliance_id` query, optional (integer) — Filter the data with Local Appliance Id.Multiples values are allowed with comma (,) separation.
- `remote_appliance_id` query, optional (integer) — Filter the data with Remote Appliance Id.Multiples values are allowed with comma (,) separation.
- `local_network_interface` query, optional (integer) — Filter the data with Local Wan Interface.Multiples values are allowed with comma (,) separation.
- `remote_network_interface` query, optional (integer) — Filter the data with Remote Wan Interface.Multiples values are allowed with comma (,) separation.
- `flow_direction` query, optional (FlowDirection) — The parameter is used to specify the direction of flow data the user wants to view lan_to_wan or wan_to_lan. Allowed values are lan_to_wan and wan_to_lan and also both as combine as lan_to_wan,wan_to_lan. If no value is provided it is both…

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/sites/{id}/eqs/worst`

Operation: `site360WorstEqsInfo`

Get worst 10 Eqs API

Get worst 10 Eqs api will return Eqs data for worst 10 Eqs group by application or application group.

Tags: `Site 360`

Parameters:

- `id` path, required (integer) — the site id.
- `start_time` query, required (integer) — (required) Start time is epoch time in seconds. It represents the start of the time range (start - end) from which the flow data for Eqs will be fetched.
- `end_time` query, required (integer) — (required) End time is epoch time in seconds. It represents the end of the time range (start - end) upto which the flow data for Eqs will be fetched.
- `group_by` query, required (string) — (required) Filter the result of Eqs group by applicationGroup or application.
- `criticality_id` query, optional (integer) — Filter the data with criticality. Multiples vales are allowed with comma (,) separation.
- `application_id` query, optional (integer) — Filter the data with Application. Multiples vales are allowed with comma (,) separation.
- `application_group_id` query, optional (integer) — Filter the data with application group. Multiples vales are allowed with comma (,) separation.
- `dst_site_id` query, optional (integer) — Filter the data with Remote Site Id. Multiples values are allowed with comma (,) separation.
- `remote_site_id` query, optional (integer) — Filter the data with Remote Site Id. Multiples values are allowed with comma (,) separation.
- `src_network_id` query, optional (integer) — Filter the data with Local Network Id. Multiples values are allowed with comma (,) separation.
- `local_network_id` query, optional (integer) — Filter the data with Local Network Id. Multiples values are allowed with comma (,) separation.
- `dst_network_id` query, optional (integer) — Filter the data with Remote Network Id. Multiples values are allowed with comma (,) separation.
- `remote_network_id` query, optional (integer) — Filter the data with Remote Network Id. Multiples values are allowed with comma (,) separation.
- `local_appliance_id` query, optional (integer) — Filter the data with Local Appliance Id. Multiples values are allowed with comma (,) separation.
- `remote_appliance_id` query, optional (integer) — Filter the data with Remote Appliance Id. Multiples values are allowed with comma (,) separation.
- `local_network_interface` query, optional (integer) — Filter the data with Local Wan Interface. Multiples values are allowed with comma (,) separation.
- `remote_network_interface` query, optional (integer) — Filter the data with Remote Wan Interface. Multiples values are allowed with comma (,) separation.
- `flow_direction` query, optional (FlowDirection) — The parameter is used to specify the direction of flow data the user wants to view lan_to_wan or wan_to_lan. Allowed values are lan_to_wan and wan_to_lan and also both as combine as lan_to_wan,wan_to_lan. If no value is provided it is both…

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/sites/{id}/eqs/worst/timeseries`

Operation: `site360WorstEqsTimeSeriesInfo`

Get Eqs Evolution by worst 10 application API

Get Eqs Worst 10 Application Time series API will return Eqs evolution data grouped by Worst Application.

Tags: `Site 360`

Parameters:

- `id` path, required (integer) — the site id
- `start_time` query, required (integer) — (required)start time is epoch time in seconds. It represents the start of the time range (start - end) from which the flow data for Eqs will be fetched.
- `end_time` query, required (integer) — (required)end time is epoch time in seconds. It represents the end of the time range (start - end) upto which the flow data for Eqs will be fetched.
- `criticality_id` query, optional (integer) — Filter the data with criticality.Multiples values are allowed with comma (,) separation.
- `application_id` query, optional (integer) — Filter the data with Application.Multiples values are allowed with comma (,) separation.
- `application_group_id` query, optional (integer) — Filter the data with application group.Multiples values are allowed with comma (,) separation.
- `remote_site_id` query, optional (integer) — Filter the data with Remote Site Id.Multiples values are allowed with comma (,) separation.
- `local_network_id` query, optional (integer) — Filter the data with Local Network Id.Multiples values are allowed with comma (,) separation.
- `remote_network_id` query, optional (integer) — Filter the data with Remote Network Id.Multiples values are allowed with comma (,) separation.
- `local_appliance_id` query, optional (integer) — Filter the data with Local Appliance Id.Multiples values are allowed with comma (,) separation.
- `remote_appliance_id` query, optional (integer) — Filter the data with Remote Appliance Id.Multiples values are allowed with comma (,) separation.
- `local_network_interface` query, optional (integer) — Filter the data with Local Wan Interface.Multiples values are allowed with comma (,) separation.
- `remote_network_interface` query, optional (integer) — Filter the data with Remote Wan Interface.Multiples values are allowed with comma (,) separation.
- `flow_direction` query, optional (FlowDirection) — The parameter is used to specify the direction of flow data the user wants to view lan_to_wan or wan_to_lan. Allowed values are lan_to_wan and wan_to_lan and also both as combine as lan_to_wan,wan_to_lan. If no value is provided it is both…

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/sites/{id}/volume/top`

Operation: `site360VolumeInfo`

Get Top 10 Volume API

Get Top 10 Volume api will return Volume data for top 10 Volume group by application or application group.

Tags: `Site 360`

Parameters:

- `id` path, required (integer) — the unique id for site.
- `start_time` query, required (integer) — (required) Start time is epoch time in seconds. It represents the start of the time range (start - end) from which the flow data for Volume will be fetched.
- `end_time` query, required (integer) — (required) End time is epoch time in seconds. It represents the end of the time range (start - end) upto which the flow data for Volume will be fetched.
- `group_by` query, required (string) — (required) Filter the result of Volume group by applicationGroup or application.
- `criticality_id` query, optional (integer) — Filter the data with criticality. Multiples vales are allowed with comma (,) separation.
- `application_id` query, optional (integer) — Filter the data with Application. Multiples vales are allowed with comma (,) separation.
- `application_group_id` query, optional (integer) — Filter the data with application group. Multiples vales are allowed with comma (,) separation.
- `dst_site_id` query, optional (integer) — Filter the data with Remote Site Id. Multiples values are allowed with comma (,) separation.
- `remote_site_id` query, optional (integer) — Filter the data with Remote Site Id. Multiples values are allowed with comma (,) separation.
- `src_network_id` query, optional (integer) — Filter the data with Local Network Id. Multiples values are allowed with comma (,) separation.
- `local_network_id` query, optional (integer) — Filter the data with Local Network Id. Multiples values are allowed with comma (,) separation.
- `dst_network_id` query, optional (integer) — Filter the data with Remote Network Id. Multiples values are allowed with comma (,) separation.
- `remote_network_id` query, optional (integer) — Filter the data with Remote Network Id. Multiples values are allowed with comma (,) separation.
- `local_appliance_id` query, optional (integer) — Filter the data with Local Appliance Id.Multiples values are allowed with comma (,) separation.
- `remote_appliance_id` query, optional (integer) — Filter the data with Remote Appliance Id.Multiples values are allowed with comma (,) separation.
- `local_network_interface` query, optional (integer) — Filter the data with Local Wan Interface.Multiples values are allowed with comma (,) separation.
- `remote_network_interface` query, optional (integer) — Filter the data with Remote Wan Interface.Multiples values are allowed with comma (,) separation.
- `flow_direction` query, optional (FlowDirection) — The parameter is used to specify the direction of flow data the user wants to view lan_to_wan or wan_to_lan. Allowed values are lan_to_wan and wan_to_lan and also both as combine as lan_to_wan,wan_to_lan. If no value is provided it is both…

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/sites/{id}/metrics/wans/throughput`

Operation: `site360WanServicesThroughput`

Get WAN throughput evolution API

Get throughput evolution API will returns throughput evolution data for each existing Wan Service.

Tags: `Site 360`

Parameters:

- `id` path, required (integer) — the site id.
- `start_time` query, required (integer) — (required) Start is epoch time in seconds. It represents the start of the time range (start - end) from which the throughput data will be fetched.
- `end_time` query, required (integer) — (required) End is epoch time in seconds. It represents the end of the time range (start - end) upto which the throughput data will be fetched.
- `criticality_id` query, optional (integer) — Filter the data with criticality. Multiples vales are allowed with comma (,) separation.
- `application_id` query, optional (integer) — Filter the data with Application. Multiples vales are allowed with comma (,) separation.
- `application_group_id` query, optional (integer) — Filter the data with application group. Multiples vales are allowed with comma (,) separation.
- `dst_site_id` query, optional (integer) — Filter the data with Remote Site Id. Multiples values are allowed with comma (,) separation.
- `remote_site_id` query, optional (integer) — Filter the data with Remote Site Id. Multiples values are allowed with comma (,) separation.
- `src_network_id` query, optional (integer) — Filter the data with Local Network Id. Multiples values are allowed with comma (,) separation.
- `local_network_id` query, optional (integer) — Filter the data with Local Network Id. Multiples values are allowed with comma (,) separation.
- `dst_network_id` query, optional (integer) — Filter the data with Remote Network Id. Multiples values are allowed with comma (,) separation.
- `remote_network_id` query, optional (integer) — Filter the data with Remote Network Id. Multiples values are allowed with comma (,) separation.
- `local_appliance_id` query, optional (integer) — Filter the data with Local Appliance Id. Multiples values are allowed with comma (,) separation.
- `remote_appliance_id` query, optional (integer) — Filter the data with Remote Appliance Id. Multiples values are allowed with comma (,) separation.
- `local_network_interface` query, optional (integer) — Filter the data with Local Wan Interface. Multiples values are allowed with comma (,) separation.
- `remote_network_interface` query, optional (integer) — Filter the data with Remote Wan Interface. Multiples values are allowed with comma (,) separation.
- `flow_direction` query, optional (FlowDirection) — The parameter is used to specify the direction of flow data the user wants to view lan_to_wan or wan_to_lan. Allowed values are lan_to_wan and wan_to_lan and also both as combine as lan_to_wan,wan_to_lan. If no value is provided it is both…

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/sites/{id}/metrics/wans/eqs`

Operation: `site360WanServicesEqs`

Get WAN EQS evolution API

Get EQS evolution API will returns EQS evolution data for each existing Wan Service.

Tags: `Site 360`

Parameters:

- `id` path, required (integer) — the site id
- `start_time` query, required (integer) — (required)start is epoch time in seconds. It represents the start of the time range (start - end) from which the EQS data will be fetched.
- `end_time` query, required (integer) — (required)end is epoch time in seconds. It represents the end of the time range (start - end) upto which the EQS data will be fetched.
- `criticality_id` query, optional (integer) — Filter the data with criticality.Multiples values are allowed with comma (,) separation.
- `application_id` query, optional (integer) — Filter the data with Application.Multiples values are allowed with comma (,) separation.
- `application_group_id` query, optional (integer) — Filter the data with application group.Multiples values are allowed with comma (,) separation.
- `remote_site_id` query, optional (integer) — Filter data with Remote Site Id.Multiples values are allowed with comma (,) separation.
- `local_network_id` query, optional (integer) — Filter data with Local Network Id..Multiples values are allowed with comma (,) separation.
- `remote_network_id` query, optional (integer) — Filter data with Remote Network Id.Multiples values are allowed with comma (,) separation.
- `local_appliance_id` query, optional (integer) — Filter the data with Local Appliance Id.Multiples values are allowed with comma (,) separation.
- `remote_appliance_id` query, optional (integer) — Filter the data with Remote Appliance Id.Multiples values are allowed with comma (,) separation.
- `local_network_interface` query, optional (integer) — Filter the data with Local Wan Interface.Multiples values are allowed with comma (,) separation.
- `remote_network_interface` query, optional (integer) — Filter the data with Remote Wan Interface.Multiples values are allowed with comma (,) separation.
- `flow_direction` query, optional (FlowDirection) — The parameter is used to specify the direction of flow data the user wants to view lan_to_wan or wan_to_lan. Allowed values are lan_to_wan and wan_to_lan and also both as combine as lan_to_wan,wan_to_lan. If no value is provided it is both…

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/metrics/timeseries`

Operation: `metricsInfo`

Get Monitoring metrics Evolution API

Get metrics API will returns EQS, Throughput and Raised alarm details in time series format.

Tags: `Appliance 360`

Parameters:

- `start_time` query, required (integer) — (required) Start time is epoch time in seconds. It represents the start of the time range (start - end) from which the metrics Throughput,EQS and Raised alarms data will be fetched.
- `end_time` query, required (integer) — (required) End time is epoch time in seconds. It represents the end of the time range (start - end) upto which the metrics Throughput,EQS and Raised alarms data will be fetched.
- `flow_direction` query, optional (FlowDirection) — The parameter is used to specify the direction of flow data the throughput will be calculated for lan_to_wan or wan_to_lan. Allowed values are lan_to_wan and wan_to_lan. If no value is provided the default value will be lan_to_wan.
- `src_site_id` query, optional (integer) — The site_src_id to filter the data by source site.
- `dst_site_id` query, optional (integer) — The site_dst_id to filter the data by remote site.
- `src_network_id` query, optional (integer) — The network_src_id to filter data by source network.
- `dst_network_id` query, optional (integer) — The network_dst_id to filter data by destination network.

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/sites/{id}/throughput/timeseries`

Operation: `site360ThroughputInfo`

Get Throughput Evolution API

Get Throughput Evolution API will returns throughput evolution data grouped by Application Group or Criticality.

Tags: `Site 360`

Parameters:

- `id` path, required (integer) — the site id.
- `start_time` query, required (integer) — (required) Start time is epoch time in seconds. It represents the start of the time range (start - end) from which the flow data for throughput will be fetched.
- `end_time` query, required (integer) — (required) End time is epoch time in seconds. It represents the end of the time range (start - end) upto which the flow data for throughput will be fetched.
- `group_by` query, required (string) — (required) Filter the result of throughput group by applicationGroup or criticality.
- `criticality_id` query, optional (integer) — Filter the data with criticality. Multiples values are allowed with comma (,) separation.
- `application_id` query, optional (integer) — Filter the data with Application. Multiples values are allowed with comma (,) separation.
- `application_group_id` query, optional (integer) — Filter the data with application group. Multiples values are allowed with comma (,) separation.
- `dst_site_id` query, optional (integer) — Filter the data with Remote Site Id. Multiples values are allowed with comma (,) separation.
- `remote_site_id` query, optional (integer) — Filter the data with Remote Site Id. Multiples values are allowed with comma (,) separation.
- `src_network_id` query, optional (integer) — Filter the data with Local Network Id. Multiples values are allowed with comma (,) separation.
- `local_network_id` query, optional (integer) — Filter the data with Local Network Id. Multiples values are allowed with comma (,) separation.
- `dst_network_id` query, optional (integer) — Filter the data with Remote Network Id. Multiples values are allowed with comma (,) separation.
- `remote_network_id` query, optional (integer) — Filter the data with Remote Network Id. Multiples values are allowed with comma (,) separation.
- `local_appliance_id` query, optional (integer) — Filter the data with Local Appliance Id.Multiples values are allowed with comma (,) separation.
- `remote_appliance_id` query, optional (integer) — Filter the data with Remote Appliance Id.Multiples values are allowed with comma (,) separation.
- `local_network_interface` query, optional (integer) — Filter the data with Local Wan Interface.Multiples values are allowed with comma (,) separation.
- `remote_network_interface` query, optional (integer) — Filter the data with Remote Wan Interface.Multiples values are allowed with comma (,) separation.
- `flow_direction` query, optional (FlowDirection) — The parameter is used to specify the direction of flow data the user wants to view lan_to_wan or wan_to_lan. Allowed values are lan_to_wan and wan_to_lan and also both as combine as lan_to_wan,wan_to_lan. If no value is provided it is both…

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/sites/{id}/eqs/timeseries`

Operation: `site360EqsInfo`

Get Eqs Evolution API

Get Eqs Evolution API will returns Eqs evolution data grouped by Criticality or Application Group.

Tags: `Site 360`

Parameters:

- `id` path, required (integer) — the site id.
- `start_time` query, required (integer) — (required)start time is epoch time in seconds. It represents the start of the time range (start - end) from which the flow data for Eqs will be fetched.
- `end_time` query, required (integer) — (required)end time is epoch time in seconds. It represents the end of the time range (start - end) upto which the flow data for Eqs will be fetched.
- `group_by` query, required (string) — (required) Filter the result of Eqs group by applicationGroup or criticality.
- `criticality_id` query, optional (integer) — Filter the data with criticality. Multiples values are allowed with comma (,) separation.
- `application_id` query, optional (integer) — Filter the data with Application. Multiples values are allowed with comma (,) separation.
- `application_group_id` query, optional (integer) — Filter the data with application group. Multiples values are allowed with comma (,) separation.
- `dst_site_id` query, optional (integer) — Filter the data with Remote Site Id. Multiples values are allowed with comma (,) separation.
- `remote_site_id` query, optional (integer) — Filter the data with Remote Site Id. Multiples values are allowed with comma (,) separation.
- `src_network_id` query, optional (integer) — Filter the data with Local Network Id. Multiples values are allowed with comma (,) separation.
- `local_network_id` query, optional (integer) — Filter the data with Local Network Id. Multiples values are allowed with comma (,) separation.
- `dst_network_id` query, optional (integer) — Filter the data with Remote Network Id. Multiples values are allowed with comma (,) separation.
- `remote_network_id` query, optional (integer) — Filter the data with Remote Network Id. Multiples values are allowed with comma (,) separation.
- `local_appliance_id` query, optional (integer) — Filter the data with Local Appliance Id.Multiples values are allowed with comma (,) separation.
- `remote_appliance_id` query, optional (integer) — Filter the data with Remote Appliance Id.Multiples values are allowed with comma (,) separation.
- `local_network_interface` query, optional (integer) — Filter the data with Local Wan Interface.Multiples values are allowed with comma (,) separation.
- `remote_network_interface` query, optional (integer) — Filter the data with Remote Wan Interface.Multiples values are allowed with comma (,) separation.
- `flow_direction` query, optional (FlowDirection) — The parameter is used to specify the direction of flow data the user wants to view lan_to_wan or wan_to_lan. Allowed values are lan_to_wan and wan_to_lan and also both as combine as lan_to_wan,wan_to_lan. If no value is provided it is both…

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/sites/{id}/throughput/top/timeseries`

Operation: `topApplicationthroughputInfo`

Get Throughput Evolution by Top 10 application API

Get Throughput Evolution API will returns throughput evolution data grouped by top 10 Application.

Tags: `Site 360`

Parameters:

- `id` path, required (integer) — the site id.
- `start_time` query, required (integer) — (required) Start time is epoch time in seconds. It represents the start of the time range (start - end) from which the flow data for throughput will be fetched.
- `end_time` query, required (integer) — (required) End time is epoch time in seconds. It represents the end of the time range (start - end) upto which the flow data for throughput will be fetched.
- `criticality_id` query, optional (integer) — Filter the data with criticality. Multiples values are allowed with comma (,) separation.
- `application_id` query, optional (integer) — Filter the data with Application. Multiples values are allowed with comma (,) separation.
- `application_group_id` query, optional (integer) — Filter the data with application group. Multiples values are allowed with comma (,) separation.
- `dst_site_id` query, optional (integer) — Filter the data with Remote Site Id. Multiples values are allowed with comma (,) separation.
- `remote_site_id` query, optional (integer) — Filter the data with Remote Site Id. Multiples values are allowed with comma (,) separation.
- `src_network_id` query, optional (integer) — Filter the data with Local Network Id. Multiples values are allowed with comma (,) separation.
- `local_network_id` query, optional (integer) — Filter the data with Local Network Id. Multiples values are allowed with comma (,) separation.
- `dst_network_id` query, optional (integer) — Filter the data with Remote Network Id. Multiples values are allowed with comma (,) separation.
- `remote_network_id` query, optional (integer) — Filter the data with Remote Network Id. Multiples values are allowed with comma (,) separation.
- `local_appliance_id` query, optional (integer) — Filter the data with Local Appliance Id. Multiples values are allowed with comma (,) separation.
- `remote_appliance_id` query, optional (integer) — Filter the data with Remote Appliance Id. Multiples values are allowed with comma (,) separation.
- `local_network_interface` query, optional (integer) — Filter the data with Local Wan Interface. Multiples values are allowed with comma (,) separation.
- `remote_network_interface` query, optional (integer) — Filter the data with Remote Wan Interface. Multiples values are allowed with comma (,) separation.
- `flow_direction` query, optional (FlowDirection) — The parameter is used to specify the direction of flow data the user wants to view lan_to_wan or wan_to_lan. Allowed values are lan_to_wan and wan_to_lan and also both as combine as lan_to_wan,wan_to_lan. If no value is provided it is both…

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/sites/application-groups`

Operation: `sitesApplicationGroups`

Get Application Groups

Get application groups will return the pre-configured application groups per criticality by the user.

Tags: `Site 360`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/flows`

Operation: `flowsView`

Get Flows View

Get Flows view api will returns data related to flows used for flows grid view.

Tags: `Application 360`

Parameters:

- `start_time` query, required (integer) — Start timestamp of the time range in epoch. Unit is seconds. Only a single value is allowed.
- `end_time` query, required (integer) — End timestamp of the time range in epoch. Unit is seconds. Only a single value is allowed.
- `local_site_id` query, optional (integer) — Filter data using local site. Multiples values are allowed with comma (,) separation. For 'all' use 0. Default value is 0 (all).
- `remote_site_id` query, optional (integer) — Filter data using remote site. Multiples values are allowed with comma (,) separation. For 'all' use 0. Default value is 0 (all).
- `application_group_id` query, optional (integer) — Filter data using application group. Multiples values are allowed with comma (,) separation. For 'all' use 0. Default value is 0 (all).
- `application_id` query, optional (integer) — Filter data using application. Multiples values are allowed with comma (,) separation. For 'all' use 0. Default value is 0 (all).
- `eqs_gt` query, optional (number) — Filter for EQS greater than the specified value.
- `eqs_lt` query, optional (number) — Filter for EQS less than the specified value.
- `eqs_eq` query, optional (number) — Filter for EQS equals the specified value.
- `eqs_gteq` query, optional (number) — Filter for EQS greater than or equal to the specified value.
- `eqs_lteq` query, optional (number) — Filter for EQS less than or equal to the specified value.
- `keyword` query, optional (string) — keyword for case-insensitive search across columns having string values. Applicable on columns - application, application group and site.
- `is_paginated` query, optional (boolean) — The boolean flag for pagination. The default value will be false, which means no pagination
- `page` query, optional (QuerryPage) — The page field for the pagination. Default value is 1 (used if set value is not an integer > 0).
- `size` query, optional (QuerryPageSize) — The number of items in each page. Default value is 20 (used if set value is not an integer > 0).
- `sort` query, optional (string) — Above example is sorting on Local Site in asc order. Sorting can applied on specified column. Specified column can be local_site_id, local_appliance_id, local_nap_index, remote_site_id, remote_appliance_id, remote_nap_index,…

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/flows/filters`

Operation: `flowslist`

Get Flows Filters

Get flows-filter api will returns the list of all local and remote sites, application groups and applications. (This api is being used by GUI for filtering).

Tags: `Application 360`

Parameters:

- `start_time` query, required (integer) — Start timestamp of the time range in epoch. Unit is seconds. Only a single value is allowed.
- `end_time` query, required (integer) — End timestamp of the time range in epoch. Unit is seconds. Only a single value is allowed.
- `local_site_id` query, optional (integer) — Filter data using local site. Multiples vales are allowed with comma (,) separation. For 'all' use 0. Default value is 0 (all).
- `remote_site_id` query, optional (integer) — Filter data using remote site. Multiples vales are allowed with comma (,) separation. For 'all' use 0. Default value is 0 (all).
- `application_group_id` query, optional (integer) — Filter data using application group. Multiples vales are allowed with comma (,) separation. For 'all' use 0. Default value is 0 (all).
- `application_id` query, optional (integer) — Filter data using application. Multiples vales are allowed with comma (,) separation. For 'all' use 0. Default value is 0 (all).

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/sites/{id}/metrics/summary`

Operation: `site360ApplicationSummaryInfo`

Get Site 360 application overview Summary API

Get Application overview Summary will return Application overview summary data group by application, application group or criticality.

Tags: `Site 360`

Parameters:

- `id` path, required (integer) — the site id
- `start_time` query, required (integer) — (required) Start time is epoch time in seconds. It represents the start of the time range (start - end) from which the aplication summary will be fetched.
- `end_time` query, required (integer) — (required) End time is epoch time in seconds. It represents the end of the time range (start - end) upto which the flow data for application summary will be fetched.
- `group_by` query, required (string) — (required) Filter the result of Eqs group by applicationGroup, application or criticality .
- `criticality_id` query, optional (integer) — Filter the data with criticality. Multiples values are allowed with comma (,) separation.
- `application_id` query, optional (integer) — Filter the data with Application. Multiples values are allowed with comma (,) separation.
- `application_group_id` query, optional (integer) — Filter the data with application group. Multiples values are allowed with comma (,) separation.
- `dst_site_id` query, optional (integer) — Filter the data with Remote Site Id. Multiples values are allowed with comma (,) separation.
- `remote_site_id` query, optional (integer) — Filter the data with Remote Site Id. Multiples values are allowed with comma (,) separation.
- `src_network_id` query, optional (integer) — Filter the data with Local Network Id. Multiples values are allowed with comma (,) separation.
- `local_network_id` query, optional (integer) — Filter the data with Local Network Id. Multiples values are allowed with comma (,) separation.
- `dst_network_id` query, optional (integer) — Filter the data with Remote Network Id. Multiples values are allowed with comma (,) separation.
- `remote_network_id` query, optional (integer) — Filter the data with Remote Network Id. Multiples values are allowed with comma (,) separation.
- `local_appliance_id` query, optional (integer) — Filter the data with Local Appliance Id. Multiples values are allowed with comma (,) separation.
- `remote_appliance_id` query, optional (integer) — Filter the data with Remote Appliance Id. Multiples values are allowed with comma (,) separation.
- `local_network_interface` query, optional (integer) — Filter the data with Local Wan Interface. Multiples values are allowed with comma (,) separation.
- `remote_network_interface` query, optional (integer) — Filter the data with Remote Wan Interface. Multiples values are allowed with comma (,) separation.
- `page` query, optional (QuerryPage) — next page number for navigation for Application Overview summary UI page used for pagination. Default value is 1 (used if set value is not an integer > 0).
- `size` query, optional (QuerryPageSize) — current page size for Application Overview summary UI page used for pagination. Default value is 20 (used if set value is not an integer > 0).
- `sort` query, optional (string) — The sort field. Sorting can applied on specified column. Sorting can be applied only on one column at a time. Specified column followed by the sorting direction (ie asc or desc) with the comma separation. Allowed columns are application,…
- `flow_direction` query, optional (FlowDirection) — The parameter is used to specify the direction of flow data the user wants to view lan_to_wan or wan_to_lan. Allowed values are lan_to_wan and wan_to_lan and also both as combine as lan_to_wan,wan_to_lan. If no value is provided it is both…

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/sites/{id}/jitter`

Operation: `sitesJitter`

Get jitter evolution for a site

Get jitter evolution for a site.

Tags: `Site 360`

Parameters:

- `id` path, required (integer) — the site id
- `start_time` query, required (integer) — start_time is epoch time in seconds. It represents the start of the time range (start_time - end_time) for which the metrics data for sites will be fetched. Only a single value is allowed.
- `end_time` query, required (integer) — end_time is epoch time in seconds. It represents the end of the time range (start_time - end_time) for which the metrics data for sites will be fetched. Only a single value is allowed.
- `criticality_id` query, optional (integer) — Filter the data with criticality. Multiples values are allowed with comma (,) separation.
- `application_id` query, optional (integer) — Filter the data with Application. Multiples values are allowed with comma (,) separation.
- `application_group_id` query, optional (integer) — Filter the data with application group. Multiples values are allowed with comma (,) separation.
- `dst_site_id` query, optional (integer) — Filter data with Remote Site Id. Multiples values are allowed with comma (,) separation.
- `remote_site_id` query, optional (integer) — Filter data with Remote Site Id. Multiples values are allowed with comma (,) separation.
- `src_network_id` query, optional (integer) — Filter data with Local Network Id. Multiples values are allowed with comma (,) separation.
- `local_network_id` query, optional (integer) — Filter data with Local Network Id. Multiples values are allowed with comma (,) separation.
- `dst_network_id` query, optional (integer) — Filter data with Remote Network Id. Multiples values are allowed with comma (,) separation.
- `remote_network_id` query, optional (integer) — Filter data with Remote Network Id. Multiples values are allowed with comma (,) separation.
- `local_appliance_id` query, optional (integer) — Filter the data with Local Appliance Id. Multiples values are allowed with comma (,) separation.
- `remote_appliance_id` query, optional (integer) — Filter the data with Remote Appliance Id. Multiples values are allowed with comma (,) separation.
- `local_network_interface` query, optional (integer) — Filter the data with Local Wan Interface. Multiples values are allowed with comma (,) separation.
- `remote_network_interface` query, optional (integer) — Filter the data with Remote Wan Interface. Multiples values are allowed with comma (,) separation.
- `flow_direction` query, optional (FlowDirection) — The parameter is used to specify the direction of flow data the user wants to view lan_to_wan or wan_to_lan. Allowed values are lan_to_wan and wan_to_lan and also both as combine as lan_to_wan,wan_to_lan. If no value is provided it is both…

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/sites/{id}/delay-jitter`

Operation: `sitesDelayJitter`

Get TCP delay and jitter evolution for a site

Get TCP delay and jitter evolution for a site.

Tags: `Site 360`

Parameters:

- `id` path, required (integer) — the site id
- `start_time` query, required (integer) — start_time is epoch time in seconds. It represents the start of the time range (start_time - end_time) for which the metrics data for sites will be fetched. Only a single value is allowed.
- `end_time` query, required (integer) — end_time is epoch time in seconds. It represents the end of the time range (start_time - end_time) for which the metrics data for sites will be fetched. Only a single value is allowed.
- `criticality_id` query, optional (integer) — Filter the data with criticality. Multiples values are allowed with comma (,) separation.
- `application_id` query, optional (integer) — Filter the data with Application. Multiples values are allowed with comma (,) separation.
- `application_group_id` query, optional (integer) — Filter the data with application group. Multiples values are allowed with comma (,) separation.
- `dst_site_id` query, optional (integer) — Filter data with Remote Site Id. Multiples values are allowed with comma (,) separation.
- `remote_site_id` query, optional (integer) — Filter data with Remote Site Id. Multiples values are allowed with comma (,) separation.
- `src_network_id` query, optional (integer) — Filter data with Local Network Id. Multiples values are allowed with comma (,) separation.
- `local_network_id` query, optional (integer) — Filter data with Local Network Id. Multiples values are allowed with comma (,) separation.
- `dst_network_id` query, optional (integer) — Filter data with Remote Network Id. Multiples values are allowed with comma (,) separation.
- `remote_network_id` query, optional (integer) — Filter data with Remote Network Id. Multiples values are allowed with comma (,) separation.
- `local_appliance_id` query, optional (integer) — Filter the data with Local Appliance Id. Multiples values are allowed with comma (,) separation.
- `remote_appliance_id` query, optional (integer) — Filter the data with Remote Appliance Id. Multiples values are allowed with comma (,) separation.
- `local_network_interface` query, optional (integer) — Filter the data with Local Wan Interface. Multiples values are allowed with comma (,) separation.
- `remote_network_interface` query, optional (integer) — Filter the data with Remote Wan Interface. Multiples values are allowed with comma (,) separation.
- `flow_direction` query, optional (FlowDirection) — The parameter is used to specify the direction of flow data the user wants to view lan_to_wan or wan_to_lan. Allowed values are lan_to_wan and wan_to_lan and also both as combine as lan_to_wan,wan_to_lan. If no value is provided it is both…

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/sites/{id}/average-sessions`

Operation: `sitesAverageSessions`

Get TCP session evolution for a site

Get average number of TCP session evolution for a site.

Tags: `Site 360`

Parameters:

- `id` path, required (integer) — the site id
- `start_time` query, required (integer) — start_time is epoch time in seconds. It represents the start of the time range (start_time - end_time) for which the metrics data for sites will be fetched. Only a single value is allowed.
- `end_time` query, required (integer) — end_time is epoch time in seconds. It represents the end of the time range (start_time - end_time) for which the metrics data for sites will be fetched. Only a single value is allowed.
- `criticality_id` query, optional (integer) — Filter the data with criticality. Multiples values are allowed with comma (,) separation.
- `application_id` query, optional (integer) — Filter the data with Application. Multiples values are allowed with comma (,) separation.
- `application_group_id` query, optional (integer) — Filter the data with application group. Multiples values are allowed with comma (,) separation.
- `dst_site_id` query, optional (integer) — Filter data with Remote Site Id. Multiples values are allowed with comma (,) separation.
- `remote_site_id` query, optional (integer) — Filter data with Remote Site Id. Multiples values are allowed with comma (,) separation.
- `src_network_id` query, optional (integer) — Filter data with Local Network Id. Multiples values are allowed with comma (,) separation.
- `local_network_id` query, optional (integer) — Filter data with Local Network Id. Multiples values are allowed with comma (,) separation.
- `dst_network_id` query, optional (integer) — Filter data with Remote Network Id. Multiples values are allowed with comma (,) separation.
- `remote_network_id` query, optional (integer) — Filter data with Remote Network Id. Multiples values are allowed with comma (,) separation.
- `local_appliance_id` query, optional (integer) — Filter the data with Local Appliance Id. Multiples values are allowed with comma (,) separation.
- `remote_appliance_id` query, optional (integer) — Filter the data with Remote Appliance Id. Multiples values are allowed with comma (,) separation.
- `local_network_interface` query, optional (integer) — Filter the data with Local Wan Interface. Multiples values are allowed with comma (,) separation.
- `remote_network_interface` query, optional (integer) — Filter the data with Remote Wan Interface. Multiples values are allowed with comma (,) separation.
- `flow_direction` query, optional (FlowDirection) — The parameter is used to specify the direction of flow data the user wants to view lan_to_wan or wan_to_lan. Allowed values are lan_to_wan and wan_to_lan and also both as combine as lan_to_wan,wan_to_lan. If no value is provided it is both…

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/sites/{id}/rtt-srt`

Operation: `sitesRttSrt`

Get TCP RTT and SRT evolution for a site

Get TCP RTT and SRT evolution for a site.

Tags: `Site 360`

Parameters:

- `id` path, required (integer) — the site id.
- `start_time` query, required (integer) — start_time is epoch time in seconds. It represents the start of the time range (start_time - end_time) for which the metrics data for sites will be fetched. Only a single value is allowed.
- `end_time` query, required (integer) — end_time is epoch time in seconds. It represents the end of the time range (start_time - end_time) for which the metrics data for sites will be fetched. Only a single value is allowed.
- `criticality_id` query, optional (integer) — Filter the data with criticality. Multiples values are allowed with comma (,) separation.
- `application_id` query, optional (integer) — Filter the data with Application. Multiples values are allowed with comma (,) separation.
- `application_group_id` query, optional (integer) — Filter the data with application group. Multiples values are allowed with comma (,) separation.
- `dst_site_id` query, optional (integer) — Filter data with Remote Site Id. Multiples values are allowed with comma (,) separation.
- `remote_site_id` query, optional (integer) — Filter data with Remote Site Id. Multiples values are allowed with comma (,) separation.
- `src_network_id` query, optional (integer) — Filter data with Local Network Id. Multiples values are allowed with comma (,) separation.
- `local_network_id` query, optional (integer) — Filter data with Local Network Id. Multiples values are allowed with comma (,) separation.
- `dst_network_id` query, optional (integer) — Filter data with Remote Network Id. Multiples values are allowed with comma (,) separation.
- `remote_network_id` query, optional (integer) — Filter data with Remote Network Id. Multiples values are allowed with comma (,) separation.
- `local_appliance_id` query, optional (integer) — Filter the data with Local Appliance Id. Multiples values are allowed with comma (,) separation.
- `remote_appliance_id` query, optional (integer) — Filter data with Remote Appliance Id. Multiples values are allowed with comma (,) separation.
- `local_network_interface` query, optional (integer) — Filter the data with Local Wan Interface. Multiples values are allowed with comma (,) separation.
- `remote_network_interface` query, optional (integer) — Filter the data with Remote Wan Interface. Multiples values are allowed with comma (,) separation.
- `flow_direction` query, optional (FlowDirection) — The parameter is used to specify the direction of flow data the user wants to view lan_to_wan or wan_to_lan. Allowed values are lan_to_wan and wan_to_lan and also both as combine as lan_to_wan,wan_to_lan. If no value is provided it is both…

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/sites/{id}/throughput`

Operation: `sitesThroughput`

Get the throughput evolution for a site

Get the throughput evolution for a site.

Tags: `Site 360`

Parameters:

- `id` path, required (integer) — the site id.
- `start_time` query, required (integer) — start_time is epoch time in seconds. It represents the start of the time range (start_time - end_time) for which the metrics data for sites will be fetched. Only a single value is allowed.
- `end_time` query, required (integer) — end_time is epoch time in seconds. It represents the end of the time range (start_time - end_time) for which the metrics data for sites will be fetched. Only a single value is allowed.
- `criticality_id` query, optional (integer) — Filter the data with criticality. Multiples values are allowed with comma (,) separation.
- `application_id` query, optional (integer) — Filter the data with Application. Multiples values are allowed with comma (,) separation.
- `application_group_id` query, optional (integer) — Filter the data with application group. Multiples values are allowed with comma (,) separation.
- `dst_site_id` query, optional (integer) — Filter data with Remote Site Id. Multiples values are allowed with comma (,) separation.
- `remote_site_id` query, optional (integer) — Filter data with Remote Site Id. Multiples values are allowed with comma (,) separation.
- `src_network_id` query, optional (integer) — Filter data with Local Network Id. Multiples values are allowed with comma (,) separation.
- `local_network_id` query, optional (integer) — Filter data with Local Network Id. Multiples values are allowed with comma (,) separation.
- `dst_network_id` query, optional (integer) — Filter data with Remote Network Id. Multiples values are allowed with comma (,) separation.
- `remote_network_id` query, optional (integer) — Filter data with Remote Network Id. Multiples values are allowed with comma (,) separation.
- `local_appliance_id` query, optional (integer) — Filter the data with Local Appliance Id. Multiples values are allowed with comma (,) separation.
- `remote_appliance_id` query, optional (integer) — Filter the data with Remote Appliance Id. Multiples values are allowed with comma (,) separation.
- `local_network_interface` query, optional (integer) — Filter the data with Local Wan Interface. Multiples values are allowed with comma (,) separation.
- `remote_network_interface` query, optional (integer) — Filter the data with Remote Wan Interface. Multiples values are allowed with comma (,) separation.
- `flow_direction` query, optional (FlowDirection) — The parameter is used to specify the direction of flow data the user wants to view lan_to_wan or wan_to_lan. Allowed values are lan_to_wan and wan_to_lan and also both as combine as lan_to_wan,wan_to_lan. If no value is provided it is both…

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/sites/{id}/packet-retransmission`

Operation: `sitesPacketRetransmission`

Get TCP packets retransmission

Get TCP packets retransmission evolution for a site.

Tags: `Site 360`

Parameters:

- `id` path, required (integer) — the site id.
- `start_time` query, required (integer) — start_time is epoch time in seconds. It represents the start of the time range (start_time - end_time) for which the metrics data for sites will be fetched. Only a single value is allowed.
- `end_time` query, required (integer) — end_time is epoch time in seconds. It represents the end of the time range (start_time - end_time) for which the metrics data for sites will be fetched. Only a single value is allowed.
- `criticality_id` query, optional (integer) — Filter the data with criticality. Multiples values are allowed with comma (,) separation.
- `application_id` query, optional (integer) — Filter the data with Application. Multiples values are allowed with comma (,) separation.
- `application_group_id` query, optional (integer) — Filter the data with application group. Multiples values are allowed with comma (,) separation.
- `dst_site_id` query, optional (integer) — Filter data with Remote Site Id. Multiples values are allowed with comma (,) separation.
- `remote_site_id` query, optional (integer) — Filter data with Remote Site Id. Multiples values are allowed with comma (,) separation.
- `src_network_id` query, optional (integer) — Filter data with Local Network Id. Multiples values are allowed with comma (,) separation.
- `local_network_id` query, optional (integer) — Filter data with Local Network Id. Multiples values are allowed with comma (,) separation.
- `dst_network_id` query, optional (integer) — Filter data with Remote Network Id. Multiples values are allowed with comma (,) separation.
- `remote_network_id` query, optional (integer) — Filter data with Remote Network Id. Multiples values are allowed with comma (,) separation.
- `local_appliance_id` query, optional (integer) — Filter the data with Local Appliance Id. Multiples values are allowed with comma (,) separation.
- `remote_appliance_id` query, optional (integer) — Filter the data with Remote Appliance Id. Multiples values are allowed with comma (,) separation.
- `local_network_interface` query, optional (integer) — Filter the data with Local Wan Interface. Multiples values are allowed with comma (,) separation.
- `remote_network_interface` query, optional (integer) — Filter the data with Remote Wan Interface. Multiples values are allowed with comma (,) separation.
- `flow_direction` query, optional (FlowDirection) — The parameter is used to specify the direction of flow data the user wants to view lan_to_wan or wan_to_lan. Allowed values are lan_to_wan and wan_to_lan and also both as combine as lan_to_wan,wan_to_lan. If no value is provided it is both…

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/sites/{id}/packet-loss`

Operation: `sitesPacketLoss`

Get TCP packets loss evolution for a site

Get TCP packets loss evolution for a site.

Tags: `Site 360`

Parameters:

- `id` path, required (integer) — the site id
- `start_time` query, required (integer) — start_time is epoch time in seconds. It represents the start of the time range (start_time - end_time) for which the metrics data for sites will be fetched. Only a single value is allowed.
- `end_time` query, required (integer) — end_time is epoch time in seconds. It represents the end of the time range (start_time - end_time) for which the metrics data for sites will be fetched. Only a single value is allowed.
- `criticality_id` query, optional (integer) — Filter the data with criticality. Multiples values are allowed with comma (,) separation.
- `application_id` query, optional (integer) — Filter the data with Application. Multiples values are allowed with comma (,) separation.
- `application_group_id` query, optional (integer) — Filter the data with application group. Multiples values are allowed with comma (,) separation.
- `dst_site_id` query, optional (integer) — Filter data with Remote Site Id. Multiples values are allowed with comma (,) separation.
- `remote_site_id` query, optional (integer) — Filter data with Remote Site Id. Multiples values are allowed with comma (,) separation.
- `src_network_id` query, optional (integer) — Filter data with Local Network Id. Multiples values are allowed with comma (,) separation.
- `local_network_id` query, optional (integer) — Filter data with Local Network Id. Multiples values are allowed with comma (,) separation.
- `dst_network_id` query, optional (integer) — Filter data with Remote Network Id. Multiples values are allowed with comma (,) separation.
- `remote_network_id` query, optional (integer) — Filter data with Remote Network Id. Multiples values are allowed with comma (,) separation.
- `local_appliance_id` query, optional (integer) — Filter the data with Local Appliance Id. Multiples values are allowed with comma (,) separation.
- `remote_appliance_id` query, optional (integer) — Filter the data with Remote Appliance Id. Multiples values are allowed with comma (,) separation.
- `local_network_interface` query, optional (integer) — Filter the data with Local Wan Interface. Multiples values are allowed with comma (,) separation.
- `remote_network_interface` query, optional (integer) — Filter the data with Remote Wan Interface. Multiples values are allowed with comma (,) separation.
- `flow_direction` query, optional (FlowDirection) — The parameter is used to specify the direction of flow data the user wants to view lan_to_wan or wan_to_lan. Allowed values are lan_to_wan and wan_to_lan and also both as combine as lan_to_wan,wan_to_lan. If no value is provided it is both…

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/sites/{id}/eqs`

Operation: `sitesEqs`

Get the EQS evolution for a site

Get the EQS evolution for a site.

Tags: `Site 360`

Parameters:

- `id` path, required (integer) — the site id.
- `start_time` query, required (integer) — start_time is epoch time in seconds. It represents the start of the time range (start_time - end_time) for which the metrics data for sites will be fetched. Only a single value is allowed.
- `end_time` query, required (integer) — end_time is epoch time in seconds. It represents the end of the time range (start_time - end_time) for which the metrics data for sites will be fetched. Only a single value is allowed.
- `criticality_id` query, optional (integer) — Filter the data with criticality. Multiples values are allowed with comma (,) separation.
- `application_id` query, optional (integer) — Filter the data with Application. Multiples values are allowed with comma (,) separation.
- `application_group_id` query, optional (integer) — Filter the data with application group. Multiples values are allowed with comma (,) separation.
- `dst_site_id` query, optional (integer) — Filter data with Remote Site Id. Multiples values are allowed with comma (,) separation.
- `remote_site_id` query, optional (integer) — Filter data with Remote Site Id. Multiples values are allowed with comma (,) separation.
- `src_network_id` query, optional (integer) — Filter data with Local Network Id. Multiples values are allowed with comma (,) separation.
- `local_network_id` query, optional (integer) — Filter data with Local Network Id. Multiples values are allowed with comma (,) separation.
- `dst_network_id` query, optional (integer) — Filter data with Remote Network Id. Multiples values are allowed with comma (,) separation.
- `remote_network_id` query, optional (integer) — Filter data with Remote Network Id. Multiples values are allowed with comma (,) separation.
- `local_appliance_id` query, optional (integer) — Filter the data with Local Appliance Id. Multiples values are allowed with comma (,) separation.
- `remote_appliance_id` query, optional (integer) — Filter the data with Remote Appliance Id. Multiples values are allowed with comma (,) separation.
- `local_network_interface` query, optional (integer) — Filter the data with Local Wan Interface. Multiples values are allowed with comma (,) separation.
- `remote_network_interface` query, optional (integer) — Filter the data with Remote Wan Interface. Multiples values are allowed with comma (,) separation.
- `flow_direction` query, optional (FlowDirection) — The parameter is used to specify the direction of flow data the user wants to view lan_to_wan or wan_to_lan. Allowed values are lan_to_wan and wan_to_lan and also both as combine as lan_to_wan,wan_to_lan. If no value is provided it is both…

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/sites/{id}/delay`

Operation: `sitesDelay`

Get TCP delay evolution for a site

Get TCP delay evolution for a site.

Tags: `Site 360`

Parameters:

- `id` path, required (integer) — the site id
- `start_time` query, required (integer) — start_time is epoch time in seconds. It represents the start of the time range (start_time - end_time) for which the metrics data for sites will be fetched. Only a single value is allowed.
- `end_time` query, required (integer) — end_time is epoch time in seconds. It represents the end of the time range (start_time - end_time) for which the metrics data for sites will be fetched. Only a single value is allowed.
- `criticality_id` query, optional (integer) — Filter the data with criticality. Multiples values are allowed with comma (,) separation.
- `application_id` query, optional (integer) — Filter the data with Application. Multiples values are allowed with comma (,) separation.
- `application_group_id` query, optional (integer) — Filter the data with application group. Multiples values are allowed with comma (,) separation.
- `remote_site_id` query, optional (integer) — Filter data with Remote Site Id. Multiples values are allowed with comma (,) separation.
- `local_network_id` query, optional (integer) — Filter data with Local Network Id. Multiples values are allowed with comma (,) separation.
- `remote_network_id` query, optional (integer) — Filter data with Remote Network Id. Multiples values are allowed with comma (,) separation.
- `local_appliance_id` query, optional (integer) — Filter the data with Local Appliance Id. Multiples values are allowed with comma (,) separation.
- `remote_appliance_id` query, optional (integer) — Filter the data with Remote Appliance Id. Multiples values are allowed with comma (,) separation.
- `local_network_interface` query, optional (integer) — Filter the data with Local Wan Interface. Multiples values are allowed with comma (,) separation.
- `remote_network_interface` query, optional (integer) — Filter the data with Remote Wan Interface. Multiples values are allowed with comma (,) separation.
- `flow_direction` query, optional (FlowDirection) — The parameter is used to specify the direction of flow data the user wants to view lan_to_wan or wan_to_lan. Allowed values are lan_to_wan and wan_to_lan and also both as combine as lan_to_wan,wan_to_lan. If no value is provided it is both…

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/sites/{id}/rtt`

Operation: `sitesRtt`

Get TCP RTT evolution for a site

Get TCP RTT evolution for a site.

Tags: `Site 360`

Parameters:

- `id` path, required (integer) — the site id
- `start_time` query, required (integer) — start_time is epoch time in seconds. It represents the start of the time range (start_time - end_time) for which the metrics data for sites will be fetched. Only a single value is allowed.
- `end_time` query, required (integer) — end_time is epoch time in seconds. It represents the end of the time range (start_time - end_time) for which the metrics data for sites will be fetched. Only a single value is allowed.
- `criticality_id` query, optional (integer) — Filter the data with criticality. Multiples values are allowed with comma (,) separation.
- `application_id` query, optional (integer) — Filter the data with Application. Multiples values are allowed with comma (,) separation.
- `application_group_id` query, optional (integer) — Filter the data with application group. Multiples values are allowed with comma (,) separation.
- `remote_site_id` query, optional (integer) — Filter data with Remote Site Id. Multiples values are allowed with comma (,) separation.
- `local_network_id` query, optional (integer) — Filter data with Local Network Id. Multiples values are allowed with comma (,) separation.
- `remote_network_id` query, optional (integer) — Filter data with Remote Network Id. Multiples values are allowed with comma (,) separation.
- `local_appliance_id` query, optional (integer) — Filter the data with Local Appliance Id. Multiples values are allowed with comma (,) separation.
- `remote_appliance_id` query, optional (integer) — Filter the data with Remote Appliance Id. Multiples values are allowed with comma (,) separation.
- `local_network_interface` query, optional (integer) — Filter the data with Local Wan Interface. Multiples values are allowed with comma (,) separation.
- `remote_network_interface` query, optional (integer) — Filter the data with Remote Wan Interface. Multiples values are allowed with comma (,) separation.
- `flow_direction` query, optional (FlowDirection) — The parameter is used to specify the direction of flow data the user wants to view lan_to_wan or wan_to_lan. Allowed values are lan_to_wan and wan_to_lan and also both as combine as lan_to_wan,wan_to_lan. If no value is provided it is both…

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/sites/{id}/srt`

Operation: `sitesSrt`

Get SRT evolution for a site

Get SRT evolution for a site.

Tags: `Site 360`

Parameters:

- `id` path, required (integer) — the site id
- `start_time` query, required (integer) — start_time is epoch time in seconds. It represents the start of the time range (start_time - end_time) for which the metrics data for sites will be fetched. Only a single value is allowed.
- `end_time` query, required (integer) — end_time is epoch time in seconds. It represents the end of the time range (start_time - end_time) for which the metrics data for sites will be fetched. Only a single value is allowed.
- `criticality_id` query, optional (integer) — Filter the data with criticality. Multiples values are allowed with comma (,) separation.
- `application_id` query, optional (integer) — Filter the data with Application. Multiples values are allowed with comma (,) separation.
- `application_group_id` query, optional (integer) — Filter the data with application group. Multiples values are allowed with comma (,) separation.
- `remote_site_id` query, optional (integer) — Filter data with Remote Site Id. Multiples values are allowed with comma (,) separation.
- `local_network_id` query, optional (integer) — Filter data with Local Network Id. Multiples values are allowed with comma (,) separation.
- `remote_network_id` query, optional (integer) — Filter data with Remote Network Id. Multiples values are allowed with comma (,) separation.
- `local_appliance_id` query, optional (integer) — Filter the data with Local Appliance Id. Multiples values are allowed with comma (,) separation.
- `remote_appliance_id` query, optional (integer) — Filter the data with Remote Appliance Id. Multiples values are allowed with comma (,) separation.
- `local_network_interface` query, optional (integer) — Filter the data with Local Wan Interface. Multiples values are allowed with comma (,) separation.
- `remote_network_interface` query, optional (integer) — Filter the data with Remote Wan Interface. Multiples values are allowed with comma (,) separation.
- `flow_direction` query, optional (FlowDirection) — The parameter is used to specify the direction of flow data the user wants to view lan_to_wan or wan_to_lan. Allowed values are lan_to_wan and wan_to_lan and also both as combine as lan_to_wan,wan_to_lan. If no value is provided it is both…

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/sites/{id}/appliances-wans`

Operation: `site360AppliacesWansInfo`

Get appliances-wans for a site

Get appliances-wans for a site.

Tags: `Site 360`

Parameters:

- `id` path, required (integer) — Site ID
- `start_time` query, required (integer) — Start time is epoch time in seconds. It represents the start of the time range (start - end) from which the appliances-wans will be fetched.
- `end_time` query, required (integer) — End time is epoch time in seconds. It represents the end of the time range (start - end) upto from which the appliances-wans will be fetched.

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/sites/overview/filters`

Operation: `site360ApplicationOverviewFilter`

Get Site 360 Filters API

Get filters API will returns filters available for the site360 Overview .

Tags: `Site 360`

Parameters:

- `site_id` query, optional (integer) — Filter Local WAN Service with site. Multiples values are not allowed.

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/sites/performance/filters`

Operation: `performanceFilters`

Get Site performance Filters API

Get filters API will returns filters available for the Site performance.

Tags: `Site 360`

Parameters:

- `site_id` query, optional (integer) — Filter Local WAN Service with site. Multiples values are not allowed.

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/metrics/wans/throughput`

Operation: `wanServicesThroughput`

Get throughput evolution API

Get throughput evolution API will returns throughput evolution data for each existing Wan Service.

Tags: `WAN 360`

Parameters:

- `start_time` query, required (integer) — (required)start is epoch time in seconds. It represents the start of the time range (start - end) from which the throughput data will be fetched.
- `end_time` query, required (integer) — (required)end is epoch time in seconds. It represents the end of the time range (start - end) upto which the throughput data will be fetched.
- `flow_direction` query, required (FlowDirection) — The parameter is used to specify the direction of flow data the user wants to view lan_to_wan or wan_to_lan. Allowed values are lan_to_wan and wan_to_lan. If no value is provided or an invalid value is provided then error message will be…
- `criticality_id` query, optional (integer) — Filter the data with criticality. Multiple values are allowed with comma (,) separation.
- `application_id` query, optional (integer) — Filter the data with Application. Multiple values are allowed with comma (,) separation.
- `application_group_id` query, optional (integer) — Filter the data with application group. Multiple values are allowed with comma (,) separation.
- `src_site_id` query, optional (integer) — Filter data with Local Site Id. Multiple values are allowed with comma (,) separation.
- `None` , optional
- `dst_site_id` query, optional (integer) — Filter data with Remote Site Id. Multiple values are allowed with comma (,) separation.
- `None` , optional
- `src_appliance_id` query, optional (integer) — Filter the data with local appliance Id. Multiple values are allowed with comma (,) separation.
- `None` , optional
- `dst_appliance_id` query, optional (integer) — Filter the data with remote appliance Id. Multiple values are allowed with comma (,) separation.
- `None` , optional
- `src_network_interface` query, optional (integer) — Filter the data with source wan interface. Multiple values are allowed with comma (,) separation.
- `None` , optional
- `dst_network_interface` query, optional (integer) — Filter the data with destination wan interface. Multiple values are allowed with comma (,) separation.
- `None` , optional
- `src_network_id` query, optional (integer) — Filter data with Local Network Id. Multiple values are allowed with comma (,) separation.
- `None` , optional
- `dst_network_id` query, optional (integer) — Filter data with Remote Network Id. Multiple values are allowed with comma (,) separation.
- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/metrics/wans`

Operation: `wanServicesInfo`

Get Wan Services Informations API

Get wan services state for a customer in a given timerange representing both the LAN to WAN and WAN to LAN direction with weighted average.

Tags: `WAN 360`

Parameters:

- `start_time` query, required (integer) — (required)start is epoch time in seconds. It represents the start of the selected time range (start - end).
- `end_time` query, required (integer) — (required)end is epoch time in seconds. It represents the end of the selected time range (start - end).
- `criticality_id` query, optional (integer) — Filter the data with criticality.Multiples values are allowed with comma (,) separation.
- `application_id` query, optional (integer) — Filter the data with Application.Multiples values are allowed with comma (,) separation.
- `application_group_id` query, optional (integer) — Filter the data with application group.Multiples values are allowed with comma (,) separation.
- `local_site_id` query, optional (integer) — Filter the data with local site Id.Multiples values are allowed with comma (,) separation.
- `remote_site_id` query, optional (integer) — Filter the data with remote Site Id.Multiples values are allowed with comma (,) separation.
- `local_appliance_id` query, optional (integer) — Filter the data with local appliance Id.Multiples values are allowed with comma (,) separation.
- `remote_appliance_id` query, optional (integer) — Filter the data with remote appliance Id.Multiples values are allowed with comma (,) separation.
- `local_network_interface` query, optional (integer) — Filter the data with source wan interface.Multiples values are allowed with comma (,) separation.
- `remote_network_interface` query, optional (integer) — Filter the data with destination wan interface.Multiples values are allowed with comma (,) separation.
- `local_network_id` query, optional (integer) — Filter data with Local Network Id..Multiples values are allowed with comma (,) separation.
- `remote_network_id` query, optional (integer) — Filter data with Remote Network Id.Multiples values are allowed with comma (,) separation.
- `page` query, optional (integer) — next page number used for pagination. Default value is 1 (used if set value is not an integer > 0).
- `size` query, optional (integer) — current page size used for pagination. Default value is 20 (used if set value is not an integer > 0).
- `sort` query, optional (string) — Sorting column used for column sorting, specified column followed by the sorting direction (ie asc or desc) with the comma separation. Allowed columns are network_name,throughput, eqs,…

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/metrics/wans/local/availability`

Operation: `wanLocalAvailability`

Get local availability and EQS API

Get local availability and EQS API will return local availability and EQS data grouped by date time and networks.

Tags: `WAN 360`

Parameters:

- `start_time` query, required (integer) — (required)start time is epoch time in seconds. It represents the start of the time range (start - end) from which the flow data for Eqs will be fetched.
- `end_time` query, required (integer) — (required)end time is epoch time in seconds. It represents the end of the time range (start - end) upto which the flow data for Eqs will be fetched.
- `criticality_id` query, optional (integer) — Filter the data with criticality.Multiples values are allowed with comma (,) separation.
- `application_id` query, optional (integer) — Filter the data with Application.Multiples values are allowed with comma (,) separation.
- `application_group_id` query, optional (integer) — Filter the data with application group.Multiples values are allowed with comma (,) separation.
- `local_site_id` query, optional (integer) — Filter the data with local site Id.Multiples values are allowed with comma (,) separation.
- `remote_site_id` query, optional (integer) — Filter the data with remote Site Id.Multiples values are allowed with comma (,) separation.
- `local_appliance_id` query, optional (integer) — Filter the data with local appliance Id.Multiples values are allowed with comma (,) separation.
- `remote_appliance_id` query, optional (integer) — Filter the data with remote appliance Id.Multiples values are allowed with comma (,) separation.
- `local_network_interface` query, optional (integer) — Filter the data with source wan interface.Multiples values are allowed with comma (,) separation.
- `remote_network_interface` query, optional (integer) — Filter the data with destination wan interface.Multiples values are allowed with comma (,) separation.
- `local_network_id` query, optional (integer) — Filter the data with Local Network Id.Multiples values are allowed with comma (,) separation.
- `remote_network_id` query, optional (integer) — Filter the data with Remote Network Id.Multiples values are allowed with comma (,) separation.

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/metrics/wans/end-end/availability`

Operation: `wanEndAvailability`

Get end to end availabilty and EQS API

Get end to end availabilty and EQS API will return end to end availability and EQS data grouped by date time and networks.

Tags: `WAN 360`

Parameters:

- `start_time` query, required (integer) — (required)start time is epoch time in seconds. It represents the start of the time range (start - end) from which the flow data for Eqs will be fetched.
- `end_time` query, required (integer) — (required)end time is epoch time in seconds. It represents the end of the time range (start - end) upto which the flow data for Eqs will be fetched.
- `criticality_id` query, optional (integer) — Filter the data with criticality.Multiples values are allowed with comma (,) separation.
- `application_id` query, optional (integer) — Filter the data with Application.Multiples values are allowed with comma (,) separation.
- `application_group_id` query, optional (integer) — Filter the data with application group.Multiples values are allowed with comma (,) separation.
- `local_site_id` query, optional (integer) — Filter the data with local site Id.Multiples values are allowed with comma (,) separation.
- `remote_site_id` query, optional (integer) — Filter the data with remote Site Id.Multiples values are allowed with comma (,) separation.
- `local_appliance_id` query, optional (integer) — Filter the data with local appliance Id.Multiples values are allowed with comma (,) separation.
- `remote_appliance_id` query, optional (integer) — Filter the data with remote appliance Id.Multiples values are allowed with comma (,) separation.
- `local_network_interface` query, optional (integer) — Filter the data with source wan interface.Multiples values are allowed with comma (,) separation.
- `remote_network_interface` query, optional (integer) — Filter the data with destination wan interface.Multiples values are allowed with comma (,) separation.
- `local_network_id` query, optional (integer) — Filter the data with Local Network Id.Multiples values are allowed with comma (,) separation.
- `remote_network_id` query, optional (integer) — Filter the data with Remote Network Id.Multiples values are allowed with comma (,) separation.

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/metrics/wans/eqs`

Operation: `wanServicesEqs`

Get EQS evolution API

Get EQS evolution API will returns EQS evolution data for each existing Wan Service.

Tags: `WAN 360`

Parameters:

- `start_time` query, required (integer) — (required)start is epoch time in seconds. It represents the start of the time range (start - end) from which the EQS data will be fetched.
- `end_time` query, required (integer) — (required)end is epoch time in seconds. It represents the end of the time range (start - end) upto which the EQS data will be fetched.
- `flow_direction` query, required (string) — The parameter is used to specify the direction of flow data the user wants to view lan_to_wan or wan_to_lan. Allowed values are lan_to_wan and wan_to_lan. If no value is provided or an invalid value is provided then error message will be…
- `criticality_id` query, optional (integer) — Filter the data with criticality.Multiples values are allowed with comma (,) separation.
- `application_id` query, optional (integer) — Filter the data with Application.Multiples values are allowed with comma (,) separation.
- `application_group_id` query, optional (integer) — Filter the data with application group.Multiples values are allowed with comma (,) separation.
- `local_site_id` query, optional (integer) — Filter the data with local site Id.Multiples values are allowed with comma (,) separation.
- `remote_site_id` query, optional (integer) — Filter the data with remote Site Id.Multiples values are allowed with comma (,) separation.
- `local_appliance_id` query, optional (integer) — Filter the data with local appliance Id.Multiples values are allowed with comma (,) separation.
- `remote_appliance_id` query, optional (integer) — Filter the data with remote appliance Id.Multiples values are allowed with comma (,) separation.
- `local_network_interface` query, optional (integer) — Filter the data with source wan interface.Multiples values are allowed with comma (,) separation.
- `remote_network_interface` query, optional (integer) — Filter the data with destination wan interface.Multiples values are allowed with comma (,) separation.
- `local_network_id` query, optional (integer) — Filter data with Local Network Id..Multiples values are allowed with comma (,) separation.
- `remote_network_id` query, optional (integer) — Filter data with Remote Network Id.Multiples values are allowed with comma (,) separation.

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/wans/filters`

Operation: `wanFiltersServices`

Get Wan Overview Filters API

Get Application overview filters API will returns filters available for the Wan overview .

Tags: `WAN 360`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/appliances/status`

Operation: `getSdwanApplianceStatusList`

Get Appliance Status List

Get Appliance Status List.

Tags: `Appliance 360`

Parameters:

- `id` query, required (array) — Comma separated list of Appliance IDs

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/appliances/{id}/status`

Operation: `getApplianceStatus`

Get Appliance Status

Get Appliance Status.

Tags: `Appliance 360`

Parameters:

- `id` path, required (integer) — ID of the Appliance

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/appliances/{id}/cpu-usage`

Operation: `getApplianceCpuUsage`

Get Appliance CPU Usage

Get Appliance CPU Usage.

Tags: `Appliance 360`

Parameters:

- `id` path, required (integer) — ID of the Appliance.

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/appliances/{id}/fabric-peers`

Operation: `getApplianceFabricPeerStatus`

Get Appliance's Fabric Peer Status

Get the status of an appliance's fabric peer.

Tags: `Appliance 360`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/appliances/{id}/system-usage`

Operation: `getApplianceSystemUsage`

Get Appliance System Usage

Get system usage time-series data. Currently, CPU and memory are available.

Tags: `Appliance 360`

Parameters:

- `id` path, required (integer) — ID of the Appliance.

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/network-analysis/metrics`

Operation: `networkAnalysisMetrics`

Get network analysis metrics

Get network analysis metrics will return traffic metrics related to all the sites and appliances.

Tags: `Dashboard Domain Analysis`

Parameters:

- `start_time` query, required (integer) — start_time is epoch time in seconds. It represents the start of the time range (start_time - end_time) for which the metrics data for sites will be fetched. Only a single value is allowed.
- `end_time` query, required (integer) — end_time is epoch time in seconds. It represents the end of the time range (start_time - end_time) for which the metrics data for sites will be fetched. Only a single value is allowed.
- `flow_direction` query, required (string) — The parameter is used to specify the direction of flow data the user wants to view lan_to_wan or wan_to_lan. Allowed values are lan_to_wan and wan_to_lan. If no value is provided or an invalid value is provided then error message will be…
- `site_id` query, optional (integer) — The parameter is used to filter the traffic data based on site_id(src_site_id/dst_site_id). Multiple comma separated values are allowed.
- `appliance_id` query, optional (integer) — The parameter is used to filter the traffic data based on appliance_id(src_appliance_id/dst_appliance_id). Multiple comma separated values are allowed.
- `page` query, optional (integer) — next page number for navigation for Network Analysis Metrics grid-view. Used for pagination. Default value is 1 (used if set value is not an integer > 0).
- `size` query, optional (integer) — current page size for Network Analysis Metrics grid-view. Used for pagination. Default value is 20 (used if set value is not an integer > 0).
- `sort` query, optional (string) — The sort field. Sorting can be applied on specfied column. Sorting can be applied only on one column at a time. Specified column followed by the sorting direction (ie asc or desc) with the comma separation. Allowed columns are site_name,…

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/network-analysis/summary`

Operation: `networkAnalysisSummary`

Get network analysis summary

Get network analysis summary will return traffic summary related to all the sites and appliances.

Tags: `Dashboard Domain Analysis`

Parameters:

- `start_time` query, required (integer) — start_time is epoch time in seconds. It represents the start of the time range (start_time - end_time) for which the metrics data for sites will be fetched. Only a single value is allowed.
- `end_time` query, required (integer) — end_time is epoch time in seconds. It represents the end of the time range (start_time - end_time) for which the metrics data for sites will be fetched. Only a single value is allowed.
- `flow_direction` query, required (string) — The parameter is used to specify the direction of flow data the user wants to view lan_to_wan or wan_to_lan. Allowed values are lan_to_wan and wan_to_lan. If no value is provided or an invalid value is provided then error message will be…

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/network-analysis/filters`

Operation: `networkAnalysisFilters`

Get network analysis filters

Get network analysis filters to populate the filter panel to filter out specific sites and appliances.

Tags: `Dashboard Domain Analysis`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/network-analysis/ethernet-throughput`

Operation: `ethernetThroughputMetrics`

Get ethernet throughput metrics

Get ethernet throughput metrics will return ethernet throughput metrics aggregated on all the sites and appliances.

Tags: `Dashboard Domain Analysis`

Parameters:

- `start_time` query, required (integer) — start_time is epoch time in seconds. It represents the start of the time range (start_time - end_time) for which the metrics data for sites will be fetched. Only a single value is allowed.
- `end_time` query, required (integer) — end_time is epoch time in seconds. It represents the end of the time range (start_time - end_time) for which the metrics data for sites will be fetched. Only a single value is allowed.
- `flow_direction` query, required (string) — The parameter is used to specify the direction of flow data the user wants to view lan_to_wan or wan_to_lan. Allowed values are lan_to_wan and wan_to_lan. If no value is provided or an invalid value is provided then error message will be…
- `site_id` query, optional (string) — The parameter is used to filter the traffic data based on site_id. Multiple comma separated values are allowed.
- `appliance_id` query, optional (string) — The parameter is used to filter the traffic data based on appliance_id. Multiple comma separated values are allowed.

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/network-analysis/ip-throughput`

Operation: `ipThroughputMetrics`

Get IP throughput metrics

Get IP throughput metrics will return IP throughput metrics aggregated on all the sites and appliances.

Tags: `Dashboard Domain Analysis`

Parameters:

- `start_time` query, required (integer) — start_time is epoch time in seconds. It represents the start of the time range (start_time - end_time) for which the metrics data for sites will be fetched. Only a single value is allowed.
- `end_time` query, required (integer) — end_time is epoch time in seconds. It represents the end of the time range (start_time - end_time) for which the metrics data for sites will be fetched. Only a single value is allowed.
- `flow_direction` query, required (string) — The parameter is used to specify the direction of flow data the user wants to view lan_to_wan or wan_to_lan. Allowed values are lan_to_wan and wan_to_lan. If no value is provided or an invalid value is provided then error message will be…
- `site_id` query, optional (string) — The parameter is used to filter the traffic data based on site_id. Multiple comma separated values are allowed.
- `appliance_id` query, optional (string) — The parameter is used to filter the traffic data based on appliance_id. Multiple comma separated values are allowed.

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## POST `/monitoring/v1/flows/live/sessions`

Operation: `flowsCreateRealTimeMonitoringSession`

Create Real Time Monitoring Session

Create a real time monitoring session for a particular flow.

Tags: `Flows`

Request body:

- `application/json` — RtgCreateSessionRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## POST `/monitoring/v1/flows/live/sessions/create`

Operation: `flowsRealTimeMonitoringSessionCreate`

Create Real Time Monitoring Session

Create a real time monitoring session for a particular flow.

Tags: `Flows`

Request body:

- `application/json` — RtgCreateSessionRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/flows/live/sessions/{id}`

Operation: `flowsGetRealTimeMonitoringSession`

Get Real Time Monitoring data

Get real time data for a existing session.

Tags: `Flows`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## DELETE `/monitoring/v1/flows/live/sessions/{id}`

Operation: `flowsDeleteRealTimeMonitoringSession`

Delete Real Time Monitoring Session

Delete Real Time Monitoring Session.

Tags: `Flows`

Responses:

- `204` — No Content
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## POST `/monitoring/v1/rtg/sessions`

Operation: `rtgCreateRealTimeMonitoringSession`

Create Real Time Monitoring Session

Create a real time monitoring session for a particular flow.

Tags: `RTG`

Request body:

- `application/json` — RtgCreateSessionRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## POST `/monitoring/v1/rtg/sessions/create`

Operation: `rtgRealTimeMonitoringSessionCreate`

Create Real Time Monitoring Session

Create a real time monitoring session for a particular flow.

Tags: `RTG`

Request body:

- `application/json` — RtgCreateSessionRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/monitoring/v1/rtg/sessions/{id}`

Operation: `rtgGetRealTimeMonitoringSession`

Get Real Time Monitoring data

Get real time data for a existing session.

Tags: `RTG`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## DELETE `/monitoring/v1/rtg/sessions/{id}`

Operation: `rtgDeleteRealTimeMonitoringSession`

Delete Real Time Monitoring Session

Delete Real Time Monitoring Session.

Tags: `RTG`

Responses:

- `204` — No Content
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/manage/devices`

Operation: `getSdwanManageableDevices`

Get devices with their configuration status

Returns manageable SD-WAN devices.

Tags: `Appliance Configuration`

Parameters:

- `sort` query, optional (string) — Sorted properties (same as filterable properties)
- `filter` query, optional (string) — Filterable properties: - name - managed - description - model - serial_number - firmware_version - site.name - device_template.name - connectivity.connected - configuration.in_sync - configuration.last_deployed_at - last_updated_at -…

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/manage/devices/{applianceId}`

Operation: `getSdwanManageableDeviceByApplianceId`

Get Device by Appliance Id

Returns manageable SD-WAN device by Appliance Id.

Tags: `Appliance Configuration`

Parameters:

- `None` , optional

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/network-policies/{policyId}/vpn-zones`

Operation: `getVpnZones`

Get VPN Zones

Returns VPN Zones for a network policy.

Tags: `Security Configuration`

Parameters:

- `None` , optional

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## POST `/configuration/v1/network-policies/{policyId}/vpn-zones`

Operation: `addVpnZones`

Add VPN Zones

Add one or more VPN Zones to a network policy.

Tags: `Security Configuration`

Parameters:

- `None` , optional

Request body:

- `application/json` — VpnZoneCreateRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## PUT `/configuration/v1/network-policies/{policyId}/vpn-zones`

Operation: `updateVpnZones`

Update VPN Zones

Update one or more VPN Zones related to a network policy.

Tags: `Security Configuration`

Parameters:

- `None` , optional

Request body:

- `application/json` — VpnZoneUpdateRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## DELETE `/configuration/v1/network-policies/{policyId}/vpn-zones`

Operation: `deleteVpnZones`

Delete VPN Zones

Delete one or more VPN Zones related to a network policy.

Tags: `Security Configuration`

Parameters:

- `None` , optional
- `ids` query, required (array) — IDs of VPN Zones to delete

Responses:

- `204` — No Content
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/network-policies/{policyId}/vpn-zones/{id}`

Operation: `getVpnZone`

Get a VPN Zone

Returns a VPN Zone related to a network policy based on a single ID.

Tags: `Security Configuration`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/network-policies/{policyId}/overlays`

Operation: `getOverlay`

Get Overlay Configuration

Get overlay Configuration.

Tags: `Overlay Configuration`

Parameters:

- `None` , optional
- `sort` query, optional (string) — Sortable properties: - name - description - type
- `filter` query, optional (string) — Filterable properties: - name - description Example: ``` ?filter=name=ilike=Azure ```

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## DELETE `/configuration/v1/network-policies/{policyId}/overlays`

Operation: `deleteOverlay`

Delete Overlay Configuration

Delete Overlay Configuration.

Tags: `Overlay Configuration`

Parameters:

- `ids` query, required (array) — IDs of policies to delete
- `None` , optional

Responses:

- `204` — No Content
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## POST `/configuration/v1/network-policies/{policyId}/overlays/hub-and-spokes`

Operation: `createHubAndSpokeOverlays`

Create Hub and Spoke Overlay Configuration

Create Hub and Spoke Overlay Configuration.

Tags: `Overlay Configuration`

Request body:

- `application/json` — CreateHubAndSpokeOverlay

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## PUT `/configuration/v1/network-policies/{policyId}/overlays/hub-and-spokes`

Operation: `updateHubAndSpokeOverlays`

Update Hub and Spoke Overlay Configuration

Update Hub and Spoke Overlay Configuration.

Tags: `Overlay Configuration`

Request body:

- `application/json` — UpdateHubAndSpokeOverlay

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## POST `/configuration/v1/network-policies/{policyId}/overlays/third-party-vpns`

Operation: `createThirdPartyVpnOverlays`

Create Third Party Vpn Configuration

Create Third Party Vpn Configuration.

Tags: `Overlay Configuration`

Request body:

- `application/json` — CreateThirdPartyVpnOverlay

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## PUT `/configuration/v1/network-policies/{policyId}/overlays/third-party-vpns`

Operation: `updateThirdPartyVpnOverlays`

Update Third Party Vpn Configuration

Update Third Party Vpn Configuration.

Tags: `Overlay Configuration`

Request body:

- `application/json` — UpdateThirdPartyVpnOverlay

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/network-policies/{policyId}/overlays/{id}`

Operation: `getOverlayById`

Get Overlay Configuration by Id

Get overlay Configuration.

Tags: `Overlay Configuration`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/network-policies/{policyId}/overlays/associations`

Operation: `getOverlayWithAssociations`

Get Overlay with Hub/Spoke/WAN Associations

Get overlay configuration with Hubs, Spokes and WANs associated to it.

Tags: `Overlay Configuration`

Parameters:

- `None` , optional
- `sort` query, optional (string) — Sortable properties: - name - description - type
- `filter` query, optional (string) — Filterable properties: - name - description Example: ``` ?filter=name=ilike=Azure ```

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/network-policies/{policyId}/application-performance/application-groups`

Operation: `getApplicationGroups`

Get application groups

Returns application groups for a network policy.

Tags: `Application Performance`

Parameters:

- `None` , optional

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## POST `/configuration/v1/network-policies/{policyId}/application-performance/application-groups`

Operation: `addApplicationGroups`

Create application groups

Add one or more application groups to a network policy.

Tags: `Application Performance`

Parameters:

- `None` , optional

Request body:

- `application/json` — ApplicationGroupsCreateRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## PUT `/configuration/v1/network-policies/{policyId}/application-performance/application-groups`

Operation: `updateApplicationGroups`

Update application groups

Update one or more application groups related to a network policy.

Tags: `Application Performance`

Parameters:

- `None` , optional

Request body:

- `application/json` — ApplicationGroupsUpdateRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## DELETE `/configuration/v1/network-policies/{policyId}/application-performance/application-groups`

Operation: `deleteApplicationGroups`

Delete application groups

Delete one or more application groups related to a network policy.

Tags: `Application Performance`

Parameters:

- `None` , optional
- `ids` query, required (array) — ID of application groups to delete

Responses:

- `204` — No Content
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/network-policies/{policyId}/application-performance/application-groups/{id}`

Operation: `getApplicationGroup`

Get an application group

Returns an application group for a network policy based on a single ID.

Tags: `Application Performance`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/appliances`

Operation: `getOnboardedAppliances`

Get Appliances

Returns List of Appliances by Owner Id.

Tags: `Onboarding`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## POST `/configuration/v1/appliances`

Operation: `onboardAppliances`

Onboard Appliances

Onboard Appliances.

Tags: `Onboarding`

Request body:

- `application/json` — OnboardApplianceRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## DELETE `/configuration/v1/appliances`

Operation: `deleteAppliance`

Trigger deletion of appliances

Delete Appliance.

Tags: `Onboarding`

Parameters:

- `ids` query, required (array) — IDs of Appliances to be deleted

Responses:

- `204` — No Content
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/appliances/{applianceId}`

Operation: `getOnboardedAppliance`

Get Appliance by Appliance Id

Returns Appliance Details.

Tags: `Onboarding`

Parameters:

- `None` , optional

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## PATCH `/configuration/v1/appliances/{applianceId}`

Operation: `patchAppliancesNameAndSerialNumber`

Patch an appliance's name and serial number

Patch an appliance's name.

Tags: `Onboarding`

Parameters:

- `None` , optional

Request body:

- `application/json` — PatchApplianceNameAndSerialNumberRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## POST `/configuration/v1/appliances-csv`

Operation: `onboardAppliancesCsv`

Onboard Appliances by uploading CSV

Upload a comma separated CSV file with headers returns a success and failure counts and lists of devices with counts.

Tags: `Onboarding`

Request body:

- `binary` — OnboardApplianceCsvRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/appliances/serial-number/{serialNumber}`

Operation: `getOnboardedApplianceBySerialNumber`

Get Appliance by Serial Number

Returns Appliance Details.

Tags: `Onboarding`

Parameters:

- `None` , optional

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/templates`

Operation: `getApplianceTemplate`

Get Appliance Template

Get Appliance template.

Tags: `Templates`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## POST `/configuration/v1/templates`

Operation: `createApplianceTemplate`

Create Appliance Template

Create Appliance Template.

Tags: `Templates`

Request body:

- `application/json` — CreateApplianceTemplateRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## PUT `/configuration/v1/templates`

Operation: `updateApplianceTemplate`

Update Appliance Template

Update Appliance Template.

Tags: `Templates`

Request body:

- `application/json` — UpdateApplianceTemplateRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## DELETE `/configuration/v1/templates`

Operation: `deleteApplianceTemplate`

Delete Appliance Template

Delete Appliance Template.

Tags: `Templates`

Parameters:

- `ids` query, required (array) — IDs of policies to delete

Responses:

- `204` — No Content
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/templates/{id}`

Operation: `getApplianceTemplateById`

Get Appliance Template by Id

Get Appliance template.

Tags: `Templates`

Parameters:

- `id` path, required (integer) — ID of the LAN

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/templates/associations`

Operation: `getApplianceTemplateWithAssociations`

Get Templates with Associations

Get templates with appliances associated to it.

Tags: `Templates`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/appliances/{applianceId}/general-settings`

Operation: `getGeneralSettings`

Get general settings of an appliance

Returns general settings for an appliance.

Tags: `Appliance Configuration`

Parameters:

- `None` , optional

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## PUT `/configuration/v1/appliances/{applianceId}/general-settings`

Operation: `updateGeneralSettings`

Update general settings of an appliance

Update general settings of an appliance.

Tags: `Appliance Configuration`

Parameters:

- `None` , optional

Request body:

- `application/json` — DeviceGeneralSettingsUpdateRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## POST `/configuration/v1/appliances/{applianceId}/general-settings/reset-to-template`

Operation: `resetGeneralSettings`

Reset general settings to template default

Returns general settings of an appliance after reset to template default.

Tags: `Appliance Configuration`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/appliances/{applianceId}/lan-settings`

Operation: `getLanSettings`

Get LAN settings of an appliance

Returns the LAN settings for an appliance.

Tags: `Appliance Configuration`

Parameters:

- `None` , optional

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## PUT `/configuration/v1/appliances/{applianceId}/lan-settings`

Operation: `updateLanSettings`

Update LAN settings for an appliance

Update the LAN settings for an appliance.

Tags: `Appliance Configuration`

Parameters:

- `None` , optional

Request body:

- `application/json` — DeviceLanInterfacesUpdateRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## POST `/configuration/v1/appliances/{applianceId}/lan-settings/reset-to-template`

Operation: `resetLanSettings`

Reset LAN settings to template default

Returns the LAN settings of an appliance after reset to template default.

Tags: `Appliance Configuration`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/appliances/{applianceId}/wan-settings`

Operation: `getAllWanSettings`

Get all WAN settings of an appliance

Returns all WAN settings for an appliance.

Tags: `Appliance Configuration`

Parameters:

- `None` , optional

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## POST `/configuration/v1/appliances/{applianceId}/wan-settings/reset-to-template`

Operation: `resetAllWanSettings`

Reset WAN settings to template default

Returns all WAN settings of an appliance after reset to template default.

Tags: `Appliance Configuration`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/appliances/{applianceId}/wan-settings/{name}`

Operation: `getWanSettings`

Get WAN settings of appliance by interface's name

Get WAN settings of an appliances based on the interface's name.

Tags: `Appliance Configuration`

Parameters:

- `None` , optional
- `name` path, required (string) — Name of the WAN Interface

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## PUT `/configuration/v1/appliances/{applianceId}/wan-settings/{name}`

Operation: `updateWanSettings`

Update WAN settings of an appliance WAN settings

Update WAN settings of an appliances based on the interface's name.

Tags: `Appliance Configuration`

Parameters:

- `None` , optional
- `name` path, required (string) — Name of the WAN Interface

Request body:

- `application/json` — WanInterfaceUpdateRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/network-policies`

Operation: `getSdwanPolicy`

Get SD-WAN Policy

Get SD-WAN policy.

Tags: `Policy Configuration`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## POST `/configuration/v1/network-policies`

Operation: `createSdwanPolicy`

Create SD-WAN Policy

Create SD-WAN policy.

Tags: `Policy Configuration`

Request body:

- `application/json` — CreatePolicyRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## PUT `/configuration/v1/network-policies`

Operation: `updateSdwanPolicy`

Update SD-WAN Policy

Update SD-WAN policy.

Tags: `Policy Configuration`

Request body:

- `application/json` — UpdatePolicyRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/network-policies/{id}`

Operation: `getNetworkPolicyById`

Get Network Policy by Id

Returns a Network Policy based on a single ID.

Tags: `Policy Configuration`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/network-policies/active-policy`

Operation: `getActiveSdwanPolicy`

Get Active SD-WAN Policy

Get Active SD-WAN policy.

Tags: `Policy Configuration`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/common-objects/vlans`

Operation: `getVlans`

Get all VLAN

Returns all VLAN.

Tags: `Appliance Configuration`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## POST `/configuration/v1/common-objects/vlans`

Operation: `addVlans`

Add new VLANs

Add one or more VLAN.

Tags: `Appliance Configuration`

Request body:

- `application/json` — CreateApplianceTemplateVlanRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## PUT `/configuration/v1/common-objects/vlans`

Operation: `updateVlans`

Update VLAN

Update one or more VLAN.

Tags: `Appliance Configuration`

Request body:

- `application/json` — UpdateApplianceTemplateVlanRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## DELETE `/configuration/v1/common-objects/vlans`

Operation: `deleteVlans`

Delete VLAN

Delete one or more VLAN.

Tags: `Appliance Configuration`

Parameters:

- `ids` query, required (array) — IDs of VLAN to delete

Responses:

- `204` — No Content
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/common-objects/vlans/{id}`

Operation: `getVlanById`

Get VLAN by Id

Returns a VLAN based on a single ID.

Tags: `Appliance Configuration`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/lans`

Operation: `getLans`

Get all LANs

Returns LANs.

Tags: `Templates`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## POST `/configuration/v1/lans`

Operation: `addLans`

Create new LANs

Add one or more LANs.

Tags: `Templates`

Request body:

- `application/json` — LanCreateRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## PUT `/configuration/v1/lans`

Operation: `updateLans`

Update LANs

Update one or more LANs.

Tags: `Templates`

Request body:

- `application/json` — LanUpdateRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## DELETE `/configuration/v1/lans`

Operation: `deleteLans`

Delete LANs

Delete one or more LANs.

Tags: `Templates`

Parameters:

- `ids` query, required (array) — IDs of LAN to delete

Responses:

- `204` — No Content
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/lans/{id}`

Operation: `getLanById`

Get LAN by Id

Returns a LAN based on a single ID.

Tags: `Templates`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/network-policies/{policyId}/application-performance/transport-networks`

Operation: `getTransportNetworks`

Get transport networks

Returns transport networks for a network policy.

Tags: `Application Performance`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## POST `/configuration/v1/network-policies/{policyId}/application-performance/transport-networks`

Operation: `addTransportNetworks`

Add transport networks

Add one or more transport networks to a network policy.

Tags: `Application Performance`

Request body:

- `application/json` — TransportNetworksCreateRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## PUT `/configuration/v1/network-policies/{policyId}/application-performance/transport-networks`

Operation: `updateTransportNetworks`

Update transport networks

Update one or more transport networks related to a network policy.

Tags: `Application Performance`

Request body:

- `application/json` — TransportNetworksUpdateRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## DELETE `/configuration/v1/network-policies/{policyId}/application-performance/transport-networks`

Operation: `deleteTransportNetworks`

Delete transport networks

Delete one or more transport networks related to a network policy.

Tags: `Application Performance`

Parameters:

- `ids` query, required (array) — ID of transport networks to delete

Responses:

- `204` — No Content
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/network-policies/{policyId}/application-performance/transport-networks/{id}`

Operation: `getTransportNetwork`

Get a transport network

Returns a transport network for a network policy based on a single ID.

Tags: `Application Performance`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/wans`

Operation: `getApplianceTemplateWan`

Get WAN Configuration

Get Appliance template.

Tags: `Templates`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## POST `/configuration/v1/wans`

Operation: `createApplianceTemplateWan`

Create WAN Configuration

Create WAN Configuration.

Tags: `Templates`

Request body:

- `application/json` — CreateApplianceTemplateWanRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## PUT `/configuration/v1/wans`

Operation: `updateApplianceTemplateWan`

Update WAN Configuration

Update WAN Configuration.

Tags: `Templates`

Request body:

- `application/json` — UpdateApplianceTemplateWanRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## DELETE `/configuration/v1/wans`

Operation: `deleteApplianceTemplateWan`

Delete WAN Configuration

Delete WAN Configuration.

Tags: `Templates`

Parameters:

- `ids` query, required (array) — IDs of policies to delete

Responses:

- `204` — No Content
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/wans/{id}`

Operation: `getApplianceTemplateWanById`

Get WAN Configuration by Id

Get Appliance template.

Tags: `Templates`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/sites`

Operation: `getSites`

Get all Sites

Returns a List of sites based on the Owner ID.

Tags: `Onboarding`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/sites/{siteId}`

Operation: `getSite`

Get Site by Site ID

Returns Site Details.

Tags: `Onboarding`

Parameters:

- `None` , optional

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## POST `/configuration/v1/sites/assign-appliances`

Operation: `assignAppliances`

Assign Appliances to Sites

Assign Appliances to Sites.

Tags: `Onboarding`

Request body:

- `application/json` — AssignApplianceRequestWrapper

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/sites/associations`

Operation: `getSitesWithStats`

Get Sites with statistics

Returns a List of sites and some statistics based on the Owner ID.

Tags: `Onboarding`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## POST `/configuration/v1/manage/configuration/validate`

Operation: `validateConfiguration`

Request current configuration validation

Either validate the current configuration and return issues if any or schedule it (when async parameter is set). The system may decide to **delay** validation and return a 202 status.

Tags: `Onboarding`

Parameters:

- `async` query, optional (string) — Mode of validation

Responses:

- `200` — Configuration validated (async=NO or async=AUTO)
- `202` — Configuration validation pending (asynchronous validation triggered, async=AWLAYS or async=AUTO)
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/manage/configuration/validation-status/{snapshotId}`

Operation: `configurationValidationStatus`

Configuration validation status

Get the status of the configuration validation by snapshot ID.

Tags: `Onboarding`

Parameters:

- `snapshotId` path, required (integer) — ID of the deployment snapshot being validated

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## POST `/configuration/v1/manage/configuration/deploy`

Operation: `deployConfiguration`

Validate and deploy Configuration

Trigger configuration validation and deployment, if valid, to the devices. Validation is synchronous.

Tags: `Onboarding`

Responses:

- `202` — Deployment scheduled
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## POST `/configuration/v1/manage/configuration/deploy/{id}`

Operation: `deployConfigurationById`

Deploy pre-validated Configuration by ID

Trigger deployment of a valid configuration snapshot.

Tags: `Onboarding`

Parameters:

- `id` path, required (integer) — ID of the already validated deployment snapshot

Responses:

- `202` — Deployment scheduled
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## POST `/configuration/v1/manage/configuration/async-validation`

Operation: `asyncConfigurationValidation`

Trigger an asynchronous validation

Trigger an asynchronous validation of the current configuration and get the ID of the snapshot.

Tags: `Onboarding`

Responses:

- `202` — Asynchronous validation triggered
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/manage/configuration/async-validation/{snapshotId}`

Operation: `asyncConfigurationValidationResult`

Asynchronous configuration validation result

Get the result of the configuration validation by snapshot ID.

Tags: `Onboarding`

Parameters:

- `snapshotId` path, required (integer) — ID of the deployment snapshot being validated

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/network-policies/{policyId}/vpn-policies`

Operation: `getVpnPolicies`

Get VPN Policies

Returns VPN Policies for a network policy.

Tags: `Security Configuration`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## PUT `/configuration/v1/network-policies/{policyId}/vpn-policies`

Operation: `updateVpnPolicies`

Update VPN Policies

Update one or more VPN Policies related to a network policy.

Tags: `Security Configuration`

Request body:

- `application/json` — VpnPolicyUpdateRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/network-policies/{policyId}/vpn-policies/{id}`

Operation: `getVpnPolicy`

Get a VPN Policy

Returns a VPN Policy related to a network policy based on a single ID.

Tags: `Security Configuration`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/network-policies/{policyId}/port-based-application-sets`

Operation: `getPortBasedApplicationSets`

Get Port Based Application Sets

Returns Port Based Application Sets for a network policy.

Tags: `Security Configuration`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## POST `/configuration/v1/network-policies/{policyId}/port-based-application-sets`

Operation: `createPortBasedApplicationSets`

Create Port Based Application Sets

Create one or more Port Based Application Sets related to a network policy.

Tags: `Security Configuration`

Request body:

- `application/json` — PortBasedApplicationSetCreateRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## PUT `/configuration/v1/network-policies/{policyId}/port-based-application-sets`

Operation: `updatePortBasedApplicationSets`

Port Based Application Sets

Update one or more Port Based Application Sets related to a network policy.

Tags: `Security Configuration`

Request body:

- `application/json` — PortBasedApplicationSetUpdateRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## DELETE `/configuration/v1/network-policies/{policyId}/port-based-application-sets`

Operation: `deletePortBasedApplicationSets`

Delete Port Based Application Sets

Delete one or more Port Based Application set(s) related to a network policy.

Tags: `Security Configuration`

Parameters:

- `ids` query, required (array) — ID of Port Based Application sets to delete

Responses:

- `204` — No Content
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/network-policies/{policyId}/port-based-application-sets/{id}`

Operation: `getPortBasedApplicationSet`

Get a Port Based Application Set

Returns a Port Based Application set related to a network policy based on a single ID.

Tags: `Security Configuration`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/network-policies/{policyId}/internet-access-policies`

Operation: `getInternetAccessPolicies`

Get Internet Access Policies

Returns Internet Access Policies for a network policy.

Tags: `Security Configuration`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## PUT `/configuration/v1/network-policies/{policyId}/internet-access-policies`

Operation: `updateInternetAccessPolicies`

Update Internet Access Policies

Update one or more Internet Access Policies related to a network policy.

Tags: `Security Configuration`

Request body:

- `application/json` — InternetAccessPolicyUpdateRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/network-policies/{policyId}/internet-access-policies/{id}`

Operation: `getInternetAccessPolicy`

Get a Internet Access Policy

Returns a Internet Access Policy related to a network policy based on a single ID.

Tags: `Security Configuration`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/network-policies/{policyId}/saas-application-sets`

Operation: `getSaasApplicationSets`

Get Saas Application Sets

Returns Saas Application Sets for a network policy.

Tags: `Security Configuration`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## POST `/configuration/v1/network-policies/{policyId}/saas-application-sets`

Operation: `createSaasApplicationSets`

Saas Application Sets

Create one or more Saas Application Sets related to a network policy.

Tags: `Security Configuration`

Request body:

- `application/json` — SaasApplicationSetCreateRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## PUT `/configuration/v1/network-policies/{policyId}/saas-application-sets`

Operation: `updateSaasApplicationSets`

Saas Application Sets

Update one or more Saas Application Sets related to a network policy.

Tags: `Security Configuration`

Request body:

- `application/json` — SaasApplicationSetUpdateRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## DELETE `/configuration/v1/network-policies/{policyId}/saas-application-sets`

Operation: `deleteSaaApplicationSets`

Delete Saas Application Sets

Delete one or more saas application set(s) related to a network policy.

Tags: `Security Configuration`

Parameters:

- `ids` query, required (array) — ID of saas application sets to delete

Responses:

- `204` — No Content
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/network-policies/{policyId}/saas-application-sets/{id}`

Operation: `getSaasApplicationSet`

Get a Saas Application Set

Returns a Saas application set related to a network policy based on a single ID.

Tags: `Security Configuration`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/network-policies/{policyId}/secure-web-gateways`

Operation: `getSecureWebGateway`

Get Secure Web Gateway

Returns a detailed list of Secure Web Gateway.

Tags: `Security Configuration`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## POST `/configuration/v1/network-policies/{policyId}/secure-web-gateways`

Operation: `createSecureWebGateway`

Create Secure Web Gateway

Secure Web Gateway.

Tags: `Security Configuration`

Request body:

- `application/json` — CreateSecureWebGateway

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## PUT `/configuration/v1/network-policies/{policyId}/secure-web-gateways`

Operation: `updateSecureWebGateway`

Update Secure Web Gateway

Update Secure Web Gateway.

Tags: `Security Configuration`

Request body:

- `application/json` — UpdateSecureWebGateway

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## DELETE `/configuration/v1/network-policies/{policyId}/secure-web-gateways`

Operation: `deleteSecureWebGateway`

Delete Secure Web Gateway

Delete Secure Web Gateway.

Tags: `Security Configuration`

Parameters:

- `ids` query, required (array) — IDs of Secure Web Gateway to delete

Responses:

- `204` — No Content
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/network-policies/{policyId}/secure-web-gateways/{id}`

Operation: `getSecureWebGatewayById`

Get Secure Web Gateway by secure web gateway id

Returns Secure Web Gateway details.

Tags: `Security Configuration`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/vpn-sites`

Operation: `getVpnSites`

Get all User Sites

Returns list of User Sites (physical and RVC). If criteria value 'notAssignedToVpnZone' is provided then already used vpn sites will be filtered out.

Tags: `Security Configuration`

Parameters:

- `criteria` query, optional (string) — if criteria value 'notAssignedToVpnZone' is provided then already used vpn sites will be filtered out

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/vpn-sites/{siteId}`

Operation: `getVpnSiteById`

Get any User Site by ID

Returns Site Details.

Tags: `Security Configuration`

Parameters:

- `None` , optional

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/network-policies/{policyId}/application-performance/applications`

Operation: `getApplications`

Get applications

Returns applications for a network policy.

Tags: `Application Performance`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## POST `/configuration/v1/network-policies/{policyId}/application-performance/applications`

Operation: `addApplications`

Add applications

Add one or more applications to a network policy.

Tags: `Application Performance`

Request body:

- `application/json` — ApplicationsCreateRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## PUT `/configuration/v1/network-policies/{policyId}/application-performance/applications`

Operation: `updateApplications`

Update applications

Update one or more applications related to a network policy.

Tags: `Application Performance`

Request body:

- `application/json` — ApplicationsUpdateRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## DELETE `/configuration/v1/network-policies/{policyId}/application-performance/applications`

Operation: `deleteApplications`

Delete applications

Delete one or more applications related to a network policy.

Tags: `Application Performance`

Parameters:

- `ids` query, required (array) — ID of applications to delete

Responses:

- `204` — No Content
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/network-policies/{policyId}/application-performance/applications/{id}`

Operation: `getApplication`

Get an application

Returns an application for a network policy based on a single ID.

Tags: `Application Performance`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/network-policies/{policyId}/application-performance/applications/inventory`

Operation: `getApplicationsInventory`

Get applications inventory

Returns applications for a network policy base on query parameter.

Tags: `Application Performance`

Parameters:

- `groupHeader` query, optional (string) — Based on this parameter 'application_count' is calculated. Lets say, groupHeader is 'protocol.family' then 'application_count is the number of applications under this protocol family. Value can be any one of protocol.name or protocol.family
- `filter` query, optional (string) — Applications are filtered based on this parameter. Filter keys can be: - protocol.name - protocol.family - application_groups.name Example: ``` filter=protocol.name=="HTTPS (HTTP Secure)" filter=protocol.family="Mail Service"…

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/network-policies/{policyId}/application-performance/saas-applications`

Operation: `getSaasApplications`

Get SaaS Applications

Returns SaaS applications for a network policy.

Tags: `Application Performance`

Parameters:

- `filter` query, optional (string) — SaaS applications are filtered based on this parameter. Filter keys can be: - application_groups.name - application_sets.name Example: ``` filter=application_groups.name=="Mail Service" filter=application_sets.name=="SaaS Application Set"…

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## POST `/configuration/v1/network-policies/{policyId}/application-performance/saas-applications`

Operation: `addSaasApplications`

Create SaaS Applications

Add SaaS Applications.

Tags: `Application Performance`

Request body:

- `application/json` — SaasApplicationsCreateRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## PUT `/configuration/v1/network-policies/{policyId}/application-performance/saas-applications`

Operation: `updateSaasApplications`

Update SaaS applications

Update one or more SaaS applications related to a network policy.

Tags: `Application Performance`

Request body:

- `application/json` — SaasApplicationsUpdateRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## DELETE `/configuration/v1/network-policies/{policyId}/application-performance/saas-applications`

Operation: `deleteSaasApplications`

Delete SaaS Applications

Delete one or more applications related to a network policy.

Tags: `Application Performance`

Parameters:

- `ids` query, required (array) — ID of applications to delete

Responses:

- `204` — No Content
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/network-policies/{policyId}/application-performance/saas-applications/{id}`

Operation: `getSaasApplication`

Get a SaaS Application by ID

Returns an SaaS Application based on a single ID.

Tags: `Application Performance`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/network-policies/{policyId}/application-performance/qos-profiles`

Operation: `getQosProfiles`

Get QoS profiles

Returns QoS profiles for a network policy.

Tags: `Application Performance`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## POST `/configuration/v1/network-policies/{policyId}/application-performance/qos-profiles`

Operation: `addQosProfiles`

Add QoS profiles

Add one or more QoS profiles to a network policy.

Tags: `Application Performance`

Request body:

- `application/json` — QosProfilesCreateRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## PUT `/configuration/v1/network-policies/{policyId}/application-performance/qos-profiles`

Operation: `updateQosProfiles`

Update QoS profiles

Update one or more QoS profiles related to a network policy.

Tags: `Application Performance`

Request body:

- `application/json` — QosProfilesUpdateRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## DELETE `/configuration/v1/network-policies/{policyId}/application-performance/qos-profiles`

Operation: `deleteQosProfiles`

Delete QoS profiles

Delete one or more QoS profiles related to a network policy.

Tags: `Application Performance`

Parameters:

- `ids` query, required (array) — ID of QoS profiles to delete

Responses:

- `204` — No Content
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/network-policies/{policyId}/application-performance/qos-profiles/{id}`

Operation: `getQosProfile`

Get a QoS profile

Returns a QoS profile for a network policy based on a single ID.

Tags: `Application Performance`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/network-policies/{policyId}/application-performance/dws-policies`

Operation: `getDwsPolicies`

Get DWS policies

Returns DWS policies for a network policy.

Tags: `Application Performance`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## POST `/configuration/v1/network-policies/{policyId}/application-performance/dws-policies`

Operation: `addDwsPolicies`

Add DWS policies

Add one or more custom DWS policies to a network policy.

Tags: `Application Performance`

Request body:

- `application/json` — DwsPoliciesCreateRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## PUT `/configuration/v1/network-policies/{policyId}/application-performance/dws-policies`

Operation: `updateDwsPolicies`

Update DWS policies

Update one or more custom DWS policies related to a network policy.

Tags: `Application Performance`

Request body:

- `application/json` — DwsPoliciesUpdateRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## DELETE `/configuration/v1/network-policies/{policyId}/application-performance/dws-policies`

Operation: `deleteDwsPolicies`

Delete DWS policies

Delete one or more custom DWS policies related to a network policy.

Tags: `Application Performance`

Parameters:

- `ids` query, required (array) — ID of DWS policies to delete

Responses:

- `204` — No Content
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/network-policies/{policyId}/application-performance/dws-policies/{id}`

Operation: `getDwsPolicy`

Get a DWS policy

Returns a DWS policy for a network policy based on a single ID.

Tags: `Application Performance`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/appliances/fabric-settings`

Operation: `getAllFabricAppliances`

Get all configured fabric appliances

Returns all configured fabric appliances.

Tags: `Appliance Configuration`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## PUT `/configuration/v1/appliances/fabric-settings`

Operation: `updateFabricAppliances`

Configured fabric appliances

Returns all configured fabric appliances.

Tags: `Appliance Configuration`

Request body:

- `application/json` — FabricDeviceRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/common-objects/dhcp-services`

Operation: `getDhcpServices`

Get all DHCP Services

Returns all DHCP Services.

Tags: `Appliance Configuration`

Parameters:

- `sort` query, optional (string) — Sorted properties (same as filterable properties)
- `filter` query, optional (string) — Filterable properties: - name - description - role - primary_server - secondary_server - dns_servers - dns_domain_name - lease_time Example: ``` ?filter=role=ilike=SERVER ```

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## POST `/configuration/v1/common-objects/dhcp-services`

Operation: `addDhcpServices`

Add DHCP Service

Add one or more DHCP services.

Tags: `Appliance Configuration`

Request body:

- `application/json` — DhcpServiceCreateRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## PUT `/configuration/v1/common-objects/dhcp-services`

Operation: `updateDhcpServices`

Update DHCP Services

Update one or more DHCP Services.

Tags: `Appliance Configuration`

Request body:

- `application/json` — DhcpServiceUpdateRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## DELETE `/configuration/v1/common-objects/dhcp-services`

Operation: `deleteDhcpServices`

Delete DHCP Services

Delete one or more DHCP Services.

Tags: `Appliance Configuration`

Parameters:

- `ids` query, required (array) — IDs of DHCP Service to delete

Responses:

- `204` — No Content
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/common-objects/dhcp-services/{id}`

Operation: `getDhcpServiceById`

Get DHCP Service by Id

Returns a DHCP Service based on a single ID.

Tags: `Appliance Configuration`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/appliances/{applianceId}/available-bgp-peer-appliances`

Operation: `getAllBgpPeerAvailable`

Get all BGP peer appliances of an appliance

Returns all BGP peer appliances available for an appliance.

Tags: `Appliance Configuration`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/network-policies/{policyId}/application-performance/ihap-profiles`

Operation: `getIhapProfiles`

Get all IHAP Profiles

Returns all IHAP Profiles.

Tags: `Application Performance`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## POST `/configuration/v1/network-policies/{policyId}/application-performance/ihap-profiles`

Operation: `addIhapProfiles`

Add IHAP Profile

Add one or more IHAP Profiles.

Tags: `Application Performance`

Request body:

- `application/json` — IhapProfileCreateRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## PUT `/configuration/v1/network-policies/{policyId}/application-performance/ihap-profiles`

Operation: `updateIhapProfiles`

Update IHAP Profiles

Update one or more IHAP Profiles.

Tags: `Application Performance`

Request body:

- `application/json` — IhapProfileUpdateRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## DELETE `/configuration/v1/network-policies/{policyId}/application-performance/ihap-profiles`

Operation: `deleteIhapProfiles`

Delete IHAP Profiles

Delete one or more IHAP Profiles.

Tags: `Application Performance`

Parameters:

- `ids` query, required (array) — IDs of IHAP Profile to delete

Responses:

- `204` — No Content
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/network-policies/{policyId}/application-performance/ihap-profiles/{id}`

Operation: `getIhapProfileById`

Get IHAP Profile by Id

Returns a IHAP Profile based on a single ID.

Tags: `Application Performance`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/network-policies/{policyId}/application-performance/vrrp-profiles`

Operation: `getVrrpProfiles`

Get all VRRP Profiles

Returns all VRRP Profiles.

Tags: `Application Performance`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## POST `/configuration/v1/network-policies/{policyId}/application-performance/vrrp-profiles`

Operation: `addVrrpProfiles`

Add VRRP Profile

Add one or more VRRP Profiles.

Tags: `Application Performance`

Request body:

- `application/json` — VrrpProfileCreateRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## PUT `/configuration/v1/network-policies/{policyId}/application-performance/vrrp-profiles`

Operation: `updateVrrpProfiles`

Update VRRP Profiles

Update one or more VRRP Profiles.

Tags: `Application Performance`

Request body:

- `application/json` — VrrpProfileUpdateRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## DELETE `/configuration/v1/network-policies/{policyId}/application-performance/vrrp-profiles`

Operation: `deleteVrrpProfiles`

Delete VRRP Profiles

Delete one or more VRRP Profiles.

Tags: `Application Performance`

Parameters:

- `ids` query, required (array) — IDs of VRRP Profile to delete

Responses:

- `204` — No Content
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/network-policies/{policyId}/application-performance/vrrp-profiles/{id}`

Operation: `getVrrpProfileById`

Get VRRP Profile by Id

Returns a VRRP Profile based on a single ID.

Tags: `Application Performance`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/network-policies/{policyId}/application-performance/vrrp-profiles/associations`

Operation: `getVrrpProfileAssociations`

Get VRRP Profile Associations

Returns appliances associated with a VRRP Profile.

Tags: `Application Performance`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/appliances/{applianceId}/wan-settings/connections`

Operation: `getDeviceExternalConnections`

Get WAN External Connections

Returns WAN External Connections.

Tags: `Appliance Configuration`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/appliances/{applianceId}/wan-settings/{name}/connections`

Operation: `getDeviceExternalConnectionsByName`

Get WAN External Connections By Wan Name

Returns WAN External Connections By Name of Wan.

Tags: `Appliance Configuration`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/appliances/{applianceId}/wan-settings/{name}/connections/hub-and-spoke-synthesis`

Operation: `getWanHubSpokeConnectionsCount`

Get WAN Hub and Spoke Connections Synthesis

Returns WAN Hub and Spoke Connections Synthesis.

Tags: `Appliance Configuration`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/appliances/{applianceId}/wan-settings/{name}/connections/{type}`

Operation: `getDeviceExternalConnectionsByType`

Get WAN External Connections By Type

Returns WAN External Connections By Type.

Tags: `Appliance Configuration`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/appliances/{applianceId}/wan-settings/{name}/available-site-to-site-endpoints`

Operation: `getDeviceWanRemoteEndpoints`

Get Available Remote Site to Site Endpoints

Get Available Remote Site to Site Endpoints.

Tags: `Appliance Configuration`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/sites/{siteId}/appliances`

Operation: `getApplianceBySite`

Get appliances by Site ID

Returns appliances for a site.

Tags: `Appliance Configuration`

Parameters:

- `None` , optional

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/common-objects/protocols`

Operation: `getProtocols`

Get protocols

Returns the protocols available.

Tags: `Appliance Configuration`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/common-objects/protocols/{id}`

Operation: `getProtocolById`

Get Protocol by Id

Returns a Protocol based on a single ID.

Tags: `Appliance Configuration`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/network-policies/{policyId}/routing/settings`

Operation: `getRoutingSettings`

Get routing settings

Returns routing settings for a network policy.

Tags: `Policy Configuration`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## PUT `/configuration/v1/network-policies/{policyId}/routing/settings`

Operation: `updateRoutingSettings`

Update routing settings

Update routing settings related to a network policy.

Tags: `Policy Configuration`

Request body:

- `application/json` — RoutingSettingsRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/network-policies/{policyId}/routing/settings/{id}`

Operation: `getRoutingSettingsById`

Get a routing settings

Returns the routing settings for a network policy based on a single ID.

Tags: `Policy Configuration`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/policy-advanced-settings`

Operation: `getAdvancedSettings`

Get advanced settings

Get advanced settings of a policy.

Tags: `Policy Configuration`

Parameters:

- `sort` query, optional (string) — Sorted properties (same as filterable properties)
- `filter` query, optional (string) — Filterable properties: - key - value Example: ``` ?filter=key=="monitor_disk" ```

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## POST `/configuration/v1/policy-advanced-settings`

Operation: `createAdvancedSettings`

Create advanced settings

Create advanced settings of a policy.

Tags: `Policy Configuration`

Request body:

- `application/json` — PolicyAdvancedSettingsCreateRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## PUT `/configuration/v1/policy-advanced-settings`

Operation: `updateAdvancedSettings`

Update advanced settings

Update advanced settings of a policy.

Tags: `Policy Configuration`

Request body:

- `application/json` — PolicyAdvancedSettingsUpdateRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## DELETE `/configuration/v1/policy-advanced-settings`

Operation: `deleteAdvancedSettings`

Delete advanced settings

Delete advanced settings of a policy.

Tags: `Policy Configuration`

Parameters:

- `ids` query, required (array) — IDs of advanced settings of a policy to delete

Responses:

- `204` — No Content
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/policy-advanced-settings/{id}`

Operation: `getAdvancedSettingsById`

Get an advanced settings

Return an advanced settings of a policy based on a single ID.

Tags: `Policy Configuration`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/rvc-destinations`

Operation: `getRvcDestinations`

Get RVC destinations

Returns RVC destinations.

Tags: `RVC Configuration`

Parameters:

- `sort` query, optional (string) — Sortable properties: - name - access_bandwidth_up - access_bandwidth_down - state
- `filter` query, optional (string) — Filterable properties: - name - description - access_bandwidth_up - access_bandwidth_down - subnets.subnet - wan_service.name - overlays.name - state Example: ``` ?filter=name=ilike=Internet ```

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## POST `/configuration/v1/rvc-destinations`

Operation: `addRvcDestinations`

Add RVC destinations

Add one or more custom RVC destination.

Tags: `RVC Configuration`

Request body:

- `application/json` — RvcDestinationsCreateRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## PUT `/configuration/v1/rvc-destinations`

Operation: `updateRvcDestinations`

Update RVC destinations

Update one or more custom RVC destinations.

Tags: `RVC Configuration`

Request body:

- `application/json` — RvcDestinationsUpdateRequest

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## DELETE `/configuration/v1/rvc-destinations`

Operation: `deleteRvcDestinations`

Delete RVC Destinations

Delete one or more custom RVC destinations.

Tags: `RVC Configuration`

Parameters:

- `ids` query, required (array) — IDs of RVC destinations to delete

Responses:

- `204` — No Content
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/rvc-destinations/{id}`

Operation: `getRvcDestination`

Get a RVC destination

Returns a RVC destination based on a single ID.

Tags: `RVC Configuration`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/saas-catalog`

Operation: `getSaasCatalog`

Get SaaS catalog

Returns SaaS catalog.

Tags: `SaaS Configuration`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/configuration/v1/saas-catalog/info`

Operation: `getSaasCatalogInfo`

Get SaaS catalog info

Returns SaaS catalog meta information.

Tags: `SaaS Configuration`

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/tools/v1/upgrade/catalog`

Operation: `getFirmware`

Firmware catalog

Retrieve available versions of Appliance firmware; pagination is not applied as data is obtained runtime from catalog file on firmware server.

Tags: `Onboarding`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## POST `/tools/v1/upgrade/activate`

Operation: `postUpgrade`

Activate upgrade

Request Appliance(s) for upgrade to specified firmware at given schedule.

Tags: `Onboarding`

Request body:

- `application/json` — UpgradeRequestData

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/tools/v1/upgrade/status`

Operation: `getUpgrade`

Upgrade status

Retrieve status of firmware upgrade on Appliance(s).

Tags: `Onboarding`

Parameters:

- `request_id` query, optional (string) — List of request id(s)
- `serial_number` query, optional (string) — List of serial number(s)
- `page` query, optional (integer) — Page number (default 0)
- `size` query, optional (integer) — Page size (default 20)

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## DELETE `/tools/v1/upgrade/cancel`

Operation: `cancelUpgrade`

Cancel a scheduled upgrade

Cancel a scheduled upgrade.

Tags: `Onboarding`

Request body:

- `application/json` — CancelScheduledUpgradeRequestData

Responses:

- `204` — No Content
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## POST `/tools/v1/troubleshooting/start`

Operation: `troubleshootstart`

Start Appliance troubleshooting

Start Appliance troubleshooting.

Tags: `Troubleshooting`

Request body:

- `application/json` — TroubleshootRequest

Responses:

- `202` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/tools/v1/troubleshooting/stats`

Operation: `troubleshootstats`

Appliance troubleshooting stats

Get Appliance troubleshooting stats.

Tags: `Troubleshooting`

Parameters:

- `request_id` query, required (string) — This id is unique id for a request to fetch troubleshooting data for an appliance.
- `serial_number` query, required (string) — Serial number is unique identity for an appliance.

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/tools/v1/troubleshooting/graph`

Operation: `troubleshootgraph`

Appliance troubleshooting graph

Get Appliance troubleshooting graph.

Tags: `Troubleshooting`

Parameters:

- `request_id` query, required (string) — This id is unique id for a request to fetch troubleshooting data for an appliance.
- `serial_number` query, required (string) — Serial number is unique identity for an appliance.

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## POST `/tools/v1/troubleshooting/stop/{request_id}`

Operation: `troubleshootstop`

Stop Appliance troubleshooting

Stop Appliance troubleshooting.

Tags: `Troubleshooting`

Request body:

- `application/json` — TroubleshootRequest

Responses:

- `204` — No Content
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/tools/v1/scripts/catalog`

Operation: `appliancescripts`

Get scripts catalog

Get list of available scripts.

Tags: `Scripts`

Parameters:

- `page` query, optional (integer) — The page field for the pagination, by default value is set to 0
- `size` query, optional (integer) — The size field for the pagination , default size is 20.

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## POST `/tools/v1/scripts/execute/{script_name}`

Operation: `toolsRunScript`

Run a script

API to run a script.

Tags: `Scripts`

Parameters:

- `script_name` path, required (string) — Name of the script

Request body:

- `application/json` — ExecuteScriptRequest

Responses:

- `202` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/tools/v1/scripts/status`

Operation: `getScriptStatus`

Get script status

Returns the result from appliance.

Tags: `Scripts`

Parameters:

- `request_id` query, optional (string) — This id is unique id for any request for execute script command sent by the user.
- `page` query, optional (integer) — The page field for the pagination, by default value is set to 0
- `size` query, optional (integer) — The size field for the pagination. Default size is 20.

Responses:

- `200` — Success
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/tools/v1/scripts/result`

Operation: `scriptsresult`

Get script result(s)

Get script responses received from appliance.

Tags: `Scripts`

Parameters:

- `request_id` query, optional (string) — This id is unique id for any request for execute script command sent by the user.
- `page` query, optional (integer) — The page field for the pagination, by default value is set to 0
- `size` query, optional (integer) — The size field for the pagination. Default size is 20.
- `sort` query, optional (array) — contains combination of sorting key and ASC or DESC orders. As of now supporting only two columns script_name & created_at.

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## POST `/tools/v1/scripts/result/delete`

Operation: `deleteApplianceResult`

Delete result(s)

Delete Appliance result.

Tags: `Scripts`

Request body:

- `application/json` — DeleteResultRequest

Responses:

- `204` — No Content
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/tools/v1/scripts/result/download`

Operation: `scriptsResultDownload`

Download script result

Download script results received from appliance.

Tags: `Scripts`

Parameters:

- `file_path` query, required (string) — This is the location of the Result file.

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/system/v1/audit/records`

Operation: `getAuditRecords`

Get All Audit Records

The get audit records operation will return all audit records related to events and user actions performed in the orchestrator.

Tags: `Audit`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/system/v1/audit/records/{id}`

Operation: `getAuditRecordDetails`

Get Audit Record Details

This operation retrieves a comprehensive audit record containing detailed information.

Tags: `Audit`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/system/v1/audit/filters`

Operation: `getAuditRecordFilters`

Get Audit Record Filters

This operation retrieves all the filters for audit records.

Tags: `Audit`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## POST `/reporting/v1/reports/config`

Operation: `createConfig`

Create report API

create-report API is to create report configs.

Tags: `Reports`

Request body:

- `application/json` — CreateReportConfigReq

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/reporting/v1/reports`

Operation: `generatedReportList`

Get all report configs with generated report list

Get report-widgets api will returns data related to generated reports used for report list grid view.

Tags: `Reports`

Parameters:

- `page` query, optional (integer) — The page field for the pagination. Default value is 1 (used if set value is not an integer > 0).
- `size` query, optional (integer) — The size field for the pagiantion. Default value is 20 (used if set value is not an integer > 0).
- `sort` query, optional (string) — The sort field. Sorting can applied on specfied column. Specified column followed by the sorting direction (ie asc or desc) with the comma separation. By default sort applied on field 'updatedAt'

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## DELETE `/reporting/v1/reports`

Operation: `removeReports`

Delete Report/Reports

Delete Report/Reports.

Tags: `Reports`

Parameters:

- `config_id` query, optional (integer) — Report config id which needs to be deleted. For multi-delete, multiple query parameters can be passed.
- `report_id` query, optional (integer) — Report id which needs to be deleted. For multi-delete, multiple query parameters can be passed.

Responses:

- `204` — No Content
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## PUT `/reporting/v1/reports/{config_id}`

Operation: `updateReport`

Put update report config API

Put update config API is to update report configs.

Tags: `Reports`

Parameters:

- `config_id` path, required (integer) — Report config id which needs to be updated.

Request body:

- `application/json` — UpdateReportConfigReq

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/reporting/v1/reports/{report_id}/download`

Operation: `downloadData`

download report

This API is to download generated PDF report. The Report will be in zip format.

Tags: `Reports`

Parameters:

- `report_id` path, required (integer) — Report id which needs be passed to download the report.

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/reporting/v1/reports/components`

Operation: `reportComponents`

Report Widget list API

Get report-widgets api will returns widgets.

Tags: `Reports`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/reporting/v1/reports/templates`

Operation: `templateList`

Template List API

Get Template-List api will returns list of templates.

Tags: `Reports`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## POST `/reporting/v1/reports/templates`

Operation: `saveTemplate`

Save template API

save-template API is to save report template.

Tags: `Reports`

Request body:

- `application/json` — SaveReportTemplateReq

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## DELETE `/reporting/v1/reports/templates`

Operation: `deleteTemplateList`

Template Delete API

Delete Template api will delete list of templates.

Tags: `Reports`

Parameters:

- `template_id` query, optional (integer) — Report template id which needs to be deleted. For multi-delete, multiple query parameters can be passed.

Responses:

- `204` — No Content
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## GET `/reporting/v1/reports/templates/{template_id}`

Operation: `templateData`

Template metadata API

Get report-template data api will returns template metadata.

Tags: `Reports`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## PUT `/reporting/v1/reports/templates/{template_id}`

Operation: `updateTemplate`

Update template API

Update report template.

Tags: `Reports`

Parameters:

- `template_id` path, required (integer) — Report Template id id which needs to be updated.

Request body:

- `application/json` — UpdateReportTemplateReq

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## POST `/reporting/v1/reports/templates/clone`

Operation: `cloneTemplate`

Clone Template

Clone the Template.

Tags: `Reports`

Request body:

- `application/json` — CloneTemplateReq

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

