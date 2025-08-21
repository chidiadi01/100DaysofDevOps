# 🗓️ Day 12 / 100

100 Days of DevOps 🚀

Today’s task stressed me out. I learnt something strange (and still a bit confusing): sometimes when you use netstat to check active ports, it won’t show the PID of the process using a port. But if you pipe the output through grep for the specific port, suddenly the PID shows up. 🤯 This tripped me up because my desired service couldn’t start — the port was already in use, but nothing seemed to be using it.

The challenge: troubleshoot why an Apache web server was down and make it accessible on a specific port.

Here’s how I approached it:

1️⃣ SSH into the app server

2️⃣ Checked the httpd.service status — it wasn’t running, so I tried starting it

3️⃣ Looked into journalctl logs and found the port conflict error

4️⃣ Used netstat (with grep) to identify and kill the process blocking the port

5️⃣ Restarted Apache successfully

6️⃣ Verified accessibility from the server itself (✅ worked)

7️⃣ From the jumphost it still wasn’t reachable, so I added an iptables input rule to allow traffic on the port

After that, the server was fully reachable 🎉

Big lesson: sometimes the smallest quirks (like how you run netstat) can make debugging way harder than it looks.

#100DaysOfDevOps #DevOps #Linux #SystemAdministration #Networking #Apache #Troubleshooting #LearningByDoing #DevOpsJourney #Netstat #Iptables

![alt text](<images/day-12 2025-08-21 131759.png>)
![alt text](<images/day-12 2025-08-21 133727.png>)