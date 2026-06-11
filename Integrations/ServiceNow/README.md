
# ServiceNow

An incident ticketing integration exchanges ticket data between your ServiceNow instance and Google SecOps system.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Root|API root of the ServiceNow instance.|True|String|https://{dev-instance}.service-now.com/api/now/v1/|
|Username|Username of the ServiceNow account. Note: "Username" and "Password" need to be provided together to authenticate to API via "password" flow.|False|String||
|Password|Password of the ServiceNow account. Note: "Username" and "Password" need to be provided together to authenticate to API via "password" flow.|False|Password|*****|
|Incident Table|Default table that should be used across actions that work with incidents.|False|String|incident|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the ServiceNow server is valid.|False|Boolean|true|
|Client ID|Client ID of the ServiceNow account. Note: "Client ID" and "Client Secret" need to be provided together to authenticate to API via "client_credentials" flow. If "Refresh Token" is provided, then integration will use "refresh_token" flow.|False|String||
|Client Secret|Client Secret of the ServiceNow account. Note: "Client ID" and "Client Secret" need to be provided together to authenticate to API via "client_credentials" flow. If "Refresh Token" is provided, then integration will use "refresh_token" flow.|False|Password|*****|
|Refresh Token|Refresh Token for the "refresh_token" flow. Note: "Client ID" and "Client Secret" need to be provided.|False|Password|*****|
|Use Oauth Authentication|If enabled, integration will try to use "client_credentials" or "refresh_token" flow.|False|Boolean|false|


#### Dependencies
| |
|-|
|uritemplate-4.1.1-py2.py3-none-any.whl|
|httpx-0.27.2-py3-none-any.whl|
|h11-0.14.0-py3-none-any.whl|
|httplib2-0.22.0-py3-none-any.whl|
|anyio-4.6.2.post1-py3-none-any.whl|
|proto_plus-1.24.0-py3-none-any.whl|
|google_auth-2.36.0-py2.py3-none-any.whl|
|urllib3-2.2.3-py3-none-any.whl|
|pycryptodome-3.21.0-cp36-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|google_auth_httplib2-0.2.0-py2.py3-none-any.whl|
|requests-2.32.3-py3-none-any.whl|
|idna-3.10-py3-none-any.whl|
|EnvironmentCommon-1.0.2-py2.py3-none-any.whl|
|six-1.16.0-py2.py3-none-any.whl|
|httpcore-1.0.6-py3-none-any.whl|
|pyparsing-3.2.0-py3-none-any.whl|
|charset_normalizer-3.3.2-py3-none-any.whl|
|pyasn1_modules-0.4.1-py3-none-any.whl|
|googleapis_common_protos-1.65.0-py2.py3-none-any.whl|
|google_api_core-2.23.0-py3-none-any.whl|
|sniffio-1.3.1-py3-none-any.whl|
|certifi-2024.8.30-py3-none-any.whl|
|rsa-4.9-py3-none-any.whl|
|protobuf-5.28.2-cp38-abi3-manylinux2014_x86_64.whl|
|google_api_python_client-2.151.0-py2.py3-none-any.whl|
|pyasn1-0.6.1-py3-none-any.whl|
|cachetools-5.5.0-py3-none-any.whl|
|TIPCommon-2.2.2-py2.py3-none-any.whl|


## Actions
#### Create Alert Incident
Create an incident related to a Siemplify alert
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Impact|Specify impact of the incident. Possible values: 1 for High, 2 for Medium and 3 for Low.|True|String|1|
|Urgency|Specify urgency of the incident. Possible values: 1 for High, 2 for Medium and 3 for Low.|True|String|1|
|Category|Specify category of the incident.|False|String|None|
|Assignment group ID|Specify full name of the group that was assigned to the incident.|False|String|None|
|Assigned User ID|Specify full name of the user that was assigned to the incident.|False|String|None|
|Description|Specify description of the incident.|False|Content|None|





#### Download Attachments
Download attachments related to a table record in ServiceNow.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Table Name|Specify name of the table, where the record from which you want to download attachments is located. Example: incident.|True|String||
|Record Sys ID|Specify sys id of the record from which you want to download attachment.|True|String||
|Download Folder Path|Specify the absolute folder path, where you want to store the downloaded attachments.|True|String||
|Overwrite|If enabled, action will overwrite files with the same name.|False|Boolean|false|





#### Get Incident
Retrieve information about a ServiceNow incident
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Incident Number|Specify number of the incident. Format: INCxxxxxxx|True|String||





#### Add Comment To Record
Add a comment to a specific table record in ServiceNow. Note: Action is running as async if "Wait For Reply" is enabled, please adjust script timeout value in Siemplify IDE for action as needed.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Table Name|Specify the name of the table to which you want to add a comment or work note. Example: incident.|True|String||
|Type|Specify whether comment or work note should be added to the record.|True|List|Comment|
|Record Sys ID|Specify the record ID to which you want to add a comment or work note.|True|String||
|Text|Specify the content of the comment or work note.|True|String||
|Wait For Reply|If enabled, action will wait for reply. Note: action will track comments, if comments are sent and work notes, if work notes are sent.|False|Boolean|false|





#### Get User Details
Retrieve information about the user by the sys_id or email in ServiceNow.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|User Sys IDs|Specify a comma-separated list of sys_ids of the users for which you want to retrieve details. Example: sys_id_1,sys_id_2|False|String||
|Emails|Specify a comma-separated list of emails of the users for which you want to retrieve details. Example: email1@example.com,email2@example.com|False|String||





#### List Records Related To User
List records from a table related to a user in ServiceNow.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Table Name|Specify name of the table, where you want to search for related records. Example: incident.|True|String||
|Usernames|Specify a comma-separated list of usernames for which you want to retrieve related records.|True|String||
|Max Days Backwards|Specify how many days backwards to fetch related records.|True|String|1|
|Max Records To Return|Specify how many records to return per user. Default: 50|False|String|50|





#### Wait For Comments
Wait for comments related to a specific table record in ServiceNow. Note: Action is running as async, please adjust script timeout value in Siemplify IDE for action as needed.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Table Name|Specify the name of the table in which you want to wait for a comment or work note. Example: incident.|True|String||
|Record Sys ID|Specify the record ID in which you want to wait for a comment or work note.|True|String||
|Type|Specify for what type of object action needs to wait.|True|List|Comment|
|Wait Mode|Specify the wait mode for the action. If "Until Timeout" is selected, action will wait until and return all of the comments in that timeframe. If "Until First Message" is selected, action will wait until a new message appears after action execution. If "Until Specific Text" is selected, action will wait until there is a message that is equal to the string provided in the "Text" parameter. Note: "Text" parameter is mandatory, if "Until Specific Text" is provided.|True|List|Until Timeout|
|Text|Specify the text for which action needs to wait. Note: this parameter is only relevant, if "Until Specific Text" is selected for "Wait Mode" parameter.|False|String||





#### Add Attachment
Add attachment to a table record in ServiceNow.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Table Name|Specify name of the table, where is located the record to which you want to add attachment.|True|String||
|Record Sys ID|Specify sys id of the record to which you want to add attachment.  |True|String||
|File Path|Specify a comma-separated list of absolute paths to the files that need to be attached.|True|String||
|Mode|Specify the mode for the action. If “Add New Attachment” is selected, action will add a new attachment, if it even has the same name. If “Overwrite Existing Attachment” is selected, action will remove other attachments with the same name and add a new attachment.|False|List|Add New Attachment|





#### Get Record Details
Retrieve information about specific table records in ServiceNow.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Table Name|Specify name of the table, where you want to search for the record. Example: incident.|True|String||
|Record Sys ID|Specify the record ID for which you want to retrieve details.|True|String||
|Fields|Specify a comma-separated list of fields that should be returned for that record. If nothing is specified, action will return the default fields for that record. Example: field_1,field_2.|False|String||





#### Add Comment And Wait For Reply
Wait for new comment to be added to the given incident. Action result is the content of the new comments
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Incident Number|Specify number of the incident. Format: INCxxxxxxx|True|String|None|
|Comment|Specify what comment to add to the incident.|True|Content||



#### Get Oauth Token
Get an Oauth refresh token for ServiceNow. Requires: Username, Password, Client ID and Client Secret to be provided in the configuration tab.
Timeout - 600 Seconds





#### Close Incident
Close a ServiceNow incident
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Incident Number|Specify number of the incident. Format: INCxxxxxxx|True|String||
|Close Reason|Specify the reason, why incident was closed.|True|String||
|Resolution Code|Specify the resolution code for the incident.|True|List|Solution provided|
|Close Notes|Specify the close notes for the incident.|True|String||



#### List Record Comments
List comments related to a specific table record in ServiceNow.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Table Name|Specify the name of the table for which you want to list comments or work notes. Example: incident.|True|String||
|Record Sys ID|Specify the record ID for which you want to list comments or work notes.|True|String||
|Type|Specify whether comment or work note should be listed.|True|List|Comment|
|Max Results To Return|Specify how many results to return. Default: 50.|False|String|50|





#### Add Parent Incident
Add the parent incident for the incidents in ServiceNow.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Parent Incident Number|Parent incident number. All of the incidents in the “Child Incident Numbers” parameter will be added as children for the parent incident. Configure this parameter in the following format: INCxxxxxxx|True|String||
|Child Incident Numbers|Comma-separated list of numbers that are related to the incident and used as children for the parent incident. Configure this parameter in the following format: INCxxxxxxx|True|String||





#### Ping
Test Connectivity
Timeout - 600 Seconds



#### Wait For Field Update

Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Table Name|Specify what table should be used to create a record. |True|String|None|
|Record Sys ID|Specify Sys ID of the needed record.|True|String|None|
|Field - Column name|Specify name of the column that is expected to be updated.|True|String|None|
|Field - Values|Specify values that are expected in the column. Example: In Progress,Resolved.|True|String|None|





#### Update Incident
Update incident information
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Incident Number|Specify number of the incident. Format: INCxxxxxxx|True|String||
|Short Description|Specify short description of the incident.|False|String||
|Impact|Specify impact of the incident. Possible values: 1 for High, 2 for Medium and 3 for Low.|False|String||
|Urgency|Specify urgency of the incident. Possible values: 1 for High, 2 for Medium and 3 for Low.|False|String||
|Category|Specify category of the incident.|False|String||
|Assignment group ID|Specify full name of the group that was assigned to the incident.|False|String||
|Assigned User ID|Specify email address or the username of the user that was assigned to the incident.|False|String||
|Description|Specify description of the incident.|False|String||
|Incident State|Status name or status id.|False|String||
|Custom Fields|Specify a comma-separated list of fields and values. Format: field_1:value_1,field_2:value_2. You can also specify a JSON object as input. Note: this parameter has priority and all of the fields will be overwritten with the value that is provided for this parameter. Example: {"field":"value"}|False|String||





#### Get CMDB Record Details
Get detailed CMDB records from the same class in ServiceNow.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Class Name|Specify name of the class, from where you want to list records. Example: cmdb_ci_appl.|True|String||
|Sys ID|Specify a comma-separated list of record sys ids for which you want to retrieve details.|True|String||
|Max Records To Return|Specify how many record relations per type to return.|False|String|50|





#### Get Child Incident Details
Retrieve information about child incidents based on the parent incident in ServiceNow.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Parent Incident Number|Specify a number of the incident for which you want to retrieve child incident details. Format: INCxxxxxxx|True|String||
|Max Child Incident To Return|Specify how many child incidents to return. Default: 50.|False|String|50|





#### Add Comment
Add a comment to a ServiceNow incident
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Incident Number|Specify number of the incident. Format: INCxxxxxxx|True|String||
|Comment|Specify what comment to add to the incident.|True|Content|test|



#### List CMDB Records
List CMDB records from the same class in ServiceNow.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Class Name|Specify name of the class, from where you want to list records. Example: cmdb_ci_appl.|True|String||
|Query Filter|Specify query filter for the results. Visit documentation to get more details. Example of the filter: sys_idLIKE1^sys_idSTARTSWITH0.|False|String||
|Max Records To Return|Specify how many records to return.|False|String|50|





#### Update Record
Update available records in different tables of Service Now.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Table Name|Specify what table should be used to update a record.|False|String|None|
|Object Json Data|Specify JSON data that is needed to update a record.|True|String|None|
|Record Sys ID|Specify Sys ID of the needed record.|True|String|None|





#### Wait For Status Update
ServiceNow - Wait For Status Update
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Incident Number|Specify number of the incident. Format: INCxxxxxxx|True|String|None|
|Statuses|Specify what statuses of the incident are expected. Example: In Progress,Resolved.|True|String|None|





#### Create Incident
Create a new incident in the ServiceNow system
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Short Description|Specify short description of the incident.|True|String||
|Impact|Specify impact of the incident. Possible values: 1 for High, 2 for Medium and 3 for Low.|True|String||
|Urgency|Specify urgency of the incident. Possible values: 1 for High, 2 for Medium and 3 for Low.|True|String||
|Category|Specify category of the incident.|False|String||
|Assignment group ID|Specify full name of the group that was assigned to the incident.|False|String||
|Assigned User ID|Specify full name or the username of the user that was assigned to the incident.|False|String||
|Description|Specify description of the incident.|False|Content||
|Custom Fields|Specify a comma-separated list of fields and values. Format: field_1:value_1,field_2:value_2. You can also specify a JSON object as input. Note: this parameter has priority and all of the fields will be overwritten with the value that is provided for this parameter. Example: {"field":"value"}|False|String||





#### Create Record
Create new records in different tables of Service Now.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Table Name|Specify what table should be used to create a record.|False|String|None|
|Object Json Data|Specify JSON data that is needed to create a record.|False|String|None|








## Jobs

#### Sync Incidents Job
This job will synchronize incidents fields and attachments that are related to case/alerts in ServiceNow. For the job to work, you need to have the "ServiceNow Incident Sync" tag added to the case and "TICKET_ID" context value added to either Case or Alert depending on the parameter "Sync Level". Example of the "TICKET_ID": "INC0000050,INC0000051".

|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|API Root|True|String|https://{dev-instance}.service-now.com/api/now/v1/|
|Username|True|String||
|Password|True|Password|*****|
|Sync Level|True|String|Case|
|Max Hours Backwards|True|Int|24|
|Verify SSL|False|Boolean|true|

#### Sync Table Record Comments By Tag
This job will synchronize comments in ServiceNow table records and Siemplify cases. Additionally, in order for the job to work, it’s required for the case to have 2 tags. First tag should be "ServiceNow {table name}", for example, "ServiceNow incident" and the second should be with the prefix "ServiceNow TicketId: {TICKET_ID}". Example of the "TICKET_ID": "INC0000050,INC0000051".

|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|API Root|True|String|https://{dev-instance}.service-now.com/api/now/v1/|
|Username|True|String||
|Password|True|Password|*****|
|Table Name|True|String||
|Verify SSL|False|Boolean|true|

#### Sync Closed Incidents
This job will synchronize closed ServiceNow incidents and Google SecOps alerts. This job works with ServiceNow incidents that were ingested as alerts and also cases, which contains tag “ServiceNow” and “TICKET_ID” context value with Incident Number inside of it.

|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|Api Root|True|String|https://{dev-instance}.service-now.com/api/now/v1/|
|Username|True|String||
|Password|True|Password|*****|
|Verify SSL|False|Boolean|true|
|Client ID|False|String||
|Client Secret|False|Password|*****|
|Refresh Token|False|Password|*****|
|Use Oauth Authentication|False|Boolean|false|
|Max Hours Backwards|False|Int|24|
|Table Name|True|String||

#### Sync Table Record Comments
This job will synchronize comments in ServiceNow table records and Siemplify cases.

|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|Api Root|True|String|https://{dev-instance}.service-now.com/api/now/v1/|
|Username|True|String||
|Password|True|Password|*****|
|Verify SSL|False|Boolean|true|
|Client ID|False|String||
|Client Secret|False|Password|*****|
|Refresh Token|False|Password|*****|
|Use Oauth Authentication|False|Boolean|false|
|Table Name|True|String||



## Connectors
#### ServiceNow Connector
Fetching incidents from ServiceNow to Siemplify

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Days Backwards|Fetch incidents from 'x' days backwards. e.g. 3|False|Int|5|
|Rule Generator|The field name used to determine the rule generator.|False|String||
|Api Root|https://{dev-instance}.service-now.com/api/now/v1/|True|String||
|Incident Table|This parameter is defining what API root ServiceNow integration is going to use for actions that revolve around incidents. By default the integration uses the “table/incident” path. |False|String|incident|
|Username|Username|True|String||
|Password|Password|True|Password|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the ServiceNow server is valid.|False|Boolean|true|
|Client ID|Client ID of Service Now application. Required for Oauth authentication.|False|String||
|Client Secret|Client Secret of Service Now application. Required for Oauth authentication.|False|Password|*****|
|Refresh Token|Refresh token for Service Now application. Required for Oauth authentication.|False|Password|*****|
|Assignment Group|Name of the assignment group for which you want to ingest records.|False|String||
|Use sys_domain Environment|When enabled, the connector will use the incident's 'sys_domain' from ServiceNow as the environment for the ingested case. If the field doesn't exist, connector will use the environment defined in the 'Environment' parameter.|False|Boolean|true|
|Use Oauth Authentication|If enabled, integration will use Oauth authentication. Parameters “Client ID“, “Client Secret“ and “Refresh Token“ are mandatory.|False|Boolean|false|
|Disable Overflow|If enabled, connector will ignore the overflow mechanism.|False|Boolean|false|
|Max Incidents Per Cycle|Fetch max 'x' incidents. e.g. 10|False|Int|10|
|Server Time Zone|The timezone configured in the server, ex. UTC, Asia/Jerusalem etc.|False|String|UTC|
|Environments Whitelist|The environments (domains) to ingest into Siemplify, comma separated list (env1,env2)|False|String||
|Table Name|The table to fetch from. e.g. incident|False|String||
|Event Name|The name of the event in Siemplify. e.g. ServiceNowEvent|False|String||
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|
|Get User Information|If enabled, connector will additionally retrieve information about the users related to the incident.|False|Boolean|false|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|Boolean|false|




