
# Tools

A set of utility actions for data manipulation and common platform tasks to power up playbook capabilities.

Python Version - V3_11


#### Dependencies
| |
|-|
|proto_plus-1.27.0-py3-none-any.whl|
|requests-2.32.5-py3-none-any.whl|
|httplib2-0.31.2-py3-none-any.whl|
|uritemplate-4.2.0-py3-none-any.whl|
|nltk-3.9.1-py3-none-any.whl|
|dnspython-2.7.0-py3-none-any.whl|
|certifi-2026.1.4-py3-none-any.whl|
|anyio-4.12.1-py3-none-any.whl|
|tldextract-5.1.3-py3-none-any.whl|
|typing_extensions-4.15.0-py3-none-any.whl|
|pyasn1_modules-0.4.2-py3-none-any.whl|
|pyopenssl-25.3.0-py3-none-any.whl|
|google_auth-2.47.0-py3-none-any.whl|
|google_api_core-2.29.0-py3-none-any.whl|
|psycopg2_binary-2.9.10-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|requests_toolbelt-1.0.0-py2.py3-none-any.whl|
|charset_normalizer-3.4.4-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|httpcore-1.0.9-py3-none-any.whl|
|google_auth_httplib2-0.3.0-py3-none-any.whl|
|pyparsing-3.3.2-py3-none-any.whl|
|urllib3-2.6.3-py3-none-any.whl|
|click-8.3.1-py3-none-any.whl|
|protobuf-6.33.4-py3-none-any.whl|
|tqdm-4.67.1-py3-none-any.whl|
|filelock-3.20.3-py3-none-any.whl|
|httpx-0.28.1-py3-none-any.whl|
|cryptography-46.0.3-cp311-abi3-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|croniter-6.0.0-py2.py3-none-any.whl|
|google_api_python_client-2.188.0-py3-none-any.whl|
|joblib-1.5.3-py3-none-any.whl|
|pytz-2025.2-py2.py3-none-any.whl|
|pycryptodome-3.23.0-cp37-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|TIPCommon-2.3.9-py3-none-any.whl|
|idna-3.11-py3-none-any.whl|
|googleapis_common_protos-1.72.0-py3-none-any.whl|
|pycparser-3.0-py3-none-any.whl|
|h11-0.16.0-py3-none-any.whl|
|cffi-2.0.0-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|regex-2026.1.15-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|EnvironmentCommon-1.0.3-py3-none-any.whl|
|requests_file-3.0.1-py2.py3-none-any.whl|
|python_dateutil-2.9.0.post0-py2.py3-none-any.whl|
|six-1.17.0-py2.py3-none-any.whl|
|pyasn1-0.6.2-py3-none-any.whl|
|pyspellchecker-0.8.2-py3-none-any.whl|
|rsa-4.9.1-py3-none-any.whl|


## Actions
#### Append to Context Value
Append a value to an existing context property or create a new context property and add the value.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Scope|The scope of the context value. Options: Alert or Case or Global|True|List|Alert|
|Key|The context property key.|True|String||
|Value|The value to append to the context property.|True|String||
|Delimiter|The delimiter for the value of the context property.|True|String|,|





#### Create Entities with Separator
Creates entities and adds them to the requested alert.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Entities Identifiers|The entity or entities to be added to the alert.|True|String|<insert string>|
|Entity Type|Siemplify entity type. Example: HOSTNAME / USERNAME / etc.|True|Entity_Type|HOSTNAME|
|Is Internal|Mark if entities are part of an internal network.|False|Boolean|false|
|Entities Separator|The character to split the Entities Identifiers field by.|True|String|,|
|Enrichment JSON|Enrichment JSOn data|False|Code||
|PrefixForEnrichment|The prefix to be added to the enrichment data.|False|String|None|





#### Add Alert Scoring Information
This action will add an entry to the alert scoring database.  Alert score is based off the ratio: 5 Low = 1 Medium.  3 Medium = 1 High.  2 High = 1 Critical.  Optional tag added to case.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Name|The name of the check being performed on the alert.|True|String||
|Description|The description of the check being performed on the alert.|True|String||
|Severity|The severity.|True|List|Informational|
|Category|The category of the check that was performed.|True|String||
|Source|Optional. The part of the alert that the score was derived from.  Examples are Files, Email, User... |False|String||





#### Delay Playbook Synchronous
This action will temporarily stop a playbook from continuing execution for up to 30 seconds. If you need to delay the playbook for longer, use action "Delay Playbook V2"
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Seconds|Seconds|True|String||





#### Get Case SLA
Gets the Case SLA and critical SLA in multiple formats.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|DateTime Format|Specify the DateTime Format in which the SLA expiration time will be presented by the action. Defaults to "%Y-%m-%d %H:%M:%S"|True|String|%Y-%m-%d %H:%M:%S|





#### Delay Playbook V2
This action will temporarily stop a playbook from completing for a period of time.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Seconds|The amount of seconds to delay the playbook for.|False|String|0|
|Minutes|The amount of minutes to delay the playbook for.|False|String|1|
|Hours|The amount of hours to delay the playbook for.|False|String|0|
|Days|The amount of days to delay the playbook for.|False|String|0|
|Cron Expression|Determines when the playbook should proceed using a cron expression. Will be prioritized over the other parameters.|False|String||





#### Change Case Name
The action changes the case's name (title)
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|New Name|The new name of the case|False|String|None|
|Only If First Alert|If marked as True, will only change the case's name if the action was executed on the first alert in the case|False|Boolean|false|





#### Check Entities Fields In Text
This actions allows to search for a specific field from each entity in the scope (or multiple fields using regex) and compare it with one or more values. The compared values can also go through regex. A match is found if one of the post regex values from the entity enrichment is in one or more values searched in.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|SearchInData|A JSON that represents the string(s) you want to search in[{ "Data": "", "RegEx": ""}]|True|String|[     {         "Data": "[Event.from]",         "RegEx": "(?<=@)[^.]+(?=\\.)"     } ]|
|FieldsInput|A JSON that describes what fields should be tested for[{ "RegexForFieldName": "", "FieldName": "Field name to search", "RegexForFieldValue": ""}]|True|String|[     {         "RegexForFieldName": "",         "FieldName": "body",         "RegexForFieldValue": ""     },     {         "RegexForFieldName": ".*(_url_).*",         "FieldName": "",         "RegexForFieldValue": ""     },     {         "RegexForFieldName": "",         "FieldName": "body",         "RegexForFieldValue": "HostName: (.*?)"     } ]|
|ShouldEnrichEntity|If set to "<VAL>" will also put an enrichment value on the entity to be recognized as "matched" with the value. The key will be "<VAL>"|False|String|domain_matched|
|IsCaseSensitive|Is the field case sensitive |False|Boolean|false|





#### Assign Case to User
This action will assign a user to a case.  
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Case Id|Case to merge with.|True|String||
|Assign To|assign|True|String|@Admin|
|Alert Id|Alert Id|True|String|id|





#### Get Context Value
The action gets a key and value in a specific context (alert or case)
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Scope|Alert or Case or Global|True|List|Alert|
|Key|Key|True|String|Key|





#### Get Integration Instances
Returns all the integration instances for an environment.
Timeout - 600 Seconds





#### Create Entity Relationships
Creates a relationship between the supplied entities and the linked entities.  If the supplied entities do not exist, it will create them.
Supports Siemplify 5.6+ ONLY.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Entity Identifier(s)|Create new or use existing entity identifier or comma-separated list of identifiers (Example: value1, value2, value3)|True|String||
|Entity Identifier(s) Type|Siemplify Entity type. Example: Host Name / User Name / etc.|True|Entity_Type|USERUNIQNAME|
|Connect As|Connect entity identifiers using source, destination, or linked relationship to the target entity identifiers.|True|List|Source|
|Target Entity Type|Connect the entity identifier(s) to entities of this type.  |True|Entity_Type|ADDRESS|
|Target Entity Identifier(s)|Entities in this comma separated list, of the type from Target Entity Type, will be linked to the entities in the Entities Identifier(s) parameter.  |False|String||
|Enrichment JSON|An optional JSON object containing key / value pairs of attributes that can be added to the newly created entities. |False|String|None|
|Separator Character|The character to separate the list of entities in Entity Identifiers and/or Target Entity Identifiers by.  Defaults to comma.|False|String|None|





#### Get Original Alert Json
The action gets the original alert Json (raw data) and presents it as a list of Json result. 
Timeout - 600 Seconds





#### Delay Playbook
This action will temporarily stop a playbook from completing for a period of time.  
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Seconds|The amount of seconds to delay the playbook for.|True|String|0|
|Minutes|The amount of minutes to delay the playbook for.|True|String|1|
|Hours|The amount of hours to delay the playbook for.|True|String|0|
|Days|The amount of days to delay the playbook for.|True|String|0|





#### Get Siemplify Users
This action will return an object containing all users configured in the Siemplify system.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Hide Disabled Users|Hide disabled users from the result.|False|Boolean|true|





#### Get Current Time
Returns the current date and time 
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Datetime Format|The format of the date and time|True|String|%d/%m/%Y %H:%M|





#### Look-A-Like Domains
This action will compare domain entities against the list of domains defined for the environment.  If the domains are similar the entity will be marked as suspicious and enriched with the matching domain.
Timeout - 600 Seconds





#### Search Text
Search for the 'Search For' parameter in the input text or loop through the 'Search For Regex' list and find matches in the input text.  If there is a match, the action will return true.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Text|Enter the text that will be searched.|True|String||
|Search For|Optional: Enter the string that the Text will be searched for.|False|String|None|
|Search For Regex|Optional.  List of regexes that will be used to search the string.  Regex should be wrapped in double quotes.  Supports comma delimited list.|False|String|None|
|Case Sensitive|Should the search be case sensitive?|False|Boolean|false|





#### Set Context Value
The action sets a key and value in a specific context (alert or case)
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Value|Value|True|String|Value|
|Key|Key|True|String|Key|
|Scope|Alert or Case or Global|True|List|Alert|





#### Spell Check String
The Spell Check String action will check the spelling of an input string.  It will output the percent accurate, total words, amount of misspelled words, list of each misspelled word and the correction, and a corrected version of the input string.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|String|The string that will be checked for spelling errors. |True|String||





#### Create Siemplify Task
This action will assign a task to a user or a role.  The task will be related to the case the action ran on.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|SLA (in minutes)|The amount of time (in minutes) the assigned user/role has to respond to the task.|False|String|480|
|Task Content|The details of the task.|True|Content| |
|Assign To|The user or the role the task will be assigned to.|True|User_Repository|Admin|
|Task Title|The title of the task.  Supports Siemplify versions 6.0.0.0 and higher.|False|String|None|
|Due Date|Due date for the task. Expected format ISO8601. If both "Due Date" and "SLA (in minutes)" are set, then "Due Date" parameter will have a priority.|False|String|None|





#### Unflatten JSON
Unflatten a JSON.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|JSON Object|Specify a JSON object that needs to be unflattened|True|String||
|Delimiter|The flattening delimiter used to chain keys with nested values, and should be used to split the keys' names. Leaving empty will separate keys by every value that is not a letter, number or underscore.|False|String|_|





#### Update Alert Score
This will update the alert score by the amount supplied in the 'Input' parameter. 
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Input|The value to increment or decrement the alert score by.|True|String|0|





#### Wait for Playbook to Complete
This action will cause a playbook to wait until another playbook or block, that is running on the same alert, completes.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Playbook Name|The name of the playbook or block.|True|String||





#### Add Comment to Entity Log
This action will add a comment to the Entity Log for each entity in scope in the Entity Explorer.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|User|The user who created the comment.|True|User_Repository|@Administrator|
|Comment|The comment that will be added to the entity log.|True|Content|<insert comment>|





#### Find First Alert
The action will return the identifier of the first alert in a given case
Timeout - 600 Seconds





#### Extract URL Domain
This action enriches all entities with a new field "siemplifytools_extracted_domain" containing the extracted domain out of the entity identifier. If the entity has no domain (file hash for example) it will simply not return anything.
In addition to entities, the user can specify a list of URLs as a parameter and process them, without enriching, naturally.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Separator|Separator string to use to separate URLs|True|String|,|
|URLs|One or more URLs to extract the domain from|False|String|None|
|Extract subdomain|When set to True, the code will also extract the subdomain from the URLs and include it in the result.|False|Boolean|false|





#### Add Or Update Alert Additional Data
The action adds or updates fields in the alert additional data. The result will be all accumulated data that was added to the alert. 
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Json Fields|You can enter either free text (for one variable) or a string representing a JSON (Dict/List - Can be nested)|True|String|{}|





#### Attach Playbook to All Case Alerts
Attach a specific playbook to all alerts in a case
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Playbook Name|Playbook, which should be attached to all alerts|True|String||





#### Get Certificate Details
Getting the certificate of a given URL
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Url to check|Url to check|True|String|expired.badssl.com|





#### Lock Playbook
This action will cause the current playbook to pause until all playbooks from the previous alert complete.
Timeout - 600 Seconds





#### Convert Into Simulated Case

Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Push to Simulated Cases|Full Acuracy|False|Boolean|false|
|Save JSON as Case Wall File|Whether to save the json definition to the case wall for downloading|False|Boolean|true|
|Override Alert Name|Override Alert name in the config for tracking/separation|False|String|None|
|Full path name|Create a name in the full format 'source_product_eventType'|False|Boolean|false|





#### Buffer
The action receives a json and returns it as a json result
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|ResultValue|Result Value input|False|String|None|
|JSON|JSON input|False|String|None|





#### Get Email Templates
Returns all of the email templates in a system.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Template Type|HTML or Standard Template|True|List|Standard|





#### Normalize Entity Enrichment
The action receives a list of keys from the entity and replaces them
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Normalization Data|Enter a  JSON in the format of the example presented below. |True|String|[     {         "entitiy_field_name": "AT_fields_Name",         "new_name": "InternalEnrichment_Name"     },     {         "entitiy_field_name": "AT_fields_Direct-Manager",         "new_name": "InternalEnrichment_DirectManager_Name"     },     {         "entitiy_field_name": "AT_Manager_fields_Work-Email",         "new_name": "InternalEnrichment_DirectManager_Email"     } ]|





#### DNS Lookup
Perform a DNS lookup on an entity.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|DNS Servers|Single or multiple comma separated servers.|True|String|1.1.1.1|
|Data Type|Uses ANY by default; applies only to host entities|True|List|ANY|





#### Ping
Check connectivity
Timeout - 600 Seconds





#### Get Case Data
This action will get all the data from a case and return a JSON result.  The result includes comments, entity information, insights, playbooks that ran, alert information and events.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Case Id|The Case ID to query.  Optional. Will use current case if empty.|False|String|None|
|Fields to Return|Specify a comma-separated list of fields that need to be returned. If nothing is provided, all fields are returned. Getting nested values can be done using "Nested Keys Delimiter" value to chain nested keys and list indexes. For example, if the delimiter is ".": key_1.nested_key_1.0.nested_key_2, key_2, key_3.1.nested_key_1|False|String|None|
|Nested Keys Delimiter|The delimiter to split nested keys. If missing or not provided fetching nested keys is not possible. Cannot be a comma (",")|False|String|.|





#### Check List Subset
Check if one list is a subset of another list.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Original|List of items to check against. Json list or comma separated.|True|String||
|Subset|Subset list.  Json list or comma separated.|True|String||





#### Attach Playbook to Alert
This action can attach a playbook or block to an alert.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Playbook Name|Comma-separated list of playbooks that need to be attached to the alert|True|String||
|Allow Duplicates|If selected, action will allow the same playbook to be attached multiple times to the alert.|False|Boolean|true|





#### Re-Attach Playbook
This action will remove a playbook from a case, delete any result data in the case from that playbook, and re-attach the playbook so it will run again.
Requires installation of PostgreSQL integration, configured to the Shared Environment with an instance name of Siemplify.  See CSM / Support for additional details.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Playbook Name|This is the name of the playbook that will be removed from the case and re-attached.  Once re-attached, it will run again.|True|WFS_Repository|Basic Phishing PB - Zero to Hero|





#### Update Case Description
This action will update the description of the case.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Case Description|The description of the case will be updated to this value.|True|String|<insert value>|








## Jobs

#### Close Cases Based On Search
This job will close all cases based on a search query.  The Search Payload is the payload used in the 'CaseSearchEverything' API call.  To get an example of this value, go to Search in the UI and open Developer Tools.  Search for the cases to delete.  Look for the "CaseSearchEverything" api call in DevTools.  Copy the JSON payload of the POST request and paste in "Search Payload".  The Close Reason should be 0 or 1.   0 = malicious 1  = not malicious.  Root Cause comes from Settings -> Case Data -> Case Close Root Cause

|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|Search Payload|False|String|{}|
|Close Comment|True|String||
|Close Reason|True|Int|1|
|Root Cause|True|String||

#### Tag Untouched Cases
This job will search all open cases, and identify cases that have not been touched in Max Time hours, and apply the tag/tags listed in the tags parameter

|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|Tags|True|String|Open Case Review|
|Unmodified Time|True|Int|8|



