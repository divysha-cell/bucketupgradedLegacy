
# PerimeterX

Integration of PerimeterX Code Defender alerting with Google SecOps

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Slack API Key|API Key used to connect to Slack|True|Password|*****|
|Slack Channel|Enter the slack channel name without the preceding "#". If your slack channel name is "#cd_alerts", then enter "cd_alerts"|True|String|cd_alerts|


#### Dependencies
| |
|-|
|certifi-2025.6.15-py3-none-any.whl|
|idna-3.10-py3-none-any.whl|
|charset_normalizer-3.4.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|urllib3-2.5.0-py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|


## Actions
#### Ping
The Ping action is used by Siemplify to test connectivity to slack once you have configured a connector.
Timeout - 600 Seconds



##### JSON Results
```json
{}
```









## Connectors
#### Slack Connector For Code Defender
This connector is used to connect to a Slack Channel that has been configured to receive PerimeterX Code Defender alerts. Any alerts discovered on the channel are imported into Siemplify via this connector.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Slack Channel|Enter the slack channel name without the preceding "#". If your slack channel name is "#cd_alerts", then enter "cd_alerts"|True|String|cd_alerts|
|Slack API Key|API Key used to connect to Slack|True|Password|*****|
|PythonProcessTimeout|The timeout limit (in seconds) for the python process running current script|True|String|30|
|EventClassId|The field name used to determine the event name (sub-type)|True|String|event_type|
|DeviceProductField|The field name used to determine the device product|True|String|PerimterXCodeDefender|




