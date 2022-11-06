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

## Bundle 3

### Exercise 1

```bash
yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (ft/team-page)
$ git checkout main
Switched to branch 'main'

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (main)
$ git checkout ft/contact-page
error: pathspec 'ft/contact-page' did not match any file(s) known to git

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (main)
$ git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (ft/contact-page)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (ft/team-page)
$ git log
commit 1ebfbd1f300957aba445c478ef977f31685fb9bd (HEAD -> ft/team-page, origin/ft/team-page)
Author: ivad <yvesyvad@gmail.com>
Date:   Thu Nov 3 19:29:46 2022 +0200

    Create and add changes to team page

commit e6b97ad873544c4bb83093654c9aaf122da8e47e (origin/main, main, ft/contact-page)
Author: ivad <yvesyvad@gmail.com>
Date:   Thu Nov 3 18:50:53 2022 +0200

    Add changes to the service page from main

commit cea7285dbbf03a434744cc5ad25ab4b0a987674c
Merge: 801b2bb 7d02efe
Author: Chrissie <chrissiemhrk@gmail.com>
Date:   Thu Nov 3 11:04:53 2022 +0200

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (ft/team-page)
$ git cherry-pick yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (ft/team-page)   
$ git checkout main
Switched to branch 'main'

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (main)
$ git checkout ft/contact-page
error: pathspec 'ft/contact-page' did not match any file(s) known to git

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (main)
$ git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (ft/contact-page)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (ft/team-page)   
$ git log
commit 1ebfbd1f300957aba445c478ef977f31685fb9bd (HEAD -> ft/team-page, origin/ft/team-page)
Date:   Thu Nov 3 11:04:53 2022 +0200^Cm>87674c (origin/main, main, ft/contact-page)

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (ft/team-page)
$ git cherry-pick 1ebfbd1f300957aba445c478ef977f31685fb9bd
The previous cherry-pick is now empty, possibly due to conflict resolution.
If you wish to commit it anyway, use:

    git commit --allow-empty

Otherwise, please use 'git cherry-pick --skip'
On branch ft/team-page
You are currently cherry-picking commit 1ebfbd1.
  (all conflicts fixed: run "git cherry-pick --continue")
  (use "git cherry-pick --skip" to skip this patch)
  (use "git cherry-pick --abort" to cancel the cherry-pick operation)

nothing to commit, working tree clean

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (ft/team-page|CHERRY-PICKING)
$ git checkout ft/contact-page
Switched to branch 'ft/contact-page'
warning: cancelling a cherry picking in progress

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (ft/contact-page)
$ git checkout ft/contact-page
Already on 'ft/contact-page'

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (ft/contact-page)
$ git cherry-pick 1ebfbd1f300957aba445c478ef977f31685fb9bd
[ft/contact-page 81df6ff] Create and add changes to team page
 Date: Thu Nov 3 19:29:46 2022 +0200
 1 file changed, 13 insertions(+)
 create mode 100644 team.html

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (ft/contact-page)
$ git add .

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (ft/contact-page)
$ git commit -m "added new changes from team branch"

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (ft/contact-page)
$ git commit -m "added new changes from team branch"
On branch ft/contact-page
nothing to commit, working tree clean

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (ft/contact-page)
$ git push origin ft/contact-page 
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 511 bytes | 102.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: This repository moved. Please use the new location:
remote:   https://github.com/Yvad60/git-exercises-sandbox.git
remote: 
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/Yvad60/git-exercises-sandbox/pull/new/ft/contact-page
remote:
To https://github.com/Yvad60/git-bundle1-exercise1.git
 * [new branch]      ft/contact-page -> ft/contact-page

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (ft/contact-page)
$ git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (ft/faq-page)
$ git add .

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (ft/faq-page)
$ git commit
[ft/faq-page bc7a45b] Add faq page
 1 file changed, 12 insertions(+)
 create mode 100644 faq.html

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (ft/faq-page)
$ git push origin ft/faq-page 
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 454 bytes | 22.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: This repository moved. Please use the new location:
remote:   https://github.com/Yvad60/git-exercises-sandbox.git
remote: 
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/Yvad60/git-exercises-sandbox/pull/new/ft/faq-page
remote:
To https://github.com/Yvad60/git-bundle1-exercise1.git
 * [new branch]      ft/faq-page -> ft/faq-page

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (ft/faq-page)
$ git revert 1ebfbd1f300957aba445c478ef977f31685fb9bd
[ft/faq-page c9c8cbe] Revert "Create and add changes to team page"
 1 file changed, 13 deletions(-)
 delete mode 100644 team.html

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (ft/faq-page)
$ git push origin ft/faq-page 
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 279 bytes | 139.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: This repository moved. Please use the new location:
remote:   https://github.com/Yvad60/git-exercises-sandbox.git
To https://github.com/Yvad60/git-bundle1-exercise1.git
   bc7a45b..c9c8cbe  ft/faq-page -> ft/faq-page
```

### Exercise 2

## Bundle 4

### Exercise 1

```bash
yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (ft/home-page-redesign)
$ git checkout main
Switched to branch 'main'

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (main)
$ git remote add git-copy https://github.com/Yvad60/git-exercise-repo-2.git

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (main)
$ git remote 
git-copy
origin

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (main)
$ git add .

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (main)
$ git commit -m "add a new home heading"
[main ac7cfe7] add a new home heading
 1 file changed, 1 insertion(+)

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (main)
$ git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 344 bytes | 172.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote: This repository moved. Please use the new location:
remote:   https://github.com/Yvad60/git-exercises-sandbox.git
To https://github.com/Yvad60/git-bundle1-exercise1.git
   5e68747..ac7cfe7  main -> main

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (main)
$ git push git-copy main
Enumerating objects: 20, done.
Counting objects: 100% (20/20), done.
Delta compression using up to 4 threads
Compressing objects: 100% (19/19), done.
Writing objects: 100% (20/20), 2.47 KiB | 315.00 KiB/s, done.
Total 20 (delta 9), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (9/9), done.
To https://github.com/Yvad60/git-exercise-repo-2.git
 * [new branch]      main -> main

```

### Exercise 2

```bash
yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (ft/footer)
$ git checkout main
Switched to branch 'main'

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (main)
$ git checkout -b ft/squashing
Switched to a new branch 'ft/squashing'

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (ft/squashing)
$ git checkout main
Switched to branch 'main'

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (main)
$ git checkout -b ft/squashing
fatal: a branch named 'ft/squashing' already exists

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (main)
$ git checkout ft/squashing 
Switched to branch 'ft/squashing'

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (ft/squashing)
$ git merge squash ft/footer
merge: squash - not something we can merge

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (ft/squashing)
$ git merge --squash ft/footer 
Updating ac7cfe7..a147759
Fast-forward
Squash commit -- not updating HEAD
 home.html | 5 +++++
 1 file changed, 5 insertions(+)

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (ft/squashing)
$ git commi -m 'footer changes squashing'
git: 'commi' is not a git command. See 'git --help'.

The most similar commands are
        commit
        column
        config

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (ft/squashing)
$ git commit -m 'footer changes squashing'
[ft/squashing 228bdd3] footer changes squashing
 1 file changed, 5 insertions(+)

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (ft/squashing)
$ git push origin ft/s
ft/service-redesign   ft/squashing

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (ft/squashing)
$ git push origin ft/s
ft/service-redesign   ft/squashing

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/sweeton-project (ft/squashing)
$ git push origin ft/squashing 
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 414 bytes | 207.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote: This repository moved. Please use the new location:
remote:   https://github.com/Yvad60/git-exercises-sandbox.git
remote: 
remote: Create a pull request for 'ft/squashing' on GitHub by visiting:
remote:      https://github.com/Yvad60/git-exercises-sandbox/pull/new/ft/squashing
remote:
To https://github.com/Yvad60/git-bundle1-exercise1.git
 * [new branch]      ft/squashing -> ft/squashing

```

## Bundle 5

### Exercise 2
```bash
PS C:\Users\yvesy\OneDrive\Desktop\New folder> gh repo clone Yvad60/git-cafe-exercise
Cloning into 'git-cafe-exercise'...
remote: Enumerating objects: 107, done.
remote: Counting objects: 100% (107/107), done.
remote: Compressing objects: 100% (101/101), done.
remote: Total 107 (delta 5), reused 104 (delta 4), pack-reused 0Receiving objects:  96% (103/107), 1.91 MiB | 60.00 KiB/Receiving objects: 100% (107/107), 1.95 MiB | 65.00 KiB/s, done.

Resolving deltas: 100% (5/5), done.


A new release of gh is available: 2.18.1 → 2.19.0
https://github.com/cli/cli/releases/tag/v2.19.0

PS C:\Users\yvesy\OneDrive\Desktop\New folder> cd .\git-cafe-exercise\
PS C:\Users\yvesy\OneDrive\Desktop\New folder\git-cafe-exercise> code .
PS C:\Users\yvesy\OneDrive\Desktop\New folder\git-cafe-exercise>
yvesy@geekbook MINGW64 ~/OneDrive/Desktop/New folder/git-cafe-exercise (main)
$ git add .

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/New folder/git-cafe-exercise (main)
$ git commit 
[main 75945d6] Change the heading
 1 file changed, 2 insertions(+), 2 deletions(-)

yvesy@geekbook MINGW64 ~/OneDrive/Desktop/New folder/git-cafe-exercise (main)
$ git push origin main 
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 320 bytes | 320.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Yvad60/git-cafe-exercise.git
   d1d3f9c..75945d6  main -> main

```
