
# ObserveIT

The ObserveIT platform correlates activity and data movement, empowering security teams to identify user risk, detect to insider-led data breaches, and accelerate security incident response.  Leveraging a powerful contextual intelligence engine and a library of over 400 threat templates drawn from customers and leading cybersecurity frameworks, ObserveIT delivers rapid time to value and proven capability to streamline insider threat programs.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root||True|String|https://<address>:<port>|
|Client ID||True|String||
|Client Secret||True|Password|*****|
|Verify SSL||False|Boolean|True|


#### Dependencies
| |
|-|
|TIPCommon-1.0.11-py2.py3-none-any.whl|
|urllib3-2.6.3-py3-none-any.whl|
|EnvironmentCommon-1.0.2-py2.py3-none-any.whl|
|certifi-2026.2.25-py3-none-any.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|idna-3.11-py3-none-any.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|requests-2.32.4-py3-none-any.whl|


## Actions
#### Ping
Test connectivity to the ObserveIT with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds









## Connectors
#### ObserveIT - Alerts Connector
Pull alerts from ObserveIT.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field.Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|API Root|API root of ObserveIT server.|True|String|https://x.x.x.x:x|
|Client ID|Client ID of the ObserveIT app.|True|String||
|Client Secret|Client Secret of the ObserveIT app.|True|Password|*****|
|Lowest Severity To Fetch|Lowest severity that will be used to fetch Alerts. Possible values: Low, Medium, High, Critical.|True|String|Medium|
|Fetch Max Hours Backwards|Number of hours before the first connector iteration to retrieve alerts from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|Int|1|
|Max Alerts To Fetch|How many alerts to process per one connector iteration.|False|Int|25|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|Boolean|false|
|Use SSL|Option to enable SSL/TLS connection|False|Boolean|true|
|Proxy Server Address|The address of the proxy server to use|False|String||
|Proxy Username|The proxy username to authenticate with|False|String||
|Proxy Password|The proxy password to authenticate with|False|Password|*****|




