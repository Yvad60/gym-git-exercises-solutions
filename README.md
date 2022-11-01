# Git execises solutions
## Bundle 1

### Exercise 1

```bash

yvesy@geekbook MINGW64 ~/OneDrive/Desktop
$ mkdir sweeton-project

yvesy@geekbook MINGW64 ~/OneDrive/Desktop
$ cd sweeton-project/

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project
$ git init
Initialized empty Git repository in C:/Users/yvesy/OneDrive/Desktop/sweeton-project/.git/

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (master)
$ git branch -m main

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (main)
$ touch index.html

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (main)
$ touch styles.css

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (main)
$ git add .

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (main)
$ git commit -m "Add base files"
[main (root-commit) 801b2bb] Add base files
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 index.html
 create mode 100644 styles.css

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (main)
$ git remote add origin https://github.com/Yvad60/git-bundle1-exercise1.git

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (main)
$ git push origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 226 bytes | 226.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/Yvad60/git-bundle1-exercise1.git
 * [new branch]      main -> main

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (main)
$ git branch dev

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (main)
$ git checkout dev
Switched to branch 'dev'

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (dev)
$ git checkout -b test
Switched to a new branch 'test'

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (test)
$ git checkout dev
Switched to branch 'dev'

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (dev)
$ git branch -d test
Deleted branch test (was 801b2bb).

```
