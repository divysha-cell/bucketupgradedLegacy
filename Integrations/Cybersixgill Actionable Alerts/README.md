
# Cybersixgill Actionable Alerts

By integrating Cybersixgill actionable alerts, Google SecOps customers gain a premium,
automated threat intelligence solution based on the most comprehensive data sources from the deep, dark and surface web. It is customizable, enabling users to define key assets relevant to their brand, industry, and geolocation. Users can covertly monitor critical assets such as IP addresses, domains, vulnerabilities, and VIPs for activity on the underground and closed sources - and prioritize, as well as respond to threats directly from the Google SecOps dashboard.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Client Id|Client Id provided by Cybersixgill|True|Password|*****|
|Client Secret|credential provided by cybersixgill|True|Password|*****|


#### Dependencies
| |
|-|
|certifi-2025.6.15-py3-none-any.whl|
|idna-3.10-py3-none-any.whl|
|charset_normalizer-3.4.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|sixgill_clients-0.2.26-py2.py3-none-any.whl|
|urllib3-2.5.0-py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|


## Actions
#### Ping

Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Client Id|Client Id|True|Password|*****|
|Client Secret|Client Secret|True|Password|*****|



##### JSON Results
```json
{}
```









## Connectors
#### Cybersixgill Actionable Alerts


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alerts Limit|number of alerts|True|Integer|50|
|Client Id|Client Id|True|Password|*****|
|Client Secret|Client Secret|True|Password|*****|
|DeviceProductField|The field name used to determine the device product|True|String|Cybersixgill Actionable Alerts|
|EventClassId|The field name used to determine the event name (sub-type)|True|String|Cybersixgill Actionable Alerts|
|Organization id|Org Id|False|String||
|PythonProcessTimeout|The timeout limit (in seconds) for the python process running current script|True|String|30|
|Threat Level|level of threat|False|String||
|Threat Type|type of threat|False|String||




