
# ServiceDeskPlusV3

ServiceDesk Plus is a game changer in turning IT teams from daily fire-fighting to delivering awesome customer service.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Root|None|True|String|http://{IP or FQDN}:8080/api/v3/|
|Api Key|None|True|Password|*****|
|Verify SSL|None|False|Boolean||


#### Dependencies
| |
|-|
|uritemplate-4.1.1-py2.py3-none-any.whl|
|httplib2-0.22.0-py3-none-any.whl|
|google_api_python_client-2.170.0-py3-none-any.whl|
|google_auth-2.40.2-py2.py3-none-any.whl|
|google_api_core-2.24.2-py3-none-any.whl|
|cachetools-5.5.2-py3-none-any.whl|
|pyasn1_modules-0.4.2-py3-none-any.whl|
|googleapis_common_protos-1.70.0-py3-none-any.whl|
|typing_extensions-4.13.2-py3-none-any.whl|
|proto_plus-1.26.1-py3-none-any.whl|
|google_auth_httplib2-0.2.0-py2.py3-none-any.whl|
|requests-2.32.3-py3-none-any.whl|
|httpcore-1.0.9-py3-none-any.whl|
|TIPCommon-2.2.1-py2.py3-none-any.whl|
|idna-3.10-py3-none-any.whl|
|EnvironmentCommon-1.0.2-py2.py3-none-any.whl|
|anyio-4.9.0-py3-none-any.whl|
|httpx-0.28.1-py3-none-any.whl|
|chardet-5.2.0-py3-none-any.whl|
|pycryptodome-3.23.0-cp37-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|pyparsing-3.2.3-py3-none-any.whl|
|urllib3-2.4.0-py3-none-any.whl|
|charset_normalizer-3.4.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|h11-0.16.0-py3-none-any.whl|
|sniffio-1.3.1-py3-none-any.whl|
|pyasn1-0.6.1-py3-none-any.whl|
|protobuf-6.31.1-cp39-abi3-manylinux2014_x86_64.whl|
|certifi-2025.4.26-py3-none-any.whl|
|rsa-4.9.1-py3-none-any.whl|


## Actions
#### Add Note And Wait For Reply
Add a note to a request. Note: Please update the actual time you would like the action to run in the IDE timeout section for this action.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Request ID|The requests' ID.|True|String||
|Note|The note's content.|True|String||
|Show To Requester|Specify whether the note should be shown to the requester or not.|False|Boolean|False|
|Notify Technician|Specify whether the note should be shown to the requester or not |False|Boolean|False|
|Mark First Response|Specify whether this note should be marked as first response|False|Boolean|False|
|Add To Linked Requests|Specify whether this note should be added to the linked requests|False|Boolean|False|





#### Close Request
Close a request
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Request ID|The requests' ID.|True|String||
|Comment|Closing comment.|True|String||
|Resolution Acknowledged|Whether the resolution of the request is acknowledged or not.|False|Boolean|False|





#### Add Note
Add a note to a request
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Request ID|The requests' ID.|True|String||
|Note|The note's content.|True|String||
|Show To Requester|Specify whether the note should be shown to the requester or not.|False|Boolean|False|
|Notify Technician|Specify whether the note should be shown to the requester or not |False|Boolean|False|
|Mark First Response|Specify whether this note should be marked as first response|False|Boolean|False|
|Add To Linked Requests|Specify whether this note should be added to the linked requests|False|Boolean|False|





#### Create Alert Request
Create a request related to a Siemplify alert
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Subject|The subject of the request.|True|String||
|Requester|The requester of the request. If not specified, set to the user of the API key.|True|String||
|Assets|Names of Assets to be associated with the request|False|String||
|Status|The status of the request.|False|String||
|Technician|The name of the technician assigned to the request.|False|String||
|Priority|The priority of the request.|False|String||
|Urgency|The urgency of the request.|False|String||
|Category|The category of the request.|False|String||
|Request Template|The template of the request.|False|String||
|Request Type|The type of the request. i.e: Incident, Service Request, etc.|False|String||
|Due By Time (ms)|The due date of the request in milliseconds.|False|String||
|Mode|The mode in which this request is created.Example : E-mail|False|String||
|Level|The level of the request.|False|String||
|Site|Denotes the site to which this request belongs|False|String||
|Group|Group to which this request belongs|False|String||
|Impact|The impact of the request.|False|String||





#### Create Request
Create a new request
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Subject|The subject of the request.|True|String||
|Requester|The requester of the request. If not specified, set to the user of the API key.|True|String||
|Description|The description of the request.|False|String||
|Assets|Names of Assets to be associated with the request|False|String||
|Status|The status of the request.|False|String||
|Technician|The name of the technician assigned to the request.|False|String||
|Priority|The priority of the request.|False|String||
|Urgency|The urgency of the request.|False|String||
|Category|The category of the request.|False|String||
|Request Template|The template of the request.|False|String||
|Request Type|The type of the request. i.e: Incident, Service Request, etc.|False|String||
|Due By Time (ms)|The due date of the request in milliseconds.|False|String||
|Mode|The mode in which this request is created.Example : E-mail|False|String||
|Level|The level of the request.|False|String||
|Site|Denotes the site to which this request belongs|False|String||
|Group|Group to which this request belongs|False|String||
|Impact|The impact of the request.|False|String||





#### Get Request
Retrieve information about a request In Service Desk Plus.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Request ID|The ID of the request.|True|String||





#### Create Request - Dropdown Lists
Create a new request
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Subject|The subject of the request.|True|String||
|Requester|The requester of the request. If not specified, set to the user of the API key.|True|String||
|Description|The description of the request.|False|String||
|Assets|Names of Assets to be associated with the request|False|String||
|Status|The status of the request.|False|List|None|
|Technician|The name of the technician assigned to the request.|False|String||
|Priority|The priority of the request.|False|List|None|
|Urgency|The urgency of the request.|False|List|None|
|Category|The category of the request.|False|List|None|
|Request Template|The template of the request.|False|String||
|Request Type|The type of the request. i.e: Incident, Service Request, etc.|False|List|None|
|Due By Time (ms)|The due date of the request in milliseconds.|False|String||
|Mode|The mode in which this request is created.Example : E-mail|False|List|None|
|Level|The level of the request.|False|List|None|
|Site|Denotes the site to which this request belongs|False|String||
|Group|Group to which this request belongs|False|String||
|Impact|The impact of the request.|False|List|None|





#### Update Request
Update a ServiceDesk Plus request via it’s ID
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Request ID|The ID of the request to update.|True|String||
|Subject|The subject of the request.|False|String||
|Requester|The requester of the request. If not specified, set to the user of the API key.|False|String||
|Description|The description of the request.|False|String||
|Assets|Names of Assets to be associated with the request|False|String||
|Status|The status of the request.|False|String||
|Technician|The name of the technician assigned to the request.|False|String||
|Priority|The priority of the request.|False|String||
|Urgency|The urgency of the request.|False|String||
|Category|The category of the request.|False|String||
|Request Template|The template of the request.|False|String||
|Request Type|The type of the request. i.e: Incident, Service Request, etc.|False|String||
|Due By Time (ms)|The due date of the request in milliseconds.|False|String||
|Mode|The mode in which this request is created.Example : E-mail|False|String||
|Level|The level of the request.|False|String||
|Site|Denotes the site to which this request belongs|False|String||
|Group|Group to which this request belongs|False|String||
|Impact|The impact of the request.|False|String||





#### Wait For Field Update
Wait for a field of a request ot update to a desired value. Note: Please update the actual time you would like the action to run in the IDE timeout section for this action.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Request ID|The ID of the request.|True|String||
|Values|Desired values for the given field.|True|String||
|Field Name|The name of the field to be updated.|True|String||





#### Wait For Status Update
Wait for the status of a request ot update to a desired status. Note: Please update the actual time you would like the action to run in the IDE timeout section for this action.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Values|Desired values for the given field.|True|String||
|Request ID|The ID of the request.|True|String||





#### Ping
Test connectivity to ServiceDesk Plus instance.
Timeout - 600 Seconds






## Jobs

#### Sync Closed Requests By Tag
This job will synchronize ServiceDeskPlus requests that were created within Siemplify Case playbook and Siemplify cases. Note: in ServiceDeskPlus statuses "Cancelled", "Closed" and "Resolved" are treated as closed. Additionally, in order for the job to work, it’s required for the case to have 2 tags. First tag should be "ServiceDeskPlus" and the second should be with the prefix "ServiceDeskPlus Requests:{request id}".

|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|Api Root|True|String|http://{IP OR FQDN}:8080/api/v3/|
|Api Key|True|Password|*****|
|Max Hours Backwards|False|String|24|
|Verify SSL|False|Boolean|true|



