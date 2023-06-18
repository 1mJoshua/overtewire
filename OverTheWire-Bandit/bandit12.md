## bandit12

```bash
bandit12@bandit:~$ ls
data.txt
bandit12@bandit:~$ cat data.txt
00000000: 1f8b 0808 2773 4564 0203 6461 7461 322e  ....'sEd..data2.
00000010: 6269 6e00 0145 02ba fd42 5a68 3931 4159  bin..E...BZh91AY
bandit12@bandit:~$ mkdir /tmp/12
bandit12@bandit:~$ cp data.txt /tmp/12
bandit12@bandit:~$ cd /tmp/12
bandit12@bandit:/tmp/12$ ls
data.txt
bandit12@bandit:/tmp/12$ cat data.txt | xxd -r
'sEddata2.binE��BZh91AY&SY{O�_���o����������������׿�����������;Vhd4�A4h�4M��i�"
bandit12@bandit:/tmp/12$ cat data.txt | xxd -r > hexdump
bandit12@bandit:/tmp/12$ ls
data.txt  hexdump
bandit12@bandit:/tmp/12$ file hexdump
hexdump: gzip compressed data, was "data2.bin", last modified: Sun Apr 23 18:04:23 2023, max compression, from Unix, original size modulo 2^32 581
bandit12@bandit:/tmp/12$ mv hexdump hexdump.gz
bandit12@bandit:/tmp/12$ ls
data.txt  hexdump.gz
bandit12@bandit:/tmp/12$ gzip -d hexdump.gz
bandit12@bandit:/tmp/12$ ls
data.txt  hexdump
bandit12@bandit:/tmp/12$ file hexdump
hexdump: bzip2 compressed data, block size = 900k
bandit12@bandit:/tmp/12$ mv hexdump hexdump.bz2
bandit12@bandit:/tmp/12$ ls
data.txt  hexdump.bz2
bandit12@bandit:/tmp/12$ bzip2 -d hexdump.bz2
bandit12@bandit:/tmp/12$ file hexdump
hexdump: gzip compressed data, was "data4.bin", last modified: Sun Apr 23 18:04:23 2023, max compression, from Unix, original size modulo 2^32 20480
bandit12@bandit:/tmp/12$ mv hexdump hexdump.gz
bandit12@bandit:/tmp/12$ gzip -d hexdump.gz
bandit12@bandit:/tmp/12$ file hexdump
hexdump: POSIX tar archive (GNU)
bandit12@bandit:/tmp/12$ tar -xvf hexdump
data5.bin
bandit12@bandit:/tmp/12$ file data5.bin
data5.bin: POSIX tar archive (GNU)
bandit12@bandit:/tmp/12$ tar -xvf data5.bin
data6.bin
bandit12@bandit:/tmp/12$ file data6.bin
data6.bin: bzip2 compressed data, block size = 900k
bandit12@bandit:/tmp/12$ ls
data5.bin  data6.bin  data.txt  hexdump
bandit12@bandit:/tmp/12$ mv data6.bin hex.bz2
bandit12@bandit:/tmp/12$ ls
data5.bin  data.txt  hex.bz2  hexdump
bandit12@bandit:/tmp/12$ bzip2 -d hex.bz2
bandit12@bandit:/tmp/12$ ls
data5.bin  data.txt  hex  hexdump
bandit12@bandit:/tmp/12$ file hex
hex: POSIX tar archive (GNU)
bandit12@bandit:/tmp/12$ tar -xvf hex
data8.bin
bandit12@bandit:/tmp/12$ file data8.bin
data8.bin: gzip compressed data, was "data9.bin", last modified: Sun Apr 23 18:04:23 2023, max compression, from Unix, original size modulo 2^32 49
bandit12@bandit:/tmp/12$ mv data8.bin hex2.gz
bandit12@bandit:/tmp/12$ gzip -d hex2.gz
bandit12@bandit:/tmp/12$ file hex2
hex2: ASCII text
bandit12@bandit:/tmp/12$ cat hex2
The password is wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
```
- ` cp data.txt /tmp/12 ` - copy file to path of directory.
- ` xxd -r ` - perform the reverse operation, converting hexadecimal data back into binary form.
- ` mv ` - move file to path of directory.
