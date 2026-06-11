
# Phishrod

PhishRod is an integrated & analytics driven solution for phishing readiness, security awareness automation, threat advisory & policy compliance management. It helps organizations to empower end users and cascade the actionable human intelligence across the organization to deter cyber attacks.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|API root of the Phishrod instance.|True|String|https://{instance}.phishrod.co|
|API Key|API Key of the Phishrod account.|True|Password|*****|
|Client ID|Client ID of the Phishrod account.|True|Password|*****|
|Username|Username of the Phishrod account.|True|String||
|Password|Password of the Phishrod account. |True|Password|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Phishrod is valid.|False|Boolean|true|


#### Dependencies
| |
|-|
|idna-3.8-py3-none-any.whl|
|TIPCommon-1.0.12-py2.py3-none-any.whl|
|urllib3-2.2.2-py3-none-any.whl|
|requests-2.32.3-py3-none-any.whl|
|certifi-2024.7.4-py3-none-any.whl|
|chardet-5.2.0-py3-none-any.whl|
|charset_normalizer-3.3.2-py3-none-any.whl|
|EnvironmentCommon-1.0.1-py2.py3-none-any.whl|


## Actions
#### Update Incident
Update an incident in PhishRod.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Incident ID|Specify the ID of the incident that needs to be updated.|True|String||
|Status|Specify the status for the incident.|False|List|Delete|



#### Mark Incident

Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Incident ID|Specify the ID of the incident that needs to be marked.|True|String||
|Status|Specify how the incidents need to be marked.|False|List|Mark For Secondary Analysis|
|Comment|Specify the comment describing the reasons for the incident to be marked.|True|String||



#### Ping
Test connectivity to the PhishRod with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds









## Connectors
#### PhishRod - Incidents Connector
Pull information about incidents from PhishRod. Note: dynamic list filter works with “emailSubject” parameter.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|DeviceProductField|Enter the source field name in order to retrieve the Product Field name.|True|String|Product Name|
|EventClassId|Enter the source field name in order to retrieve the Event Field name.|True|String|Event Field|
|Environment Field Name|Describes the name of the field where the environment name is stored.If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged.Used to allow the user to manipulate the environment field via regex logic.If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|PythonProcessTimeout|Timeout limit for the python process running the current script.|True|Integer|300|
|API Root|API root of the Phishrod instance.|True|String|https://{instance}.phishrod.co|
|API Key|API key of the Phishrod account. |True|Password|*****|
|Client ID|Client ID of the Phishrod account.|True|Password|*****|
|Username|Username of the Phishrod account.|True|String||
|Password|Password of the Phishrod account.|True|Password|*****|
|Alert Severity|Set the severity for the alert based on the incident. Possible values: Informational, Low, Medium, High, Critical.|True|String|Medium|
|Use dynamic list as a blacklist|If enabled, the dynamic list is used as a blacklist.|False|Boolean|false|
|Verify SSL|If enabled, verifies that the SSL certificate for the connection to the PhishRod server is valid.|False|Boolean|true|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




