# 🗓️  Day 19 / 100

100 Days of DevOps 🚀 

----------------------------

Installed Apache and configured it to serve two webpages, the /demo page and the /beta page. Here's the process I followed:

1️⃣ Installed httpd on the server.

2️⃣ Configured it to Listen on the specified port.

3️⃣ Copied the two directories from the jumphost to the /tmp directory on the app server using scp.

4️⃣ Moved them from there to the /var/www/html directory.

5️⃣ Started the server. Now, curling localhost:6400/demo/ or localhost:6400/beta/ displayed the pages.

![Web server displaying the pages](<images/day-19.png>)