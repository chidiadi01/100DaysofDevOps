# 🗓️ Day 15 / 100
100 Days of DevOps 🚀 

Today's task was to setup SSL for Nginx. And this is how it went:
1️⃣ The first thing I did was to install nginx and enable it (to allow it restart upon reboot). Then start the service too.
2️⃣ I then used the `find` command to find out the path for the configuration file, 'nginx.conf' as I couldn't remember exactly where it was. Yes, there's Google and AI, but I'm practicing.
3️⃣ From the configuration file, I saw where to move the private and public keyfiles and the HTML file.
4️⃣ I uncommented the configurations for HTTPS and edited the server name. Then I saved the file and restarted the nginx service.

![](<images/day-15 2025-09-01 211822.png>)