# The git basics exercises

## Bundle 1

### Exercises 1

```bash


Nicole@DESKTOP-I5FEMIP MINGW64 ~ (main)
$ cd desktop

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop (main)
$ mkdir git-exercises

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop (main)
$ cd git-exercises

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (main)
$ git init
Initialized empty Git repository in C:/Users/Nicole/Desktop/git-exercises/.git/

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (master)
$ code .

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (master)
$

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (master)
$ git branch -m main


Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (main)
$ git add .

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (main)
$ git commit -m "the starting point for exercises"
[main (root-commit) 2862e9a] the starting point for exercises
 1 file changed, 30 insertions(+)
 create mode 100644 readme.md

 
Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (main)
$ git remote add origin git@github.com:Gabanicole/Gym-git-exercises.git

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (main)
$ git push -u origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 455 bytes | 30.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To github.com:Gabanicole/Gym-git-exercises.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (main)
$ git checkout -b dev
Switched to a new branch 'dev'

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)
$ git checkout -b test
Switched to a new branch 'test'

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (test)
$ git push origin test
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'test' on GitHub by visiting:
remote:      https://github.com/Gabanicole/Gym-git-exercises/pull/new/test
remote:
To github.com:Gabanicole/Gym-git-exercises.git
 * [new branch]      test -> test

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (test)
$ git checkout dev
Switched to branch 'dev'

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)
$ git push origin dev
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/Gabanicole/Gym-git-exercises/pull/new/dev
remote:
To github.com:Gabanicole/Gym-git-exercises.git
 * [new branch]      dev -> dev

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)
$ git push origin --delete test
To github.com:Gabanicole/Gym-git-exercises.git
 - [deleted]         test

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)
$

```

### Exercises 2

```bash

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)
$ git status
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)        home.html       
d" to track)

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)
$ git stash list

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)
$ git add home.html

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)
$ git stash
Saved working directory and index state WIP on dev: fbefc47 the message after done      

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)
$ git stash list
stash@{0}: WIP on dev: fbefc47 the message after done

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)
$ git status
On branch dev
Untracked files:

nothing added to commit but untracked files present (use "git add" to track)

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)
$ git add about.html

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)
$ git stash
Saved working directory and index state WIP on dev: fbefc47 the message after done      

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)
$ git stash list
stash@{0}: WIP on dev: fbefc47 the message after done
stash@{1}: WIP on dev: fbefc47 the message after done

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)
$ git status
On branch dev   
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        team.html

nothing added to commit but untracked files present (use "git add" to track)

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)
$ git add team.html

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)
$ git stash list
stash@{0}: WIP on dev: fbefc47 the message after done
stash@{1}: WIP on dev: fbefc47 the message after done

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)
$ git add team.html

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)
$ git stash
Saved working directory and index state WIP on dev: fbefc47 the message after done

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)
$ git stash list
stash@{0}: WIP on dev: fbefc47 the message after done
stash@{1}: WIP on dev: fbefc47 the message after done
stash@{2}: WIP on dev: fbefc47 the message after done

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)
$ git status
On branch dev
nothing to commit, working tree clean

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)
$ git stash list
stash@{0}: WIP on dev: fbefc47 the message after done
stash@{1}: WIP on dev: fbefc47 the message after done
stash@{2}: WIP on dev: fbefc47 the message after done

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)
$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (7539bf11941289729ee5be630a4f5c46a0e3cef5)

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)
$ git status
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html


Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)
$ git status list
On branch dev
nothing to commit, working tree clean

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)
$ git stash list
stash@{0}: WIP on dev: fbefc47 the message after done
stash@{1}: WIP on dev: fbefc47 the message after done

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)    
$ git stash pop stash@{0}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   team.html

Dropped stash@{0} (0163ac4d77a5b77fc5365f06f47cdbac698f0595)    

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)    
$ git stash list
stash@{0}: WIP on dev: fbefc47 the message after done

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)    
$ git stash pop stash@{0}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html
        new file:   team.html

Dropped stash@{0} (d0fa02f5d56b30f1ac7c222a261e678f5728ef4e)

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)    
$ git status
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html
        new file:   team.html

Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed) 
  (use "git restore <file>..." to discard changes in working directory)
        deleted:    about.html
        deleted:    home.html
        deleted:    team.html


Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)
$ git status
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html
        new file:   team.html

Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed) 
  (use "git restore <file>..." to discard changes in working directory)
        deleted:    about.html
        deleted:    home.html
        deleted:    team.html


Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)
$ git status
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        home.html

nothing added to commit but untracked files present (use "git add" to track)

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)
$ git add home.html

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)
$ git stash
Saved working directory and index state WIP on dev: fbefc47 the 
message after done

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)    
$ git stash list
stash@{0}: WIP on dev: fbefc47 the message after done

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)    
$ git status
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)        about.html

nothing added to commit but untracked files present (use "git add" to track)

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)    
$ git add about.html

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)    
$ git stash
Saved working directory and index state WIP on dev: fbefc47 the 
message after done

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)    
$ git stash list
stash@{0}: WIP on dev: fbefc47 the message after done
stash@{1}: WIP on dev: fbefc47 the message after done

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)    
$ git status
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)        team.html

nothing added to commit but untracked files present (use "git add" to track)

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)    
$ git add team.html

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)    
$ git stash
Saved working directory and index state WIP on dev: fbefc47 the 
message after done

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)    
$ git stash list
stash@{0}: WIP on dev: fbefc47 the message after done
stash@{1}: WIP on dev: fbefc47 the message after done
stash@{2}: WIP on dev: fbefc47 the message after done

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)    
$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (5884056750f84fd14708efe8792cbb6a990a8b93)

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)    
$ git stash list
stash@{0}: WIP on dev: fbefc47 the message after done
stash@{1}: WIP on dev: fbefc47 the message after done

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)    
$ git stash pop stash@{0}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   team.html

Dropped stash@{0} (4b39cb6a12561e1e5f5e6c97badd9d3cf79f1f54)

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)    
$ git stash pop
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)
$ git status
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Home.html

nothing added to commit but untracked files present (use "git add" to track)

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)
$ git add home.html

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)
$ git stash
No local changes to save

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)
$ git add Home.html

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)    
$ git stash 
Saved working directory and index state WIP on dev: fbefc47 the 
message after done

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)    
$ git stash list

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)
$ git status
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        home.html

nothing added to commit but untracked files present (use "git add" to track)

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)
$ git add home.html

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)
$ git stash
Saved working directory and index state WIP on dev: fbefc47 the 
message after done

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)    
$ git stash list
stash@{0}: WIP on dev: fbefc47 the message after done

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)    
$ git status
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)        about.html

nothing added to commit but untracked files present (use "git add" to track)

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)    
$ git add about.html

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)    
$ git stash
Saved working directory and index state WIP on dev: fbefc47 the 
message after done

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)    
$ git stash list
stash@{0}: WIP on dev: fbefc47 the message after done
stash@{1}: WIP on dev: fbefc47 the message after done

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)    
$ git status
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)        team.html

nothing added to commit but untracked files present (use "git add" to track)

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)    
$ git add team.html

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)    
$ git stash
Saved working directory and index state WIP on dev: fbefc47 the 
message after done

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)    
$ git stash list
stash@{0}: WIP on dev: fbefc47 the message after done
stash@{1}: WIP on dev: fbefc47 the message after done
stash@{2}: WIP on dev: fbefc47 the message after done

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)    
$ git stah pop stash@{1}
git: 'stah' is not a git command. See 'git --help'.

The most similar command is
        stash

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)    
$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (f524f05b972759d81d345768a9b2f65a04c1f3b4)

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)    
$ git stash list
stash@{0}: WIP on dev: fbefc47 the message after done
stash@{1}: WIP on dev: fbefc47 the message after done

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)    
$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (9934139d547f41d49f31aed273e84f684d2699d8)

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)    
$ git add --all

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)    
$ git status
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html


Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)    
$ git commit -m "done with home and about"
[dev 95fb750] done with home and about
 2 files changed, 24 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)    
$ git push --set-upstream origin dev
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 568 bytes | 113.00 KiB/s, done.    
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
To github.com:Gabanicole/Gym-git-exercises.git
   fbefc47..95fb750  dev -> dev
branch 'dev' set up to track 'origin/dev'.

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)    
$ git stash list
stash@{0}: WIP on dev: fbefc47 the message after done

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)    
$ git stash pop
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped refs/stash@{0} (1f979039f6289577ad969aa1daebf6551314a536)

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)    
$ git rest --hard
git: 'rest' is not a git command. See 'git --help'.

The most similar commands are
        restore
        reset

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)    
$ git reset --hard
HEAD is now at 95fb750 done with home and about

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)    
$ git status
On branch dev
Your branch is up to date with 'origin/dev'.

nothing to commit, working tree clean

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (dev)    
$

```

## bundle 2

### exercises 1
```bash
Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (main)
$ git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (ft/bundle-2)
$ git status
On branch ft/bundle-2
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        service.html

nothing added to commit but untracked files present (use "git add" to track)

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (ft/bundle-2)
$ git add service.html

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (ft/bundle-2)
$ git add --all

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (ft/bundle-2)
$ git commit -m"create service page"
[ft/bundle-2 b0c2e78] create service page
 1 file changed, 14 insertions(+)
 create mode 100644 service.html

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (ft/bundle-2)
$ git status
On branch ft/bundle-2
nothing to commit, working tree clean

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (ft/bundle-2)
$ git push --set-upstream origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 500 bytes | 250.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/Gabanicole/Gym-git-exercises/pull/new/ft/bundle-2
remote:
To github.com:Gabanicole/Gym-git-exercises.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (ft/bundle-2)
$

```

### Exercises 2
```bash


Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (main)
$ git checkout main
Already on 'main'
Your branch is up to date with 'origin/main'.

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (main)
$ git pull
Already up to date.


Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (main)
$ git checkout -b ft/service-redesign
Switched to a new branch 'ft/service-redesign'

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (ft/service-redesign)
$ git add .

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (ft/service-redesign)
$ git commit -m "edited the service page"
[ft/service-redesign 5e839e2] edited the service page
 1 file changed, 3 insertions(+)

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (ft/service-redesign)
$ git push origin ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 361 bytes | 180.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/Gabanicole/Gym-git-exercises/pull/new/ft/service-redesign
remote:
To github.com:Gabanicole/Gym-git-exercises.git
 * [new branch]      ft/service-redesign -> ft/service-redesign

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (ft/service-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (main)
$ git add .

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (main)
$ git stash
Saved working directory and index state WIP on main: 6f25d56  readme redo

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (main)
$ git stash pop
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   service.html

no changes added to commit (use "git add" and/or "git commit -a")
Dropped refs/stash@{0} (d761890b0a11fbb43668b64fbc355ae301b720c0)

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (main)
$ git add --all

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (main)
$ git commit -m "edited the service page added other list"
[main 6882218] edited the service page added other list
 1 file changed, 8 insertions(+)

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 379 bytes | 189.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To github.com:Gabanicole/Gym-git-exercises.git
   6f25d56..6882218  main -> main

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (main)
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (ft/service-redesign)
$ git merge main
Auto-merging service.html
CONFLICT (content): Merge conflict in service.html
Automatic merge failed; fix conflicts and then commit the result.

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (ft/service-redesign|MERGING)    
$  git diff
diff --cc service.html
index c18ff7c,4e0043d..0000000
--- a/service.html
+++ b/service.html
@@@ -10,6 -10,10 +10,13 @@@
   <h1>welcome to our service page
    <ul>
     <li>Our services</li>
++<<<<<<< HEAD
++=======
+    <li>service 1</li>
+    <li>service 1</li>
+    <li>service 1</li>
+    <li>service 1</li>
++>>>>>>> main
    </ul>

   </h1>
.

ce-redesign|MERGING)
$ git merge
error: Merging is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (ft/service-redesign|MERGING)
$ git merge main
error: Merging is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (ft/service-redesign|MERGING)
$ git add .

                                                                ce-redesign|MERGING)
Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (ft/service-redesign|MERGING)
$ git merge main
fatal: You have not concluded your merge (MERGE_HEAD exists).   
Please, commit your changes before you merge.                   ce-redesign|MERGING)

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (ft/service-redesign|MERGING)
$ git commit -m "added an new"
[ft/service-redesign 77abc67] added an new                      ce-redesign|MERGING)

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (ft/service-redesign)
$ git merge main                                                ce-redesign)
Already up to date.

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (ft/service-redesign)                                                    ce-redesign)
$


```

## Bundle 3

### Exercise 1

```bash

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (main)
$ git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (ft/team-page)
$ git status
On branch ft/team-page
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        team.html

nothing added to commit but untracked files present (use "git add" to track)

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (ft/team-page)
$ git add .

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (ft/team-page)
$ git commit -m "create team.html"
[ft/team-page 034bc2a] create team.html
 1 file changed, 12 insertions(+)
 create mode 100644 team.html

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (ft/team-page)
$ git push origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 467 bytes | 233.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/Gabanicole/Gym-git-exercises/pull/new/ft/team-page      
remote:
To github.com:Gabanicole/Gym-git-exercises.git
 * [new branch]      ft/team-page -> ft/team-page

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (ft/team-page)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (main)
$ git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (ft/contact-page)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (ft/team-page)
$ git log
commit 034bc2abdcdac7ce5535c63bc18322040e2104a2 (HEAD -> ft/team-page, origin/ft/team-page)
Author: Nicole <89022581+Gabanicole@users.noreply.github.com>
Date:   Sat May 20 16:34:26 2023 +0200

    create team.html

commit 8658448626ba29af21c2728ba8418f5d199f7bb5 (origin/main, main, ft/contact-page)    
Author: Nicole <89022581+Gabanicole@users.noreply.github.com>
Date:   Sat May 20 16:31:00 2023 +0200

    Update readme.md

commit 6882218d414ebf662bc28c48b530a4cd0a9bd1eb
Author: Nicole <89022581+Gabanicole@users.noreply.github.com>
Date:   Sat May 20 16:10:40 2023 +0200

    edited the service page added other list

commit 6f25d5620a6c7318ba927fbd03f029e7971103ac
Author: Nicole <89022581+Gabanicole@users.noreply.github.com>
Date:   Sat May 20 15:31:59 2023 +0200

     readme redo

commit be257ff245766b64729b0d97bb7f54f1762ff5fe
Merge: c92dc80 b0c2e78
Author: Nicole <89022581+Gabanicole@users.noreply.github.com>
Date:   Sat May 20 10:14:26 2023 +0200

    Merge pull request #1 from Gabanicole/ft/bundle-2

    add  service page

commit c92dc809844e542c0eafac61f0557825ca009ef5
Merge: ebe9641 b594093
Author: Nicole <89022581+Gabanicole@users.noreply.github.com>
Date:   Sat May 20 10:13:20 2023 +0200

    Merge pull request #2 from Gabanicole/dev

    Dev

commit b5940937f081d2a5429e5cf466622c9bc7bb8cd1
Merge: 95fb750 ebe9641
Author: Nicole <89022581+Gabanicole@users.noreply.github.com>
Date:   Sat May 20 10:12:55 2023 +0200

    Merge branch 'main' into dev

commit ebe96418cf2cb88c1716010405a98490ec8142b1
Author: Nicole <89022581+Gabanicole@users.noreply.github.com>
Date:   Sat May 20 00:04:49 2023 +0200

     done with exercises1 bundle 2

commit b0c2e78d015a31c58fbe934fbf9a9176e2ea3996
Author: Nicole <89022581+Gabanicole@users.noreply.github.com>
Date:   Fri May 19 23:49:36 2023 +0200

    create service page

commit ea77e85f66197a0a1421a285531bbe3bba2c2f5b
Author: Nicole <89022581+Gabanicole@users.noreply.github.com>
Date:   Fri May 19 22:55:31 2023 +0200

     done with exercise 2

commit 0926072a6924fb21f006f7a8ab2ee5c7b929d805
Author: Nicole <89022581+Gabanicole@users.noreply.github.com>
Date:   Fri May 19 22:50:41 2023 +0200

    done with exercises two

commit 95fb750576e59a8957850d96166824fafb900e98
Author: Nicole <89022581+Gabanicole@users.noreply.github.com>
Date:   Fri May 19 22:44:24 2023 +0200

    done with home and about

commit eaafae86605dfc1e8aad7a720d738f9198630609
Author: Nicole <89022581+Gabanicole@users.noreply.github.com>
Date:   Fri May 19 22:07:20 2023 +0200

    done with the readme me copying

commit fbefc47dd25d2897ebc73eb4e110974bb3d2774b
Author: Nicole <89022581+Gabanicole@users.noreply.github.com>
Date:   Fri May 19 22:05:00 2023 +0200

    the message after done

commit 4024ecc6ba437de2888d25c21a470600fa2ea7df
Author: Nicole <89022581+Gabanicole@users.noreply.github.com>
Date:   Fri May 19 22:00:22 2023 +0200

     done with exercise 1

commit 2862e9a8da93eafac6d9db34634afae7bf4700b1
Author: Nicole <89022581+Gabanicole@users.noreply.github.com>
Date:   Fri May 19 21:52:21 2023 +0200
$ git checkout ft/contact-page
Switched to branch 'ft/contact-page'

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (ft/contapage)ct-page)
$ git cherry-pick commit 034bc2abdcdac7ce5535c63bc18322040e2104a2
fatal: bad revision 'commit'                                    ct-page)
                                                                2
Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (ft/contact-page)
$ git cherry-pick  034bc2abdcdac7ce5535c63bc18322040e2104a2     ct-page)
[ft/contact-page f0cb672] create team.html
 Date: Sat May 20 16:34:26 2023 +0200
 1 file changed, 12 insertions(+)
 create mode 100644 team.html

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (ft/contact-page)                                                        ct-page)
$ it add .
bash: it: command not found

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (ft/contact-page)
$ git add .

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (ft/contact-page)
$ git push origin ft/contact-page
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/Gabanicole/Gym-git-exercises/pull/new/ft/contact-page   
remote:
To github.com:Gabanicole/Gym-git-exercises.git
 * [new branch]      ft/contact-page -> ft/contact-page

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (ft/contact-page)
$ git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (ft/faq-page)
$ git add .

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (ft/faq-page)
$ git status
On branch ft/faq-page   
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   faq.html


Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (ft/faq-page)
$ git commit -m"created a faq page"
[ft/faq-page 0e51663] created a faq page
 1 file changed, 14 insertions(+)
 create mode 100644 faq.html

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (ft/faq-page)
$ git push origin ft/faq-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 478 bytes | 159.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/Gabanicole/Gym-git-exercises/pull/new/ft/faq-page       
remote:
To github.com:Gabanicole/Gym-git-exercises.git
 * [new branch]      ft/faq-page -> ft/faq-page

Nicole@DESKTOP-I5FEMIP MINGW64 ~/desktop/git-exercises (ft/faq-page)
$

```
