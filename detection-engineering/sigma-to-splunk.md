# Sigma to Splunk Conversion – Brute Force Login

This is the converted Sigma rule logic for use in Splunk.

```spl
sourcetype=apache_access status=401 
| stats count by src_ip 
| where count > 5

---

## ✅ Step 4: Add `mitre-mapping.md`

File:

### 🔽 Paste this:
```markdown
# MITRE ATT&CK Mapping – Detection Engineering

This Sigma rule targets the following ATT&CK technique:

- **Technique ID**: T1110
- **Name**: Brute Force
- **Tactic**: Credential Access
- **Link**: https://attack.mitre.org/techniques/T1110/

Used for detection of brute force attempts via repeated failed logins from a single IP address.
