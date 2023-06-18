## leviathan1

```bash
leviathan1@gibson:~$ ls
check
leviathan1@gibson:~$ file check 
check: setuid ELF 32-bit LSB executable, Intel 80386, version 1 (SYSV), dynamically linked, interpreter /lib/ld-linux.so.2, BuildID[sha1]=aab009a1eb3940df51c668d1c35dc9cdc1191805, for GNU/Linux 3.2.0, not stripped
leviathan1@gibson:~$ ./check 
password: 123
Wrong password, Good Bye ...
leviathan1@gibson:~$ ltrace ./check 
__libc_start_main(0x80491e6, 1, 0xffffd604, 0 <unfinished ...>
printf("password: ")                       = 10
getchar(0xf7fbe4a0, 0xf7fd6f80, 0x786573, 0x646f67password: helo
) = 104
getchar(0xf7fbe4a0, 0xf7fd6f68, 0x786573, 0x646f67) = 101
getchar(0xf7fbe4a0, 0xf7fd6568, 0x786573, 0x646f67) = 108
strcmp("hel", "sex")                       = -1
puts("Wrong password, Good Bye ..."Wrong password, Good Bye ...
)       = 29
+++ exited (status 0) +++
leviathan1@gibson:~$ ./check 
password: sex
$ 
$ whoami
leviathan2
$ cat /etc/leviathan_pass/leviathan2
mEh5PNl10e
$ exit
```

` ltrace /check ` - used the command "ltrace ./check" to trace the library calls made by the program. The trace shows that the program uses the "strcmp" function to compare the entered password with a predefined password. In this case, the entered password was "helo," and the predefined password was "sex." Since the two strings are not the same, the "strcmp" function returned a value of "-1," indicating that they are different. Consequently, the program printed "Wrong password, Good Bye ..." and terminated again.