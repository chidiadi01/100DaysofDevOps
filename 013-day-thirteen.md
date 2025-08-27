# 🗓️ Day 13 / 100

100 Days of DevOps 🚀 

Install and configure iptables. Block all traffic coming to port 8088 on all three app servers except traffic from the load balancer. Also, make sure that the rules are persistent. How I went about it:

1️⃣ Installed iptables and iptables-services. iptables-services will help us make the rules persistent across reboots.

2️⃣ Enabled the iptables service. That helps it to start on reboot.

3️⃣ Wrote the rules, first to accept traffic from LB host to the port, then the rule to reject all traffic to the port.

4️⃣ Made the rules persistent with 'sudo iptables-save | sudo tee /etc/sysconfig/iptables'. Upon reboot, iptables.service will load the rules from here using iptables-restore.

5️⃣ Logged into the LB host to confirm it could reach the servers.

Funny enough, I recently wrote an article about iptables, which includes everything you need to know to start using it. You can read it here: https://thenetworkbits.substack.com/p/firewalls-in-linux-a-deep-dive-into

#100DaysofDevOps #Linux KodeKloud #SysAdmin 

![](<images/day-13 2025-08-26 201930.png>)