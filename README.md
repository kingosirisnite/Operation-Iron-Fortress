# Operation Iron Fortress

## Project Overview
Operation Iron Fortress is a personal cybersecurity
home lab designed to develop practical skills in
network security, vulnerability assessment, and
security documentation.

## Lab Environment
## Skills Demonstrated

- Virtualization and isolated lab configuration
- Network connectivity and service enumeration
- Vulnerability identification and validation
- Security risk analysis and documentation
- Git and GitHub version control- Hypervisor: Oracle VirtualBox
- Security Workstation: Kali Linux
- Target System: Metasploitable 2
- Network: Isolated virtual lab
- Version Control: Git

## Security Findings

The following findings were identified during authorized
security assessments of intentionally vulnerable lab systems.

| ID | Finding | Assessment Status | Report |
|---|---|---|---|
| OIF-001 | Anonymous FTP Access Enabled | Confirmed | [View Report](docs/reports/OIF-001-Anonymous-FTP.md) |

### Assessment Methodology

Security assessments follow a structured process:

1. Define the authorized testing scope.
2. Identify accessible hosts and network services.
3. Validate potential security misconfigurations.
4. Assess observed risks and potential impacts.
5. Document findings and recommend remediation.
6. Retest configurations after remediation, when performed.

### Security and Ethical Testing

Operation Iron Fortress is an educational cybersecurity
home lab using isolated, intentionally vulnerable virtual
machines. All assessments are conducted against authorized
training systems.

Raw assessment evidence remains local and is excluded
from the public repository.## Skills Demonstrated
- Virtual machine deployment and configuration
- Virtual network configuration and troubleshooting
- Linux command-line administration
- Network discovery and service enumeration
- Vulnerability identification and validation
- Security evidence collection and documentation
- Git version control

## Completed Exercises

### OIF-001: Anonymous FTP Access
**Target:** Metasploitable 2

**Tools:** Nmap, FTP client

**Finding:** Anonymous FTP authentication was
permitted on the target system.

**Validation:** Successfully authenticated
anonymously and listed the accessible directory.

**Recommendation:** Disable anonymous FTP access
unless specifically required.

## Ethical Use
All security testing is conducted against
authorized systems within a controlled home lab.
