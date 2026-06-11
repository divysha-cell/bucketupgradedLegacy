
# QualysEDR

Qualys Multi-Vector EDR unifies different context vectors like asset discovery, rich normalized software inventory, end-of-life visibility, vulnerabilities and exploits, misconfigurations, in-depth endpoint telemetry, and network reachability with a powerful backend to correlate it all for accurate assessment, detection and response – all in a single, cloud-based app.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root||True|String|http://x.x.x.x|
|Username||True|String||
|Password||True|Password|*****|
|Verify SSL||False|Boolean|true|


#### Dependencies
| |
|-|
|idna-3.13-py3-none-any.whl|
|urllib3-2.6.3-py3-none-any.whl|
|TIPCommon-1.0.10-py3-none-any.whl|
|EnvironmentCommon-1.0.0-py3-none-any.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|requests-2.32.4-py3-none-any.whl|
|certifi-2026.4.22-py3-none-any.whl|


## Actions
#### Ping
Test connectivity to the Qualys EDR with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds









## Connectors
#### Qualys EDR - Events Connector
Pull information about events from Qualys EDR.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|DeviceProductField|Enter the source field name in order to retrieve the Product Field name.|True|String|Product Name|
|EventClassId|Enter the source field name in order to retrieve the Event Field name.|True|String|type|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|PythonProcessTimeout|Timeout limit for the python process running the current script.|True|Integer|180|
|API Root|API root of the Qualys EDR instance.|True|String|http://x.x.x.x|
|Username|Username of the Qualys EDR account.|True|String||
|Password|Password of the Qualys EDR account.|True|Password|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Qualys EDR server is valid.|False|Boolean|true|
|Lowest Score To Fetch|Lowest Score that needs to be used to fetch events.  Maximum: 10. If nothing is specified, connector will ingest events with all scores.|False|Integer|5|
|Type Filter|Type filter for the events. Possible values: File,mutex,process,network,registry.|True|String|file, network|
|Max Hours Backwards|Number of hours before the first connector iteration to retrieve events from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|Integer|1|
|Max Events To Fetch|How many alert logs to process per one connector iteration. Default: 100.|False|Integer|100|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|Boolean|true|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




