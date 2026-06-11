
# EclecticIQ

EclecticIQ is a global provider of threat intelligence technology and services.  

The most targeted organizations in the world – including governments and large enterprises – use our platform to automate intelligence management at scale and accelerate collaboration across security teams.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|EclecticIQ URL|Host URL|True|IP|http://eclecticiq.local|
|API Token|API Token to access the IC Platform|True|Password|*****|
|Verify SSL|Verify SSL|False|Boolean|true|


#### Dependencies
| |
|-|
|TIPCommon-1.0.12-py2.py3-none-any.whl|
|certifi-2025.6.15-py3-none-any.whl|
|idna-3.10-py3-none-any.whl|
|chardet-5.2.0-py3-none-any.whl|
|charset_normalizer-3.4.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|urllib3-2.5.0-py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|


## Actions
#### Send Entities to EclecticIQ
By default, this action sends entities to EclecticIQ as sightings. Additionally, users have the option to configure parameters to create an indicator entity.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Group Name|EclecticIQ Intelligence Center Group Name (e.g.:Testing Group)|True|String|Testing Group|
|Create Indicator|If this field is set to true, both a sighting and an indicator will be created. If false, only a sighting will be created in EclecticIQ.|False|Boolean|false|



##### JSON Results
```json
{}
```



#### Ping
This action facilitates testing connectivity with EclecticIQ.
Timeout - 600 Seconds



##### JSON Results
```json
{}
```



#### Enrich Entities
This action helps in  enrichment of entities with EclecticIQ.
Timeout - 600 Seconds



##### JSON Results
```json
[{"Entity": "entity", "EntityResult": {"observable_type": "ipv4", "confidence": "low", "created_at": "2023-09-06T15:00:12.428401+00:00", "last_updated_at": "2024-05-08T06:01:41.413741+00:00", "observable_id": "123", "entities": [{"created_at": "2024-05-08T06:01:41.413741+00:00", "description": "desc", "title": "title", "sources": ["test"], "last_updated_at": "2024-05-08T06:01:41.413741+00:00", "type": "indicator", "tags": ["test"], "estimated_observed_time": "2024-05-08T06:01:41.413741+00:00", "estimated_threat_start_time": "2024-05-08T06:01:41.413741+00:00", "half_life": "7", "platform_link": "http://eclecticic.local/entity"}], "platform_link": "http://eclecticic.local/observable"}}]
```









## Connectors
#### EclecticIQ - Feed Connector
This connector facilitates data retrieval from outgoing feeds configured by users via  parameters

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Token|toekn|True|Password|*****|
|DeviceProductField|The field name used to determine the device product|True|String|EclecticIQ|
|EclecticIQ URL|url|True|String|https://eclecticiq.local|
|EventClassId|The field name used to determine the event name (sub-type)|True|String|Threat Intelligence|
|Outgoing Feed ID|Outgoing Feed ID from which you want to fetch the entities.|True|String|1|
|PythonProcessTimeout|The timeout limit (in seconds) for the python process running current script|True|String|30|
|Verify SSL|verify|False|Boolean|true|




