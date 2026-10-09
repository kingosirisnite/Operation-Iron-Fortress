# OIF-001: Anonymous FTP Access Enabled

## 1. Executive Summary

During an authorized security assessment of an intentionally vulnerable Metasploitable 2 virtual machine, anonymous FTP authentication was successfully validated.

Anonymous FTP access permits users to connect without individual user credentials. Depending on the accessible files and permissions, this configuration may introduce unauthorized information disclosure risks.

No sensitive files were observed during testing, and write permissions were not assessed.

## 2. Assessment Scope

- **Project:** Operation Iron Fortress
- **Finding ID:** OIF-001
- **Assessment Type:** Network Service Configuration Review
- **Target:** Metasploitable 2
- **Service:** FTP (TCP Port 21)
- **Testing Environment:** Isolated VirtualBox Training Lab
- **Finding Status:** Confirmed
- **Remediation Status:** Not Implemented

## 3. Assessment Methodology

1. Verified connectivity between the Kali Linux workstation and the training target.
2. Performed network service enumeration using Nmap.
3. Identified an FTP service operating on TCP port 21.
4. Attempted anonymous FTP authentication.
5. Successfully authenticated and performed a directory listing.
6. Documented the observed behavior and supporting evidence.

## 4. Technical Findings

The FTP service accepted anonymous authentication and permitted directory enumeration.

**Observed results:**

- FTP service detected on TCP port 21.
- Anonymous login succeeded.
- Directory listing returned only the current and parent directory entries.
- No sensitive files were observed.
- File upload or modification permissions were not tested.

## 5. Risk Assessment

**Preliminary Severity: Low (Lab-Specific)**

Anonymous FTP access may allow unauthenticated users to browse content exposed by the FTP service.

The actual severity depends on network exposure, accessible files, business sensitivity, and effective permissions.

No sensitive data disclosure or unauthorized modification was demonstrated.

## 6. Recommended Remediation

1. Disable anonymous FTP authentication unless explicitly required.
2. Require individually assigned user accounts for authorized access.
3. Restrict service accessibility using network controls.
4. Review FTP directory permissions and service logs.
5. Prefer encrypted transfer mechanisms such as SFTP where appropriate.

## 7. Evidence and Validation

Evidence was collected through Nmap service enumeration and an interactive FTP authentication test.

Raw scan results and terminal evidence are retained locally and excluded from the public repository.

The misconfiguration was confirmed. Remediation has not been performed or retested.

## 8. Ethical Testing Statement

All testing was performed within an authorized, isolated cybersecurity training environment using intentionally vulnerable virtual machines. No third-party systems were assessed.
