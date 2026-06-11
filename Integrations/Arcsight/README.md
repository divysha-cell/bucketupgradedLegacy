
# Arcsight

Real-time threat detection and automated response backed by a powerful, open, and intelligent SIEM (Security Information and Event Management).

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Root|None|True|String|https://{IP_ADDR}:{PORT}|
|Username|None|True|String|None|
|Password|None|True|Password|*****|
|CA Certificate File|None|False|String||
|Verify SSL|None|False|Boolean|false|


#### Dependencies
| |
|-|
|TIPCommon-1.0.16-py2.py3-none-any.whl|
|netaddr-1.3.0-py3-none-any.whl|
|idna-3.7-py3-none-any.whl|
|urllib3-2.2.2-py3-none-any.whl|
|requests-2.32.3-py3-none-any.whl|
|certifi-2024.7.4-py3-none-any.whl|
|simplejson-3.19.2-cp311-cp311-manylinux_2_5_x86_64.manylinux1_x86_64.manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|EnvironmentCommon-1.0.2-py2.py3-none-any.whl|
|charset_normalizer-3.3.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|


## Actions
#### Is Value In Activelist Column
Action checks, if entities were found in ArcSight Activelist
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Active list UUID|Specify the UUID of the active list, where you want to search for entities. Note: parameter “Active list UUID“ takes priority over “Active list name“. Example: HLZRc9yYBABC-lHtlf3-f0Q==|False|String||
|Column name|Specify the name of the column, where you want to search for the entity.|True|String||
|Active list name|Specify the name of the active list, where you want to search for entities. Note: parameter “Active list UUID“ takes priority over “Active list name“.|False|String||





#### Get Activelist Entries
Retrieve active list entries in ArcSight
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Active list UUID|Specify the UUID of the active list for which you want to retrieve entries. Note: parameter “Active list UUID“ takes priority over “Active list name“. Example: HLZRc9yYBABC-lHtlf3-f0Q==|False|String||
|Active list name|Specify the name of the active list for which you want to retrieve entries. Note: parameter “Active list UUID“ takes priority over “Active list name“.|False|String||
|Map Columns|If enabled, action will map columns to the values in the JSON result.|False|Boolean|false|
|Max Entries To Return|Specify how many entries to return.|False|String||





#### Add Entries To Activelist
Add new entry to active list in ArcSight. Column values are separated by delimiter ‘|' and entries are separated by ‘;’ in parameter ‘Entries’. Column names are separated by delimiter ‘;’ in parameter ‘Columns’. You can also use Entries JSON instead of ‘Columns’ + 'Entries’“.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Columns|Specify the name of the columns, where you want to put values for the entries. Format: Column_name1;Column_name2|False|String||
|Entries|Specify the entries. Format entry1_value1|entry1_value2;entry2_value1|entry2_value2|False|String||
|Active List UUID|Specify the UUID of the active list, where you want to add new entries. Note: parameter “Active list UUID“ takes priority over “Active list name“. Example: HLZRc9yYBABC-lHtlf3-f0Q==|False|String||
|Active list name|Specify the name of the active list, where you want to add new entries. Note: parameter “Active list UUID“ takes priority over “Active list name“.|False|String||
|Entries JSON|Specify a list of JSON objects that contain information about the entry. Note: Combination of ‘Columns' and ‘Entries’ parameters have priority over 'Entries JSON’. Format: [{"Column_1": "Value_1", "Column_2": "Value_2"}, {"Column_1": "Value_3", "Column_2": "Value_4"}]|False|String||



#### List Resources
List available queries in ArcSight.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Return Active Lists|If enabled, action will return available active lists.|False|Boolean|true|
|Return Queries|If enabled, action will return available queries|False|Boolean|true|
|Return Cases|If enabled, action will return available cases.|False|Boolean|false|
|Return Reports|If enabled, action will return available reports.|False|Boolean|false|
|Max Resources To Return|Specify how many resources to return per type.|False|String|50|





#### Add Entities To Active List
Add entities to the active list in ArcSight.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Active List Name|Specify the name of the active list to which you want to add entities.|True|String||
|Entity Column|Specify the name of the column, where entity value should be put.|True|String||
|Additional Fields|Specify additional fields that should be added alongside the entity in the active list. Format is a JSON object. Example: {"Column_1": "Value_1","Column_2": "Value_2"}|False|String||



#### Search
Search for available resources in ArcSight
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Search Query|Specify the search query.|True|String|None|
|Max Items To Return|Specify how many items to return in the response.|False|String|100|





#### Ping
Test Connectivity
Timeout - 600 Seconds



#### Get Query Results
Get results for the provided query in ArcSight
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Max Items To Return|Specify how many items to return in the response.|False|String|100|
|Query ID|Specify the ID of the query for which you want to return results. Note: parameter “Query ID“ takes priority over “Query Name“. Example: cyUJKRz4BABCFwS9iFPq+aA==|False|String||
|Query Name|Specify the name of the query for which you want to return results. Note: parameter “Query ID“ takes priority over “Query Name“.|False|String||





#### Get Report
Get details about report in ArcSight.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Report Full Path (URI)|Specify the URI to the report. Example: /All Reports/ArcSight Foundation/MITRE ATT&CK/Mitre ATT&CK Summary|True|String|None|
|Field 2|The dynamic fields for the query to generate the report|False|String|None|
|Field 3|The dynamic fields for the query to generate the report|False|String|None|
|Field 4|The dynamic fields for the query to generate the report|False|String|None|
|Field 5|The dynamic fields for the query to generate the report|False|String|None|
|Field 6|The dynamic fields for the query to generate the report|False|String|None|
|Field 7|The dynamic fields for the query to generate the report|False|String|None|
|Field 8|The dynamic fields for the query to generate the report|False|String|None|
|Field 9|The dynamic fields for the query to generate the report|False|String|None|
|Field 10|The dynamic fields for the query to generate the report|False|String|None|





#### Change Case Stage
Update the stage of the case in ArcSight.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Case Name|Specify the name of the case for which you want to update the stage.|True|String||
|Stage|Specify a new stage for the case. Possible values: INITIAL, QUEUED, CLOSED, FINAL, and FOLLOW_UP.|True|String||









## Connectors
#### ArcSight - Security Events Connector
Pull correlations from ArcSight. Note: dynamic list works with "name" parameter. Please refer to the doc portal for the configuration setup. This connector is suitable for Saas deployment of Chronicle SOAR and is the recommended one for production use.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|API Root|API root of the ArcSight instance.|True|String|https://{ip}|
|Username|Username of the ArcSight account.|True|String||
|Password|Password of the ArcSight account.|True|Password|*****|
|Report Name|Name of the report that will be used to fetch events.|True|String||
|Fetch Base Events|If enabled, connector will also fetch base events.|False|Boolean|true|
|Lowest Priority To Fetch|Lowest priority that will be used to fetch events. Possible values are in range 1 to 10. If nothing is provided, all events will be ingested.|False|String||
|Max Events To Fetch|How many alerts to process per one connector iteration. Maximum is 1000.|False|Int|100|
|Use dynamic list as a blocklist|If enabled, dynamic lists will be used as a blocklist.|False|Boolean|false|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the ArcSight server is valid.|False|Boolean|false|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|


#### Arcsight ESM Connector
Arcsight ESM Connector

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Server Address|Server address of the ArcSight instance|True|String||
|Username|Username of the ArcSight account|True|String||
|Password|Password of the ArcSight account|True|Password|*****|
|Events Count Limit|How many events to process per one alert|True|Int|15|
|Cases Folder Path|Absolute path to cases. Example: /opt/Correlations|True|String|/opt/Correlations|
|Alerts Count Limit|How many alerts to process per one iteration|True|Int|10|
|Environment Field Name|The name of the environment's field. e.g. event.CustomerURI|True|String|event.CustomerURI|
|Secondary Device Product Field|Secondary field for Device Product|False|String||
|Alert Custom Fields Names|Additional fields that should be added to Siemplify Alert. Example: source_address|False|String||
|Done files retention days|For how many days to leave files in the “Done” folder |True|Int|3|
|Error files retention days|For how many days to leave files in the “Error” folder|True|Int|14|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the ArcSight ESM server is valid.|False|Boolean|false|
|CA Certificate File|Base 64 encoded CA certificate file.|False|String||




