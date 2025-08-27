# 🗓️ Day 4/100

100 Days of DevOps. Today's task exposed knowledge gaps. 

The task was to grant executable permissions to a file so that all the users can execute the file. Initially, I just tried to give executable permissions to all (111 or ---x--x--x). It didn't work. So, I tried giving rwx permissions to the user, r-x to the group, and r-x to the others (755). And it worked. 

Upon doing a little research later, I found out it's because bash needs to be able to read the script to execute it. Learnt something little today.

![](<images/day-4 2025-08-08 071616.png>)