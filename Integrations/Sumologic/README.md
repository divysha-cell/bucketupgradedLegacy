
# Sumologic

Sumo Logic is a cloud-based Machine data analytics company focusing on security, operations and BI usecases. It provides log management and analytics services that leverage machine-generated big data to deliver real-time IT insights.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Root||True|String|https://{IP}|
|Access ID||True|String||
|Access Key||True|Password|*****|
|Verify SSL||False|Boolean|False|


#### Dependencies
| |
|-|
|idna-3.13-py3-none-any.whl|
|urllib3-2.6.3-py3-none-any.whl|
|TIPCommon-1.0.10-py3-none-any.whl|
|EnvironmentCommon-1.0.0-py3-none-any.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|types_python_dateutil-2.9.0.20260408-py3-none-any.whl|
|arrow-1.3.0-py3-none-any.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|requests-2.32.4-py3-none-any.whl|
|python_dateutil-2.9.0.post0-py2.py3-none-any.whl|
|six-1.17.0-py2.py3-none-any.whl|
|certifi-2026.4.22-py3-none-any.whl|


## Actions
#### Ping
Test Connectivity to Sumologic
Timeout - 600 Seconds



#### Search
Run a query and get search resutls from Sumologic
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Query|Sumologic query to run. e.g: _collector=*|True|String||
|Delete Search Job|If checked, delete the jobs after a search is completed.|False|Boolean|False|
|Since|Start date of the search, ISO-8601 or unixtime (milliseconds). e.g. 1970-01-01T00:00:00. Default: Last 30 days.|False|String||
|To|End date of the search, ISO-8601 or unixtime (milliseconds). e.g. 1970-01-01T00:00:00. Default: now (current utc unixtime).|False|String||
|Limit|Number of results to return. e.g. 10. Default: 25.|False|String||



##### JSON Results
```json
[{"_messageid": "-9223372036854773772", "_messagetime": "1359407049529", "_blockid": "-9223372036854775674", "_sourcecategory": "service", "_format": "plain:atp:o:0:l:29:p:yyyy-MM-dd HH:mm:ss,SSS ZZZZ", "_sourcename": "/Users/some-user/Development/sumo/ops/assemblies/latest/service-20.1-SNAPSHOT/logs/service.log", "_source": "service", "_receipttime": "1359407051885", "_collectorid": "1579", "_sourceid": "1640", "_raw": "2013-01-28 13:04:09,529 -0800 INFO  [module=SERVICE] [logger=com.netflix.config.sources.DynamoDbConfigurationSource] [thread=pollingConfigurationSource] Successfully polled Dynamo for a new configuration based on table:raychaser-chiapetProperties", "_size": "246", "_collector": "local", "_messagecount": "2035", "_sourcehost": "Chiapet.local"}]
```









## Connectors
#### Sumologic Connector
Sumologic Connector

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|DeviceProductField|The field name used to determine the device product. e.g. _type|True|String|device_product|
|EventClassId|The field name used to determine the event name (sub-type). e.g. _source_match_event_id|False|String|_source|
|PythonProcessTimeout|The timeout limit (in seconds) for the python process running current script|True|String|180|
|Api Root|The Sumologic Api root, i.e: https://api.{region}.sumologic.com|True|String||
|Access ID|Sumologic access ID|False|String||
|Access Key|Sumologic access key|False|Password|*****|
|Verify SSL|Whether to use ssl on connection or not|False|Boolean|false|
|Alert Name Field|The name of the field where the alert name is located (flat field path). e.g. _sourcecategory|True|String|_sourcecategory|
|Timestamp Field|The name of the field where the timestamp is located (flat field path). e.g. _receipttime|True|String|_receipttime|
|Environment Field|The name of the field where the environment is located (flat field path). e.g. _collector|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|Indexes|Indexes to get alerts in|False|String|*|
|Alerts Count Limit|Max count of alerts to pull in one cycle. e.g. 20|True|Integer|10|
|Max Days Backwards|Number of days before the first connector iteration to retrieve alerts since. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires. e.g. 3|True|Integer|1|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




