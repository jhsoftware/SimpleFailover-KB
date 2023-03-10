---
category: 5
frontpage: false
comments: true
refs: 4
created-utc: 2019-01-01
modified-utc: 2019-01-01
---
# Retired features and breaking changes in Simple Failover v. 2.0

To make Simple Failover even simpler to use and also to "make room" for new stuff, we have done a bit of cleaning up.
A number of older features have been retired because there are now better alternatives, or because they are no longer relevant.  

1. **No longer runs on older Windows versions**  
Simple Failover v. 2 requires Windows Vista / Server 2008 or later.

1. **New configuration file format**  
Simple Failover v. 2 cannot use v. 1.x configuration files directly. However a conversion tool is included.

1. **Incompatible HTTP API**  
The v. 2 HTTP API is not compatible with that from Simple Failover v. 1.x (v. 2 is REST based and uses JSON / v. 1.x is not REST based and uses XML)

1. **RETIRED: DNS update method "Microsoft DNS via WMI"**  
Possible workarounds:
    - Use new update method "Microsoft DNS Server (dnscmd.exe)" (requires new [update agent](https://simplefailover.com/mdua) installed on DNS server computer when updating remote server).
    - Use new "execute command line" update method to run your own a script / program (not available from us) to perform the update via WMI or dnscmd.exe.
    - Use new option to serve DNS directly.
    - Use another DNS update method and/or DNS server.

1. **RETIRED: DNS update method "Scripting"**  
Possible workarounds:
    - Use new "execute command line" DNS update method to run the script via cscript.exe (requires minor updates to script).
    - Use another DNS update method.

1. **RETIRED: VBScript / JScript scripts for server status events and problems event**  
Possible workarounds:
    - Use new "execute command line" notification method to run the script via cscript.exe (requires minor updates to script).  
    - Use another notification method.  

1. **RETIRED: VBScript / JScript scripts for log events**  
Log events can no longer be scripted.
Simple Failover v. 2 instead has built-in feature for logging to disk.  

1. **RETIRED: Problem knowledge base**  
For v. 2, the on-line "problem knowledge base" will be merged into our general support knowledge base.