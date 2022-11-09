## Git Exercise

This repository contains solutions to git exercise

## Bundle 1

## Exercise 1:

```bash
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents$ mkdir gym-git-exercises && cd gym-git-exercises
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git init
Initialized empty Git repository in /home/thegym/Documents/gym-git-exercises/.git/
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git branch -M main
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ touch README.md
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ vim README.md
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git add README.md
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git commit -m "feat: added some content to the README.md"
[main (root-commit) 6abd885] feat: added some content to the README.md
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 README.md
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git remote add origin https://github.com/mbukeRepo/Gym-Git-Exercise-Solutions.git
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git push origin main
Username for 'https://github.com': mbukeRepo
Password for 'https://mbukeRepo@github.com':
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 233 bytes | 233.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/mbukeRepo/Gym-Git-Exercise-Solutions.git
 * [new branch]      main -> main
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git switch -c dev
Switched to a new branch 'dev'
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git branch
* dev
  main
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git switch -c test
Switched to a new branch 'test'
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git checkout dev
Switched to branch 'dev'
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git branch -d test
Deleted branch test (was 6abd885).
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git branch
* dev
  main
```

## Exercise 2:

```bash
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ nano home.html
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git add home.html
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git stash push -m "home page"
Saved working directory and index state On master: home page
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ nano about.html
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git add about.html
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git stash push -m "about page"
Saved working directory and index state On master: about page
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ nano team.html
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git add team.html
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git stash push -m "team page"
Saved working directory and index state On master: team page
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git stash list
stash@{0}: On master: team page
stash@{1}: On master: about page
stash@{2}: On master: home page
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git stash pop 1
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	new file:   about.html

Dropped refs/stash@{1} (fee7b9ed2e5f7f19b2e1d2c5fdb9a9ecb078ade6)
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git stash pop 1
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	new file:   about.html
	new file:   home.html

Dropped refs/stash@{1} (5139ed1b9a177bcd5afa0d5d59ccce61f01d4d25)
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git add home.html about.html
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git commit -m "feat: added home and about page"
[dev a79981b] feat: added home and about page
 2 files changed, 22 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git push origin dev
Username for 'https://github.com': mbukeRepo
Password for 'https://mbukeRepo@github.com':
Enumerating objects: 9, done.
Counting objects: 100% (9/9), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (7/7), 850 bytes | 425.00 KiB/s, done.
Total 7 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 1 local object.
To https://github.com/mbukeRepo/Gym-Git-Exercise-Solutions.git
   09271fc..a79981b  dev -> dev
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git stash pop
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	new file:   team.html

Dropped refs/stash@{0} (7f8b195ed67e8e3cda8e0dbd80d84f3c11ad30db)
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git reset --hard
HEAD is now at a79981b feat: added home and about page
```
