# Web Server Hacking: Metasploitable 2 Case Study

An ethical-hacking project documenting a controlled penetration-testing exercise against the intentionally vulnerable **Metasploitable 2** virtual machine.

## Project overview

This project explored how an exposed and vulnerable FTP service can create a serious security risk. The assessment used Kali Linux as the testing machine and Metasploitable 2 as the target inside an isolated Oracle VM VirtualBox lab.

The report covers:

- Lab setup and scope
- Network reconnaissance and service discovery
- Identification of the `vsftpd 2.3.4` backdoor vulnerability (**CVE-2011-2523**)
- A high-level overview of exploitation using a Metasploit module
- Post-exploitation enumeration and security impact
- Mitigation and hardening recommendations

## Lab environment

| Component | Details |
|---|---|
| Attacker machine | Kali Linux |
| Target machine | Metasploitable 2 |
| Virtualization | Oracle VM VirtualBox |
| Network | Host-only / internal network |
| Target service discussed | FTP on TCP port 21 |
| Vulnerability discussed | CVE-2011-2523, vsftpd 2.3.4 backdoor |

The original report records the target lab address as `192.168.56.101`. This is a private lab address and should not be assumed to identify any live system.

## Key finding

The report identifies a backdoored version of `vsftpd 2.3.4`. In the lab, report obtaining remote shell access through a Metasploit module targeting CVE-2011-2523. The report discusses the potential consequences, including unauthorized command execution, data exposure, and system compromise.

## Recommendations from the project

- Replace the vulnerable service with a trusted, clean, supported version.
- Prefer SFTP where appropriate instead of unencrypted FTP.
- Restrict network access to services to systems that require them.
- Regularly review running services and monitor for suspicious activity.
- Keep systems and software patched and securely configured.

## Repository contents

```text
web-server-hacking-metasploitable2/
├── README.md
├── report/
│   └── web-server-hacking-report.pdf
├── .gitignore
└── LICENSE
```

The complete project report is available at [`report/web-server-hacking-report.pdf`](report/web-server-hacking-report.pdf).

## Scope and responsible-use statement

This work was conducted as an educational exercise in an isolated virtual lab using an intentionally vulnerable target. Do not test systems without explicit authorization. The techniques discussed are intended for legal learning, defensive validation, and security education only.

## Project credit

**Ethical Hacking**  
**Project:** Web Server Hacking  
**Case study:** Metasploitable 2  
**Date stated in report:** January 2026

Refer to the PDF for the original presentation/report and references.
