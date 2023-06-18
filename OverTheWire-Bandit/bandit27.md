## bandit27

```bash
bandit27@bandit:~$ mktemp -d
/tmp/tmp.xMSuZJhn9b
bandit27@bandit:~$ cd /tmp/tmp.xMSuZJhn9b
bandit27@bandit:/tmp/tmp.xMSuZJhn9b$ cat /etc/bandit_pass/bandit27
YnQpBuifNMas1hcUFk70ZmqkhUU2EuaS
bandit27@bandit:/tmp/tmp.xMSuZJhn9b$ git clone  ssh://bandit27-git@localhost:2220/home/bandit27-git/repo
bandit27-git@localhost's password:
bandit27@bandit:/tmp/tmp.xMSuZJhn9b$ ls
repo
bandit27@bandit:/tmp/tmp.xMSuZJhn9b$ cd repo/
bandit27@bandit:/tmp/tmp.xMSuZJhn9b/repo$ ls
README
bandit27@bandit:/tmp/tmp.xMSuZJhn9b/repo$ cat README
The password to the next level is: AVanL161y9rsbcJIsFHuw35rjaOM19nR
```
- ` git clone ` - used to create a local copy of a Git repository. It allows you to obtain a complete copy of a remote repository, including all of its files, commit history, and branches.
