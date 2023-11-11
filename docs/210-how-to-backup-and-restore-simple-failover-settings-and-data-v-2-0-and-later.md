---
category: 1
frontpage: false
comments: true
vgroup: 1
vname: Simple Failover v. 2.0 and later
vsort: 1
created-utc: 2019-01-01
modified-utc: 2019-01-01
---
# How to backup and restore settings and data? (Simple Failover v. 2.0 and later)

The different settings (Options dialog, Server sets properties) are stored in the "sfo.config.json" file, 
and the polling history is stored in the "poll-history.sdf" file (SQL Server Compact data file). 
Both files are located in the in the Simple Failover application data directory - typically: "C:\ProgramData\JH Software\Simple Failover" 
("ProgramData" is usually a hidden folder).

**To backup:** Copy both files.

**To restore:** Install a fresh copy of Simple Failover and copy the backup files back to their original location.

**Restoring settings and data from Simple Failover v. 1.x:**
Simple Failover v. 2.0 includes a tool "v1.upgrade.exe" which can convert a v. 1.x configuration file (sfo-config.xml) into 
a v. 2.0 configuration file (sfo.config.json). This tool is found in the directory where Simple Failover v. 2.0 is installed.