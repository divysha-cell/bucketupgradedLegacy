
# MicrosoftGraphSecurityTools

Expands on the MicrosoftGraphSecurity integration by providing additional alerting functionality for SOC, along with entity enrichment and remediation actions.
Additional documentation: https://github.com/snags141/SiemplifyIntegration_MicrosoftGraphSecurityTools

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Certificate Password|Optional, if certificate is password-protected, specify the password to open the certificate file.|False|Password|*****|
|Client ID|Client ID from Azure|True|String|clientIdhere|
|Secret ID|Secret ID from Azure|False|Password|*****|
|Tenant ID|Tenant ID from Azure here|True|String|tenantidhere|
|Certificate Path|If authentication based on certificates is  used instead of client secret, specify path to the certificate on Siemplify server|False|String|None|


#### Dependencies
| |
|-|
|typing_extensions-4.14.0-py3-none-any.whl|
|PyJWT-2.10.1-py3-none-any.whl|
|pyopenssl-25.1.0-py3-none-any.whl|
|cryptography-45.0.4-cp311-abi3-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|pycparser-2.22-py3-none-any.whl|
|certifi-2025.6.15-py3-none-any.whl|
|idna-3.10-py3-none-any.whl|
|cffi-1.17.1-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|charset_normalizer-3.4.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|urllib3-2.5.0-py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|


## Actions
#### List Messages
List the messages in a user's mailbox
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Query Parameters|Should begin with '$' - See MS Graph docs for query-parameters. EG: $filter=subject eq 'test'|False|String|None|
|Select Filter|CSV list of fields to return, eg: sender,subject|False|String|None|
|User ID|User ID/userPrincipalName (email)|True|String|john.smith@mail.com|





#### Delete Attachment
Delete an attachment from a user's mailbox.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|User ID|User ID/userPrincipalName (email)|True|String|john.smith@mail.com|
|Message ID|ID of the message|True|String|someb64=|
|Attachment ID|ID of the attachment to delete.|True|String|someb64=|





#### Get User MFA
Search for given user and return MFA stats. Queries a given User Email field including any valid email entities. JSON result will always return your User Email input first at index zero.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Create Insight|Create an insight for each email checked with MFA stats.|False|Boolean|false|
|User Email|Users email address to search for (userPrincipalName). Valid target entities (emails) will also be checked.|True|String|user@email.com|





#### Ping
Test Connectivity
Timeout - 600 Seconds





#### List Attachments
Retrieve a list of attachment objects attached to a message.
https://docs.microsoft.com/en-us/graph/api/message-list-attachments?view=graph-rest-1.0&tabs=http
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|User ID|Either email (userPrincipalName) or ID|True|String|john.smith@mail.com|
|Message ID|ID of message to retrieve attachment list from|False|String|None|





#### Get Message
Get Email Message from a user's inbox
https://docs.microsoft.com/en-us/graph/api/message-get?view=graph-rest-1.0&tabs=http
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|User ID|User ID/userPrincipalName (email)|True|String|john.smith@email.com|
|Message ID|ID of the message to retrieve|True|String|AAMkADhMGAAA=|





#### List Mail Rules
Get all the messageRule objects defined for the user's Inbox.
https://docs.microsoft.com/en-us/graph/api/mailfolder-list-messagerules?view=graph-rest-1.0&tabs=http
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|User ID|User ID/userPrincipalName (email)|True|String|john.smith@mail.com|





#### Delete Message
Delete a message in the specified user's mailbox, or delete a relationship of the message.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Message ID|ID of the message to delete|True|String|someb64=|
|User ID|User ID/userPrincipalName (email) of the user who's mailbox you want to delete a message from. Supports a CSV input to delete from several mailboxes|True|String|john.smith@mail.com|











## Connectors
#### MS365 MFA Alert
Alert on negative changes to user MFA registration. Use the allowlist to prevent alerts for legacy service accounts that don't support MFA, etc.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Tenant ID|Tenant ID from Azure|True|String|x|
|Self Service Reset Alert|Create alert when a user has the ability to self-service reset their password/MFA.|False|Boolean|false|
|Secret ID|Secret ID from Azure|True|Password|*****|
|MFA Registration Alert|Create alert when a user is not registered for MFA. Recommended.|False|Boolean|true|
|Exclude Guests|Exclude guests/external users from alerts (emails containing #EXT#)|False|Boolean|false|
|Client ID|Client ID from Azure|True|String|x|
|Certificate Path|If authentication based on certificates is used instead of client secret, specify path to the certificate on Siemplify server|False|String||
|Certificate Password|Optional, if certificate is password-protected, specify the password to open the certificate file.|False|Password|*****|


#### MS SecureScore Alert
Allows for easy monitoring of Secure Score. Set a threshold and you will be alerted when the score drops below.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Threshold|Specify the Secure Score threshold. If your Secure Score drops below this threshold, an alert will be raised.|False|Int|0|
|Tenant ID|Tenant ID  from Azure|True|String|x|
|Secret ID|Secret ID from Azure|True|Password|*****|
|Default Priority|Set the default priority (-1 to 100). Informative = -1, Low = 40, Medium = 60, High = 80, Critical = 100|True|Int|60|
|Client ID|Client ID from Azure|True|String|x|
|Certificate Path|If authentication based on certificates is used instead of client secret, specify path to the certificate on Siemplify server|False|String||
|Certificate Password|Optional, if certificate is password-protected, specify the password to open the certificate file.|False|Password|*****|




