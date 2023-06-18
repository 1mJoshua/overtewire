## bandit31

```bash
bandit31@bandit:~$ mktemp -d
/tmp/tmp.TWF80h5iO6
bandit31@bandit:~$ cd /tmp/tmp.TWF80h5iO6
bandit31@bandit:/tmp/tmp.TWF80h5iO6$ git clone ssh://bandit31-git@localhost:2220/home/bandit31-git/repo
bandit31-git@localhost's password:
bandit31@bandit:/tmp/tmp.TWF80h5iO6$ ls
repo
bandit31@bandit:/tmp/tmp.TWF80h5iO6$ cd repo/
bandit31@bandit:/tmp/tmp.TWF80h5iO6/repo$ ls
README.md
bandit31@bandit:/tmp/tmp.TWF80h5iO6/repo$ cat README.md
This time your task is to push a file to the remote repository.

Details:
    File name: key.txt
    Content: 'May I come in?'
    Branch: master

bandit31@bandit:/tmp/tmp.TWF80h5iO6/repo$ git branch
* master
bandit31@bandit:/tmp/tmp.TWF80h5iO6/repo$ touch key.txt
bandit31@bandit:/tmp/tmp.TWF80h5iO6/repo$ echo "May I come in?" >
 key.txt
bandit31@bandit:/tmp/tmp.TWF80h5iO6/repo$ git add key.txt
The following paths are ignored by one of your .gitignore files:
key.txt
hint: Use -f if you really want to add them.
hint: Turn this message off by running
hint: "git config advice.addIgnoredFile false"
bandit31@bandit:/tmp/tmp.TWF80h5iO6/repo$ ls -al
total 24
drwxrwxr-x 3 bandit31 bandit31 4096 Jun 14 10:10 .
drwx------ 3 bandit31 bandit31 4096 Jun 14 10:08 ..
drwxrwxr-x 8 bandit31 bandit31 4096 Jun 14 10:11 .git
-rw-rw-r-- 1 bandit31 bandit31    6 Jun 14 10:08 .gitignore
-rw-rw-r-- 1 bandit31 bandit31   15 Jun 14 10:11 key.txt
-rw-rw-r-- 1 bandit31 bandit31  147 Jun 14 10:08 README.md
bandit31@bandit:/tmp/tmp.TWF80h5iO6/repo$ cat .gitignore
*.txt
bandit31@bandit:/tmp/tmp.TWF80h5iO6/repo$ rm .gitignore
bandit31@bandit:/tmp/tmp.TWF80h5iO6/repo$ git add key.txt
bandit31@bandit:/tmp/tmp.TWF80h5iO6/repo$ git commit -m "Upload a file"
[master f6c3ff0] Upload a file
 1 file changed, 1 insertion(+)
 create mode 100644 key.txt
bandit31@bandit:/tmp/tmp.TWF80h5iO6/repo$ git push origin master
bandit31-git@localhost's password:
remote: Well done! Here is the password for the next level:
remote: rmCBvG56y58BXzv98yZGdO7ATVL5dW8y
```
- ` touch ` - create a file.
- ` git add ` - used to add changes or new files to the staging area.
- ` rm ` - remove file or directory.
- ` gitignore `- used to specify intentionally untracked files and directories that Git should ignore. It allows you to specify patterns for files or directories that you don't want to include in your Git repository or track changes for.
- ` git commit ` - used to create a new commit. It takes a snapshot of the current state of the repository and adds it to the history.
- ` -m "Upload a file" ` - The `-m` option allows you to specify a commit message in the command itself. The commit message is a brief description that summarizes the changes made in the commit.