
# GoogleSecurityCommandCenter

Security management, data risk & compliance monitoring platform to help with vulnerability management. Detect & respond to security vulnerabilities.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|API root of the Google Security Command Center instance.|True|String|https://securitycenter.googleapis.com|
|Organization ID|ID of the organization that should be used in Google Security Command Center integration.|False|String||
|Project ID|ID of the project that should be used in the integration. Takes priority over Organization ID, if both are provided.|False|String||
|Quota Project ID|ID of your Google Cloud project for Google Cloud API usage and billing. If no value is provided, the project ID defined in your Google Cloud service account is used. For this parameter to work, make sure to grant the "Service Usage Consumer" IAM role to your Google Cloud service account.|False|String||
|Location ID|ID of the location that should be used in Google Security Command Center integration. Defaults to ‘global’.|False|String|global|
|User's Service Account|Service account of the Google Security Command Center instance. A full content of the service account JSON file should be provided. This or "Workload Identity Email" must be provided.|False|Password|*****|
|Workload Identity Email|A Service Account Client Email to replace the usage of "User's Service Account", which will be used for Impersonation. Note that the SOAR Service Account must be granted the "Service Account Token Creator" IAM role on the User Service Account.|False|String||
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Google Security Command Center server is valid.|False|Boolean|true|


#### Dependencies
| |
|-|
|uritemplate-4.1.1-py2.py3-none-any.whl|
|idna-3.8-py3-none-any.whl|
|httplib2-0.22.0-py3-none-any.whl|
|protobuf-5.28.0-cp38-abi3-manylinux2014_x86_64.whl|
|google_api_python_client-2.143.0-py2.py3-none-any.whl|
|soupsieve-2.6-py3-none-any.whl|
|proto_plus-1.24.0-py3-none-any.whl|
|urllib3-2.2.2-py3-none-any.whl|
|google_api_core-2.19.2-py3-none-any.whl|
|google_auth_httplib2-0.2.0-py2.py3-none-any.whl|
|beautifulsoup4-4.12.3-py3-none-any.whl|
|TIPCommon-1.1.6.1-py2.py3-none-any.whl|
|requests-2.32.3-py3-none-any.whl|
|pyparsing-3.1.4-py3-none-any.whl|
|google_auth-2.34.0-py2.py3-none-any.whl|
|charset_normalizer-3.3.2-py3-none-any.whl|
|googleapis_common_protos-1.65.0-py2.py3-none-any.whl|
|EnvironmentCommon-1.0.1-py2.py3-none-any.whl|
|pyasn1-0.6.0-py2.py3-none-any.whl|
|certifi-2024.8.30-py3-none-any.whl|
|rsa-4.9-py3-none-any.whl|
|cachetools-5.5.0-py3-none-any.whl|
|pyasn1_modules-0.4.0-py3-none-any.whl|


## Actions
#### List Asset Vulnerabilities
List vulnerabilities related to the entities in Google Security Command Center.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Asset Resource Names|Specify a comma-separated list of resource names of the assets for which you want to return data.|True|String||
|Timeframe|Specify the timeframe for the vulnerabilities/misconfiguration search.|False|List|All Time|
|Record Types|Specify what kind of records should be returned.|False|List|Vulnerabilities + Misconfigurations|
|Output Type|Specify what kind of output should be returned in the JSON result for the asset.|False|List|Statistics|
|Max Records To Return|Specify how many records to return per record type per assets: Default: 50.|False|String|100|





#### Push Finding To Pub-Sub
Utility action that will push the finding to pub/sub. Only available for SCC Enterprise.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Finding Names|Specify a comma-separated list of finding names which you want to push. Note: finding name has the following structure:organizations/{organization_id}/sources/{source_id}/findings/{finding_id}|True|String|organizations/{organization_id}/sources/{source_id}/locations/global/findings/{finding_id}|



#### Update Finding
Update finding in Google Security Command Center.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Finding Name|Specify a comma-separated list of finding names which you want to update. Note: finding name has the following structure: organizations/{organization_id}/sources/{source_id}/findings/{finding_id}|True|String|organizations/{organization_id}/sources/{source_id}/locations/global/findings/{finding_id}|
|Mute Status|Specify the mute status for the finding.|False|List|Select One|
|State Status|Specify the state status for the finding.|False|List|Select One|





#### Get Finding Details
Get details about a finding in Google Security Command Center.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Finding Name|Specify a comma-separated list of finding names for which you want to return details. Note: finding name has the following structure:organizations/{organization_id}/sources/{source_id}/findings/{finding_id}|True|String|organizations/{organization_id}/sources/{source_id}/locations/global/findings/{finding_id}|





#### Ping
Test connectivity to the Google Security Command Center with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds









## Connectors
#### Google Security Command Center - Findings Connector
Pull information about findings from Google Security Command Center. Note: dynamic list filter works with category.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|API Root|API root of the Google Security Command Center instance.|True|String|https://securitycenter.googleapis.com|
|Organization ID|ID of the organization that should be used in Google Security Command Center integration.|False|String||
|Project ID|ID of the project that should be used in Google Security Command Center integration. Takes priority over Organization ID, if both are provided.|False|String||
|Quota Project ID|ID of your Google Cloud project for Google Cloud API usage and billing. If no value is provided, the project ID defined in your Google Cloud service account is used. For this parameter to work, make sure to grant the “Service Usage Consumer” IAM role to your Google Cloud service account.|False|String||
|Location ID|ID of the location that should be used in Google Security Command Center integration. Defaults to ‘global’|False|String|global|
|User's Service Account|Service account of the Google Security Command Center instance. A full content of the service account JSON file should be provided. This or "Workload Identity Email" must be provided.|False|Password|*****|
|Workload Identity Email|A Service Account Client Email to replace the usage of "User's Service Account", which will be used for Impersonation. Note that the SOAR Service Account must be granted the "Service Account Token Creator" IAM role on the User Service Account.|False|String||
|Finding Class Filter|Finding classes that should be ingested. Possible values: Threat, Vulnerability, Misconfiguration, SCC_Error, Observation, Toxic_Combination, Chokepoint.  If nothing is provided, findings from all classes will be ingested.|False|String|Threat,Vulnerability,Misconfiguration,SCC_Error,Observation,Toxic_Combination,Chokepoint|
|Lowest Severity To Fetch|The lowest severity that is used to fetch findings. Possible values: Low, Medium, High, Critical. Note: If finding with undefined severity is ingested, it has the "Fallback Severity" severity, and it will not be filtered out by this parameter. If nothing is provided, findings with all types of severity are ingested.|False|String||
|Fallback Severity|Fallback severity that is used for the finding that has undefined severity. If nothing is provided, the parameter is set to "Medium". Possible values: Low, Medium, High, Critical.|False|String|Medium|
|Max Hours Backwards|Number of hours before the first connector iteration to retrieve findings from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|Int|1|
|Max Findings To Fetch|How many findings to process per one connector iteration. Default: 100. Maximum: 1000.|False|Int|100|
|Use dynamic list as a blacklist|If enabled, dynamic lists will be used as a blacklist.|False|Boolean|false|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Microsoft 365 Defender server is valid.|False|Boolean|true|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




