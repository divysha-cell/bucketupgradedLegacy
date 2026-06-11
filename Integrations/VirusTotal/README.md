
# VirusTotal

VirusTotal is a service that analyzes files and URLs for viruses, worms, trojans and other kinds of malicious content. VirusTotal aggregates many antivirus products and online scan engines to check for viruses that the user's own antivirus may have missed, or to verify against any false positives. Use VirusTotal to investigate suspicious files, domains, URLs, IP addresses, and hashes.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Key||True|Password|*****|
|Verify SSL||False|Boolean|None|


#### Dependencies
| |
|-|
|TIPCommon-1.0.11-py2.py3-none-any.whl|
|paramiko-3.4.0-py3-none-any.whl|
|idna-3.13-py3-none-any.whl|
|cryptography-47.0.0-cp311-abi3-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|urllib3-2.6.3-py3-none-any.whl|
|bcrypt-5.0.0-cp39-abi3-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|pycparser-3.0-py3-none-any.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|cffi-2.0.0-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|pynacl-1.6.2-cp38-abi3-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|requests-2.32.4-py3-none-any.whl|
|certifi-2026.4.22-py3-none-any.whl|


## Actions
#### Get Domain Report
Scan Domain via VirusTotal. *Check online report for full details.
Timeout - 600 Seconds





#### Scan Hash
Scan Hash via VirusTotal. *Mark entity as suspicious and show insights if risk score matches a given threshold.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Threshold|Mark entity as suspicious if number of negative engines is equal or above the given threshold|True|String||
|Rescan after days|Action will fetch the latest result. If the result is older than mentioned days it will automatically rescan the entity|False|String||





#### Scan URL
Scan URL via VirusTotal. *Mark entity as suspicious and show insights if risk score matches a given threshold.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Threshold|Mark entity as suspicious if number of negative engines is equal or above the given threshold|True|String||
|Rescan after days|Action will fetch the latest result. If the result is older than mentioned days it will automatically rescan the entity|False|String||





#### Scan IP
Scan IP via VirusTotal. Returns table of reverse domains and full Json result
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Threshold|Specify the accepted threshold for the detected samples related to the IP address. If the number of engines that marked related samples as malicious is higher than the specified threshold, IP address will be marked as suspicious.|False|String|25|





#### Ping
Test Connectivity
Timeout - 600 Seconds



#### Upload And Scan Files
Upload and scan files via VirusTotal. *Files can be uploaded from remote path (Windows share or Linux remote server).
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Threshold|Entity risk threshold.|True|String||
|File Paths|Target file path.|True|String||
|Linux Server Address|Linux server address(e.g: x.x.x.x).|False|String||
|Linux User|Linux User|False|String||
|Linux Password|Linux Password|False|Password|*****|











