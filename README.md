# SOC Security Monitoring & Incident Response Project
This project demonstrates the deployment of a virtual RDP honeypot on an Azure VM, the integration of Microsoft Sentinel SIEM for log ingestion, and the creation of custom analytics rules to detect and mitigate cyber threats. It is designed to showcase real-world threat detection and automated incident response.

Features:

    Configured a virtual RDP honeypot on Azure VM to simulate a vulnerable endpoint.
    Integrated with Microsoft Sentinel SIEM using data connectors.
    Designed custom KQL analytics rules for:
        Detecting brute force attacks.
        Identifying suspicious logins.
        Flagging unauthorized access attempts.
    Automated incident generation and SOC monitoring based on threat intelligence.

Setup Instructions:

    Deploy Azure VM as RDP Honeypot:
        Use Windows Server and enable RDP access.
        Restrict access to simulate an attack surface.

    Configure Microsoft Sentinel SIEM:
        Create a Log Analytics Workspace.
        Set up data connectors to ingest Security Events.

    Deploy Custom KQL Rules:
        Use the queries stored in the /queries/ folder:
            rdp-brute-force.kql: Detects brute force attempts based on Event ID 4625.
            suspicious-logins.kql: Flags unusual login attempts.

    Automate Incident Responses:
        Configure alert rules to trigger:
            Blocking IPs using PowerShell (/scripts/response-playbook.ps1).
            Sending SOC notifications.

Technologies Used:

    Microsoft Sentinel SIEM
    Azure Virtual Machines (Windows Server)
    KQL (Kusto Query Language)
    PowerShell
    MITRE ATT&CK Framework (T1110: Brute Force)

Results:

    Detected brute force attempts in real-time.
    Generated automated alerts and incident reports.
    Improved SOC monitoring through actionable intelligence.

Screenshots:
![image](https://github.com/user-attachments/assets/b74cfa9e-640c-48f2-8b46-95cac69c8927)



