
# CBCloud

The VMware Carbon Black Cloud is a cloud-native endpoint protection platform (EPP) that combines the intelligent system hardening and behavioral prevention needed to keep emerging threats at bay, using a single lightweight agent, and an easy-to-use console.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|None|True|String||
|Organization Key|None|True|String||
|API ID|None|True|Password|*****|
|API Secret Key|None|True|Password|*****|
|Verify SSL|None|False|Boolean||


#### Dependencies
| |
|-|
|uritemplate-4.1.1-py2.py3-none-any.whl|
|idna-3.8-py3-none-any.whl|
|h11-0.14.0-py3-none-any.whl|
|httplib2-0.22.0-py3-none-any.whl|
|proto_plus-1.24.0-py3-none-any.whl|
|TIPCommon-2.2.0-py2.py3-none-any.whl|
|cachetools-5.4.0-py3-none-any.whl|
|urllib3-2.2.2-py3-none-any.whl|
|types_python_dateutil-2.9.0.20240821-py3-none-any.whl|
|google_auth_httplib2-0.2.0-py2.py3-none-any.whl|
|protobuf-5.27.2-cp38-abi3-manylinux2014_x86_64.whl|
|requests-2.32.3-py3-none-any.whl|
|pycryptodome-3.20.0-cp35-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|anyio-3.7.1-py3-none-any.whl|
|google_api_core-2.19.1-py3-none-any.whl|
|six-1.16.0-py2.py3-none-any.whl|
|chardet-5.2.0-py3-none-any.whl|
|pyparsing-3.1.2-py3-none-any.whl|
|charset_normalizer-3.3.2-py3-none-any.whl|
|arrow-1.3.0-py3-none-any.whl|
|google_auth-2.32.0-py2.py3-none-any.whl|
|httpcore-0.17.3-py3-none-any.whl|
|google_api_python_client-2.137.0-py2.py3-none-any.whl|
|EnvironmentCommon-1.0.1-py2.py3-none-any.whl|
|pyasn1-0.6.0-py2.py3-none-any.whl|
|httpx-0.24.1-py3-none-any.whl|
|sniffio-1.3.1-py3-none-any.whl|
|certifi-2024.8.30-py3-none-any.whl|
|googleapis_common_protos-1.63.2-py2.py3-none-any.whl|
|rsa-4.9-py3-none-any.whl|
|python_dateutil-2.9.0.post0-py2.py3-none-any.whl|
|exceptiongroup-1.1.1-py3-none-any.whl|
|pyasn1_modules-0.4.0-py3-none-any.whl|


## Actions
#### Enable Bypass Mode for Device
Create enable bypass mode task for device on VMware Carbon Black Cloud server based on Siemplify IP or Host Siemplify entities.
Timeout - 600 Seconds



#### List Reputation Overrides
List reputation overrides configured in VMware Carbon Black Cloud. Note that action is not working on Siemplify entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Reputation Override List|Specify override list action should return.|False|List|Not Specified|
|Reputation Override Type|Specify override type action should return.|False|List|Not Specified|
|Start from Row|Specify from which row action should fetch data.|False|String|0|
|Max Rows to Return|Specify how many rows action should return.|False|String|50|
|Rows Sort Order|Specify sort order for the returned rows. Rows are sorted based on "create_time" value.|False|List|ASC|





#### Quarantine Device
Create quarantine device task on the VMware Carbon Black Cloud server based on the Siemplify IP or Host Siemplify entities.
Timeout - 600 Seconds





#### Device Background Scan
Create a device background scan task on VMware Carbon Black Cloud server based on the Siemplify IP or Host Siemplify entities.
Timeout - 600 Seconds



#### Create a Reputation Override for SHA-256 Hash
Create a Reputation Override for the provided hash in SHA-256 format. Note: The SHA-256 hash can be provided either as a Siemplify FileHash (artifact) or as an action input parameter. If the hash is passed to action both as an entity and input parameter - action will be executed on the input parameter.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|SHA-256 Hash|Specify a SHA-256 hash value to create override for.|False|String||
|Filename|Specify a corresponding file name to add to reputation override.|True|String||
|Description|Specify a description for the created reputation override.|False|String||
|Reputation Override List|Specify override list to create.|True|List|Not Specified|





#### List Host Vulnerabilities
List vulnerabilities found on the host in Сarbon Black Cloud. Supported entities: IP Address and Hostname.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Severity Filter|Specify the comma-separated list of severities for vulnerabilities. If nothing is provided, action will ingest all related vulnerabilities. Possible values: Critical, Important, Moderate, Low.|False|String||
|Max Vulnerabilities To Return|Specify how many vulnerabilities to return per host. If nothing is provided, action will process all of the related vulnerabilities.|False|String|100|





#### Create a Reputation Override for Certificate
Create a Reputation Override for the certificate. Note that action is not working on Siemplify entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Certificate Authority|Specify the Certificate Authority that authorizes the validity of the certificate to add to reputation override.|False|String||
|Signed By|Specify the name of the signer to add to reputation override.|True|String||
|Description|Specify a description for the created reputation override.|False|String||
|Reputation Override List|Specify override list to create.|True|List|Not Specified|





#### Dismiss VMware Carbon Black Cloud Alert
Dismiss VMware Carbon Black Cloud alert. Note: action accepts alert id in format 27162661199ea9a043c11ea9a29a93652bc09fd, not in format that is shown in UI as DONAELUN.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert ID|Alert ID to dismiss on VMware Carbon Black Cloud server.|True|String||
|Reason for dismissal|VMware Carbon Black Cloud reason for alert dismissal.|True|List|No dismissal reason|
|Determination|Specify the determination to set for an alert.|True|List|None|
|Message for alert dismissal|Message to add to alert dismissal.|False|String|The alert has been dismissed by Siemplify|



#### Delete a Reputation Override
Delete a Reputation Override based on the provided reputation override id. Note that action is not working on Siemplify entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Reputation Override ID|Specify a Reputation Override ID to delete.|True|String||



#### Update a Policy for Device by Policy ID
Change a policy on VMware Carbon Black Cloud sensor on a host. The action scope is IP or Host entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Policy ID|Specify a policy to associate with the VMware Carbon Black Cloud sensor.|True|String||



#### Create a Reputation Override for IT Tool
Create a Reputation Override for the specific IT Tool based on a file name and path. Note: The file name can be provided either as a Siemplify File (artifact) or as an action input parameter. If the file name is passed to action both as an entity and input parameter - action will be executed on the input parameter. File name will be appended to the File Path parameter to get the resulting path to add to the override.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|File Name|Specify a corresponding file name to add to reputation override.|False|String||
|File Path|Specify a file path where corresponding IT Tool is stored on disk to add to reputation override. Example format: C:\TMP\ |True|String||
|Description|Specify a description for the created reputation to override.|False|String||
|Reputation Override List|Specify override list to create.|True|List|Not Specified|
|Include Child Processes|If enabled, include IT Tool's child processes on approved list|False|Boolean|False|





#### Unquarantine Device
Create unquarantine device task on the VMware Carbon Black Cloud server based on the Siemplify IP or Host Siemplify entities.
Timeout - 600 Seconds



#### Disable Bypass Mode for Device
Create disable bypass mode task for devices on the VMware Carbon Black Cloud server based on the Siemplify IP or Host Siemplify entities.
Timeout - 600 Seconds



#### Execute Entity Processes Search
Execute Carbon Black Cloud Process Search based on the Siemplify Entity. Action can be used to search information about processes stored in Carbon Black Cloud with action input parameters and following Siemplify entities: IP, Host, User, Hash, Process.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Start from Row|Specify from which row action should fetch data.|False|String|0|
|Max Rows to Return|Specify how many rows action should return.|False|String|50|
|Create Insight|If enabled, action will create a Siemplify insight based on process info from Carbon Black Cloud.|False|Boolean|false|





#### Enrich Entities
Enrich Siemplify Host or IP entities based on the device information from the VMware Carbon Black Cloud.
Timeout - 600 Seconds





#### Ping
Test connectivity to the VMware Carbon Black Cloud
Timeout - 600 Seconds









## Connectors
#### VMware Carbon Black Cloud Alerts and Events Baseline Connector
Fetch Carbon Black Cloud Alerts and Events that reached specific baseline (were classified by default as Threat in Carbon Black Cloud)

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is ""|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is ""|False|Int|.*|
|API Root|Vmware Carbon Black Cloud API Root URL|True|String||
|Organization Key|Vmware Carbon Black Cloud Organization Key, Eg. 7DDDD9DD|True|String||
|API ID|Vmware Carbon Black Cloud API ID (Custom API Key ID)|True|Password|*****|
|API Secret Key|Vmware Carbon Black Cloud API Secret Key (Custom API Secret Key)|True|Password|*****|
|Verify SSL|Verify SSL certificates for HTTPS requests to Microsoft Azure.|False|Boolean|false|
|Max Alerts Per Cycle|How many alerts should be processed during one connector run.|True|Int|100|
|Offset Time In Hours|Number of hours before the first connector iteration to retrieve alerts from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|True|Int|24|
|Minimum Severity to Fetch|Minimum severity of Carbon Black Cloud alert to be ingested to Siemplify, for example, 4 or 7|False|Int||
|What Alert Field to use for Name field|What Carbon Black Cloud alert field should be used for the Siemplify Alert Name field. Possible values are: type, policy_name|True|String|type|
|What Alert Field to use for Rule Generator|What Carbon Black Cloud alert field should be used for the Siemplify Alert Rule Generator field. Possible values are: type, policy_name|True|String|type|
|Alert Reputation to Ingest|What Carbon Black Cloud alert reputation alert can have to be ingested. Parameter accepts multiple values as a comma separated string. If "N/A" is provided, connector will ingest alerts without reputation.|False|String||
|Watchlist Name Filter|If provided, for CB Cloud alerts with the type “Watchlist“ ingest only that were triggered by the respective whatchlist. Parameter accepts multiple values as a comma separated string. If nothing is specified - ingest everything regardless of watchlist name.|False|String||
|Events Limit to Ingest per Alert|Specify how many events can be ingested per single CB Cloud alert.|True|Int|25|
|Proxy Server Address|Proxy server to use for connection.|False|IP||
|Proxy Server Username|Proxy server username|False|String||
|Proxy Server Password|Proxy server password|False|Password|*****|
|Alerts Backlog Timer|Time frame in minutes for which connector should try to fetch again the alerts from backlog it previously failed to process.|True|Int|60|
|Max Backlog Alerts per Cycle|How many alerts  connector should try to fetch from the backlog during one connector run.|True|Int|10|
|Alert Name Template|If specified, connector will use this value from the CB Cloud API response for alert data for Siemplify Alert Name. You can provide placeholders in the following format: [name of the field]. Example: CBCLOUD Alert - [reason]. Note: the maximum length for the field is 256 characters. If nothing is provided or user provides an invalid template, connector will use the default alert name.|False|String||
|Rule Generator Template|If specified, connector will use this value from the CB Cloud API response for alert data for Siemplify Rule Generator. You can provide placeholders in the following format: [name of the field]. Example: CBCLOUD - [reason]. Note: the maximum length for the field is 256 characters. If nothing is provided or user provides an invalid template, connector will use the default rule generator value.|False|String||


#### VMware Carbon Black Cloud Alerts Connector
Siemplify VMware Carbon Black Cloud Alerts Connector should be used to ingest alerts from Carbon Black Cloud (Platform) instances. Note that this connector is deprecated and not recommended to use. Consider switching to "VMware Carbon Black Cloud Alerts and Events Baseline Connector" or "VMware Carbon Black Cloud Alerts and Events Tracking Connector"

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is ""|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is ""|False|Int|.*|
|API Root|Vmware Carbon Black Cloud API Root URL|True|String||
|Organization Key|Vmware Carbon Black Cloud Organization Key|True|String||
|API ID|Vmware Carbon Black Cloud API ID (Custom API Key ID)|True|Password|*****|
|API Secret Key|Vmware Carbon Black Cloud API Secret Key (Custom API Secret Key)|True|Password|*****|
|Verify SSL|Verify SSL certificates for HTTPS requests to Microsoft Azure.|False|Boolean|false|
|Max Alerts Per Cycle|How many alerts should be processed during one connector run.|True|Int|10|
|Offset Time In Hours|Number of hours before the first connector iteration to retrieve alerts from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|True|Int|24|
|Minimum Severity to Fetch|Minimum severity of Carbon Black Cloud alert to be ingested to Siemplify|False|Int||
|What Alert Field to use for Name field|What Carbon Black Cloud alert field should be used for the Siemplify Alert Name field. Possible values are: type, policy_name|True|String|type|
|What Alert Field to use for Rule Generator|What Carbon Black Cloud alert field should be used for the Siemplify Alert Rule Generator field. Possible values are: type, policy_name|True|String|type|
|Proxy Server Address|Proxy server to use for connection.|False|IP||
|Proxy Server Username|Proxy server username|False|String||
|Proxy Server Password|Proxy server password|False|Password|*****|


#### VMware Carbon Black Cloud Alerts and Events Tracking Connector
Fetch Carbon Black Cloud Alerts and Events as Events are added to Carbon Black Cloud Alerts. Connector can create multiple Siemplify alerts for single Carbon Black Cloud Alert, if Cloud Alert was updated with new events after initial ingestion by Siemplify.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|Vmware Carbon Black Cloud API Root URL|True|String||
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is ""|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is ""|False|Int|.*|
|Organization Key|Vmware Carbon Black Cloud Organization Key, Eg. 7DDDD9DD|True|String||
|API ID|Vmware Carbon Black Cloud API ID (Custom API Key ID)|True|Password|*****|
|API Secret Key|Vmware Carbon Black Cloud API Secret Key (Custom API Secret Key)|True|Password|*****|
|Verify SSL|Verify SSL certificates for HTTPS requests to Microsoft Azure.|False|Boolean|false|
|Max Alerts Per Cycle|How many alerts should be processed during one connector run.|True|Int|100|
|Offset Time In Hours|Number of hours before the first connector iteration to retrieve alerts from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|True|Int|24|
|Minimum Severity to Fetch|Minimum severity of Carbon Black Cloud alert to be ingested to Siemplify, for example, 4 or 7|False|Int||
|What Alert Field to use for Name field|What Carbon Black Cloud alert field should be used for the Siemplify Alert Name field. Possible values are: type, policy_name|True|String|type|
|What Alert Field to use for Rule Generator|What Carbon Black Cloud alert field should be used for the Siemplify Alert Rule Generator field. Possible values are: type, policy_name|True|String|type|
|Alert Reputation to Ingest|What Carbon Black Cloud alert reputation alert can have to be ingested. Parameter accepts multiple values as a comma separated string. If "N/A" is provided, connector will ingest alerts without reputation.|False|String||
|Events Padding Period (hours)|Specify how many hours connector should track new events for already ingested alert.|True|Int|24|
|Events Limit to Ingest per Alert|Specify how many events can be ingested per single CB Cloud alert per Connector iteration.|True|Int|25|
|Total Limit of Events per Alert|Specify a total number of events connector should get per single CB Cloud alert. If this limit is reached, no new events will be fetched for alert. In order to not limit the total number of events, please leave this parameter empty.|False|Int|100|
|Max Backlog Alerts per Cycle|How many alerts connector should try to fetch from the backlog during one connector run.|True|Int|10|
|Alerts Backlog Timer|Time frame in minutes for which connector should try to fetch again the alerts from backlog it previously failed to process.|True|Int|60|
|Proxy Server Address|Proxy server to use for connection.|False|IP||
|Proxy Server Username|Proxy server username|False|String||
|Proxy Server Password|Proxy server password|False|Password|*****|
|Watchlist Name Filter|If provided, for CB Cloud alerts with the type “Watchlist“ ingest only that were triggered by the respective whatchlist. Parameter accepts multiple values as a comma separated string. If nothing is specified - ingest everything regardless of watchlist name.|False|String||
|Alert Name Template|If specified, connector will use this value from the CB Cloud API response for alert data for Siemplify Alert Name. You can provide placeholders in the following format: [name of the field]. Example: CBCLOUD Alert - [reason]. Note: the maximum length for the field is 256 characters. If nothing is provided or user provides an invalid template, connector will use the default alert name.|False|String||
|Rule Generator Template|If specified, connector will use this value from the CB Cloud API response for alert data for Siemplify Rule Generator. You can provide placeholders in the following format: [name of the field]. Example: CBCLOUD - [reason]. Note: the maximum length for the field is 256 characters. If nothing is provided or user provides an invalid template, connector will use the default rule generator value.|False|String||




