
# FireEyeHelix

To protect against advanced threats, organizations need to integrate their security and apply the right expertise and processes. FireEye Helix is a cloud-hosted security operations platform that allows organizations to take control of any incident from alert to fix.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|None|True|String|https://helix.eu.fireeye.com/helix/id/{id}/|
|API Token|None|True|Password|*****|
|Verify SSL|None|False|Boolean|False|


#### Dependencies
| |
|-|
|netaddr-1.3.0-py3-none-any.whl|
|tldextract-5.1.2-py3-none-any.whl|
|TIPCommon-1.0.12-py2.py3-none-any.whl|
|idna-3.7-py3-none-any.whl|
|urllib3-2.2.2-py3-none-any.whl|
|filelock-3.15.4-py3-none-any.whl|
|requests-2.32.3-py3-none-any.whl|
|certifi-2024.7.4-py3-none-any.whl|
|charset_normalizer-3.3.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|chardet-5.2.0-py3-none-any.whl|
|requests_file-2.1.0-py2.py3-none-any.whl|
|EnvironmentCommon-1.0.1-py2.py3-none-any.whl|


## Actions
#### Add Entities To a List
Add Siemplify entities to the FireEye Helix list.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|List Short Name|Specify the short name of the list.|True|String||
|Risk|Specify the risk of the items.|False|List|Medium|
|Note|Specify notes that should be added to the items.|False|String||





#### Enrich User
Fetch information about users from FireEye Helix.
Timeout - 600 Seconds





#### Archive Search
Perform archive search in FireEye Helix.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Query|Specify the query for the search, for example: srcserver=172.30.202.130|True|String||
|Time Frame|Specify the time frame for the search. Only hours and days are supported. Note: end time will be 4 hours earlier than current time and time frame will start calculation from that point. For example, if 'Time Frame' is 3h, then the start time will be the current time - 7h, while the end time will be the current time -4h. API doesn't allow archive search to be performed on events that are only 3 hours old. This is the FireEye Helix limitation. Examples of the values: 7h - 7 hours, 1d - 1 day|True|String||
|Max Results To Return|Specify how many results to return.|False|String|100|





#### Get List Items
Return information about FireEye Helix lists items.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|List Short Name|Specify the short name of the list.|True|String||
|Value|Specify value filter for the items.|False|String||
|Type|Specify type filter for the items.|False|List|ALL|
|Sort By|Specify which parameter should be used for sorting results.|False|List|Value|
|Sort Order|Specify the sorting order for the results.|False|List|Ascending|
|Max Items To Return|Specify how many items to return.|False|String|100|





#### Ping
Test connectivity to the FireEye Helix with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds



#### Enrich Endpoint
Fetch endpoint's system information by its hostname.
Timeout - 600 Seconds





#### Get Alert Details
Retrieve information about Alert from FireEye Helix.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert ID|Specify ID of the Alert that needs to be enriched in FireEye Helix.|True|String||
|Max Notes To Return|Specify how many associated notes to return.|False|String|50|





#### Index Search
Perform index search in FireEye Helix.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Query|Specify the query for the search, for example: srcserver=172.30.202.130|True|String||
|Time Frame|Specify the time frame for the search. Only hours and days are supported. This is the FireEye Helix limitation. Examples of the values: 7h - 7 hours 1d - 1 day|False|String||
|Max Results To Return|Specify how many results to return.|False|String|100|





#### Close Alert
Close Alert in FireEye Helix.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert ID|Specify ID of the Alert that needs to be closed in FireEye Helix.|True|String||
|Revision Note|Specify revision note for the alert.|False|String||



#### Add Note To Alert
Add a Note to Alert in FireEye Helix.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert ID|Specify Alert ID to add note to.|True|String||
|Note|Specify note for the alert.|True|String||



#### Suppress Alert
Suppress Alert in FireEye Helix.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert ID|Specify ID of the Alert that needs to be suppressed in FireEye Helix.|True|String||
|Duration|Specify for how long the Alert should be suppressed in minutes.|True|String||



#### Get Lists
Return information about FireEye Helix lists.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Name|Specify name filter.|False|String||
|Short Name|Specify short name filter.|False|String||
|Active|Specify, whether action should only return active lists.|False|Boolean|false|
|Internal|Specify, whether action should only return internal lists.|False|Boolean|false|
|Protected|Specify, whether action should only return protected lists.|False|Boolean|false|
|Sort By|Specify which parameter should be used for sorting results.|False|List|Name|
|Sort Order|Specify the sorting order for the results.|False|List|Ascending|
|Max Lists To Return|Specify how many lists to return.|False|String|100|











## Connectors
#### FireEye Helix - Alerts Connector
Pull alerts from FireEye Helix.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|API Root|API Root of the FireEye Helix instance. Example: https://helix.eu.fireeye.com/helix/id/aaaqsj477/|True|String|https://helix.eu.fireeye.com/helix/id/{id}/|
|API Token|API Token of the FireEye Helix account.|True|Password|*****|
|Server Timezone|Specify which timezone is set on the FireEye Helix server in regards to UTC. For example, +1, -1, etc. If nothing is specified, the connector will use UTC as a default timezone.|False|String||
|Lowest Risk To Fetch|Lowest risk that will be used to fetch Alert. Possible values: Low, Medium, High, Critical.|True|String|Medium|
|Fetch Max Hours Backwards|Number of hours before the first connector iteration to retrieve alerts from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|Int|1|
|Max Alerts To Fetch|How many alerts to process per one connector iteration.|False|Int|50|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|Boolean|false|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the FireEye Helix server is valid.|False|Boolean|false|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




