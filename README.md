# Operation Iron Fortress

**Cybersecurity Home Lab | Vulnerability Assessment | Network Security | GRC Documentation**

## Project Overview

Operation Iron Fortress is an ongoing cybersecurity home lab designed to develop practical skills in network security, vulnerability assessment, security analysis, and risk documentation.

The project uses an authorized virtual environment to identify security misconfigurations, validate findings, assess potential risks, and document remediation recommendations.

## Lab Environment

The lab uses the following technologies:

- Host operating system: Windows
- Virtualization platform: Oracle VirtualBox
- Security workstation: Kali Linux (OIF-KALI-01)
- Training target: Metasploitable 2 (OIF-TARGET-01-VM)
- Isolated lab network: OIF-LAB
- Private lab subnet: 192.168.56.0/24
- Assessment tools: Nmap and FTP client
- Version control: Git and GitHub

Kali Linux uses a NAT adapter for internet connectivity and a separate internal network adapter for authorized testing. The Metasploitable target is connected to the isolated internal network.

## Network Architecture

A reviewed, sanitized network architecture diagram will be added in a future update.

## Skills Demonstrated

- Virtual machine deployment and configuration
- Virtual networking and connectivity troubleshooting
- Linux command-line administration
- Network discovery and service enumeration
- Security misconfiguration identification and validation
- Vulnerability assessment and risk documentation
- Remediation recommendation development
- Git and GitHub version control

## Security Findings

The following finding was identified during authorized testing of an intentionally vulnerable virtual machine.

| Finding ID | Finding | Status | Report |
| --- | --- | --- | --- |
| OIF-001 | Anonymous FTP Access Enabled | Confirmed | [View Report](docs/reports/OIF-001-Anonymous-FTP.md) |

Raw technical evidence is maintained locally and excluded from the public repository.

## Assessment Methodology

1. Define the authorized assessment scope.
2. Establish and validate network connectivity.
3. Identify accessible network services.
4. Investigate and validate potential security misconfigurations.
5. Assess observed risks and potential impacts.
6. Document technical evidence and remediation recommendations.
7. Retest configurations following remediation, when performed.

## Completed Exercises

### OIF-001: Anonymous FTP Access

**Target:** Metasploitable 2

**Service:** FTP (TCP port 21)

**Tools:** Nmap and FTP client

**Observation:** Anonymous FTP authentication was successful.

**Validation:** Anonymous authentication succeeded, and the accessible directory was listed. No sensitive files were observed, and write access was not tested.

**Risk:** Anonymous FTP access may expose files to users without individually assigned credentials, depending on the server configuration and accessible content.

**Recommendation:** Disable anonymous FTP unless specifically required, restrict access, and review authentication and file permissions.

**Remediation status:** Not implemented or retested.

[Read the complete OIF-001 assessment](docs/reports/OIF-001-Anonymous-FTP.md)

## Ethical Use and Information Protection

Operation Iron Fortress is an educational cybersecurity project. Testing is conducted exclusively against authorized, intentionally vulnerable virtual machines in a controlled training environment.

Public documentation excludes passwords, authentication tokens, sensitive personal information, and raw assessment evidence.

No third-party or production systems are included in the assessment scope.

## Future Development

- Publish a reviewed network architecture diagram.
- Expand authorized vulnerability assessments.
- Develop consistent risk-rating documentation.
- Add sanitized technical evidence summaries.
- Document remediation and retesting exercises.
- Build additional defensive security and GRC-focused projects.

## Project Status

**Active — October 2026**

Operation Iron Fortress is an ongoing practical learning and cybersecurity portfolio project.
