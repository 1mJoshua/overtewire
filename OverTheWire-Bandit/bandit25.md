## bandit25

```bash
bandit25@bandit:~$ cat /etc/passwd | grep "bandit26"
bandit26:x:11026:11026:bandit level 26:/home/bandit26:/usr/bin/showtext
bandit25@bandit:~$ cat /usr/bin/showtext
#!/bin/sh

export TERM=linux

exec more ~/text.txt
exit 0
```

- make a small size of terminal.
```bash
bandit25@bandit:~$ ls
bandit26.sshkey
bandit25@bandit:~$ ssh bandit26@localhost -i bandit26.sshkey -p 2220
```

- type v to use vim
```bash
:r /etc/bandit_pass/bandit26

c7GvcKlw9mC7aUQaPx7nwFstuAIBw1o1
```

