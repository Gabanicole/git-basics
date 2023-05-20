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
