
# Extrahop

ExtraHop provides cloud-native cybersecurity solutions to help enterprises detect and respond to advanced threats—before they compromise your business.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|None|True|String|https://{instance}.extrahop.com|
|Client ID|None|True|String||
|Client Secret|None|True|Password|*****|
|Verify SSL|None|False|Boolean|true|


#### Dependencies
| |
|-|
|uritemplate-4.1.1-py2.py3-none-any.whl|
|h11-0.14.0-py3-none-any.whl|
|httplib2-0.22.0-py3-none-any.whl|
|urllib3-2.3.0-py3-none-any.whl|
|charset_normalizer-3.4.1-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|google_auth-2.38.0-py2.py3-none-any.whl|
|google_api_core-2.24.2-py3-none-any.whl|
|TIPCommon-2.2.0-py2.py3-none-any.whl|
|cachetools-5.5.2-py3-none-any.whl|
|certifi-2025.1.31-py3-none-any.whl|
|pyasn1_modules-0.4.2-py3-none-any.whl|
|proto_plus-1.26.1-py3-none-any.whl|
|googleapis_common_protos-1.69.2-py3-none-any.whl|
|google_auth_httplib2-0.2.0-py2.py3-none-any.whl|
|requests-2.32.3-py3-none-any.whl|
|pycryptodome-3.22.0-cp37-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|idna-3.10-py3-none-any.whl|
|EnvironmentCommon-1.0.2-py2.py3-none-any.whl|
|typing_extensions-4.13.0-py3-none-any.whl|
|anyio-4.9.0-py3-none-any.whl|
|httpx-0.28.1-py3-none-any.whl|
|protobuf-6.30.2-cp39-abi3-manylinux2014_x86_64.whl|
|pyparsing-3.2.3-py3-none-any.whl|
|google_api_python_client-2.166.0-py2.py3-none-any.whl|
|sniffio-1.3.1-py3-none-any.whl|
|rsa-4.9-py3-none-any.whl|
|pyasn1-0.6.1-py3-none-any.whl|
|httpcore-1.0.7-py3-none-any.whl|


## Actions
#### Update Detection
Update a detection in Extrahop.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Detection ID|Specify the ID of the detection that needs to be updated.|True|String||
|Status|Specify the status for the detection.|False|List|Select One|
|Resolution|Specify the resolution for the detection. Resolution parameter is needed, if Status parameter is set to  "Closed"|False|List|Select One|
|Assign To|Specify the name of the analyst to whom the alert needs to be assigned. If “Unassign '' is provided, action will remove assignment from the alert.|False|String||





#### Ping
Test connectivity to the Extrahop with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds









## Connectors
#### Extrahop - Detections Connector
Pull information about detections from Extrahop. Note: whitelist filter works with "type" parameter.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|API Root|API root of the Extrahop instance.|True|String|https://{instance}.api.cloud.extrahop.com|
|Client ID|Client ID of the Extrahop instance.|True|String||
|Client Secret|Client Secret of the Extrahop instance.|True|Password|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Extrahop server is valid.|False|Boolean|true|
|Lowest Risk Score To Fetch|Lowest risk score that needs to be used to fetch detections. Maximum: 100. If nothing is provided, the connector will ingest detections with all risk scores.|False|Int||
|Max Hours Backwards|Number of hours before the first connector iteration to retrieve detections from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|Int|1|
|Max Detections To Fetch|How many detections to process per one connector iteration. Default: 100.|False|Int|100|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|Boolean|false|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




