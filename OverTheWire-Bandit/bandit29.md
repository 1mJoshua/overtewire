## bandit29

```bash
bandit29@bandit:~$ mktemp -d
/tmp/tmp.PepSol2z36
bandit29@bandit:~$ cd /tmp/tmp.PepSol2z36
bandit29@bandit:/tmp/tmp.PepSol2z36$ git clone ssh://bandit29-git@localhost:2220/home/bandit29-git/repo
bandit29-git@localhost's password:
bandit29@bandit:/tmp/tmp.PepSol2z36$ ls
repo
bandit29@bandit:/tmp/tmp.PepSol2z36$ cd repo/
bandit29@bandit:/tmp/tmp.PepSol2z36/repo$ ls
README.md
bandit29@bandit:/tmp/tmp.PepSol2z36/repo$ cat README.md
# Bandit Notes
Some notes for bandit30 of bandit.

## credentials

- username: bandit30
- password: <no passwords in production!>

bandit29@bandit:/tmp/tmp.PepSol2z36/repo$ git branch
* master
bandit29@bandit:/tmp/tmp.PepSol2z36/repo$ git branch -r
  origin/HEAD -> origin/master
  origin/dev
  origin/master
  origin/sploits-dev
bandit29@bandit:/tmp/tmp.PepSol2z36/repo$ git log
commit 4bd5389f9f2b9e96ba517aa751ee58d051905761 (HEAD -> master, origin/master, origin/HEAD)
Author: Ben Dover <noone@overthewire.org>
Date:   Sun Apr 23 18:04:40 2023 +0000

    fix username

commit 1a57cf10158f133c4f40ff82251f605a7618631d
Author: Ben Dover <noone@overthewire.org>
Date:   Sun Apr 23 18:04:40 2023 +0000

    initial commit of README.md
bandit29@bandit:/tmp/tmp.PepSol2z36/repo$ git checkout dev
Branch 'dev' set up to track remote branch 'dev' from 'origin'.
Switched to a new branch 'dev'
bandit29@bandit:/tmp/tmp.PepSol2z36/repo$ ls
code  README.md
bandit29@bandit:/tmp/tmp.PepSol2z36/repo$ cat README.md
# Bandit Notes
Some notes for bandit30 of bandit.

## credentials

- username: bandit30
- password: xbhV3HpNGlTIdnjUrdAlPzc2L6y9EOnS
```
- ` git branch -r ` - used to manage branches within a repository. It allows you to list, create, delete, and rename branches, ` -r ` - remote.