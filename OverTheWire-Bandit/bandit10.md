## bandit10

```bash
bandit10@bandit:~$ ls
data.txt
bandit10@bandit:~$ cat data.txt
VGhlIHBhc3N3b3JkIGlzIDZ6UGV6aUxkUjJSS05kTllGTmI2blZDS3pwaGxYSEJNCg==
bandit10@bandit:~$ cat data.txt | base64 -d
The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
```
- ` base64 `
	-  ` A - Z ` - 26 characters.
	- ` a- z ` - 26 characters.
	- ` 0 - 9 ` - 10 characters.
	- ` +, / ` - 2 characters.
	- ` = ` - 1 characters.
- ` base64 -d ` - base64 decoder.

- another technique
```bash
bandit10@bandit:~$ echo "VGhlIHBhc3N3b3JkIGlzIDZ6UGV6aUxkUjJSS05kTllGTmI2blZDS3pwaGxYSEJNCg==" | base64 -d  The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
```