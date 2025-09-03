# 🗓️ Day 16 / 100

100 Days of DevOps 🚀 

Setup nginx as a load balancer. I don't have much experience with nginx, but I'm learning by doing. Today, I got myself educated on nginx contexts, and how the configuration files work. How did I go about this setup?

✅ Checked my app servers, and ensured that the Apache services on all three were running. 

✅ I then confirmed the port numbers by checking the configuration file. I don't have all the time to scroll, to I used grep. `sudo cat /etc/httpd/conf/httpd.conf | grep Listen`.

✅ I used cURL to verify the servers were accessible from the load balancer host. Then I added their addresses (with port numbers) to an upstream context in the http context in my nginx configuration file.

✅ In the server context, I added a location context that referenced my upstream context with a few header-setting directives: `location / {proxy_pass http://app_servers: . . .}`.

✅ Reloaded nginx and it worked!

![](<images/day-16 2025-09-03 131517.png>)