---
category: 3
frontpage: false
comments: true
created-utc: 2019-01-01
modified-utc: 2019-01-01
---
# Can I not achieve the same result just using DNS round robin?

No.

DNS Round Robin can be used for simple load balancing - rotating traffic between two or more servers.
But it is not a failover solution.

If one of the servers in the round robin set go down, a portion of your visitors are still directed to this failed server.
Under the best circumstances, the visitor's browser may detect the problem after about 20 seconds and try the next server in the round robin set. Unfortunately 20 seconds is an eternity when waiting for a website to respond, and most people will have moved on long before then.

Besides, because visitors may hit either server at any time, DNS round robin requires that you keep the servers perfectly synchronized with identical contents and databases etc.
With Simple Failover you can just keep a simple backup version of your web-site (with no dynamic contents or database access) on a less expensive backup server, because this will only serve as a temporary backup when/if your primary server is ever unavailable.