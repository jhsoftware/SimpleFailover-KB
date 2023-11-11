---
category: 5
frontpage: false
comments: true
refs: 6
created-utc: 2019-01-01
modified-utc: 2019-01-01
---
# New in Simple Failover v. 2.0

1. **Faster!**  
The Simple Failover engine has been redesigned using modern programming tools and principles. Asynchronous programming techniques throughout the program allows it to continuously monitor and failover protect a much larger number of servers than previous versions.  

1. **Support for latest Windows versions**  
Runs on Windows Vista / Server 2008 and later - including 64 bit Windows.  

1. **IPv6**  
Full support for IPv6 - polling, DNS updating, etc.  

1. **IDNs (Internationalized Domain Names)**  
Enter host names with native international characters.  
[Screenshot](img/212/lnk1.png)  

1. **Serve DNS requests directly**  
You can use Simple Failover as your Internet facing DNS server. Any DNS request received that Simple Failover does not have data for is forwarded on to your real DNS server.  
This eliminates the need to update DNS records on the DNS server (still supported).  
[Screenshot](img/212/lnk2.png)  

1. **Weighted Round Robin**  
Balance the traffic sent to your servers.  
(only available when serving DNS requests directly / through extended forwarding)   
[Screenshot](img/212/lnk3.png)  

1. **Polling history recorded for each server**  
For quick review of each server's history and evidence of server reliability.  
Can be exported to disk in csv format.  
[Screenshot](img/212/lnk4.png)  

1. **Enhanced server monitoring / polling methods**  
For example HTTP GET with check for specific return value (earlier versions only supports HTTP HEAD).  
It can also monitor SSL web-sites (https://...).  
The "TCP connect" polling method can now also check for configurable value in server greeting response.  
And It will possible run your own or 3rd party custom polling code through a new "execute command line" polling method.  
[Screenshot](img/212/lnk5.png)  

1. **New notification methods / options**  
In addition to e-mail / Windows Event Log notification, you can send problem notification via a HTTP GET/POST - for example to a SMS / text messaging service API, or by executing a custom command line.  
You can also select which type of events you want to be notified about.  
[Screenshot](img/212/lnk6.png)  

1. **Notify multiple e-mail addresses / receivers per server set**  
[Screenshot](img/212/lnk7.png)  

1. **New DNS update methods**  
We have added 2 new DNS update methods: "Execute command line" (replaces "Scripting") and "Microsoft DNS server (dnscmd.exe)" (see below)  
[Screenshot](img/212/lnk8.png)  

1. **Update Microsoft DNS servers securely without WMI.**  
A new DNS update option uses "dnscmd.exe" to update Microsoft DNS servers - local or remote - without any of the configuration / authentication problems associated with the WMI method used in v. 1.x.  

1. **Support for wildcard host names (*.hostname.tld)**  
No need to enter a long list of sub-names.  
[Screenshot](img/212/lnk9.png)  

1. **"All fail" server IP address option**  
If all servers are down (as seen by Simple Failover), send traffic to a specific server IP address.  
[Screenshot](img/212/lnk10.png)  

1. **Option to poll a different server IP address than the IP address set in DNS**  
For monitoring servers behind same NAT router as Simple Failover, you can now specify both public and private IP addresses for a server.  
[Screenshot](img/212/lnk11.png)  

1. **Web-server polling host name independent of DNS host name**  
This makes it possible to update a different host name in DNS than the host name sent in the HTTP "host" header when monitoring/polling a web-server.  

1. **Force individual servers off-line (disable)**  
For example during maintenance.  
[Screenshot](img/212/lnk12.png)  

1. **Automatically pause a server set if specific server(s) fail**  
To prevent auto failback.  
[Screenshot](img/212/lnk13.png)  

1. **REST / JSON based HTTP API**  
The HTTP API has been redesigned according to REST principles and the JSON data format.  

1. **Other new features and improvements**  
    - Separate engine (Windows service) and user interface processes enables remote desktop (RDP) access without any special settings etc.  
    - Always runs as Windows Service (no need to enable this first).  
    - Send e-mail notifications via SSL / TLS (SMTP).  
    - Built-in logging to disk.  
    - New TSIG-algorithms SHA1, SHA256, SHA384, and SHA512 for signing dynamic DNS updates.  
    - Option for how often DNS records are re-checked (not necessary to check after every server poll).  
    - Optional notification when a server comes back online (after previous failure) and for other events.  
    - All configuration files / data in JSON format.  
    - DNS servers can now also be configured using host names instead of just IP addresses.  
    - New option to play a user specified sound file when a problem is detected.  
    - Based on Microsoft's .NET Framework 4.5.