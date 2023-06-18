## bandit30

```bash
bandit30@bandit:~$ mktemp -d
/tmp/tmp.3wHV1EkoAj
bandit30@bandit:~$ cd /tmp/tmp.3wHV1EkoAj
bandit30@bandit:/tmp/tmp.3wHV1EkoAj$ git clone ssh://bandit30-git@localhost:2220/home/bandit30-git/repo
bandit30-git@localhost's password:
bandit30@bandit:/tmp/tmp.3wHV1EkoAj$ ls
repo
bandit30@bandit:/tmp/tmp.3wHV1EkoAj$ cd repo/
bandit30@bandit:/tmp/tmp.3wHV1EkoAj/repo$ ls
README.md
bandit30@bandit:/tmp/tmp.3wHV1EkoAj/repo$ cat README.md
just an epmty file... muahaha
bandit30@bandit:/tmp/tmp.3wHV1EkoAj/repo$ git tag
secret
bandit30@bandit:/tmp/tmp.3wHV1EkoAj/repo$ git show secret
OoffzGDlzhAlerFJ2cAiz1D41JW1Mhmt
```
- ` git tag ` - used to manage tags, which are references to specific points in Git history. Tags are often used to mark significant commits, such as releases or important milestones, lists all the tags in your repository.
- ` git show ` - used to display detailed information about a specific Git object, such as a commit, tag, or tree. It provides a comprehensive view of the changes and metadata associated with the object.