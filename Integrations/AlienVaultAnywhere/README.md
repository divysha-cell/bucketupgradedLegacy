
# AlienVaultAnywhere

AlienVault USM Anywhere delivers powerful threat detection, incident response, and compliance management for cloud, on-premises, and hybrid environments.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Root|None|True|IP_OR_HOST||
|Username|None|True|String||
|Password|None|True|Password|*****|
|Product Version|None|True|String|V2|
|Verify SSL|None|False|Boolean|True|


#### Dependencies
| |
|-|
|uritemplate-4.1.1-py2.py3-none-any.whl|
|httpx-0.27.2-py3-none-any.whl|
|idna-3.8-py3-none-any.whl|
|h11-0.14.0-py3-none-any.whl|
|httplib2-0.22.0-py3-none-any.whl|
|protobuf-5.28.0-cp38-abi3-manylinux2014_x86_64.whl|
|httpcore-1.0.5-py3-none-any.whl|
|proto_plus-1.24.0-py3-none-any.whl|
|types_python_dateutil-2.9.0.20240906-py3-none-any.whl|
|urllib3-2.2.2-py3-none-any.whl|
|google_api_core-2.19.2-py3-none-any.whl|
|google_auth_httplib2-0.2.0-py2.py3-none-any.whl|
|google_api_python_client-2.144.0-py2.py3-none-any.whl|
|requests-2.32.3-py3-none-any.whl|
|pycryptodome-3.20.0-cp35-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|anyio-4.4.0-py3-none-any.whl|
|pyparsing-3.1.4-py3-none-any.whl|
|six-1.16.0-py2.py3-none-any.whl|
|google_auth-2.34.0-py2.py3-none-any.whl|
|charset_normalizer-3.3.2-py3-none-any.whl|
|arrow-1.3.0-py3-none-any.whl|
|TIPCommon-1.1.9.0-py2.py3-none-any.whl|
|googleapis_common_protos-1.65.0-py2.py3-none-any.whl|
|pyasn1-0.6.0-py2.py3-none-any.whl|
|sniffio-1.3.1-py3-none-any.whl|
|certifi-2024.8.30-py3-none-any.whl|
|rsa-4.9-py3-none-any.whl|
|python_dateutil-2.9.0.post0-py2.py3-none-any.whl|
|cachetools-5.5.0-py3-none-any.whl|
|pyasn1_modules-0.4.0-py3-none-any.whl|


## Actions
#### Get Alarm Details
Retrieve details for an alarm by ID
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alarm ID|The alarm ID. Can be obtained by running connector.|True|String||





#### List Events
Search for AlienVault events.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Account Name|The account name.|False|String||
|Event Name|The name of the event.|False|String||
|Source Name|The source name.|False|String||
|Start Time|Filtered results will include events that occurred after this timestamp. format: DD/MM/YYYY|False|String||
|End Time|Filtered results will include events that occurred before this timestamp. format: DD/MM/YYYY|False|String||
|Suppressed|Whether to filter events by the suppressed flag.|False|Boolean|False|
|Events Limit|Maximum number of events to return.|False|String|100|





#### Ping
Test connectivity
Timeout - 600 Seconds









## Connectors
#### AlienVault USM Anywhere Connector
AlienVault USM Anywhere Connector

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Root|e.g. https://<instance>.alienvault.com|True|String||
|ClientID|ClientID|True|String||
|Secret|Secret|True|Password|*****|
|Product Version|AlienVault Anywhere version - V1, V2|True|String|V2|
|Verify SSL|Indicate whether to use SSL in the session or not|False|Boolean|FALSE|
|Max Alerts Per Cycle|Limit the number of alerts in every cycle. e.g. 10|True|Int|10|
|Max Days Backwards|This field is used in the connector first running cycle and determine the start time. e.g. 3|True|Int|1|
|Padding Period|Padding period (hours) for the connector execution.|False|Int|0|
|Show Suppressed|Whether to include suppressed alarms in the search|False|Boolean||
|Use Suppressed Filter|This parameter will be used to determine whether to filter the incoming alerts using the "Show Suppressed" filter or not.|False|Boolean|True|
|Priority|Filter by alarm priority, comma separated. Valid value: high/medium/low.|False|String||
|Rule Intent|Filter alarms by the purpose of the alarm. The intent describes the context of the behavior that is being observed. These are the threat categories: System Compromise, Exploitation & Installation, Delivery & Attack, Reconnaissance & Probing, Environmental Awareness|False|String||
|Rule Strategy|The strategy of the rule that triggered the alarm. For example, use Client-Side Attack - Known Vulnerability when trying to exploit a known vulnerability in a web browser the attacker|False|String||
|Rule Method|Filter alarms by rule method. The method would provide additional detail on the target of the attack and the particular vulnerability. e.g. Firefox - CVE-2008-4064|False|String||
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




