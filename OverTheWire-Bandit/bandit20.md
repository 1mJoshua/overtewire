## bandit20

```bash
server 1

bandit20@bandit:~$ cat /etc/bandit_pass/bandit20
VxCazJaVykI6W36BkBU0mJTCM8rR95XT
bandit20@bandit:~$ nc -lvnp 3333
Listening on 0.0.0.0 3333
```

```bash
server 2

bandit20@bandit:~$ ls
suconnect
bandit20@bandit:~$ ./suconnect 3333
```

```bash
server 1

Connection received on 127.0.0.1 35974
VxCazJaVykI6W36BkBU0mJTCM8rR95XT
NvEJF7oVjkddltPSrdKEFOllh9V1IBcq
```

```bash
server 2

Read: VxCazJaVykI6W36BkBU0mJTCM8rR95XT
Password matches, sending next password
```
- ` nc -lvnp 3333 ` - start connection with with netcat on port 3333.