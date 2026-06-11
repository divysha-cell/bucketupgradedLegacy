
# McAfeeESM

McAfee® Enterprise Security Manager, the industry-leading SIEM solution from McAfee, provides an intelligent, actionable, and integrated platform to protect your customers’ business and grow yours.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|API root for the instance.|True|String|https://{ip}/rs/|
|Username|Username for the instance.|True|String||
|Password|Password for the instance.|True|Password|*****|
|Product Version|Product version. Possible values: 11.1-11.5|True|String||
|Use AES Encryption|If enabled, integration will authenticate using AES Encryption and will not do Base64 inside the code. Note: you need to provide Login and Password already as Base64 encoded strings.|False|Boolean|false|
|Verify SSL|If enabled, verifies that the SSL certificate for the connection to the McAfee ESM server is valid.|False|Boolean||


#### Dependencies
| |
|-|
|idna-3.8-py3-none-any.whl|
|TIPCommon-1.0.12-py2.py3-none-any.whl|
|types_python_dateutil-2.9.0.20240906-py3-none-any.whl|
|urllib3-2.2.2-py3-none-any.whl|
|requests-2.32.3-py3-none-any.whl|
|pycryptodome-3.20.0-cp35-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|six-1.16.0-py2.py3-none-any.whl|
|chardet-5.2.0-py3-none-any.whl|
|charset_normalizer-3.3.2-py3-none-any.whl|
|arrow-1.3.0-py3-none-any.whl|
|EnvironmentCommon-1.0.1-py2.py3-none-any.whl|
|certifi-2024.8.30-py3-none-any.whl|
|python_dateutil-2.9.0.post0-py2.py3-none-any.whl|


## Actions
#### Send Advanced Query To ESM
Send an advanced query to ESM. Note: Action is running as async, please adjust script timeout value in Chronicle SOAR IDE for action as needed. Please refer to the documentation portal for more information.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Query Payload|Specify the JSON object that would need to be executed. Note: action will at max return only 200 results.|True|String||





#### Remove Values From Watchlist
Remove values from a watchlist in McAfee ESM.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Watchlist Name|Specify the name of the watchlist that needs to be updated.|True|String||
|Values to Remove|Specify a comma-separated list of values that need to be removed from a watchlist.|True|String||



#### Add Values To Watchlist
Add values to a watchlist in McAfee ESM. Note: McAfee ESM will allow values of the invalid type to be passed, for example, API will not raise error adding hash to the IP watchlist. Please pay attention to the input.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Watchlist Name|Specify the name of the watchlist that needs to be updated.|True|String||
|Values to Add|Specify a comma-separated list of values that need to be added to a watchlist.|True|String||



#### Send Query To ESM
Send a query to ESM. Note: Action is running as async, please adjust script timeout value in Chronicle SOAR IDE for action as needed.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Time Range|Specify a time frame for the results. If "Custom" is selected, you also need to provide "Start Time".|True|List|LAST_HOUR|
|Start Time|Specify the start time for the results. This parameter is mandatory, if "Custom" is selected for the "Time Frame" parameter. Format: ISO 8601|False|String||
|End Time|Specify the end time for the results. Format: ISO 8601. If nothing is provided and "Custom" is selected for the "Time Frame" parameter then this parameter will use current time.|False|String||
|Filter Field Name|Specify the field name that will be used for filtering.|True|String||
|Filter Operator|Specify the operator that should be used in the filter.|True|List|EQUALS|
|Filter Values|Specify a comma-separated list of values that will be used in the filter.|True|String||
|Fields To Fetch|Specify a comma-separated list of fields that should be returned. If nothing is provided, action will use the predefined fields.|False|String||
|Sort Field|Specify what parameter should be used for sorting. Note: this parameter expects the field in the format {table}.{key name}. If the parameter is provided in another format, action will skip it. Example: Alert.LastTime.|False|String||
|Sort Order|Specify the order of sorting.|False|List|ASC|
|Query Type|Specify what needs to be queried.|False|List|EVENT|
|Max Results To Return|Specify how many results to return. Default: 50. Maximum: 200.|False|String|50|





#### Send Entity Query To ESM
Send a query to ESM based on entities. Supported entities: IP Address, Hostname. Note: Action is running as async, please adjust script timeout value in Chronicle SOAR IDE for action as needed.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|IP Address Entity Key|Specify the key that will be used with the IP Address entity during filtering. Note: if invalid key is provided, the action will still return results, but they will be unexpected.|True|String|Alert.SrcIP|
|Hostname Entity Key|Specify the key that will be used with the Hostname entity during filtering. Note: if invalid key is provided, the action will still return results, but they will be unexpected.|True|String|Alert.4|
|Time Range|Specify a time frame for the results. If "Custom" is selected, you also need to provide "Start Time".|True|List|LAST_HOUR|
|Start Time|Specify the start time for the results. This parameter is mandatory, if "Custom" is selected for the "Time Frame" parameter. Format: ISO 8601|False|String||
|End Time|Specify the end time for the results. Format: ISO 8601. If nothing is provided and "Custom" is selected for the "Time Frame" parameter then this parameter will use current time.|False|String||
|Filter Field Name|Specify the field name that will be used for filtering.|True|String||
|Filter Operator|Specify the operator that should be used in the filter.|True|List|EQUALS|
|Filter Values|Specify a comma-separated list of values that will be used in the filter.|True|String||
|Fields To Fetch|Specify a comma-separated list of fields that should be returned. If nothing is provided, action will use the predefined fields.|False|String||
|Sort Field|Specify what parameter should be used for sorting. Note: this parameter expects the field in the format {table}.{key name}. If the parameter is provided in another format, action will skip it. Example: Alert.LastTime.|False|String||
|Sort Order|Specify the order of sorting.|False|List|ASC|
|Max Results To Return|Specify how many results to return. Default: 50. Maximum: 200.|False|String|50|





#### Ping
Test connectivity to McAfee ESM with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds



#### Get Similar Events
Get events related to the entities in McAfee ESM. Supported entities: Hostname, IP Address, User. Note: Action is running as async, please adjust script timeout value in Chronicle SOAR IDE for action as needed.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Hours Back|Specify how many hours backwards to search.|True|String|1|
|IPS ID|Specify the IP SID for the search.|False|String|144115188075855872/8|
|Result Limit|Specify how many results to return. Max: 200 per entity.|False|String|50|











## Connectors
#### McAfee ESM Correlations Connector
Pull information about сorrelations from McAfee ESM. Note: The dynamic list filter works with the "ruleName" parameter.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Secondary Device Product Field|Fallback product field name.|False|String||
|Rule Generator Field Name|Name of the field that will be used in the rule generator. Note: action will use "ruleName", if invalid value is provided.|False|String|app|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String|srcZone|
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|API Root|API root of the McAfee ESM instance. Format: https://{ip address}/rs/|True|String|https://{ip address}/rs/|
|Username|Username of the McAfee ESM account.|True|String||
|Password|Password of the McAfee ESM account.|True|Password|*****|
|Product Version|Version of Mcafee ESM. Possible values: 11.1, 11.2, 11.3, 11.4, 11.5.|True|String||
|Use AES Encryption|If enabled, integration will authenticate using AES Encryption and will not do Base64 inside the code. Note: you need to provide Login and Password already as Base64 encoded strings.|False|Boolean|false|
|Verify SSL|If enabled, verifies that the SSL certificate for the connection to the McAfee ESM server is valid.|False|Boolean|false|
|Lowest Average Severity To Fetch|The lowest average severity that needs to be used to fetch correlations. Possible values are in range from 0 to 100. If nothing is specified, the connector ingests correlations with all severities.|False|Int|0|
|Ingest 0 Source Event Correlations|If enabled, action will ingest alarms that have 0 source events. Note: this can have an impact on the values that come from parameters “Product Field Name”, “Event Field Name”, “Rule Generator Field Name”. Connector will wait the time that is provided in the parameter “Padding Time”, if the parameter is disabled.|False|Boolean|false|
|Padding Time|The number of hours that connector will use for padding. Note: this parameter describes how long the connector will wait to ingest the correlation with 0 source events, if "Ingest 0 Source Event Correlations" is disabled. Maximum: 6 hours.|False|Int|1|
|Time Format|Time format that will be used to read the timestamp provided in McAfee ESM. If nothing is provided or invalid time format is provided, then the connector will not perform the transformation.|False|String|%m/%d/%Y %H:%M:%S|
|Time Zone|Time zone of the source event. This parameter is needed to transform the timestamp into the format that reflects UTC+0 time. Note: this parameter is ignored, if invalid values are provided in the "Time Format" parameter or nothing is provided there.|False|Int||
|Max Hours Backwards|Number of hours before the first connector iteration to retrieve correlations from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|Int|1|
|Max Correlations To Fetch|The number of correlations to process per one connector iteration. Default: 20.|False|Int|20|
|IPSIDs Filter|Comma-separated list of IPSIDs that will be used to fetch data. If nothing is provided, the connector will use default IPSID.|False|Int||
|SIGIDs Filter|Comma-separated list of signature ids that will be used during ingestion. If nothing is provided, the connector will ingest correlations from all rules.|False|Int||
|Use dynamic list as a blacklist|If enabled, dynamic lists will be used as a blacklist.|False|Boolean|false|
|Disable Overflow|If enabled, the connector will disable the overflow mechanism.|False|Boolean|false|
|Disable Overflow For SigIDs|A comma-separated list of signature ids for which connector will ignore overflow. Note: requires "Disable Overflow" to be enabled.|False|String||
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|


#### McAfee ESM Connector
Pull information about alarms from McAfee ESM. Note: The dynamic list filter works with the "alarmName" parameter.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String|srcZone|
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|API Root|API root of the McAfee ESM instance. Format: https://{ip address}/rs/|True|String|https://{ip address}/rs/|
|Username|Username of the McAfee ESM account.|True|String||
|Password|Password of the McAfee ESM account.|True|Password|*****|
|Product Version|Version of Mcafee ESM. Possible values: 11.1, 11.2, 11.3, 11.4, 11.5.|True|String||
|Use AES Encryption|If enabled, integration will authenticate using AES Encryption and will not do Base64 inside the code. Note: you need to provide Login and Password already as Base64 encoded strings.|False|Boolean|false|
|Verify SSL|If enabled, verifies that the SSL certificate for the connection to the McAfee ESM server is valid.|False|Boolean|false|
|Lowest Severity To Fetch|The lowest severity that needs to be used to fetch alarms. Possible values are in range from 0 to 100. If nothing is specified, the connector ingests alarms with all severities.|False|Int|0|
|Ingest 0 Source Event Alarms|If enabled, action will ingest alarms that have 0 source events. Note: this can have an impact on the values that come from parameters “Product Field Name”, “Event Field Name”, “Rule Generator Field Name”. Connector will wait the time that is provided in the parameter “Padding Time”, if the parameter is disabled.|False|Boolean|true|
|Padding Time|The number of hours that connector will use for padding. Note: this parameter describes how long the connector will wait to ingest the alarm with 0 source events, if "Ingest 0 Source Event Alarms" is disabled. Maximum: 6 hours.|False|Int|1|
|Time Format|Time format that will be used to read the timestamp provided in McAfee ESM. If nothing is provided or invalid time format is provided, then the connector will not perform the transformation.|False|String|%m/%d/%Y %H:%M:%S|
|Time Zone|Time zone of the source event. This parameter is needed to transform the timestamp into the format that reflects UTC+0 time. Note: this parameter is ignored, if invalid values are provided in the "Time Format" parameter or nothing is provided there.|False|Int||
|Max Hours Backwards|Number of hours before the first connector iteration to retrieve alarms from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|Int|1|
|Max Alarms To Fetch|The number of alarms to process per one connector iteration. Default: 100.|False|Int|100|
|Use dynamic list as a blacklist|If enabled, dynamic lists will be used as a blacklist.|False|Boolean|false|
|Rule Generator Field Name|Name of the field that will be used in the rule generator. Note: action will use "alarmName", if value is not available and this parameter is only applied to the values that come from source events.|False|String|alarmName|
|Secondary Device Product Field|Fallback product field name.|False|String||
|Disable Overflow|If enabled, the connector will disable the overflow mechanism.|False|Boolean|false|
|Disable Overflow For Alarm Names|A comma-separated list of alarm names for which connector will ignore overflow. Note: requires "Disable Overflow" to be enabled.|False|String||
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




