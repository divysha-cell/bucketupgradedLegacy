
# Intsights

The only all-in-one external threat protection platform designed to neutralize cyberattacks outside the wire.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Root||True|String|https://<server-address>|
|Account ID||True|String|None|
|Api Key||True|Password|*****|
|Verify SSL||False|Boolean|False|


#### Dependencies
| |
|-|
|idna-3.13-py3-none-any.whl|
|TIPCommon-1.0.12.1-py2.py3-none-any.whl|
|urllib3-2.6.3-py3-none-any.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|types_python_dateutil-2.9.0.20260408-py3-none-any.whl|
|arrow-1.3.0-py3-none-any.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|requests-2.32.4-py3-none-any.whl|
|python_dateutil-2.9.0.post0-py2.py3-none-any.whl|
|six-1.17.0-py2.py3-none-any.whl|
|certifi-2026.4.22-py3-none-any.whl|


## Actions
#### Reopen Alert
Reopen alert in IntSights.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert ID|Specify the ID of the alert which you want to reopen.|True|String||



#### Ask An Analyst
Ask an analyst regarding the alert in IntSights.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert ID|Specify the ID of the alert where you want to ask the analyst.|True|String||
|Comment|Specify the comment for the analyst.|True|String||



#### Search IOCs
Search IOCs
Timeout - 600 Seconds





#### Download Alert CSV
Download CSV file containing information related to alert in IntSights.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert ID|Specify the ID of the alert for which you want to download CSV.|True|String||
|Download Folder Path|Specify the path to the folder, where you want to store the CSV file.|True|String||
|Overwrite|If enabled, action will overwrite the file with the same name.|False|Boolean|false|





#### Assign Alert
Assign alert to an analyst in IntSights.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert ID|Specify the ID of the alert on which you want to change the assignment.|True|String||
|Assignee ID|Specify the ID of the analyst that should be assigned to the alert. Note: If both Assignee ID and Assignee Email Address are specified, action will prioritize Assignee ID.|False|String||
|Assignee Email Address|Specify the email address of the analyst that should be assigned to the alert. Note: If both Assignee ID and Assignee Email Address are specified, action will prioritize Assignee ID.|False|String||



#### Ping
Check connectivity
Timeout - 600 Seconds



#### Close Alert
Close alert in IntSights.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert ID|Specify the ID of the alert which you want to close.|True|String||
|Additional Info|Specify additional information explaining why the alert should be closed.|False|String||
|Rate|Specify the rating of the alert. Maximum is 5.|False|String||
|Reason|Specify the reason why the alert needs to be closed.|True|List|Problem Solved|



#### Add Note
Add a note to the alert in IntSights.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert ID|Specify the ID of the alert to which you want to add a note.|True|String||
|Note|Specify the note for the alert.|True|String||



#### Get Alert Image
Retrieve information about alert images in IntSights.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert Image IDs|Specify the comma-separated list of alert image IDs. Example: id1,id2.|True|String||











## Connectors
#### Intsights Connector


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Root|The api root of the Intsights server|True|String|https://api.intsights.com|
|Account ID|The account ID to login with|True|String||
|Api Key|The API key to login with.|True|Password|*****|
|Verify SSL|Whether to verify the SSL certificate of the server|False|Boolean|FALSE|
|Max Days Backwards|Number of days before the first connector iteration to retrieve alerts from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|True|Int|3|
|Max Alerts Per Cycle|Max number of alerts to fetch per single connector cycle|True|Int|10|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




