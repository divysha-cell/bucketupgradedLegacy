
# Lists

A set of tools to facilitate managing custom lists within Google SecOps.

Python Version - 3


#### Dependencies
| |
|-|
|proto_plus-1.27.0-py3-none-any.whl|
|requests-2.32.5-py3-none-any.whl|
|TIPCommon-2.3.7-py3-none-any.whl|
|httplib2-0.31.2-py3-none-any.whl|
|uritemplate-4.2.0-py3-none-any.whl|
|certifi-2026.1.4-py3-none-any.whl|
|anyio-4.12.1-py3-none-any.whl|
|typing_extensions-4.15.0-py3-none-any.whl|
|pyasn1_modules-0.4.2-py3-none-any.whl|
|pyopenssl-25.3.0-py3-none-any.whl|
|google_auth-2.47.0-py3-none-any.whl|
|google_api_core-2.29.0-py3-none-any.whl|
|requests_toolbelt-1.0.0-py2.py3-none-any.whl|
|charset_normalizer-3.4.4-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|httpcore-1.0.9-py3-none-any.whl|
|google_auth_httplib2-0.3.0-py3-none-any.whl|
|pyparsing-3.3.2-py3-none-any.whl|
|urllib3-2.6.3-py3-none-any.whl|
|protobuf-6.33.4-py3-none-any.whl|
|httpx-0.28.1-py3-none-any.whl|
|cryptography-46.0.3-cp311-abi3-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|google_api_python_client-2.188.0-py3-none-any.whl|
|pycryptodome-3.23.0-cp37-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|idna-3.11-py3-none-any.whl|
|googleapis_common_protos-1.72.0-py3-none-any.whl|
|pycparser-3.0-py3-none-any.whl|
|h11-0.16.0-py3-none-any.whl|
|cffi-2.0.0-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|EnvironmentCommon-1.0.3-py3-none-any.whl|
|pyasn1-0.6.2-py3-none-any.whl|
|rsa-4.9.1-py3-none-any.whl|


## Actions
#### Remove String from Custom List
The action removes a string from a custom list.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Category|Custom list Category|True|String|WhiteList|
|ListItem|The list item string to add to the custom list.|True|String|cajs3i|



##### JSON Results
```json
[{"Entity": "1.2.3.4", "EntityResult": false}, {"Entity": "google.com", "EntityResult": true}, {"Entity": "yahoo.co.uk", "EntityResult": false}]
```



#### Add String to Custom List
The action adds a string to a custom list.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|ListItem|The list item string to add to the custom list.|True|String|cajs3i|
|Category|Custom list Category|True|String|WhiteList|



##### JSON Results
```json
[{"Entity": "1.2.3.4", "EntityResult": false}, {"Entity": "google.com", "EntityResult": true}, {"Entity": "yahoo.co.uk", "EntityResult": false}]
```



#### Is String In Custom List
The action checks if a specific string exists in a custom list
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|IdentifierList|A list of "strings" to compare against the custom list (for the current environment) in a specific category |True|String|1.2.3.4,google.com,yahoo.co.uk|
|Category|Custom list Category|True|String|WhiteList|



##### JSON Results
```json
[{"Entity": "1.2.3.4", "EntityResult": false}, {"Entity": "google.com", "EntityResult": true}, {"Entity": "yahoo.co.uk", "EntityResult": false}]
```



#### Ping
Check connectivity
Timeout - 600 Seconds



##### JSON Results
```json
{}
```



#### Search Custom Lists
Search a specified string within the records of a custom list. (If no values are provided will return all custom lists records)
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|String to Search|String to search within list values|False|String||
|Categories|Comma separated values|False|String||



##### JSON Results
```json
[{"entityIdentifier": "1.1.1.1", "category": "vuln_scanner", "forDBMigration": false, "environments": ["Default Environment"], "id": 5, "name": "test", "creationTimeUnixTimeInMs": 1673953571935, "modificationTimeUnixTimeInMs": 1673953571935}, {"entityIdentifier": "1.1.1.1", "category": "vuln_scanner", "forDBMigration": false, "environments": ["Default Environment"], "id": 6, "name": "test", "creationTimeUnixTimeInMs": 1673953584305, "modificationTimeUnixTimeInMs": 1673953584305}]
```



#### Search Environment Custom Lists
Search a specified string within the records of an environment's custom list. (If no values are provided will return all custom lists records)
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|String to Search|String to search within list values|False|String||
|Categories|Comma separated values|False|String||



##### JSON Results
```json
[{"entityIdentifier": "1.1.1.1", "category": "vuln_scanner", "forDBMigration": false, "environments": ["Default Environment"], "id": 5, "name": "test", "creationTimeUnixTimeInMs": 1673953571935, "modificationTimeUnixTimeInMs": 1673953571935}, {"entityIdentifier": "1.1.1.1", "category": "vuln_scanner", "forDBMigration": false, "environments": ["Default Environment"], "id": 6, "name": "test", "creationTimeUnixTimeInMs": 1673953584305, "modificationTimeUnixTimeInMs": 1673953584305}]
```









