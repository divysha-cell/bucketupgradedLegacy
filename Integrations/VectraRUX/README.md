
# VectraRUX

Vectra AI’s cloud-native threat detection platform consolidates cloud, data center, networks, and IoT into one view, seamlessly integrating with existing systems. This integration enables investigative and generic actions on the Chronicle SOAR platform, allowing users to implement various use cases on the Vectra Cloud platform. This integration was tested with the APIs of Team Vectra. In case of any queries, please reach out to support@vectra.ai

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|The base URL of the API, used as the entry point for all API requests.|True|String|https://<address>:<port>|
|Client ID|A unique identifier assigned to each client to authenticate and authorize API requests.|True|String|12345|
|Client Secret|A confidential key associated with the client ID, used to authenticate and securely authorize API requests.|True|Password|*****|


#### Dependencies
| |
|-|
|TIPCommon-1.0.12-py2.py3-none-any.whl|
|certifi-2025.6.15-py3-none-any.whl|
|idna-3.10-py3-none-any.whl|
|EnvironmentCommon-1.0.2-py2.py3-none-any.whl|
|chardet-5.2.0-py3-none-any.whl|
|charset_normalizer-3.4.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|urllib3-2.5.0-py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|


## Actions
#### Download PCAP
Download the PCAP file for the given detection ID.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Detection ID|Detection ID to download PCAP file of that detection.|True|String| |





#### Assign Entity
Assign an entity to the given user ID.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Entity ID|Entity ID which will be assigned. Entity can be of type Account or Host.|True|String| |
|Entity Type|Entity can be of type Account or Host.|True|List|Account|
|User ID|User to which assignment will be assigned.|True|String| |





#### Remove Group
Remove members from the given group ID.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Group ID|ID of specific group|True|String|1|
|Members|Comma separated members to remove from group |True|String|test|





#### Describe Entity
Show all the details of an entity for the given ID.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Entity ID|Unique id for Entity to get entity|True|String|0|
|Entity Type|Type of entity either Account or Host|True|List|Account|





#### Mark Entity Fixed
Mark all detections for the entity as fixed.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Entity ID|Unique Entity ID to mark as fixed|True|String| |
|Entity Type|Type can be of Account or Host.|True|List|Account|





#### List Entities
List all the entities based on the query parameters.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Entity Type|Request entities of a specific type, valid values: “account”, “host”.|True|List||
|Order By|Sorts records by fields like last_timestamp, threat_score, and certainty_score. Use “-” for descending order.|False|List||
|Fields|filter the fields wanted to show|False|MultipleChoiceParameter||
|Name|filter based on entity Name|False|String|None|
|State|filter based on State|False|List||
|Last Detection Timestamp GTE|filter based on Last Detection Timestamp GTE|False|String|None|
|Last Detection Timestamp LTE|filter based on Last Detection Timestamp LTE|False|String|None|
|Tags|filter based on Tags(pass comma separated values)|False|String|None|
|Note Modified Timestamp GTE|filter based on Note Modified Timestamp GTE|False|String|None|
|Prioritized|filter based on if the entity is prioritized or not|False|List||
|Limit|Fetch this number of Entities|False|String|None|
|Order|filter based on ascending or descending|False|List||





#### List Outcomes
List all the assignment outcomes.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Limit|Specify the limit for fetching the records.|False|String|None|





#### Update Assignment
Updates the assigned user in the assignment for the given entity.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Entity ID|Entity ID of assignment to update|True|String| N/A|
|Entity Type|Entity Type of entity|True|List||
|User ID|User ID to assign assignment to that user|True|String| N/A|





#### Add Note
Add a note to the given entity ID.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Note|Note to be added to provided entity id and entity type|True|String|This is test note|
|Entity ID|Entity ID in which the note will be added|True|String|101|
|Entity Type|Type of the entity in which the note will be added|True|List|Account|





#### List Detections
List all the detections for the given entity ID.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Detection Category|Filter detections by Detection Category|False|List||
|Threat GTE|Filter detections whose threat is greater then given value|False|String|None|
|Certainty GTE|Filter detections if the certainty is greater or equal to given value|False|String|None|
|Last Timestamp GTE|Filter detections based on timestamp|False|String|None|
|Last Timestamp LTE|Filter detections based on last time stamp|False|String|None|
|Tags|Provide tags with coma separated values to filter detections|False|String|None|
|Entity Type|Type of Entity|False|List||
|Entity ID|ID of entity|False|String|None|
|Is Targeting Key Asset|Filter detections based on if it's targeting key asset or not|False|List||
|Note Modified Timestamp GTE|Filter detections based on note modified timestamp|False|String|None|
|Limit|Number of records to fetch|False|String|None|
|Order|Order records by ascending or descending|False|List||
|Order By|Order records by  last_timestamp, threat_score, and certainty_score|False|List||
|State|Filter detections by State|False|List||
|Detection Type|Filter detections by detection type|False|String|None|





#### Remove Note
Remove a note from the given entity ID.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Entity ID|ID of the Entity from which user wants to remove note.|True|String|101|
|Note ID|ID of the specific note which user wants to remove from the provided entity ID|True|String|1010|
|Entity Type|Type of the entity from user wants to remove note|True|List|Account|





#### Describe Assignment
Show all the details of an assignment for the given ID.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Assignment ID|Unique assignment ID to get assignment|True|String|0|





#### Add Tags
Add tags to the given entity IDs.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Tags|List of the Tags which user wants to add to the account, host or detection.|True|String|test-tag|
|Entity IDs|List of the Entity IDs in which user wants to add Tags|True|String|101|
|Entity Type|The type of the entity in which tags will be added.|True|List|Account|





#### Describe Detection
Show all the details of a detection for the given ID.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Detection ID|Unique ID of detection to get detection.|True|String|0|





#### List Entity Detections
List all the detections for the given entity ID.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Entity ID|Unique ID value of an entity|True|String||
|Entity Type|Type of an entity, It could be either Account or Host.|True|List|Account|
|Limit|Limit for page size.|False|String|None|
|State|State of detections to filter.|True|List|Active|





#### Mark Detection Fixed
Mark the given detections as fixed.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Detection IDs|Comma separated values of IDs|True|String|N/A|





#### Ping
Tests the connectivity of the Chronicle SOAR server to the Vectra platform.
Timeout - 600 Seconds





#### Unmark Detection Fixed
Unmark the given detections as fixed.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Detection IDs|Comma separated values of IDs|True|String|N/A|





#### Assign Group
Add members to the given group ID.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Group ID|ID of specific group|True|String|1|
|Members|Comma separated members to assign to group |True|String|test|





#### List Users
List users based on the query parameters.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Role|Role of user|False|String|None|
|Email|Email of user|False|String|None|
|Last Login GTE|Filter user whose login timestamp is greater or equal|False|String|None|
|Limit|Specify limit for fetching records.|False|String|None|





#### List Groups
List groups based on the query parameters.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Last Modified Timestamp GTE|Last modified timestamp (greater or equal) of group|False|String|None|
|Last Modified By|Username who has modified the group|False|String|None|
|Name|Name of group|False|String|None|
|Type|Type of group|False|List|None|
|Limit|Specify limit for fetching records.|False|String|None|
|Account Names|Comma separated values of account names|False|String|None|
|Domains|Comma separated values of domains|False|String|None|
|Host Ids|Comma separated values of host ids|False|String|None|
|Host Names|Comma separated values of host names|False|String|None|
|Importance|Importance of group|False|List|None|
|IPs|Comma separated values of ips|False|String|None|
|Description|Description of group (case insensitive match)|False|String|None|





#### Remove Assignment
Remove the assignment for the given entity ID.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Entity ID|Entity ID to remove assignment of that entity|True|String|0|
|Entity Type|Entity Type(Account, Host)|True|List|Account|





#### Remove Tags
Remove tags from the given entity ID.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Tags|List of the Tags which user wants to remove from the account, host or detection.|True|String|test-tag|
|Entity ID|Entity IDs from which user wants to remove Tags|True|String|101|
|Entity Type|The type of the entity in which tags will be added.|True|List|Account|





#### Resolve Assignment
Resolve assignment based on the given assignment ID and outcome ID.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Outcome ID|Outcome for resolving an assignment. 1(Benign True Positive), 2(Malicious True Positive), 3(False Positive), (Custom outcome is allowed).|True|String|1|
|Note Title|A note to be added for resolving an assignment in the entity|False|String| |
|Triage As|Triage rule for resolving an assignment in the entity|False|String| |
|Detection IDs|Provide a list of Integer detection IDs separated by commas or a single detection ID in the list.|False|String| |
|Assignment ID|Specify the ID of the assignment.|True|String|0|





#### List Assignments
List all the assignments based on the query parameters.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Accounts IDs|Comma-separated account ids to filter out accounts.|False|String|None|
|Assignees IDs|Comma-separated user ids to filter out accounts.|False|String|None|
|Resolution IDs|Comma-separated outcome ids to filter out accounts.|False|String|None|
|Resolved|Filter by resolved status.[true/false]|False|List|None|
|Created After|Filter by created after the timestamp.Supported formats: 2 minutes, 2 hours, 2 days, 2 weeks, 2 months, 2 years, yyyy-mm-dd, yyyy-mm-ddTHH: MM:SSZ. |False|String|None|
|Limit|Specify the limit for fetching the records.|False|String|None|
|Hosts IDs|Comma-separated host ids to filter out accounts.|False|String| |








## Jobs

#### Vectra RUX - Clear Empty Cases Job
Job to close empty cases and alerts based on the given filters

|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|Max Hours Backwards|False|String|24|
|Environments|True|String|Default Environment|
|Products|True|String|Vectra RUX|



## Connectors
#### Vectra RUX - Entities Connector
The connector retrieves entities and detections from the Vectra RUX platform. Each Vectra entity is mapped to an alert, and the detections associated with the entity are mapped as alert events. The alert grouping rule should be set with the Source Grouping Identifier to attach the updated alert to the same case, and the grouping limit should be set to the maximum possible value.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|The base URL of the API, used as the entry point for all API requests.|True|String|https://<address>:<port>|
|Client ID|A unique identifier assigned to each client to authenticate and authorize API requests.|True|String|12345|
|Client Secret|A confidential key associated with the client ID, used to authenticate and securely authorize API requests.|True|Password|*****|
|Entity Type|Type of the Entity(Account, Host)|True|String|Host|
|Limit|Number of entities to fetch|False|Int||
|Max Hours Backwards|Number of hours before the first connector iteration to retrieve alerts from for the first time. Default: 0|False|Int|0|
|Prioritized|If it is set (present), only entities whose priority score is abovethe configured priority threshold will be included in theresponse|False|Boolean|false|
|Specific Tag|A specific tag to filter results|False|String||




