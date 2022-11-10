## Git Exercise

This repository contains solutions to git exercise

## Bundle 1:

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

## Bundle 2:

### Exercise 1:

```bash
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git switch -c ft/bundle-2
Switched to a new branch 'ft/bundle-2'
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ nano service.html
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git add service.html
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git commit -m "feat: added service.html"
[ft/bundle-2 6df171d] feat: added service.html
 1 file changed, 12 insertions(+)
 create mode 100644 service.html
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git push origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 459 bytes | 229.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/mbukeRepo/Gym-Git-Exercise-Solutions.git
* [new branch]      ft/bundle-2 -> ft/bundle-2
```

### Exercise 2:

```bash
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git checkout main
Switched to branch 'main'
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git pull
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (1/1), 630 bytes | 78.00 KiB/s, done.
From https://github.com/edson-pro/git-exercises
  e0edd9a..3a3bfff  main       -> origin/main
Updating e0edd9a..3a3bfff
Fast-forward
about.html    | 12 ++++++++++++
home.html     | 12 ++++++++++++
service.html | 12 ++++++++++++
3 files changed, 36 insertions(+)
create mode 100644 about.html
create mode 100644 home.html
create mode 100644 service.html
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git checkout -b ft/service-redesign
Switched to a new branch 'ft/service-redesign'
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ nano service.html
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git add service.html
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git commit -m "feat: updated service.html"
[ft/service-redesign 6df171d] feat: updated service.html
 1 file changed, 11 insertions(+)
 create mode 100644 service.html
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git push origin ft/service-redesign
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 459 bytes | 229.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/mbukeRepo/Gym-Git-Exercise-Solutions.git
* [new branch]      ft/service-redesign -> ft/service-redesign
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git checkout main
Switched to branch 'main'
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ nano service.html
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git add service.html
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git commit -m "feat: updated service page"
[main 6df171d] feat: updated service page
 1 file changed, 11 insertions(+)
 create mode 100644 service.html
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git push origin main
Username for 'https://github.com': mbukeRepo
Password for 'https://mbukeRepo@github.com':
Enumerating objects: 11, done.
Counting objects: 100% (11/11), done.
Delta compression using up to 4 threads
Compressing objects: 100% (9/9), done.
Writing objects: 100% (9/9), 3.07 KiB | 629.00 KiB/s, done.
Total 9 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), done.
To https://github.com/mbukeRepo/Gym-Git-Exercise-Solutions.git
 + 1f0b6f1...4b06eea main -> main
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git diff
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git checkout main
Switched to branch 'main'
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git merge ft/service-redesign
Auto-merging notes
CONFLICT (content): Merge conflict in notes
Automatic merge failed; fix conflicts and then commit the result.
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git add .
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git commit -m "fix: resolved conflicts and merge"
[main 6df171d] fix: resolved conflicts and merge
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git push origin ft/service-redesign
Username for 'https://github.com': mbukeRepo
Password for 'https://mbukeRepo@github.com':
Enumerating objects: 11, done.
Counting objects: 100% (11/11), done.
Delta compression using up to 4 threads
Compressing objects: 100% (9/9), done.
Writing objects: 100% (9/9), 3.07 KiB | 629.00 KiB/s, done.
Total 9 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), done.
To https://github.com/mbukeRepo/Gym-Git-Exercise-Solutions.git
 + 1f0b6f1...4b06eea ft/service-redesign -> ft/service-redesign
```

## Bundle 3:

### Exercise 1:

```bash
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ nano team.html
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git add faq.html
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git commit -m "feat: added faq page"
[ft/faq-page 6df171d] feat: added faq page
 1 file changed, 11 insertions(+)
 create mode 100644 faq.html
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git checkout main
Switched to branch 'main'
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git log --oneline
0a58f74 (HEAD -> ft/team-page, origin/ft/team-page) feat: added team.html
914f43d (origin/main, main, ft/contact-page) feat: merged ft/service-redesign with main
0f80041 feat: updated service.html
5c1754d feat: added service.html
bbd1499 (origin/ft/service-redesign, ft/service-redesign) feat: added service list
652f43f (dev) starting bundle 2
a79981b (origin/dev) feat: added home and about page
bce0cdb fix: added remaining command for exercise 1
09271fc feat: added solution to first exercise
6abd885 feat: added some content to the README.md
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git checkout ft/contact-page
Switched to branch 'ft/contact-page'
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git cherry-pick 0a58f74
[ft/contact-page 9311567] feat: added team.html
 Date: Wed Nov 9 23:19:08 2022 +0200
 1 file changed, 11 insertions(+)
 create mode 100644 team.html
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ nano contact.html
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git add contact.html
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git commit -m "feat: added contact page"
[ft/contact-page cd333ae] feat: added contact page
 1 file changed, 15 insertions(+)
 create mode 100644 contact.html
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git push origin ft/contact-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 459 bytes | 229.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/mbukeRepo/Gym-Git-Exercise-Solutions.git
* [new branch]      ft/contact-page -> ft/contact-page
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ nano faq.html
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git add faq.html
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git commit -m "feat: added faq page "
[ft/faq-page 6df171d] feat: added faq page
 1 file changed, 11 insertions(+)
 create mode 100644 faq.html
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git push origin ft/faq-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 459 bytes | 229.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/mbukeRepo/Gym-Git-Exercise-Solutions.git
* [new branch]      ft/faq-page -> ft/faq-page
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git revert 0a58f74
[ft/faq-page 398f570] Revert "feat: added team.html"
1 file changed, 10 insertions(+), 15 deletions(-)
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git push origin ft/faq-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 459 bytes | 229.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/mbukeRepo/Gym-Git-Exercise-Solutions.git
* [new branch]      ft/faq-page -> ft/faq-page
```

### Exercise 2

```bash
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git checkout -b ft/home-page-redesign
Switched to a new branch 'ft/home-page-redesign'
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git checkout main
Switched to branch 'main'
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ nano README.md
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git add README.md
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git commit -m "feat: updated README.md"
[main 1e36623] feat: updated README.md
 1 file changed, 45 insertions(+), 2 deletions(-)
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git checkout main
Switched to branch 'main'
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git push origin main
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 459 bytes | 229.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/mbukeRepo/Gym-Git-Exercise-Solutions.git
 + 1f0b6f1...4b06eea ft/home-page-redesign -> ft/home-page-redesign
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git checkout ft/home-page-redesign
Switched to branch 'ft/home-page-redesign'
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git rebase main
Successfully rebased and updated refs/heads/ft/home-page-redesign
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ nano home.html
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git add home.html
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git commit -m "feat: added title on home page"
[ft/home-page-redesign 6df171d] feat: added title on home page
 1 file changed, 11 insertions(+)
 create mode 100644 home.html
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git push origin ft/home-page-redesign
Username for 'https://github.com': mbukeRepo
Password for 'https://mbukeRepo@github.com':
Enumerating objects: 11, done.
Counting objects: 100% (11/11), done.
Delta compression using up to 4 threads
Compressing objects: 100% (9/9), done.
Writing objects: 100% (9/9), 3.07 KiB | 629.00 KiB/s, done.
Total 9 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), done.
To https://github.com/mbukeRepo/Gym-Git-Exercise-Solutions.git
 + 1f0b6f1...4b06eea ft/home-page-redesign -> ft/home-page-redesign

```

## Bundle 4

### Exercise 1:

```bash
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git checkout main
Already on 'main'
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git remote add git-copy https://github.com/mbukeRepo/test.git
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git remote
git-copy
origin
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ ls
about.html  home.html  README.md  service.html
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ nano home.html
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git add home.html
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git commit -m "feat: added content to home page"
[main 7f9f397] feat: added content to home page
 1 file changed, 1 insertion(+)
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git push origin main
Username for 'https://github.com': mbukeRepo
Password for 'https://mbukeRepo@github.com':
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 329 bytes | 329.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/mbukeRepo/Gym-Git-Exercise-Solutions.git
   20e42ba..7f9f397  main -> main
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git remote
git-copy
origin
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git push  git-copy main
Username for 'https://github.com': mbukeRepo
Password for 'https://mbukeRepo@github.com':
Enumerating objects: 46, done.
Counting objects: 100% (46/46), done.
Delta compression using up to 4 threads
Compressing objects: 100% (42/42), done.
Writing objects: 100% (46/46), 6.85 KiB | 584.00 KiB/s, done.
Total 46 (delta 17), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (17/17), done.
To https://github.com/mbukeRepo/test.git
 * [new branch]      main -> main
```

### Exercise 2

```bash
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git checkout -b ft/footer
Switched to a new branch 'ft/footer'
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ nano footer.html
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git branch
  dev
  ft/bundle-2
  ft/contact-page
  ft/faq-page
* ft/footer
  ft/home-page-redesign
  ft/service-redesign
  ft/team-page
  main
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ ls
about.html  footer.html  home.html  README.md  service.html
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git add footer.html
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git commit -m "feat: added footer"
[ft/footer 444b3c5] feat: added footer
 1 file changed, 8 insertions(+)
 create mode 100644 footer.html
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ nano header.html
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git add header.html
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git commit -m "feat: added header page"
[ft/footer d8456a8] feat: added header page
 1 file changed, 6 insertions(+)
 create mode 100644 header.html
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git branch
  dev
  ft/bundle-2
  ft/contact-page
  ft/faq-page
* ft/footer
  ft/home-page-redesign
  ft/service-redesign
  ft/team-page
  main
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git push origin ft/footer
Username for 'https://github.com': mbukeRepo
Password for 'https://mbukeRepo@github.com':
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 694 bytes | 231.00 KiB/s, done.
Total 6 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
remote:
remote: Create a pull request for 'ft/footer' on GitHub by visiting:
remote:      https://github.com/mbukeRepo/Gym-Git-Exercise-Solutions/pull/new/ft/footer
remote:
To https://github.com/mbukeRepo/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/footer -> ft/footer
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git checkout main
Switched to branch 'main'
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git checkout -b ft/squashing
Switched to a new branch 'ft/squashing'
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git merge --squash ft/footer
Updating 7f9f397..d8456a8
Fast-forward
Squash commit -- not updating HEAD
 footer.html | 8 ++++++++
 header.html | 6 ++++++
 2 files changed, 14 insertions(+)
 create mode 100644 footer.html
 create mode 100644 header.html
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git status
On branch ft/squashing
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	new file:   footer.html
	new file:   header.html

thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git commit -m "footer changes squashing"
[ft/squashing badc4dd] footer changes squashing
 2 files changed, 14 insertions(+)
 create mode 100644 footer.html
 create mode 100644 header.html
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git push
fatal: The current branch ft/squashing has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/squashing

thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/gym-git-exercises$ git push --set-upstream origin ft/squashing
Username for 'https://github.com': mbukeRepo
Password for 'https://mbukeRepo@github.com':
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 524 bytes | 262.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'ft/squashing' on GitHub by visiting:
remote:      https://github.com/mbukeRepo/Gym-Git-Exercise-Solutions/pull/new/ft/squashing
remote:
To https://github.com/mbukeRepo/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/squashing -> ft/squashing
Branch 'ft/squashing' set up to track remote branch 'ft/squashing' from 'origin'.
```

## Bundle 5

### Exercise 1:

Done on GitHub

### Exercise 2:

```bash
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents$ git clone https://github.com/mbukeRepo/git-cafe-exercise.git
Cloning into 'git-cafe-exercise'...
remote: Enumerating objects: 107, done.
remote: Counting objects: 100% (107/107), done.
remote: Compressing objects: 100% (101/101), done.
remote: Total 107 (delta 5), reused 104 (delta 4), pack-reused 0
Receiving objects: 100% (107/107), 1.95 MiB | 43.00 KiB/s, done.
Resolving deltas: 100% (5/5), done.
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents$ cd git-cafe*
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/git-cafe-exercise$ ls
bat  images        index-2.html  index-4.html  js
css  index-1.html  index-3.html  index.html    README.md
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/git-cafe-exercise$ nano index.html
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/git-cafe-exercise$ code .
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/git-cafe-exercise$ git add index.html
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/git-cafe-exercise$ git commit -m "feat: changed welcome to our place to welcome to our restaurant"
[main 2f668f6] feat: changed welcome to our place to welcome to our restaurant
 1 file changed, 448 insertions(+), 288 deletions(-)
 rewrite index.html (88%)
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/git-cafe-exercise$ git origin
git: 'origin' is not a git command. See 'git --help'.
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/git-cafe-exercise$ git remote
origin
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/git-cafe-exercise$ git remote origin main
error: Unknown subcommand: origin
usage: git remote [-v | --verbose]
   or: git remote add [-t <branch>] [-m <master>] [-f] [--tags | --no-tags] [--mirror=<fetch|push>] <name> <url>
   or: git remote rename <old> <new>
   or: git remote remove <name>
   or: git remote set-head <name> (-a | --auto | -d | --delete | <branch>)
   or: git remote [-v | --verbose] show [-n] <name>
   or: git remote prune [-n | --dry-run] <name>
   or: git remote [-v | --verbose] update [-p | --prune] [(<group> | <remote>)...]
   or: git remote set-branches [--add] <name> <branch>...
   or: git remote get-url [--push] [--all] <name>
   or: git remote set-url [--push] <name> <newurl> [<oldurl>]
   or: git remote set-url --add <name> <newurl>
   or: git remote set-url --delete <name> <url>

    -v, --verbose         be verbose; must be placed before a subcommand

thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/git-cafe-exercise$ git branch
* main
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/git-cafe-exercise$ git push
Username for 'https://github.com': mbukeRepo
Password for 'https://mbukeRepo@github.com':
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 1.57 KiB | 403.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/mbukeRepo/git-cafe-exercise.git
   d1d3f9c..2f668f6  main -> main
thegym@thegym-ThinkPad-T470s-W10DG:~/Documents/git-cafe-exercise$ ls
bat  images        index-2.html  index-4.html  js
css  index-1.html  index-3.html  index.html    README.md
```
