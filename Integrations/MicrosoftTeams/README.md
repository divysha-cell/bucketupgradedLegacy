
# MicrosoftTeams

Microsoft Teams is a platform that combines workplace chat, meetings, notes, and attachments
Quick Guide: you must first register your app at Microsoft App Registration Portal, Configure Microsoft Teams Integration, Run the action 'Get Authorization', Run the action 'Generate Token'.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Login API Root|None|False|String|https://login.microsoftonline.com|
|API Root|None|False|String|https://graph.microsoft.com|
|Client ID|None|True|String||
|Secret ID|None|True|Password|*****|
|Tenant|None|True|String||
|Refresh Token|None|True|Password|*****|
|Redirect URL|None|False|String|http://localhost/|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Microsoft Teams server is valid.|False|Boolean|false|


#### Dependencies
| |
|-|
|requests-2.32.5-py3-none-any.whl|
|protobuf-6.33.5-cp39-abi3-manylinux2014_x86_64.whl|
|httplib2-0.31.2-py3-none-any.whl|
|uritemplate-4.2.0-py3-none-any.whl|
|soupsieve-2.6-py3-none-any.whl|
|anyio-4.12.1-py3-none-any.whl|
|cachetools-5.5.2-py3-none-any.whl|
|typing_extensions-4.15.0-py3-none-any.whl|
|pyasn1_modules-0.4.2-py3-none-any.whl|
|TIPCommon-2.3.3-py3-none-any.whl|
|pyopenssl-25.3.0-py3-none-any.whl|
|google_auth-2.47.0-py3-none-any.whl|
|proto_plus-1.27.1-py3-none-any.whl|
|requests_toolbelt-1.0.0-py2.py3-none-any.whl|
|beautifulsoup4-4.12.3-py3-none-any.whl|
|httpcore-1.0.9-py3-none-any.whl|
|google_auth_httplib2-0.3.0-py3-none-any.whl|
|pyparsing-3.3.2-py3-none-any.whl|
|urllib3-2.6.3-py3-none-any.whl|
|cryptography-46.0.5-cp311-abi3-manylinux_2_34_x86_64.whl|
|EnvironmentCommon-1.0.2-py2.py3-none-any.whl|
|google_api_core-2.30.0-py3-none-any.whl|
|certifi-2026.2.25-py3-none-any.whl|
|httpx-0.28.1-py3-none-any.whl|
|charset_normalizer-3.4.5-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|google_api_python_client-2.188.0-py3-none-any.whl|
|pycryptodome-3.23.0-cp37-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|idna-3.11-py3-none-any.whl|
|googleapis_common_protos-1.73.0-py3-none-any.whl|
|pycparser-3.0-py3-none-any.whl|
|h11-0.16.0-py3-none-any.whl|
|cffi-2.0.0-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|sniffio-1.3.1-py3-none-any.whl|
|pyasn1-0.6.2-py3-none-any.whl|
|rsa-4.9.1-py3-none-any.whl|


## Actions
#### List Chats
List available chats in Teams.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Chat Type|Specify what type of chat should be returned.|False|List|All|
|Filter Key|Specify the key that needs to be used to filter chats.|False|List|Select One|
|Filter Logic|Specify what filter logic should be applied. Filtering logic is working based on the value  provided in the Filter Key parameter.|False|List|Not Specified|
|Filter Value|Specify what value should be used in the filter. If “Equal“ is selected, action will try to find the exact match among results and if “Contains“ is selected, action will try to find results that contain that substring. If nothing is provided in this parameter, the filter will not be applied. Filtering logic is working based on the value  provided in the “Filter Key” parameter.|False|String||
|Max Records To Return|Specify how many records to return. If nothing is provided, action will return 50 records.|False|String|50|





#### Generate Token
Get an access token using the authorization url received in the previous step
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Authorization URL|Use the authorization URL received in the previous step to request an access token.|True|String||



#### Get User Details
Retrieve the properties and relationships of specific user
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Username|Username|True|String||





#### List Channels
Get all channels details that exist in specific team
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Team Name|Team Name|True|String||
|Max Channels To Return|Specify how many channels to return. Default: 50.|False|String|50|





#### Delete Channel
Delete a channel in Microsoft Teams.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Team Name|Specify the name of the team in which you need to delete the channel.|True|String||
|Channel Name|Specify a name of the channel that needs to be deleted.|True|String||



#### Get Authorization
Run the action and browse to the received url
Timeout - 600 Seconds



#### Send Message
Send Message to specific Channel
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Team Name|Team Name|True|String||
|Channel Name|Channel Name|True|String||
|Message|Message|True|String||





#### Add Users To Channel
Add users to the private channel in Microsoft Teams. Supported entities: Username, Email Address (username that matches email regex). Note: only users that are a part of the same team can be added to the channel.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Team Name|Specify the name of the team in which you want to search for the channel.|True|String||
|Channel Name|Specify the name of the channel to which you want to add users.|True|String||



#### Create Channel
Create a channel in Microsoft Teams.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Team Name|Specify the name of the team in which you need to create the channel.|True|String||
|Channel Name|Specify a unique name of the channel.|True|String||
|Channel Type|Specify the type of the channel that needs to be created. Standard channel is accessible to all members of the team, while private channel will require users to be added to it.|True|List|Standard|
|Description|Specify a description for the channel.|False|String||





#### List Teams
Retrieve details of all teams
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Max Teams To Return|Specify how many teams to return. Default: 50.|False|String|50|





#### Ping
Test Connectivity
Timeout - 600 Seconds



#### Remove Users From Channel
Remove users from the private channel in Microsoft Teams. Supported entities: Username, Email Address (username that matches email regex).
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Team Name|Specify the name of the team in which you want to search for the channel.|True|String||
|Channel Name|Specify a name of the channel in which you want to remove users.|True|String||



#### Get Team Details
Retrieve the properties of specific team
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Team Name|Team Name|True|String||





#### List Users
Get all users details
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Max Users To Return|Specify how many users to return. Default: 50.|False|String|50|





#### Create Chat
Create a user chat in Microsoft Teams. Supported entities: Username, Email Address (username that matches email regex). Note: chat will be created for each user.
Timeout - 600 Seconds





#### Send Chat Message
Send a chat message in Microsoft Teams. Note: Action is running as async if “Wait For Reply” is enabled, please adjust script timeout value in Siemplify IDE for action as needed.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Chat ID|Specify the ID of the chat to which you want to send a message.|True|String||
|Text|Specify the content of the message.|True|String||
|Wait For Reply|If enabled, action will wait until reply.|False|Boolean|true|





#### Send User Message
Send a chat message to the user in Microsoft Teams. Supported entities: Username, Email Address (username that matches email regex). Note: Action is running as async if “Wait For Reply” is enabled, please adjust script timeout value in Siemplify IDE for action as needed.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|User Identifiers|Specify a comma-separated list of user identifiers to whom you want to send a message.|False|String||
|Text|Specify the content of the message.|True|String||
|Wait For Reply|If enabled, action will wait until replies from all entities are available.|False|Boolean|true|
|Content Type|Specify the content type for the message.|False|List|Text|
|User Selection|Specify what selection should be used for users. If "From Entities & User Identifiers" is selected, then action will search in both relevant entities and values provided in the "User Identifiers" parameters. If "From Entities" is provided, action will only work with relevant entities and ignore values provided in the "User Identifiers". If "From User Identifiers" is selected, then action will only work with values from "User Identifiers" and "User Identifiers" parameter becomes mandatory.|False|List|From Entities & User Identifiers|





#### Send Message Reply
Send a reply to the channel message in Microsoft Teams.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Team Name|Specify the team to which you want to send the reply.|True|String||
|Channel Name|Specify the channel to which you want to send the reply.|True|String||
|Message ID|Specify the ID of the message to which you want to send the reply.|True|String||
|Content Type|Specify the content type for the message.|False|List|Text|
|Text|Specify the content of the message.|True|String||





#### Wait For Reply
Action waits for the reply to a specified message. Note: You need to be a part of the desired team and channel. Note: Action is running as async, please adjust script timeout value in Chronicle SOAR IDE for action as needed.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Channel Name|Specify name of the channel.|True|String||
|Message ID|Specify ID of the message that is expected to have a reply.|True|String||
|Team Name|Specify name of the team.|True|String||
|Expected Reply|Specify text of the expected reply. If this value is not provided, then action will stop execution on any reply.|False|String||
|Wait Method|Specify the wait method for the action. If "Check First Reply" is selected, action will either return the first reply or compare the first reply with expected value. If "Wait Till Timeout" is selected, action will either wait for the expected value until timeout is reached or return all of the messages that were sent during the timeout period.|False|List|Check First Reply|








## Jobs

#### Refresh Token Renewal Job
Token renewal job should be used to periodically update the refresh token configured for the integration. By default, the refresh token expires every 90 days, making integration unusable upon expiration. It is recommended to run this job every 7 or 14 days to make sure that refresh token will be up to date.

|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|Integration Environments|False|String||



