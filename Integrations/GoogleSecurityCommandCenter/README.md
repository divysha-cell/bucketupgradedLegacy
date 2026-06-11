
# GoogleSecurityCommandCenter

Security management, data risk & compliance monitoring platform to help with vulnerability management. Detect & respond to security vulnerabilities.

Python Version - 3
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



##### JSON Results
```json
[{"asset_identifier":"//compute.googleapis.com/projects/orbital-signal-0000/zones/europe-west1-b/instances/0000","results":{"siemplify_asset_display_name":"asset name","vulnerabilities":{"statistics":{"critical":0,"high":2,"medium":0,"low":0,"severity_unspecified":0},"data":[{"name":"organizations/0000/sources/0000/locations/global/findings/7c21af78xxxxxx","parent":"organizations/0000/sources/0000","resourceName":"//compute.googleapis.com/projects/orbital-signal-0000/zones/europe-west1-b/instances/0000","state":"ACTIVE","category":"OS_VULNERABILITY","externalUri":"https://console.cloud.google.com/compute/instancesDetail/zones/europe-west1-b/instances/0000?project=orbital-signal-0000&tab=os-information","sourceProperties":{"description":"In ReadLogicalParts of basicmbr.cc, there is a possible out of bounds write due to a missing bounds check. This could lead to local escalation of privilege with no additional execution privileges needed. User interaction is not needed for exploitation. Product: Android; Versions: Android-8.1, Android-9, Android-10, Android-11, Android-8.0; Android ID: A-158063095."},"securityMarks":{"name":"organizations/0000/sources/0000/locations/global/findings/7c21af780687xxxxx/securityMarks"},"eventTime":"2022-05-26T21:32:06.391Z","createTime":"2021-09-17T04:21:10.785Z","severity":"HIGH","canonicalName":"projects/0000/sources/0000/findings/7c21af78068xxxx","mute":"UNMUTED","muteAnnotation":"Unmuted by olivierba@google.com","findingClass":"VULNERABILITY","vulnerability":{"cve":{"id":"CVE-2021-0000","references":[{"source":"Distro","uri":"https://security-tracker.debian.org/tracker/CVE-2021-0000"},{"source":"NVD","uri":"https://nvd.nist.gov/vuln/detail/CVE-2021-0000"}],"cvssv3":{"baseScore":6.800000190734863,"attackVector":"ATTACK_VECTOR_PHYSICAL","attackComplexity":"ATTACK_COMPLEXITY_LOW","privilegesRequired":"PRIVILEGES_REQUIRED_NONE","userInteraction":"USER_INTERACTION_NONE","scope":"SCOPE_UNCHANGED","confidentialityImpact":"IMPACT_HIGH","integrityImpact":"IMPACT_HIGH","availabilityImpact":"IMPACT_HIGH"}}},"muteUpdateTime":"2021-11-09T10:10:20.039Z","muteInitiator":"Unmuted by asdasd@google.com","contacts":{"security":{"contacts":[{"email":"asdasd@asd.net"},{"email":"asdasd@asd.net"}]},"technical":{"contacts":[{"email":"asdasd@asd.net"}]}},"description":"In ReadLogicalParts of basicmbr.cc, there is a possible out of bounds write due to a missing bounds check. This could lead to local escalation of privilege with no additional execution privileges needed. User interaction is not needed for exploitation. Product: Android; Versions: Android-8.1, Android-9, Android-10, Android-11, Android-8.0; Android ID: A-158063095."},{"name":"organizations/0000/sources/0000/locations/global/findings/9cce4421744xxxx","parent":"organizations/0000/sources/0000","resourceName":"//compute.googleapis.com/projects/orbital-signal-0000/zones/europe-west1-b/instances/0000","state":"ACTIVE","category":"OS_VULNERABILITY","externalUri":"https://console.cloud.google.com/compute/instancesDetail/zones/europe-west1-b/instances/0000?project=orbital-signal-0000&tab=os-information","sourceProperties":{"description":"In LoadPartitionTable of gpt.cc, there is a possible out of bounds write due to a missing bounds check. This could lead to local escalation of privilege when inserting a malicious USB device, with no additional execution privileges needed. User interaction is not needed for exploitation.Product: AndroidVersions: Android-8.1 Android-9 Android-10 Android-8.0Android ID: A-152874864"},"securityMarks":{"name":"organizations/0000/sources/0000/locations/global/findings/9cce44217440xxxx/securityMarks"},"eventTime":"2022-05-26T21:32:06.391Z","createTime":"2021-09-17T04:21:10.779Z","severity":"HIGH","canonicalName":"projects/0000/sources/0000/findings/9cce4421744xxxxx","mute":"UNMUTED","muteAnnotation":"Unmuted by asdasd@google.com","findingClass":"VULNERABILITY","vulnerability":{"cve":{"id":"CVE-2020-0000","references":[{"source":"Distro","uri":"https://security-tracker.debian.org/tracker/CVE-2020-0000"},{"source":"NVD","uri":"https://nvd.nist.gov/vuln/detail/CVE-2020-0000"}],"cvssv3":{"baseScore":6.800000190734863,"attackVector":"ATTACK_VECTOR_PHYSICAL","attackComplexity":"ATTACK_COMPLEXITY_LOW","privilegesRequired":"PRIVILEGES_REQUIRED_NONE","userInteraction":"USER_INTERACTION_NONE","scope":"SCOPE_UNCHANGED","confidentialityImpact":"IMPACT_HIGH","integrityImpact":"IMPACT_HIGH","availabilityImpact":"IMPACT_HIGH"}}},"muteUpdateTime":"2021-11-09T10:10:20.134Z","muteInitiator":"Unmuted by asdasd@google.com","contacts":{"security":{"contacts":[{"email":"asdasd@asd.net"},{"email":"asdasd@asd.net"}]},"technical":{"contacts":[{"email":"asdasd@asd.net"}]}},"description":"In LoadPartitionTable of gpt.cc, there is a possible out of bounds write due to a missing bounds check. This could lead to local escalation of privilege when inserting a malicious USB device, with no additional execution privileges needed. User interaction is not needed for exploitation.Product: AndroidVersions: Android-8.1 Android-9 Android-10 Android-8.0Android ID: A-152874864"}]},"misconfigurations":{"statistics":{"critical":0,"high":0,"medium":3,"low":0,"severity_unspecified":0},"data":[{"name":"organizations/0000/sources/0000/locations/global/findings/f53c39c15f2xxxx","parent":"organizations/0000/sources/0000","resourceName":"//compute.googleapis.com/projects/orbital-signal-0000/zones/europe-west1-b/instances/0000","state":"ACTIVE","category":"COMPUTE_SECURE_BOOT_DISABLED","externalUri":"https://console.cloud.google.com/compute/instancesDetail/zones/europe-west1-b/instances/csp-linux-01?project=orbital-signal-0000","sourceProperties":{"Recommendation":"Go to https://console.cloud.google.com/compute/instancesDetail/zones/europe-west1-b/instances/csp-linux-01?project=orbital-signal-0000 and click \"Stop\". Once the instance has stopped, scroll down to the \"Shielded VM\" section and check the \"Turn on Secure Boot\" checkbox. Then you can start the instance back up by clicking the \"Start\" button.","ExceptionInstructions":"Add the security mark \"allow_compute_secure_boot_disabled\" to the asset with a value of \"true\" to prevent this finding from being activated again.","Explanation":"Using secure boot helps protect your virtual machines against rootkits, boot- and kernel-level malware. Learn more at: https://cloud.google.com/security/shielded-cloud/shielded-vm","ScannerName":"COMPUTE_INSTANCE_SCANNER","ResourcePath":["projects/orbital-signal-0000/","organizations/0000/"],"compliance_standards":{},"ReactivationCount":0},"securityMarks":{"name":"organizations/0000/sources/0000/locations/global/findings/f53c39c15f2xxxxx/securityMarks"},"eventTime":"2022-04-27T19:03:13.927Z","createTime":"2021-06-11T13:02:26.453Z","severity":"MEDIUM","canonicalName":"projects/0000/sources/0000/locations/global/findings/f53c39c15f2cbxxxxx","mute":"UNDEFINED","findingClass":"MISCONFIGURATION","contacts":{"security":{"contacts":[{"email":"asdasd@asd.net"},{"email":"asdasd@asd.net"}]},"technical":{"contacts":[{"email":"asdasd@asd.net"}]}},"description":"Using secure boot helps protect your virtual machines against rootkits, boot- and kernel-level malware. Learn more at: https://cloud.google.com/security/shielded-cloud/shielded-vm"}]}}}]
```



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



##### JSON Results
```json
[{"finding_name":"organizations/0000/sources/0000/locations/global/findings/asdasd","name":"organizations/0000/sources/0000/findings/asdasd","parent":"organizations/0000/sources/0000","resourceName":"//cloudresourcemanager.googleapis.com/projects/0000","state":"ACTIVE","category":"Discovery: Service Account Self-Investigation","sourceProperties":{"sourceId":{"projectNumber":"0000","customerOrganizationNumber":"0000"},"detectionCategory":{"technique":"discovery","indicator":"audit_log","ruleName":"iam_anomalous_behavior","subRuleName":"service_account_gets_own_iam_policy"},"detectionPriority":"LOW","affectedResources":[{"gcpResourceName":"//cloudresourcemanager.googleapis.com/projects/0000"}],"evidence":[{"sourceLogId":{"projectId":"orbital-signal-0000","resourceContainer":"projects/orbital-signal-0000","timestamp":{"seconds":"1622678907","nanos":448368000},"insertId":"v2rzxxxxx"}}],"properties":{"serviceAccountGetsOwnIamPolicy":{"principalEmail":"prisma-cloud-serv-zlbni@orbital-signal-0000.iam.gserviceaccount.com","projectId":"orbital-signal-0000","callerIp":"52.39.xxx.xxx","callerUserAgent":"Redlock/GCP-MDC/resource-manager/orbital-signal-0000 Google-API-Java-Client Google-HTTP-Java-Client/1.34.0 (gzip),gzip(gfe)","rawUserAgent":"Redlock/GCP-MDC/resource-manager/orbital-signal-0000 Google-API-Java-Client Google-HTTP-Java-Client/1.34.0 (gzip),gzip(gfe)"}},"contextUris":{"mitreUri":{"displayName":"Permission Groups Discovery: Cloud Groups","url":"https://attack.mitre.org/techniques/T0000/0000/"},"cloudLoggingQueryUri":[{"displayName":"Cloud Logging Query Link","url":"https://console.cloud.google.com/logs/query;query=timestamp%3D%222021-06-03T00:08:27.448368Z%22%0AinsertId%3D%22v2xxxxx%22%0Aresource.labels.project_id%3D%22orbital-signal-0000%22?project=orbital-signal-0000"}]}},"securityMarks":{"name":"organizations/0000/sources/0000/findings/hvX6Wwxxxxx/securityMarks"},"eventTime":"2021-06-03T00:08:27.448Z","createTime":"2021-06-03T00:08:31.074Z","severity":"LOW","canonicalName":"projects/0000/sources/0000/findings/hvX6Wwxxxxxx","mute":"UNDEFINED","findingClass":"THREAT","mitreAttack":{"primaryTactic":"DISCOVERY","primaryTechniques":["PERMISSION_GROUPS_DISCOVERY","CLOUD_GROUPS"]}}]
```



#### Get Finding Details
Get details about a finding in Google Security Command Center.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Finding Name|Specify a comma-separated list of finding names for which you want to return details. Note: finding name has the following structure:organizations/{organization_id}/sources/{source_id}/findings/{finding_id}|True|String|organizations/{organization_id}/sources/{source_id}/locations/global/findings/{finding_id}|



##### JSON Results
```json
[{"finding": {"name": "organizations/0000/sources/2569010957496004438/locations/global/findings/96173c0e4f3099e569ff291d07f4b235", "canonicalName": "projects/1111/sources/2569010957496004438/locations/global/findings/96173c0e4f3099e569ff291d07f4b235", "parent": "organizations/0000/sources/2569010957496004438/locations/global", "resourceName": "//storage.googleapis.com/test-123-bucket-123", "caiResource": "//storage.googleapis.com/test-123-bucket-123", "state": "ACTIVE", "category": "PUBLIC_BUCKET_ACL", "externalUri": "https://console.cloud.google.com/storage/browser/test-123-bucket-123;tab=permissions", "sourceProperties": {"Recommendation": "Go to https://console.cloud.google.com/storage/browser/test-123-bucket-123;tab=permissions and remove \"allUsers\" and \"allAuthenticatedUsers\" from the bucket's members.", "ExceptionInstructions": "Add the security mark \"allow_public_bucket_acl\" to the asset with a value of \"true\" to prevent this finding from being activated again.", "Explanation": "This bucket is public and can be accessed by anyone on the Internet. \"allUsers\" represents anyone on the Internet, and \"allAuthenticatedUsers\" represents anyone who is authenticated with a Google account; neither is constrained to users within your organization.", "ScannerName": "STORAGE_SCANNER", "ResourcePath": ["projects/xxx/", "folders/2222/", "folders/842259184804/", "organizations/0000/"], "HasAdminRoles": false, "HasEditRoles": false, "gcloud_remediation": ["gsutil iam ch -d allUsers gs://test-123-bucket-123", "gsutil iam ch -d allAuthenticatedUsers gs://test-123-bucket-123"], "cli_remediation": ["gsutil iam ch -d allUsers gs://test-123-bucket-123", "gsutil iam ch -d allAuthenticatedUsers gs://test-123-bucket-123"], "compliance_standards": {"iso": [{"ids": ["A.14.1.3", "A.8.2.3"]}, {"version": "2022", "ids": ["A.5.10", "A.5.15", "A.8.3", "A.8.4"]}], "hipaa": [{"ids": ["164.308(a)(3)(i)", "164.308(a)(3)(ii)", "164.312(a)(1)"]}], "pci": [{"ids": ["7.1"]}, {"version": "4.0", "ids": ["1.3.1"]}], "cis": [{"version": "1.0", "ids": ["5.1"]}, {"version": "1.1", "ids": ["5.1"]}, {"version": "1.2", "ids": ["5.1"]}, {"version": "1.3", "ids": ["5.1"]}, {"version": "2.0", "ids": ["5.1"]}], "ccm": [{"version": "4", "ids": ["DSP-17"]}], "cisControls": [{"version": "8.0", "ids": ["3.3"]}], "nistCsf": [{"version": "1.0", "ids": ["PR-AC-4"]}], "soc2": [{"version": "2017", "ids": ["CC5.2.3", "CC6.1.3", "CC6.1.7"]}], "nist": [{"ids": ["AC-2"]}, {"version": "r5", "ids": ["AC-3", "AC-5", "AC-6", "MP-2"]}]}, "ReactivationCount": 0}, "securityMarks": {"name": "organizations/0000/sources/2569010957496004438/locations/global/findings/96173c0e4f3099e569ff291d07f4b235/securityMarks", "marks": {"peter": "e2e1"}}, "eventTime": "2024-08-26T13:23:47.148Z", "createTime": "2023-11-28T12:00:40.141Z", "propertyDataTypes": {"HasEditRoles": {"primitiveDataType": "BOOL"}, "ResourcePath": {}, "ReactivationCount": {"primitiveDataType": "NUMBER"}, "Explanation": {"primitiveDataType": "STRING"}, "ScannerName": {"primitiveDataType": "STRING"}, "HasAdminRoles": {"primitiveDataType": "BOOL"}, "compliance_standards": {"structValue": {"fields": {"iso": {}, "hipaa": {}, "pci": {}, "cis": {}, "ccm": {}, "cisControls": {}, "nistCsf": {}, "soc2": {}, "nist": {}}}}, "ExceptionInstructions": {"primitiveDataType": "STRING"}, "Recommendation": {"primitiveDataType": "STRING"}, "gcloud_remediation": {}, "cli_remediation": {}}, "severity": "HIGH", "mute": "UNMUTED", "findingClass": "MISCONFIGURATION", "muteUpdateTime": "2024-02-13T09:19:16.414Z", "externalSystems": {"chronicle_soar": {"name": "organizations/0000/sources/2569010957496004438/findings/96173c0e4f3099e569ff291d07f4b235/externalSystems/chronicle_soar", "externalSystemUpdateTime": "1970-01-01T00:00:00Z", "ticketInfo": {"updateTime": "1970-01-01T00:00:00Z"}, "caseSla": "1970-01-01T00:00:00Z", "caseCreateTime": "1970-01-01T00:00:00Z", "caseCloseTime": "1970-01-01T00:00:00Z"}}, "muteInitiator": "Unmuted by petererdos@google.com", "compliances": [{"standard": "cis", "version": "1.0", "ids": ["5.1"]}, {"standard": "cis", "version": "1.1", "ids": ["5.1"]}, {"standard": "cis", "version": "1.2", "ids": ["5.1"]}, {"standard": "cis", "version": "1.3", "ids": ["5.1"]}, {"standard": "cis", "version": "2.0", "ids": ["5.1"]}, {"standard": "nist", "ids": ["AC-2"]}, {"standard": "nist800-53", "version": "r5", "ids": ["AC-3", "AC-5", "AC-6", "MP-2"]}, {"standard": "pci", "ids": ["7.1"]}, {"standard": "pci-dss", "version": "4.0", "ids": ["1.3.1"]}, {"standard": "iso", "ids": ["A.14.1.3", "A.8.2.3"]}, {"standard": "iso-27001", "version": "2022", "ids": ["A.5.10", "A.5.15", "A.8.3", "A.8.4"]}, {"standard": "ccm", "version": "4", "ids": ["DSP-17"]}, {"standard": "nist-csf", "version": "1.0", "ids": ["PR-AC-4"]}, {"standard": "soc2", "version": "2017", "ids": ["CC5.2.3", "CC6.1.3", "CC6.1.7"]}, {"standard": "hipaa", "ids": ["164.308(a)(3)(i)", "164.308(a)(3)(ii)", "164.312(a)(1)"]}, {"standard": "cis-controls", "version": "8.0", "ids": ["3.3"]}], "parentDisplayName": "Security Health Analytics", "description": "This bucket is public and can be accessed by anyone on the Internet. \"allUsers\" represents anyone on the Internet, and \"allAuthenticatedUsers\" represents anyone who is authenticated with a Google account; neither is constrained to users within your organization.", "attackExposure": {"latestCalculationTime": "2024-09-10T06:58:38.440429Z", "state": "CALCULATED"}, "muteInfo": {"staticMute": {"state": "UNMUTED", "applyTime": "2024-02-13T09:19:16.414Z"}}}, "resource": {"name": "//storage.googleapis.com/test-123-bucket-123", "displayName": "test-123-bucket-123", "type": "google.cloud.storage.Bucket", "cloudProvider": "GOOGLE_CLOUD_PLATFORM", "service": "storage.googleapis.com", "location": "us", "gcpMetadata": {"project": "//cloudresourcemanager.googleapis.com/projects/1111", "projectDisplayName": "xxx", "parent": "//cloudresourcemanager.googleapis.com/projects/1111", "parentDisplayName": "xxx", "folders": [{"resourceFolder": "//cloudresourcemanager.googleapis.com/folders/2222", "resourceFolderDisplayName": "TestNestedFolder123"}, {"resourceFolder": "//cloudresourcemanager.googleapis.com/folders/3333", "resourceFolderDisplayName": "TestFolder123"}], "organization": "organizations/0000"}, "resourcePath": {"nodes": [{"nodeType": "GCP_PROJECT", "id": "projects/1111", "displayName": "xxx"}, {"nodeType": "GCP_FOLDER", "id": "folders/2222", "displayName": "TestNestedFolder123"}, {"nodeType": "GCP_FOLDER", "id": "folders/3333", "displayName": "TestFolder123"}, {"nodeType": "GCP_ORGANIZATION", "id": "organizations/0000"}]}, "resourcePathString": "organizations/0000/folders/842259184804/folders/959004346707/projects/1111", "projectName": "//cloudresourcemanager.googleapis.com/projects/1111", "projectDisplayName": "xxx", "parentName": "//cloudresourcemanager.googleapis.com/projects/2222", "parentDisplayName": "xxx", "folders": [{"resourceFolder": "//cloudresourcemanager.googleapis.com/folders/2222", "resourceFolderDisplayName": "TestNestedFolder123"}, {"resourceFolder": "//cloudresourcemanager.googleapis.com/folders/3333", "resourceFolderDisplayName": "TestFolder123"}], "organization": "organizations/0000"}, "finding_name": "organizations/0000/sources/2569010957496004438/locations/global/findings/96173c0e4f3099e569ff291d07f4b235"}]
```



#### Ping
Test connectivity to the Google Security Command Center with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds









## Connectors
#### Google Security Command Center - Findings Connector
Pull information about findings from Google Security Command Center. Note: dynamic list filter works with category.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|DeviceProductField|Enter the source field name in order to retrieve the Product Field name.|True|String|findingClass|
|EventClassId|Enter the source field name in order to retrieve the Event Field name.|True|String|category|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|PythonProcessTimeout|Timeout limit for the python process running the current script.|True|Integer|180|
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
|Max Hours Backwards|Number of hours before the first connector iteration to retrieve findings from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|Integer|1|
|Max Findings To Fetch|How many findings to process per one connector iteration. Default: 100. Maximum: 1000.|False|Integer|100|
|Use dynamic list as a blacklist|If enabled, dynamic lists will be used as a blacklist.|False|Boolean|false|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Microsoft 365 Defender server is valid.|False|Boolean|true|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




