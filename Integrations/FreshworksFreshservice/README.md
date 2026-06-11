
# FreshworksFreshservice

Freshservice is a cloud-based IT Help Desk and service management solution that enables organizations to simplify their IT operations. The solution offers features that include a ticketing system, self-service portal and knowledge-base.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root||True|String|https://yourdomain.freshservice.com|
|API Key||True|Password|*****|
|Verify SSL||False|Boolean|true|


#### Dependencies
| |
|-|
|TIPCommon-1.0.12-py2.py3-none-any.whl|
|idna-3.13-py3-none-any.whl|
|urllib3-2.6.3-py3-none-any.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|EnvironmentCommon-1.0.1-py2.py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|
|certifi-2026.4.22-py3-none-any.whl|


## Actions
#### Deactivate Requester
Deactivate Freshservice requester. Note that action is not working on Siemplify entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Requester ID|Specify requester id to deactivate.|True|String||



#### List Requesters
List requesters registered in Freshservice based on the specified search criteria. Note that action is not working on Siemplify entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Requester Email|Specify the email address to return requester records for.|False|String||
|Rows per Page|Specify how many requester records should be returned per page for Freshservice pagination.|False|String|30|
|Start at Page|Specify starting from which page requester records should be returned with Freshservice pagination.|False|String|1|
|Max Rows to Return|Specify how many requester records action should return in total.|False|String|30|





#### Update Agent
Update existing Freshservice Agent. Note that action is not working on Siemplify entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Agent ID|Specify agent id to update.|True|String||
|Email|Specify the email of the agent to update.|False|String||
|First Name|Specify the first name of the agent to update.|False|String||
|Last Name|Specify the last name of the agent to update.|False|String||
|Is occasional|If enabled, agent will be updated as an occasional agent, otherwise it will be a full-time agent.|False|Boolean|false|
|Can See All Tickets From Associated Departments|If enabled, agent will be able to see all tickets from Associated departments.|False|Boolean|false|
|Departments|Specify department names associated with the agent. Parameter accepts multiple values as a comma separated string.|False|String||
|Location|Specify location name associated with the agent.|False|String||
|Group Memberships|Specify group names agent should be a member of.|False|String||
|Roles|Specify roles to add to agent. Parameter accepts multiple values as a comma separated string. Example: {'role_id':170000XXXXX,'assignment_scope': 'entire_helpdesk'}|False|String||
|Job Title|Specify agent job title.|False|String||
|Custom Fields|Specify a JSON object that contains custom fields to add to the agent. Action appends new custom fields to any existing for an agent. Example format: {"key1":"value1","key2":"value2"}|False|String||





#### Update Ticket
Update a Freshservice ticket based on provided action input parameters. Note that if new tags for the ticket are provided, due to the Freshservice API limitations action replaces existing tags in the ticket, not appending new ones to existing. Additionally, if file attachments to add are provided, the total size of the attachments must not exceed 15MB
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Ticket ID|Specify ticket id to update.|True|String||
|Status|Specify new status for the ticket.|False|List|Not Changed|
|Subject|Specify subject field to update.|False|String||
|Description|Specify description field to update.|False|String||
|Requester Email|Specify requester email to update.|False|String||
|Agent Assign To|Specify the agent email to update.|False|String||
|Group Assign To|Specify the group name to update.|False|String||
|Priority|Specify priority to update.|False|List|Not Changed|
|Urgency|Specify urgency to update.|False|List|Not Changed|
|Impact|Specify impact to update.|False|List|Not Changed|
|Tags|Specify tags to replace in the ticket. Parameter accepts multiple values as a comma separated string. Note that due to the Freshservice API limitations action replaces existing tags in the ticket, not appending new ones to existing.|False|String||
|Custom Fields|Specify a JSON object that contains custom fields to add to the ticket. Action appends new custom fields to any existing for a ticket. Example format: {"key1":"value1","key2":"value2"}|False|String||
|File Attachments to Add|Specify the full path for the file to be uploaded with the ticket. Parameter accepts multiple values as a comma separated string. The total size of the attachments must not exceed 15MB|False|String||





#### Create Agent
Create a new Freshservice Agent. Note that action is not working on Siemplify entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Email|Specify the email of the agent to create.|True|String||
|First Name|Specify the first name of the agent to create.|True|String||
|Last Name|Specify the last name of the agent to create.|False|String||
|Is occasional|If enabled, agent will be created as an occasional agent, otherwise full-time agent will be created.|False|Boolean|false|
|Can See All Tickets From Associated Departments|If enabled, agent will be able to see all tickets from Associated departments.|False|Boolean|false|
|Departments|Specify department names associated with the agent. Parameter accepts multiple values as a comma separated string.|False|String||
|Location|Specify location name associated with the agent.|False|String||
|Group Memberships|Specify group names agent should be a member of.|False|String||
|Roles|Specify roles to add to agent. Parameter accepts multiple values as a comma separated string. Example: {'role_id':17000023338,'assignment_scope': 'entire_helpdesk'}|True|String||
|Job Title|Specify agent job title.|False|String||
|Custom Fields|Specify a JSON object that contains custom fields to add to the agent. Action appends new custom fields to any existing for an agent. Example format: {"key1":"value1","key2":"value2"}|False|String||





#### List Agents
List Freshservice agents based on the specified search criteria. Note that action is not working on Siemplify entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Agent Email|Specify the email address to return agent records for.|False|String||
|Agent State|Specify agent states to return.|False|List|All|
|Include not Active Agents|If enabled, results will include not active agent records.|False|Boolean|false|
|Rows per Page|Specify how many agent records should be returned per page for Freshservice pagination.|False|String|30|
|Start at Page|Specify starting from which page agent records should be returned with Freshservice pagination|False|String|1|
|Max Rows to Return|Specify how many agent records action should return in total.|False|String|30|





#### Add Ticket Time Entry
Add a time entry to a Freshservice ticket. Note that action is not working on Siemplify entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Ticket ID|Specify ticket ID to add a time entry for.|True|String||
|Agent Email|Specify agent email for whom to add a ticket time entry.|True|String||
|Note|Specify a note to add to the ticket time entry.|False|String||
|Time Spent|Specify time spent for ticket time entry. Format: {hh:mm}|True|String||
|Billable|If enabled, ticket time entry will be marked as billable.|False|Boolean|false|
|Custom Fields|Specify a JSON object that contains custom fields to add to the ticket time entry. Action appends new custom fields to any existing for ticket time entry. Example format: {"key1":"value1","key2":"value2"}|False|String||





#### List Ticket Time Entries
List Freshservice tickets time entries based on the specified search criteria. Note that action is not working on Siemplify entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Ticket ID|Specify ticket ID to return time entries for.|True|String||
|Agent Email|Specify agent email to list ticket time entries for.|True|String||
|Rows per Page|Specify how many ticket time entries should be returned per page for Freshservice pagination.|False|String|30|
|Start at Page|Specify starting from which page ticket time entries should be returned with Freshservice pagination.|False|String|1|
|Max Rows to Return|Specify how many ticket time entries action should return in total.|False|String|30|





#### Add a Ticket Reply
Add a reply to a Freshservice ticket. Note that action is not working on Siemplify entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Ticket ID|Specify ticket ID to return conversations for.|True|String||
|Reply Text|Specify reply text to add to ticket.|True|String||





#### Add a Ticket Note
Add a note to a Freshservice ticket. Note that action is not working on Siemplify entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Ticket ID|Specify ticket ID to return conversations for.|True|String||
|Note Type|Specify the type of note action should add to the ticket.|False|List|Private|
|Note Text|Specify note text to add to ticket.|True|String||





#### Deactivate Agent
Deactivate Freshservice agent. Note that action is not working on Siemplify entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Agent ID|Specify agent id to deactivate.|True|String||





#### Delete Ticket Time Entry
Delete a time entry for a Freshservice ticket. Note that action is not working on Siemplify entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Ticket ID|Specify ticket ID to delete a time entry for.|True|String||
|Time Entry ID|Specify time entry ID to delete.|True|String||



#### Update Requester
Update existing Freshservice Requester. Note that action is not working on Siemplify entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Requester ID|Specify requester id to update.|True|String||
|Email|Specify the email of the requester to update.|False|String||
|First Name|Specify the first name of the requester to update.|False|String||
|Last Name|Specify the last name of the requester to update.|False|String||
|Can See All Tickets From Associated Departments|If enabled, requester will be able to see all tickets from associated departments.|False|Boolean|false|
|Departments|Specify department names associated with the requester. Parameter accepts multiple values as a comma separated string.|False|String||
|Location|Specify location name associated with the requester.|False|String||
|Job Title|Specify requester job title.|False|String||
|Custom Fields|Specify a JSON object that contains custom fields to add to the requester. Action appends new custom fields to any existing for requester. Example format: {"key1":"value1","key2":"value2"}|False|String||





#### Update Ticket Time Entry
Update a time entry for a Freshservice ticket. Note that action is not working on Siemplify entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Ticket ID|Specify ticket ID to update a time entry for.|True|String||
|Time Entry ID|Specify time entry ID to update.|True|String||
|Agent Email|Specify agent email for whom to change a ticket time entry.|False|String||
|Note|Specify a note for the ticket time entry.|False|String||
|Time Spent|Specify time spent for ticket time entry. Format: {hh:mm}|False|String||
|Billable|If enabled, ticket time entry will be marked as billable.|False|Boolean|false|
|Custom Fields|Specify a JSON object that contains custom fields to add to the ticket time entry. Action appends new custom fields to any existing for ticket time entry. Example format: {"key1":"value1","key2":"value2"}|False|String||





#### Create Ticket
Create a Freshservice ticket. Note: as of now, Freshservice API supports only creation of tickets with the type "Incident" and the ticket's priority is dynamically calculated according to the "Urgency" and "Impact" values, same as in FreshService's UI. Additionally, if file attachments to add are provided, the total size of the attachments must not exceed 15MB.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Subject|Specify subject field for created ticket.|True|String||
|Description|Specify description field for created ticket.|True|String||
|Requester Email|Specify requester email for created ticket.|True|String||
|Agent Assign To|Specify the agent email to assign the ticket to.|False|String||
|Group Assign To|Specify the group name to assign the ticket to.|False|String||
|Department Name|Specify the name of the department for the ticket. This parameter is case sensitive.|False|String||
|Priority|Specify priority to assign to the ticket.|True|List|Medium|
|Urgency|Specify urgency to assign to the ticket.|False|List|Medium|
|Impact|Specify impact to assign to the ticket.|False|List|Medium|
|Tags|Specify tags to assign to the ticket. Parameter accepts multiple values as a comma separated string.|False|String||
|Custom Fields|Specify a JSON object that contains custom fields to add to the ticket. Action appends new custom fields to any existing for a ticket. Example format: {"key1":"value1","key2":"value2"}|False|String||
|File Attachments to Add|Specify the full path for the file to be uploaded with the ticket. Parameter accepts multiple values as a comma separated string. The total size of the attachments must not exceed 15MB|False|String||





#### Create Requester
Create a new Freshservice requester. Note that action is not working on Siemplify entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Email|Specify the email of the requester to create.|True|String||
|First Name|Specify the first name of the requester to create.|True|String||
|Last Name|Specify the last name of the requester to create.|False|String||
|Can See All Tickets From Associated Departments|If enabled, requester will be able to see all tickets from associated departments.|False|Boolean|false|
|Departments|Specify department names associated with the requester. Parameter accepts multiple values as a comma separated string.|False|String||
|Location|Specify location name associated with the requester.|False|String||
|Job Title|Specify requester job title.|False|String||
|Custom Fields|Specify a JSON object that contains custom fields to add to the requester. Action appends new custom fields to any existing for requester. Example format: {"key1":"value1","key2":"value2"}|False|String||





#### List Ticket Conversations
List Freshservice ticket conversations based on the specified search criteria. Note that action is not working on Siemplify entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Start at Page|Specify starting from which page ticket conversations should be returned with Freshservice pagination.|False|String|1|
|Max Rows to Return|Specify how many ticket conversations action should return in total.|False|String|30|
|Ticket ID|Specify ticket ID to return conversations for.|True|String||
|Rows per Page|Specify how many ticket conversations should be returned per page for Freshservice pagination.|False|String|30|





#### List Tickets
List Freshservice tickets base on the specified search criteria. Note that action is not working on Siemplify entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Ticket Type|Specify ticket type to return.|False|List|All|
|Requester|Specify the requester email of tickets to return.|False|String||
|Include Stats|If enabled, action will return additional stats on the tickets.|False|Boolean|False|
|Search for Last X hours|Specify the timeframe to search tickets for.|False|String||
|Rows per Page|Specify how many tickets should be returned per page for Freshservice pagination.|False|String|30|
|Start at Page|Specify starting from which page tickets should be returned with Freshservice pagination.|False|String|1|
|Max Rows to Return|Specify how many tickets action should return in total.|False|String|30|
|Workspace ID|Specify the ID of the workspace that should be used to list tickets. If nothing is provided, the action will list tickets only from the primary workspace. To list tickets from all workspaces provide “0” in the parameter.|False|String||





#### Ping
Test connectivity to the Freshservice instance with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds






## Jobs

#### Freshservice Sync Tickets Conversations Job
Sync conversations (considered both replies and notes) between Siemplify alert's case and corresponding Freshservice ticket. Sync mechanism works in both ways, Siemplify → Freshservice and Freshservice → Siemplify. Note: The job supports Siemplify cases with the "Freshservice" tag only.

|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|API Root|True|String|https://yourdomain.freshservice.com|
|API Key|True|Password|*****|
|Verify SSL|False|Boolean|true|
|Offset time in hours|True|String|24|
|Siemplify Comment Prefix|True|String|SIEMPLIFY:|
|Freshservice Comment Prefix|True|String|Freshservice Comment Sync Job:|
|Conversation Types To Sync|True|String|Replies, Notes|
|Fetch Private Notes?|False|Boolean|false|
|Sync Comment from Siemplify as X|True|String|Private Note|

#### Freshservice Sync Tickets Closure Job
Close tickets in Freshservice if corresponding Siemplify alerts were closed.

|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|API Root|True|String|https://yourdomain.freshservice.com|
|API Key|True|Password|*****|
|Offset time in hours|True|String|24|
|Verify SSL|False|Boolean|true|
|Default Ticket Description|True|String|Ticket is closed by the Siemplify Freshservice Sync Tickets Closure Job.|



## Connectors
#### Freshservice Tickets Connector
Connector can be used to fetch Freshservice tickets to create Siemplify alerts from. Connector whitelist can be used to ingest only specific types of tickets - Incident or Service Request

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|API Root|Freshservice instance API Root.|True|String|https://yourdomain.freshservice.com|
|API Key|Freshservice API Key to use in integration.|True|Password|*****|
|Verify SSL|If enabled, integration will try to verify that API Root is configured with a valid certificate.|False|Boolean|true|
|Offset time in hours|Number of hours before the first connector iteration to retrieve tickets from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|True|Int|24|
|Max Tickets Per Cycle|How many tickets should be processed during one connector run.|True|Int|30|
|Minimum Priority to Fetch|Minimum priority of the ticket to be ingested to Siemplify, for example, Low or Medium. Possible values: Low, Medium, High, Urgent|False|String|Medium|
|Tickets Status to Fetch|Ticket statuses to be ingested to Siemplify. Parameter accepts multiple values as a comma separated string. Possible values: Open, Pending, Resolved, Closed|False|String|Open, Closed|
|Use dynamic list as a blocklist|If enabled, dynamic list will be used as a blocklist.|False|Boolean|false|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|
|Workspace ID|ID of the workspace that should be used to fetch tickets. If nothing is provided, the action will fetch tickets only from the primary workspace. To fetch tickets from all workspaces provide “0” in the parameter.|False|String||




