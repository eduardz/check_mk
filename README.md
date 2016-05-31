Check_MK is an extension to the Nagios monitoring system that allows creating rule-based configuration using Python and offloading work from the Nagios core to make it scale better, allowing more systems to be monitored from a single Nagios server.

Gathered some Check_MK plugins from the internet: modified some for a better function/usefulness on Linux.

The plugins require to install check-mk-agent for check_mk server.
Official documentation https://mathias-kettner.de/checkmk_linuxagent.html

CentOS based install:
```yum install check-mk-agent```

Also install xinetd to use the check_mk_agent.
```yum install xinetd```

Modify the file /etc/xinetd.d/check-mk-agent, here you can set the IP address of the monitoring server
"only from = IP / Hostname"; Also check if the agent is enabled: "disable  = no".

Start and enable at boot xinetd.
```systemctl enable xinetd ; systemctl start xinetd```
