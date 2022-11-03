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
### Exercise 2

```bash
yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (dev)
$ touch home.html

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (dev)
$ git add .

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (dev)
$ git stash
Saved working directory and index state WIP on dev: 801b2bb Add base files

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (dev)
$ touch about.html

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (dev)
$ git add .

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (dev)
$ git stash
Saved working directory and index state WIP on dev: 801b2bb Add base files

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (dev)
$ touch team.html

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (dev)
$ git add .

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (dev)
$ git stash
Saved working directory and index state WIP on dev: 801b2bb Add base files

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (dev)
$ git stash list
stash@{0}: WIP on dev: 801b2bb Add base files
stash@{1}: WIP on dev: 801b2bb Add base files
stash@{2}: WIP on dev: 801b2bb Add base files

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (dev)
$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   index.html

Dropped stash@{1} (feaeaaf6a07f14b3eaceda86f2811bcef41aedea)

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (dev)
$ git stash list
stash@{0}: WIP on dev: 801b2bb Add base files
stash@{1}: WIP on dev: 801b2bb Add base files

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (dev)
$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   index.html

Dropped stash@{1} (59569a4e0b4b6fbb477087cac43f4707562c5dfa)

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (dev)
$ git add .

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (dev)
$ git commit -m "Add home and about pages"
[dev d2ef659] Add home and about pages
 3 files changed, 24 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (dev)
$ git push origin dev
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 576 bytes | 576.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
remote: 
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/Yvad60/git-bundle1-exercise1/pull/new/dev
remote:
To https://github.com/Yvad60/git-bundle1-exercise1.git
 * [new branch]      dev -> dev

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (dev)
$ git stash list
stash@{0}: WIP on dev: 801b2bb Add base files

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (dev)
$ git stash pop stash@{0}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped stash@{0} (1455c623f6c03ec7b687967c463cd277cee6ebbf)

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (dev)
$ git reset --hard
HEAD is now at d2ef659 Add home and about pages
```

## Bundle 2

### exercise 1

### exercise 2

```bash
yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (ft/bundle-2)    
$ git checkout main
Switched to branch 'main'

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (main)
$ git pull origin main
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (1/1), 622 bytes | 77.00 KiB/s, done.
From https://github.com/Yvad60/git-bundle1-exercise1
 * branch            main       -> FETCH_HEAD
   801b2bb..cea7285  main       -> origin/main
Updating 801b2bb..cea7285
Fast-forward
 home.html     | 12 ++++++++++++
 index.html    | 12 ++++++++++++
 create mode 100644 about.html
 create mode 100644 home.html
 create mode 100644 about.html
 create mode 100644 home.html
 create mode 100644 services.html
Switched to a new branch 'ft/service-redesign'

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (ft/service-redesign)
$ git add .

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (ft/service-redesign)
$ git commit -m "Add changes to the service page"
[ft/service-redesign 5f5b07a] Add changes to the service page
 1 file changed, 1 insertion(+)

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (ft/service-redesign)
$ git push origin ft/service-redesign 
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 351 bytes | 351.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote: This repository moved. Please use the new location:
remote:   https://github.com/Yvad60/git-exercises-sandbox.git
remote: 
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/Yvad60/git-exercises-sandbox/pull/new/ft/service-redesign
remote:
To https://github.com/Yvad60/git-bundle1-exercise1.git
 * [new branch]      ft/service-redesign -> ft/service-redesign

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (ft/service-redesign)
$ git checkout main
Switched to branch 'main'

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (main)
$ git add .

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (main)
$ git commit -m "Add changes to the service page from main"
[main e6b97ad] Add changes to the service page from main
 1 file changed, 2 insertions(+)

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (main)
$ git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 408 bytes | 408.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote:   https://github.com/Yvad60/git-exercises-sandbox.git
To https://github.com/Yvad60/git-bundle1-exercise1.git
   cea7285..e6b97ad  main -> main

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (main)
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (ft/service-redesign)
$ git diff

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (ft/service-redesign)
$ git merge main
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (ft/service-redesign|MERGING)
$ git add .

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (ft/service-redesign|MERGING)
$ git commit
[ft/service-redesign 5b409c1] Merge branch 'main' into ft/service-redesign

$ git push origin ft/service-redesign
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 371 bytes | 371.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote: This repository moved. Please use the new location:
remote:   https://github.com/Yvad60/git-exercises-sandbox.git
To https://github.com/Yvad60/git-bundle1-exercise1.git
   5f5b07a..5b409c1  ft/service-redesign -> ft/service-redesign

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (ft/service-redesign)
```
