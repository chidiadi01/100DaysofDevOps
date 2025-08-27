# 🗓️ Day 14 / 100
100 Days of DevOps 🚀 

Apache is down on one of the app servers. Find it and restore the service. I did justs that — logged into all three servers and checked the status of the `httpd.service`. In app server 1, it was down. So, I used journactl to look through the logs to see the possible errors. I found that the port was in use by another service.

I used ss (Socket Stats) to check which process was using the port, and killed it. Then I started the `httpd.service` again, and it was running. Then I quickly checked `/etc/httpd/conf/httpd.conf` on all app servers to be sure they were running on the proper port. I didn't have time to scroll through it. So, I actually used grep to check for the 'Listen' keyword.

`sudo cat /etc/httpd/conf/httpd.conf | grep Listen`

All was good, so I clicked 'check' and ended my session.

![Day 14. systemctl status httpd showing service running.](<images/day-14 2025-08-27 090848.png>)
