# 🗓️ Day 28 /100

100 Days of DevOps 🚀 

Git cherry pick. The task was to merge particular commits from the feature branch into the main branch. To do that, I went through the following steps:

✅ Navigate to the repository directory

✅ Run `git log feature --oneline` to check the commits in the feature branch whithout too much text. Just a preview.

✅ Check out to the master branch and copy the first few characters of the hash of the commit to be merged.

✅ Merge with git cherry-pick `git cherry-pick <commit-hash>`

✅ Push to remote repo

![alt text](<images/day-28.png>)