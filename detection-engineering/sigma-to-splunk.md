# Sigma to Splunk Conversion – Brute Force Login

This is the converted Sigma rule logic for use in Splunk.

```spl
sourcetype=apache_access status=401 
| stats count by src_ip 
| where count > 5
