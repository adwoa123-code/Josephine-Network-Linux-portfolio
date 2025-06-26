# Josephine-Network-Linux-portfolio

Hi! I am Josephine , a Support Engineering graduate with a background in Telecommunications . I am passionate about system uptime, network health, and resolving technical issues with precision and care.

Currently, I am a graduate intern at Ericsson AB branch , where I am gaining practical experience in Support Engineering. Prior to this, I worked in a Network Operations Center (NOC) role at a different organization  where I developed foundational skills in network monitoring, incident handling.

While I am still early in my career, I have a strong drive to learn and grow. I am particularly interested in Support Engineering, DevOps, Cloud Infrastructure, and Cybersecurity but I remain open to wherever my passion and curiosity lead me in the tech world.

My goal is to secure a full-time role where I can apply my skills, grow alongside experienced professionals, and continue learning through real-world challenges. This portfolio is a reflection of the experiences I have gained and the journey I am building  one step at a time, with a hunger to keep evolving.



##PROJECT 1

#NETWORK MONITORING AND ESCALATION - SMART INFRACO LIMITED 


As a NOC Trainee, I monitored backbone and customer links across multiple sites using a custom dashboard.

## Tools Used
- Zabbix :  This is  used to monitor network and system performance metrics in real time, including uptime, latency, and service health.
- 
- Linux tools:They are seen below;
   `ping`- were used to check connectivity and latency between hosts.
   `traceroute`- Identified network path and pinpointed where delays or failures occurred.
   `netstat`-Monitored open ports, active connections, and network statistics on Linux systems.
  
- Manual reporting via Excel:Used for documenting daily monitoring reports, tracking incidents, and maintaining shift handover logs.
- Solarwinds:Assisted in advanced network performance monitoring, alerting, and identifying potential outages or bottlenecks across infrastructure.

## Scenario: VPN Tunnel Downtime
- **Issue Detected**: VPN between HQ and Regional Office down
- **Initial Checks**:
  - `ping` test failed
  - `traceroute` showed packet drop after ISP edge
  - System logs checked using `journalctl` and `dmesg`

##  Escalation
- Notified team lead within 10 minutes.
- Opened ticket via ticketing tool.
- Documented issue in shift handover.
- Continue following up on the issue till my shift is over.

##  Lessons Learned
- Developed rapid troubleshooting instincts
- Understood the flow from issue detection to resolution




#PROJECT 2

#SUPPORT GRADUATE ENGINEER -ERICCSON AB BRANCH


As a Graduate Intern in the Support Engineering team at Ericsson, I was involved in supporting critical network infrastructure for clients. My core responsibility was to assist in the health monitoring of customer nodes, perform basic diagnostics on Linux-based systems, and escalate issues to the relevant engineering teams. This role required real-time responsiveness, attention to detail, and the ability to interpret system logs and service behavior accurately.

This project highlights some of the recurring tasks I handled during my internship, including:

- Verifying service availability on remote nodes
- Analyzing system logs for fault patterns
- Identifying and reporting non-functional or misbehaving components
- Collaborating with specialized teams  for resolution

Though I was in a learning phase, this experience helped me sharpen my troubleshooting skills and gain confidence working in a real-world support environment — especially in Linux-based systems and networked environments.


##Tools & Environments

- **Linux (CentOS)** – Used for system log reviews, service status checks, disk usage monitoring, and basic CLI troubleshooting tasks.
- **Ericsson Internal Platforms** – Accessed to monitor customer node health, retrieve system logs, and track alerts or status changes.
- **Firefox** – Used to log into internal dashboards, remote monitoring platforms, and web-based interfaces for node access.
- **ILO (Integrated Lights-Out)** – Used for secure remote server management and troubleshooting when the operating system is unresponsive.
- **VPN** – Enabled secure access to customer nodes and Ericsson internal systems from remote locations.
- **WinSCP** – Used to securely transfer log files, configuration snapshots, or reports between local and remote systems.
- **Ivanti Secure Access Client** – Provided VPN connectivity and secure remote access to Ericsson's internal support tools and customer infrastructure.



 ⚠️ **Disclaimer**: The commands and examples provided in this repository are **Ericsson-specific** and were executed within an Ericsson-managed support environment. These are *not* generic Linux configurations, but tailored to the systems and customer nodes I worked with during my role as a Support Engineer.  
 No sensitive or confidential information is shared. This is strictly for **educational and demonstration purposes**.

##SCENARIO
#Perform a Health Check on AIRTEL Congo DRC_ Handover HC for New SDP23 and SDP24 , 

Below is my solution or the steps taken as a support engineer ;

##  Pre-Health Check Process – What Happens Before the Report is Sent

Before submitting a health check report, a Support Engineer follows a structured process to ensure the system’s health is thoroughly evaluated and the report reflects accurate and actionable insights. Below is a breakdown of the standard steps:

### 1. System Access & Initial Verification
- Log into the system or node (e.g., via SSH).
- Confirm system availability and verify that all necessary services are up and running.
- Validate system responsiveness and basic connectivity.

### 2.  Data Collection
- Run predefined scripts or commands to gather system health metrics such as:
  - CPU, memory, and disk utilization
  - Node uptime and load
  - Active alarms or faults
  - Software/firmware version
  - Network interface and traffic stats
- "Example command (Ericsson-specific):"
  ```bash
  sudo /opt/esa/bin/fmactivealarms


3. Data Analysis 
-Examine collected data for abnormalities or threshold violations.
-Pay attention to:
Critical or major alarms
Performance degradation
Irregular system behaviors or patterns

4.  Configuration Validation
Check for any configuration mismatches or unauthorized changes.

Ensure the system aligns with baseline or standard configurations.

5.  Documentation of Findings
Summarize observations in a structured format.

Record current system state, performance indicators, and detected issues.

6. Internal Review or Escalation (if needed)
If critical issues are identified, escalate to relevant teams or vendor support.

In some cases, findings may undergo peer review before formal reporting.

7. Report Preparation
Compile findings into a professional report.

Include:
Summary and detailed findings
Screenshots, logs, or graphs (if applicable)
Recommendations or action points

8.  Submission
Share the final report with the supervisor, client.

Optionally, we  initiate follow-up actions based on the report’s recommendations.


#BELOW IS A HEALTH CHECK I DID ON A CUSTOMER NODE ;

NODE NAME : pksdp10a 
Linux user i am logged in as :Charles 


- There are many active alarms with different severities. Clear the old alarms and check the current ones please.
- 
         [charles@pksdp10a home]$ sudo /opt/esa/bin/fmactivealarms
	Active alarms:
	!---------------------------------------------------------------
	Module             : SystemResources
	Error Code         : 990501
	Resource Id        : 1.1.1.99.5
	Timestamp First    : Wed Jun 18 10:41:59 EAT 2025
	Repeated Counter   : 1
	Timestamp Last     : Wed Jun 18 10:41:59 EAT 2025
	Model Description  : SystemResources:Process count is high
	Active Description : Process count, 470 processes are on the system
	Event Type         : 3
	Probable Cause     : 207
	Severity           : minor
	Orig Source IP     : 172.23.198.229
	Sequence Number    : 1
	---------------------------------------------------------------!
	!---------------------------------------------------------------
	Module             : FSC-SS7ManagerHD
	Error Code         : 307
	Resource Id        : 1.1.1.1.10.307
	Timestamp First    : Wed Jun 18 10:42:03 EAT 2025
	Repeated Counter   : 1
	Timestamp Last     : Wed Jun 18 10:42:03 EAT 2025
	Model Description  : M3UA: Association Unavailable For Up
	Active Description : Info: Associations unavailable for UP - SAID: 2
	Event Type         : 2
	Probable Cause     : 504
	Severity           : warning
	Orig Source IP     : 172.23.198.229
	Sequence Number    : 2
	---------------------------------------------------------------!
	!---------------------------------------------------------------
	Module             : PSC-SogInterface
	Error Code         : 140
	Resource Id        : 1.1.1.1.26.140
	Timestamp First    : Wed Jun 18 10:42:07 EAT 2025
	Repeated Counter   : 2
	Timestamp Last     : Wed Jun 18 10:42:18 EAT 2025
	Model Description  : Connection_refused:
	Active Description : Info: Host:  - Port: 5000
	Event Type         : 2
	Probable Cause     : 554
	Severity           : major
	Orig Source IP     : 172.23.198.229
	Sequence Number    : 7
	---------------------------------------------------------------!
	!---------------------------------------------------------------
	Module             : PSC-SogInterface
	Error Code         : 57
	Resource Id        : 1.1.1.1.26.57
	Timestamp First    : Wed Jun 18 10:42:30 EAT 2025
	Repeated Counter   : 1
	Timestamp Last     : Wed Jun 18 10:42:30 EAT 2025
	Model Description  : Busy processing block/unblock batch
	Active Description : Info: SogInterface is NOT ready to receive block/unblock updates
	Event Type         : 2
	Probable Cause     : 554
	Severity           : warning
	Orig Source IP     : 172.23.198.229
	Sequence Number    : 16
	---------------------------------------------------------------!
	!---------------------------------------------------------------
	Module             : SystemResources
	Error Code         : 990701
	Resource Id        : 1.1.1.99.8
	Timestamp First    : Thu Jun 19 06:00:02 EAT 2025
	Repeated Counter   : 1
	Timestamp Last     : Thu Jun 19 06:00:02 EAT 2025
	Model Description  : Dormant User(s) found, major
	Active Description : One or more users are dormant
	Event Type         : 4
	Probable Cause     : 1100
	Severity           : warning
	Orig Source IP     : 172.23.198.229
	Sequence Number    : 1906
	---------------------------------------------------------------!
	!---------------------------------------------------------------
	Module             : FSC-TraceEventLog
	Error Code         : 440
	Resource Id        : 1.1.1.1.6.440
	Timestamp First    : Wed Jun 18 10:42:06 EAT 2025
	Repeated Counter   : 44
	Timestamp Last     : Thu Jun 19 13:16:10 EAT 2025
	Model Description  : Trace activated
	Active Description : Info:
	Event Type         : 3
	Probable Cause     : 532
	Severity           : warning
	Orig Source IP     : 172.23.198.229
	Sequence Number    : 5
	---------------------------------------------------------------!




2- ERROR LOGS 


	This log has been received more than 5 times each second: 

		Jun 15 03:38:07 pksdp10a EventLogFile 1749947877.649242[20250615 03:37:57.649242] Module: FSC-SS7ManagerHD/1.0/B/2 Event: M3UA: Signaling Process State Change ID: 270068 Type: -1691238336 Count: 1 Aff.Obj:  Info: Remote SP Id: 2 connected to local SP Id: 2 has changed state to: DOWN
		Jun 19 12:43:27 pksdp10a EventLogFile 1750326206.991516[20250619 12:43:26.991516] Module: FSC-SS7ManagerHD/1.0/A/1 Event: M3UA: Signaling Process State Change ID: 270068 Type: -1691238336 Count: 1 Aff.Obj:  Info: Remote SP Id: 2 connected to local SP Id: 2 has changed state to: DOWN

	Jun 18 10:40:51 pksdp10a nm-dispatcher: Error: either "to" is duplicate, or "172.23.198.249" is a garbage.
	Jun 18 10:40:54 pksdp10a NetworkManager[1365]: <error> [1750232454.1268] device (team0): addrconf6: failed to start neighbor discovery: failure creating libndp socket: Address family not supported by protocol (97)
	Jun 18 10:41:12 pksdp10a journal: SS7 Log-daemon[5599]: File ss7c.c, row 6152, Error 2000, UserID 114, connected EINSS7_LOG_DAEMON:0->CP_MANAGER:0

	Jun 19 09:20:38 pksdp10a smad_rev: [ERR   ]: ccb has error, try next

	1750326226.092000[20250619 12:43:46.092000] Module: FSC-FileTransferHandler/1.0/B/1 Event: Cannot remove local file ID: 5700012 Type: 58348883198902273 Count: 1 Aff.Obj: AuditToEMM Info: Cannot rename/remove local file/var/opt/fds/logs/AuditToEMM/pksdp10b_audit.log.20250509.0.txt



3- NTP STATUS

	One NTP IP is at not combined status. Its better to have it in combined status at standby as a backup NTP.

	210 Number of sources = 2
	MS Name/IP address         Stratum Poll Reach LastRx Last sample               
	===============================================================================
	^* 10.161.75.130                 1  10   377   991    -16us[  -20us] +/-  344us
	^- 10.161.61.140                 1  10   377   275    +61us[  +61us] +/- 1412us


4- COMPONENT STATES

	Some components are passive.

	 33   Member2 FSC-Event/8.0/A/2                       - Passive
	 34   Member2 PSC-UssdCallback/8.2/A/2                - Passive
	 37   Member2 PSC-TrafficHandler/8.1/A/2              - Passive
	 38   Member2 PSC-SubscriberHandler/8.2/A/2           - Passive
	 39   Member2 PSC-BlockHandler/8.2/A/2                - Passive
	 40   Member2 FSC-EventLog/8.0/A/2                    - Passive
	 41   Member2 FSC-TraceEventLog/8.0/A/2               - Passive
	 42   Member2 PSC-ConfigHandler/8.0/A/2               - Passive
	 44   Member2 PSC-SogInterface/8.2/A/2                - Passive
	 45   Member2 FSC-SystemMonitor/7.1/A/2               - Passive
	 46   Member2 PSC-ExternalNotification/8.1/A/2        - Passive
	 49   Member2 FSC-SMSInterface/8.0/A/2                - Passive
	 50   Member2 FSC-DataSynchronizer/8.0/A/2            - Passive
	 53   Member2 FSC-UssdHD/1.0/A/2                      - Passive


5- MODULE CONFIGURATION :  Below are the Module(s) configuration failed

	[charles@pksdp10a home]$ sudo lecfengine module-verify
	 9001 - Module(s) failed verification,['EHardeningSetup', 'EIPCoreSetup']
 
 
6- BACKUP

	Backup is not being taken everyday.

	-rw-r--r--  1 root   root                  4349 May 29 12:23 cfbackup_pksdp10a_20250529_122309.log
	-rw-r--r--  1 root   root                  4349 May 31 02:09 cfbackup_pksdp10a_20250531_020959.log
	-rw-r--r--  1 root   root                  4349 Jun  1 02:09 cfbackup_pksdp10a_20250601_020951.log
	-rw-r--r--  1 root   root                  4349 Jun  5 02:10 cfbackup_pksdp10a_20250605_021021.log
	-rw-r--r--  1 root   root                  4349 Jun  6 02:10 cfbackup_pksdp10a_20250606_021026.log
	-rw-r--r--  1 root   root                  4349 Jun  7 02:10 cfbackup_pksdp10a_20250607_021051.log
	-rw-r--r--  1 root   root                  4349 Jun 11 02:10 cfbackup_pksdp10a_20250611_021047.log
	-rw-r--r--  1 root   root                  4349 Jun 16 02:10 cfbackup_pksdp10a_20250616_021052.log
	-rw-r--r--  1 root   root                  4349 Jun 17 02:10 cfbackup_pksdp10a_20250617_021052.log
	-rw-r--r--  1 root   root                  8578 Jun 19 09:00 Backup_ftp_Logs.txt

	Backup_ftp_Logs.txt file shows:
	
	================================================Jun 17========================================================
	Preparing Backup file for ftp
	================================================Jun 18========================================================
	Backup is still running with the Server
	================================================Jun 19========================================================
	Backup is still running with the Server
 
 
 
 
#SS7 LINK STATUS 
 
	CCN3 node is Down (both Local AS, Remote AS, Remote SP). RemoteSPC 2303 has Prohibited status under both Remote SSN and Shared Remote SSN.
	 
	Local AS	
			AS: CCN3 LocalAS#2 LocalSPC:2102, Status: Down
	 
	Remote AS
			AS: CCN3 RemoteAS#40002 RC:0, Status: Down		

	Remote SP
			SP: CCN3 RemoteSP#2 Type:IPSP serves RemoteAS#40002, Status: Unavailable		
			
	Remote SSN
			NodeID: 0, RemoteSPC: 2303, SubsystemNumber: 252, Status: Prohibited

	Shared Remote SSN
			RemoteSPC: 2303, SubsystemNumber: 252, Status: Prohibited



## THE TEAMS WORKS ON IT , WE ALSO GO LIVE TO DO THE HEALTH CHECK. THE TEAM TO WORK ON IT  REVERT TO US TO DOUBLE CHECK IF EVERYTHHING IS INTACT .

##WE CONCLUDE ON HEALTH CHECK AFTER EVERYTHING IS OKAY AND REFLECTING .



##  Lessons Learned

- Practical troubleshooting in live environments
- Importance of clear and timely escalation
- Recognizing service-level vs infrastructure-level problems
- Team communication in shift-based support models



##  Summary

This internship gave me hands-on experience in telecom support, allowing me to grow my Linux troubleshooting skills, understand the rhythm of network support operations, and develop a solid work ethic in a fast-paced technical environment. It laid the groundwork for future roles in infrastructure support, systems engineering, or cloud/network operations.



Contact: +23320970648/+233539296617
Linkedin :https://www.linkedin.com/in/josephine-obuobia-darko-3040391b1/
Emai:darkojosephine14@gmail.com

