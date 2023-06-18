## bandit28

```bash
bandit28@bandit:~$ mktemp -d
/tmp/tmp.4u9ovAPiLS
bandit28@bandit:~$ cd /tmp/tmp.4u9ovAPiLS
bandit28@bandit:/tmp/tmp.4u9ovAPiLS$ git clone ssh://bandit28-git@localhost:2220/home/bandit28-git/repo
bandit28-git@localhost's password:
bandit28@bandit:/tmp/tmp.4u9ovAPiLS$ ls
repo
bandit28@bandit:/tmp/tmp.4u9ovAPiLS$ cd repo/
bandit28@bandit:/tmp/tmp.4u9ovAPiLS/repo$ l
README.md
bandit28@bandit:/tmp/tmp.4u9ovAPiLS/repo$ cat README.md
# Bandit Notes
Some notes for level29 of bandit.

## credentials

- username: bandit29
- password: xxxxxxxxxx
bandit28@bandit:/tmp/tmp.4u9ovAPiLS/repo$ git log
commit abcff758fa6343a0d002a1c0add1ad8c71b88534
Author: Morla Porla <morla@overthewire.org>
Date:   Sun Apr 23 18:04:39 2023 +0000

    add missing data
bandit28@bandit:/tmp/tmp.4u9ovAPiLS/repo$ git checkout abcff758fa6343a0d002a1c0add1ad8c71b88534
bandit28@bandit:/tmp/tmp.4u9ovAPiLS/repo$ cat README.md
# Bandit Notes
Some notes for level29 of bandit.

## credentials

- username: bandit29
- password: tQKvmcwNYcFS6vmPHIUSI3ShmsrQZK8S
```
- ` git log ` - used to display the commit history of a Git repository. It shows a chronological list of commits, allowing you to see the author, date, and commit message for each commit.
- ` git checkout ` - used to switch between different branches, restore files from previous commits, and create new branches.