---
category: 4
frontpage: false
comments: true
created-utc: 2019-01-01
modified-utc: 2019-01-01
---
# Problems updating Microsoft DNS server via WMI

> [!Note] This article is specific to **Simple Failover v. 1.x**  
> The issues discussed here do **not** apply to Simple Failover v. 2.0 and later.

The WMI update method in Simple Failover is available only because there are no other secure ways of updating a remote Microsoft DNS server.  

When configured correctly, this update method works fine. But it can be difficult to get the client/server WMI and DCOM security configuration setup correctly for this to work.  

Unfortunately we are not WMI / DCOM experts and are not able to assist with specific WMI errors.

If you have to use Microsoft's DNS server and run into problems with WMI updates, we suggest that you check Microsoft's documentation for WMI, DCOM, and MS DNS server - and/or consult with experts in these technologies.

There is a blog article dealing with WMI and DCOM permissions issues [here](http://blogs.technet.com/jhoward/archive/2008/03/28/part-1-hyper-v-remote-management-you-do-not-have-the-requested-permission-to-complete-this-task-contact-the-administrator-of-the-authorization-policy-for-the-computer-computername.aspx).
This article is about Hyper-V, but is deals with the same WMI and DCOM issues that many Simple Failover users have reported.

Otherwise we recommend that you use a DNS server which supports TSIG signed updates, such as [BIND](https://www.isc.org) or [Simple DNS Plus](https://simpledns.com).