# 🗓️ Day 11 / 100

100 Days of DevOps 🚀

Today was all about Java on Tomcat. I deployed a Java web app and here’s the journey:


1️⃣ Set up passwordless SSH from the jump host to the app server and copied the web archive (WAR) file to the server.

 2️⃣ Installed Apache Tomcat on the app server.

 3️⃣ Tweaked `/etc/tomcat/server.xml` to set the correct port.

 4️⃣ Moved the .war file into `/usr/share/tomcat/webapps` (needed root permissions, so no direct SCP from jump host).

 5️⃣ Started the Tomcat service and the app was live!

This was a solid exercise in Linux server management, Java web app deployment, and Tomcat configuration.

![alt text](<images/day-11 2025-08-15 101244.png>)
