Commands: 
1. ssh -  Secure Shell protocol is a way to securely connect the Shell of a computer or server. We create a connection between our computer and the server with SSH.
2. ls - Short for List, and it lists the files in the directory you're in.
3. cd - Change working directory. 
4. cat - Short for "concatenate" used to read what's inside this file.
5. file - Determine file type.
6. du - Estimate file space usage. 
7. find - Search for files in a directory hierarchy.
8. grep - Print lines that match patterns.
9. man - An interface to the system reference manuals.
10. sort - Sorts the contents of a text file, line by line.
11. uniq - Reports or filters out the repeated lines in a file. 
12. strings - Looks for printable strings in a file. 
13. tr - For translating or deleting characters.
14. tar - Archiving and compressing files and folders.
15. gzip - Compresses files. 
16. bzip2 - Decompresses all specified files to the standard output.
17. xxd - Used to manage, convert, and display binary files
18. mkdir - Create new directory. 
19. cp - Copies the source file specified by the SourceFile parameter to the destination file specified by the TargetFile parameter.
20. mv - Move files within the same file system or between file systems.
21. nc - Reading and writing data between two computer networks.
22. nmap - Network exploration and security auditing.

Level 0:
bandit0@bandit:~$ ls
readme
bandit0@bandit:~$ cat readme
boJ9jbbUNNfktd78OOpsqOltutMc3MY1

Level 1:
bandit1@bandit:~$ ls
-
bandit1@bandit:~$ cat ./-
CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9

Level 2:
bandit2@bandit:~$ ls
spaces in this filename
bandit2@bandit:~$ cat "spaces in this filename"
UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK

Level 3:
bandit3@bandit:~/inhere$ ls
bandit3@bandit:~/inhere$
bandit3@bandit:~/inhere$ ls -la
total 12
drwxr-xr-x 2 root    root    4096 Oct 16 14:00 .
drwxr-xr-x 3 root    root    4096 Oct 16 14:00 ..
-rw-r----- 1 bandit4 bandit3   33 Oct 16 14:00 .hidden
bandit3@bandit:~/inhere$
bandit3@bandit:~/inhere$ cat .hidden
pIwrPrtPN36QITSp3EQaw936yaFoFgAB
bandit3@bandit:~/inhere$

Level 4:
bandit4@bandit:~/inhere$ ls -la
total 48
drwxr-xr-x 2 root    root    4096 Oct 16 14:00 .
drwxr-xr-x 3 root    root    4096 Oct 16 14:00 ..
-rw-r----- 1 bandit5 bandit4   33 Oct 16 14:00 -file00
-rw-r----- 1 bandit5 bandit4   33 Oct 16 14:00 -file01
-rw-r----- 1 bandit5 bandit4   33 Oct 16 14:00 -file02
-rw-r----- 1 bandit5 bandit4   33 Oct 16 14:00 -file03
-rw-r----- 1 bandit5 bandit4   33 Oct 16 14:00 -file04
-rw-r----- 1 bandit5 bandit4   33 Oct 16 14:00 -file05
-rw-r----- 1 bandit5 bandit4   33 Oct 16 14:00 -file06
-rw-r----- 1 bandit5 bandit4   33 Oct 16 14:00 -file07
-rw-r----- 1 bandit5 bandit4   33 Oct 16 14:00 -file08
-rw-r----- 1 bandit5 bandit4   33 Oct 16 14:00 -file09
bandit4@bandit:~/inhere$
bandit4@bandit:~/inhere$ file ./-file*
./-file00: data
./-file01: data
./-file02: data
./-file03: data
./-file04: data
./-file05: data
./-file06: data
./-file07: ASCII text
./-file08: data
./-file09: data
bandit4@bandit:~/inhere$ man xargs
bandit4@bandit:~/inhere$ cat ./-file07
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR

Level 5: 
bandit5@bandit:~$ ls
inhere
bandit5@bandit:~$ cd inhere/
bandit5@bandit:~/inhere$ find . -type f -size 1033c ! -executable
./maybehere07/.file2
bandit5@bandit:~/inhere$ cat ./maybehere07/.file2
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU

Level 6:
bandit6@bandit:~$ find / -type f -user bandit7 -group bandit6 -size 33c
find: ‘/etc/ssl/private’: Permission denied
find: ‘/etc/polkit-1/localauthority’: Permission denied
find: ‘/etc/sudoers.d’: Permission denied
find: ‘/etc/multipath’: Permission denied
find: ‘/root’: Permission denied
find: ‘/boot/efi’: Permission denied
find: ‘/var/spool/bandit24’: Permission denied
find: ‘/var/spool/cron/crontabs’: Permission denied
find: ‘/var/spool/rsyslog’: Permission denied
find: ‘/var/lib/ubuntu-advantage/apt-esm/var/lib/apt/lists/partial’: Permission denied
find: ‘/var/lib/snapd/cookie’: Permission denied
find: ‘/var/lib/snapd/void’: Permission denied
find: ‘/var/lib/private’: Permission denied
find: ‘/var/lib/chrony’: Permission denied
find: ‘/var/lib/polkit-1’: Permission denied
find: ‘/var/lib/apt/lists/partial’: Permission denied
find: ‘/var/lib/update-notifier/package-data-downloads/partial’: Permission denied
find: ‘/var/lib/amazon’: Permission denied
/var/lib/dpkg/info/bandit7.password
find: ‘/var/log’: Permission denied
find: ‘/var/cache/private’: Permission denied
find: ‘/var/cache/pollinate’: Permission denied
find: ‘/var/cache/apparmor/30d07b40.0’: Permission denied
find: ‘/var/cache/apparmor/a4dd844e.0’: Permission denied
find: ‘/var/cache/apt/archives/partial’: Permission denied
find: ‘/var/cache/ldconfig’: Permission denied
find: ‘/var/tmp’: Permission denied
find: ‘/var/snap/lxd/common/lxd’: Permission denied
find: ‘/var/crash’: Permission denied
find: ‘/sys/kernel/tracing’: Permission denied
find: ‘/sys/kernel/debug’: Permission denied
find: ‘/sys/fs/pstore’: Permission denied
find: ‘/sys/fs/bpf’: Permission denied
find: ‘/proc/tty/driver’: Permission denied
find: ‘/proc/2237039/task/2237039/fdinfo/6’: No such file or directory
find: ‘/proc/2237039/fdinfo/5’: No such file or directory
find: ‘/home/bandit31-git’: Permission denied
find: ‘/home/drifter8/chroot’: Permission denied
find: ‘/home/drifter6/data’: Permission denied
find: ‘/home/bandit27-git’: Permission denied
find: ‘/home/bandit5/inhere’: Permission denied
find: ‘/home/bandit30-git’: Permission denied
find: ‘/home/bandit29-git’: Permission denied
find: ‘/home/bandit28-git’: Permission denied
find: ‘/home/ubuntu’: Permission denied
find: ‘/tmp’: Permission denied
find: ‘/dev/mqueue’: Permission denied
find: ‘/dev/shm’: Permission denied
find: ‘/lost+found’: Permission denied
find: ‘/snap’: Permission denied
find: ‘/drifter/drifter14_src/axTLS’: Permission denied
find: ‘/run/chrony’: Permission denied
find: ‘/run/user/11010’: Permission denied
find: ‘/run/user/8003’: Permission denied
find: ‘/run/user/11027’: Permission denied
find: ‘/run/user/11029’: Permission denied
find: ‘/run/user/11009’: Permission denied
find: ‘/run/user/11032’: Permission denied
find: ‘/run/user/11030’: Permission denied
find: ‘/run/user/11008’: Permission denied
find: ‘/run/user/11019’: Permission denied
find: ‘/run/user/11028’: Permission denied
find: ‘/run/user/11006/systemd/inaccessible/dir’: Permission denied
find: ‘/run/user/11011’: Permission denied
find: ‘/run/user/11015’: Permission denied
find: ‘/run/user/11003’: Permission denied
find: ‘/run/user/11007’: Permission denied
find: ‘/run/user/11014’: Permission denied
find: ‘/run/user/11013’: Permission denied
find: ‘/run/user/11016’: Permission denied
find: ‘/run/user/11001’: Permission denied
find: ‘/run/user/11004’: Permission denied
find: ‘/run/user/11025’: Permission denied
find: ‘/run/user/11020’: Permission denied
find: ‘/run/user/11000’: Permission denied
find: ‘/run/user/11023’: Permission denied
find: ‘/run/user/11024’: Permission denied
find: ‘/run/user/11005’: Permission denied
find: ‘/run/user/11012’: Permission denied
find: ‘/run/sudo’: Permission denied
find: ‘/run/screen/S-bandit23’: Permission denied
find: ‘/run/screen/S-bandit20’: Permission denied
find: ‘/run/multipath’: Permission denied
find: ‘/run/cryptsetup’: Permission denied
find: ‘/run/log/journal/ec278654ee913a9f9e0864b461942057’: Permission denied
find: ‘/run/lvm’: Permission denied
find: ‘/run/credentials/systemd-sysusers.service’: Permission denied
find: ‘/run/systemd/propagate’: Permission denied
find: ‘/run/systemd/unit-root’: Permission denied
find: ‘/run/systemd/inaccessible/dir’: Permission denied
find: ‘/run/lock/lvm’: Permission denied
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S

Level 7: 
bandit7@bandit:~$ grep "millionth" data.txt
millionth       cvX2JJa4CFALtqS87jk27qwqGhBM9plV

Level 8:
bandit8@bandit:~$ sort data.txt > sorted.txt
-bash: sorted.txt: Permission denied
bandit8@bandit:~$ ls -la
total 56
drwxr-xr-x  2 root    root     4096 Oct 16 14:00 .
drwxr-xr-x 41 root    root     4096 Oct 16 14:00 ..
-rw-r--r--  1 root    root      220 May 15  2017 .bash_logout
-rw-r--r--  1 root    root     3526 May 15  2017 .bashrc
-rw-r-----  1 bandit9 bandit8 33033 Oct 16 14:00 data.txt
-rw-r--r--  1 root    root      675 May 15  2017 .profile
bandit8@bandit:~$ sort data.txt | uniq -u
UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR

Level 9:
bandit9@bandit:~$ strings data.txt
bandit9@bandit:~$ strings data.txt | grep "^=="
========== password
========== isa
========== truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk
bandit9@bandit:~$

Level 10:
bandit10@bandit:~$ base64 -d data.txt
The password is IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR

Level 11:
bandit11@bandit:~$ cat data.txt | tr '[A-Za-z]' '[N-ZA-Mn-za-m]'
The password is 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu
bandit11@bandit:~$

Level 12:
bandit12@bandit:~$ xxd -r data.txt | file -
/dev/stdin: gzip compressed data, was "data2.bin", last modified: Tue Oct 16 12:00:23 2018, max compression, from Unix
bandit12@bandit:~$ xxd -r data.txt | gzip -d -c | file -
/dev/stdin: bzip2 compressed data, block size = 900k
bandit12@bandit:~$ xxd -r data.txt | gzip -d -c | bzip2 -d -c | file -
/dev/stdin: gzip compressed data, was "data4.bin", last modified: Tue Oct 16 12:00:23 2018, max compression, from Unix
bandit12@bandit:~$ xxd -r data.txt | gzip -d -c | bzip2 -d -c | gzip -d -c | file -
/dev/stdin: POSIX tar archive (GNU)
bandit12@bandit:~$ xxd -r data.txt | gzip -d -c | bzip2 -d -c | gzip -d -c | tar -x -O | file -
/dev/stdin: POSIX tar archive (GNU)
bandit12@bandit:~$ xxd -r data.txt | gzip -d -c | bzip2 -d -c | gzip -d -c | tar -x -O | tar -x -O | file -
/dev/stdin: bzip2 compressed data, block size = 900k
bandit12@bandit:~$ xxd -r data.txt | gzip -d -c | bzip2 -d -c | gzip -d -c | tar -x -O | tar -x -O | bzip2 -d -c | file -
/dev/stdin: POSIX tar archive (GNU)
bandit12@bandit:~$ xxd -r data.txt | gzip -d -c | bzip2 -d -c | gzip -d -c | tar -x -O | tar -x -O | bzip2 -d -c | tar -x -O | gzip -d -c | file -
/dev/stdin: ASCII text
bandit12@bandit:~$ xxd -r data.txt | gzip -d -c | bzip2 -d -c | gzip -d -c | tar -x -O | tar -x -O | bzip2 -d -c | tar -x -O | gzip -d -c | cat
The password is 8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL

Level 13:
bandit13@bandit:~$ ssh -i sshkey.private bandit14@bandit.labs.overthewire.org
bandit13@bandit:~$ ssh -i sshkey.private bandit14@localhost

Level 14:
bandit14@bandit:~$ cat /etc/bandit_pass/bandit14
4wcYUJFw0k0XLShlDzztnTBHiqxU3b3ebandit14@bandit:~$ echo "4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e" | netcat localhost 30000
Correct!
BfMYroe26WYalil77FoDi9qh59eK5xNr

Level 15: 
openssl s_client -connect localhost:30001
BfMYroe26WYalil77FoDi9qh59eK5xNr
Correct!
cluFn7wTiGryunymYOu4RcffSxQluehd
