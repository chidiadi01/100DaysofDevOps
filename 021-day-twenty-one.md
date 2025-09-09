
🗓️ Day 21 / 100
100 Days of DevOps 🚀 

Install git on the storage server and create a bare repository on it. A bare repository is a git repository with only the .git directory which has the metadata and version history. The working files do not reside there—in other words there is no working tree. You create a bare repository by just adding the `--bare` flag to your initialize command:

`git init --bare /opt/cluster.git`

![alt text](<images/day-21.png>)