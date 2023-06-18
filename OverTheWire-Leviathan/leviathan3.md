## leviathan3

```bash
leviathan3@gibson:~$ ls
level3
leviathan3@gibson:~$ ltrace ./level3 
__libc_start_main(0x80492bf, 1, 0xffffd604, 0 <unfinished ...>
strcmp("h0no33", "kakaka")             = -1
printf("Enter the password> ")         = 20
fgets(Enter the password> hello
"hello\n", 256, 0xf7e2a620)      = 0xffffd3dc
strcmp("hello\n", "snlprintf\n")       = -1
puts("bzzzzzzzzap. WRONG"bzzzzzzzzap. WRONG
)             = 19
+++ exited (status 0) +++
leviathan3@gibson:~$ ./level3 
Enter the password> snlprintf
[You've got shell]!
$ whoami
leviathan4
$ cat /etc/leviathan_pass/leviathan4
AgvropI4OA
```
- ` ltrace ./level3 ` - to trace the library calls made by the program. The trace reveals that the program compares the entered password with a predefined password using the "strcmp" function. In this case, the entered password was "hello\n" (including a newline character), and the predefined password was "snlprintf\n" (also including a newline character). Since the two strings are not the same, the "strcmp" function returned a value of "-1," indicating that they are different. Consequently, the program printed "bzzzzzzzzap. WRONG" and terminated.