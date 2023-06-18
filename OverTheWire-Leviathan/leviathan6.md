## leviathan6

```bash
leviathan6@gibson:~$ ls
leviathan6
leviathan6@gibson:~$ ./leviathan6 
usage: ./leviathan6 <4 digit code>
leviathan6@gibson:~$ ltrace ./leviathan6 
__libc_start_main(0x80491d6, 1, 0xffffd5f4, 0 <unfinished ...>
printf("usage: %s <4 digit code>\n", "./leviathan6"usage: ./leviathan6 <4 digit code>
) = 35
exit(-1 <no return ...>
+++ exited (status 255) +++
leviathan6@gibson:~$ for i in {0000..9999} ;do echo $i;./leviathan6 $i;done;
Wrong
7123
$ whoami
leviathan7
$ cat /etc/leviathan_pass/leviathan7
8GpZ5f8Hze
```
- ` ./leviathan6 ` - executed the program without providing the required 4-digit code. As a result, the program displayed a usage message indicating the correct usage format: "./leviathan6 <4 digit code>".
- ` ltrace ./leviathan6  ` - used "ltrace" to trace the library calls made by the "leviathan6" program. The trace reveals that the program uses the "printf" function to display the usage message. The program then exits with a status of -1, indicating an error.