
# 🗓️ Day 30 / 100

100 Days of DevOps 🚀 

Task was to do a Git hard reset to a commit "add data.txt" just after the initial commit.

1️⃣ I first did `git log --oneline` to see all the commits without taking up much space.

2️⃣ I copied the hash of the commit I wanted to reset to and did `git reset --hard <commit-hash>`.

3️⃣ Then I did a rebase `git rebase -i --root` and picked just the two commits; initial and the "add data.txt".

4️⃣ Then I pushed to the remote repo, forcefully so it can also reset the remote repo's history.

![alt text](<images/day-30.png>)