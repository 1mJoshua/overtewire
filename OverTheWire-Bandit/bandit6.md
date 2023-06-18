## bandit6

```bash
bandit6@bandit:~$ find / -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null
/var/lib/dpkg/info/bandit7.password
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
```
- ` / `- starting point of the search as the root directory.
- ` -type f ` - file type.
- ` -user bandit7 ` - find username.
- ` -group bandit6 ` - group name.
- ` -size 33c ` - size of file.