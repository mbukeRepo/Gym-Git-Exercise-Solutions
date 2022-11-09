## Git Exercise

This repository contains solutions to git exercise

## Bundle 1

## Exercise 1:

```bash
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
