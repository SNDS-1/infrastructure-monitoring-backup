This project focuses on improving the monitoring, reliability and data protection of a virtualized IT infrastructure.

It is the second phase of a broader infrastructure project and builds upon the environment established in [Project 1 – Lab Active Directory & OPNsense](https://github.com/SNDS-1/Lab-Active-Directory-Opnsense).

The work extends the initial infrastructure with centralized monitoring, alert management, automated backups, restoration testing and Python scripts.
The main objectives are to:
- Monitor the availability and performance of the infrastructure.
- Detect and report service interruptions.
- Protect important configuration and database data through encrypted backups.
- Verify that backed-up data can be restored.
- Use Python to automate basic monitoring and backup checks.
The project is implemented in a virtualized lab environment using several interconnected virtual machines.

The infrastructure includes:
- OPNsense for network management and firewall services.
- Ubuntu Server for Zabbix monitoring, database management and backup operations.
- Windows Server for Active Directory services.
- Windows 11 as a client workstation.
The environment uses separate network segments to organize communication between the different systems.
Technology	Purpose
OPNsense	Firewall and network management
Zabbix 8.0	Infrastructure monitoring and alerting
MariaDB	Zabbix database
Restic	Encrypted backup and restoration
Python 3	Monitoring and automation scripts
Windows Server	Active Directory
Ubuntu Server	Monitoring and backup server
The project is organized around five main areas:
1. Infrastructure monitoring: deployment and configuration of Zabbix to monitor the virtual machines and network equipment.
2. Alert management: creation and testing of alerts through controlled service interruptions.
3. Backup management: implementation of encrypted backups using Restic.
4. Restoration testing: verification of backup availability and data integrity.
5. Python automation: development of scripts for system resource monitoring and backup verification.
Detailed technical information, configuration steps, commands and test results are available in the documentation/ directory.
This project is carried out in a controlled virtual lab environment. The tests demonstrate the main monitoring, backup and restoration procedures within this environment.

The implementation is intended for learning and practical validation. It does not represent a complete production deployment.
This second phase extends the initial infrastructure by introducing monitoring, alerting, backup and automation mechanisms. It provides practical experience in maintaining and improving the reliability of a small IT environment.
