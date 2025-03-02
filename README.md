
# Operating System course lab sessions
#### Week 2 & Week 3 lab work
```
> In week 2 we made OS_lab repository and created two files inside
text.txt
week2.sh
--------------------------------------------------------------------
sadbek@ubuntu:~/OS_lab$ git add .
asadbek@ubuntu:~/OS_lab$ ls
text.txt  week2.sh
asadbek@ubuntu:~/OS_lab$ git commit -m "VER1"
[main e0818bb] VER1
 3 files changed, 11 insertions(+)
 rename week2/test.txt => text.txt (100%)
 create mode 100644 week2.sh
 delete mode 100644 week2/week2.sh
 
asadbek@ubuntu:~/OS_lab$ git remote set-url origin https://github.com/Khai2708/OS_lab.git
asadbek@ubuntu:~/OS_lab$ git push origin main
Username for 'https://github.com': Khai2708
Password for 'https://Khai2708@github.com':
Total 13 (delta 0), reused 0 (delta 0)
To https://github.com/Khai2708/OS_lab.git
 * [new branch]      main -> main

```
![image](https://user-images.githubusercontent.com/90145797/225282497-45599009-b19d-4081-ace4-4bf325f2aee1.png)

#### Week 6 & Week 7 lab work
```
> In week 6 & 7 we have completed Oracle cloud and build our own 
vm ware woeking station with ubuntu
date_purse.sh bash file created to show 
Current Date 
Current Time
---------------------------------------------------------------------
ubuntu@instance-20230405-1802:~$ nano date_parse.sh
ubuntu@instance-20230405-1802:~$ bash date_parse.sh
Wed May 24 13:28:55 UTC 2023
Current Date is: 24-05-2023
Current Time is: 13:28:55
ubuntu@instance-20230405-1802:~$

```
![image](https://github.com/Khai2708/OS_lab/assets/90145797/14777c55-7181-47a3-a0be-4fa46bc6b262)

#### Week 13 & Week 14 lab work
```
> In week 13 & 14 we have learned about:
Analyzing and Storing Logs;
Archiving and Copying Files;
Accessing Linux File Systems

-----------------------------------------------------------------------------
> archive.tar command created with the contents of file1,file2,file3
in the user's home directory

ubuntu@instance-20230605-1452:~/oslab$ nano file1
ubuntu@instance-20230605-1452:~/oslab$ rm -r file1.pdf file2.pdf file3.pdf
ubuntu@instance-20230605-1452:~/oslab$ ls
date_parse.sh  file1
ubuntu@instance-20230605-1452:~/oslab$ touch file2 file3
ubuntu@instance-20230605-1452:~/oslab$ tar cf archive.tar file1 file2 file3
ubuntu@instance-20230605-1452:~/oslab$ ls archive.tar
archive.tar
ubuntu@instance-20230605-1452:~/oslab$ ls
archive.tar  date_parse.sh  file1  file2  file3
ubuntu@instance-20230605-1452:~/oslab$ cd ..
ubuntu@instance-20230605-1452:~$ makdir mkdir oslab1
ubuntu@instance-20230605-1452:~$ mkdir oslab1
ubuntu@instance-20230605-1452:~$ cd oslab1
ubuntu@instance-20230605-1452:~/oslab1$ tar cf ~/oslab1/oslab.tar ~/oslab
tar: Removing leading `/' from member names
ubuntu@instance-20230605-1452:~/oslab1$ tar cf /home/ubutu/oslab1/oslab.tar /home/ubuntu/oslab
tar: /home/ubutu/oslab1/oslab.tar: Cannot open: No such file or directory
tar: Error is not recoverable: exiting now
ubuntu@instance-20230605-1452:~/oslab1$ ls
oslab.tar
ubuntu@instance-20230605-1452:~/oslab1$ tar cf --xattrs /home/ubutu/oslab1/oslab.tar /home/ubuntu/oslab
tar: Removing leading `/' from member names
tar: /home/ubutu/oslab1/oslab.tar: Cannot stat: No such file or directory
tar: Removing leading `/' from hard link targets
tar: Exiting with failure status due to previous errors
ubuntu@instance-20230605-1452:~/oslab1$ ls
--xattrs  oslab.tar

>>> !!!! Contents of tar archive
ubuntu@instance-20230605-1452:~/oslab1$ tar tf oslab.tar
home/ubuntu/oslab/
home/ubuntu/oslab/file1
home/ubuntu/oslab/date_parse.sh
home/ubuntu/oslab/archive.tar
home/ubuntu/oslab/file2
home/ubuntu/oslab/file3
ubuntu@instance-20230605-1452:~/oslab1$ cd ..
```
![image](https://github.com/Khai2708/OS_lab/assets/90145797/b5902cb9-3f41-4dfa-8e42-e3a316ae7a73)
![image](https://github.com/Khai2708/OS_lab/assets/90145797/d340011a-ee5e-4836-8ac0-c3cf6799f5bb)

```
>>> Extracting a compressed tar archive
--------------------------------------------------------------------------------------
ubuntu@instance-20230605-1452:~$ mkdir oslabbackup
ubuntu@instance-20230605-1452:~$ cd oslabbackup/
ubuntu@instance-20230605-1452:~/oslabbackup$ pwd
/home/ubuntu/oslabbackup
ubuntu@instance-20230605-1452:~/oslabbackup$ tar xpf /home/ubuntu/oslab1/oslab.tar
ubuntu@instance-20230605-1452:~/oslabbackup$ ls
home
ubuntu@instance-20230605-1452:~/oslabbackup$ cd /home/ubuntu/oslab/
ubuntu@instance-20230605-1452:~/oslab$ ls
archive.tar  date_parse.sh  file1  file2  file3
ubuntu@instance-20230605-1452:~/oslab$ cd ~/
ubuntu@instance-20230605-1452:~$ ls
os  oslab  oslab1  oslabbackup
ubuntu@instance-20230605-1452:~$ pwd
/home/ubuntu
ubuntu@instance-20230605-1452:~$ mkdir oslabbackupbz2
ubuntu@instance-20230605-1452:~$ cd oslabbackupbz2/
ubuntu@instance-20230605-1452:~/oslabbackupbz2$ cd ~/oslab1/
ubuntu@instance-20230605-1452:~/oslab1$ ls
--xattrs  oslab.tar
ubuntu@instance-20230605-1452:~/oslab1$ tar cjf oslabbackup3.tar.bz2 /home/ubuntu/oslab
tar: Removing leading `/' from member names
ubuntu@instance-20230605-1452:~/oslab1$ cd ~/oslabbackupbz2/
ubuntu@instance-20230605-1452:~/oslabbackupbz2$ cd /home/ubuntu/oslab
ubuntu@instance-20230605-1452:~/oslab$ ls
archive.tar  date_parse.sh  file1  file2  file3
ubuntu@instance-20230605-1452:~/oslab$ cd ..
ubuntu@instance-20230605-1452:~$ ls
os  oslab  oslab1  oslabbackup  oslabbackupbz2
ubuntu@instance-20230605-1452:~$ oslabbackupbz2/
-bash: oslabbackupbz2/: Is a directory
ubuntu@instance-20230605-1452:~$ cd oslabbackupbz2/
ubuntu@instance-20230605-1452:~/oslabbackupbz2$ ls
home
ubuntu@instance-20230605-1452:~/oslabbackupbz2$ cd home/ubuntu/oslab/
ubuntu@instance-20230605-1452:~/oslabbackupbz2/home/ubuntu/oslab$ ls
archive.tar  date_parse.sh  file1  file2  file3
ubuntu@instance-20230605-1452:~/oslabbackupbz2/home/ubuntu/oslab$ cd ~/oslabbackupbz2/
ubuntu@instance-20230605-1452:~/oslabbackupbz2$ cd ~/oslab1/
ubuntu@instance-20230605-1452:~/oslab1$ tar tf oslabbackup3.tar.bz2
home/ubuntu/oslab/
home/ubuntu/oslab/file1
home/ubuntu/oslab/date_parse.sh
home/ubuntu/oslab/archive.tar
home/ubuntu/oslab/file2
home/ubuntu/oslab/file3
ubuntu@instance-20230605-1452:~/oslab1$

```
![image](https://github.com/Khai2708/OS_lab/assets/90145797/5be3194b-3a25-4fed-a1d4-ea0dc33038a3)

```
>>> Examining file systems 
----------------------------------------------------------------------------
ubuntu@instance-20230605-1452:~/oslab$ df
Filesystem     1K-blocks    Used Available Use% Mounted on
ude

....... skipped
tmpfs              98728       0     98728   0% /run/user/1001
ubuntu@instance-20230605-1452:~/oslab$ df -h
Filesystem      Size  Used Avail Use% Mounted on
udev            444M     0  444M   0% /dev
tmpfs            97M  1.1M   96M   2% /run
/dev/sda1        45G  2.0G   43G   5% /
tmpfs           483M     0  483M   0% /dev/shm
tmpfs           5.0M     0  5.0M   0% /run/lock
tmpfs           483M     0  483M   0% /sys/fs/cgroup
/dev/loop0       64M   64M     0 100% /snap/core20/1852
/dev/loop1.. skipped
tmpfs            97M     0   97M   0% /run/user/1001

ubuntu@instance-20230605-1452:~/oslab$ du /home
.....
516     /home/ubuntu/oslab
8       /home/ubuntu/.ssh
4       /home/ubuntu/.cache
4       /home/ubuntu/os
24      /home/ubuntu/oslabbackup/home/ubuntu/oslab
28      /home/ubuntu/oslabbackup/home/ubuntu
32      /home/ubuntu/oslabbackup/home
36      /home/ubuntu/oslabbackup
1200    /home/ubuntu

ubuntu@instance-20230605-1452:~/oslab$ du -h /home/ubuntu
......
480K    /home/ubuntu/oslab/.git
516K    /home/ubuntu/oslab
8.0K    /home/ubuntu/.ssh
4.0K    /home/ubuntu/.cache
4.0K    /home/ubuntu/os
24K     /home/ubuntu/oslabbackup/home/ubuntu/oslab
28K     /home/ubuntu/oslabbackup/home/ubuntu
32K     /home/ubuntu/oslabbackup/home
36K     /home/ubuntu/oslabbackup
1.2M    /home/ubuntu

ubuntu@instance-20230605-1452:~$ blkid
/dev/sda1: LABEL="cloudimg-rootfs" UUID="d2d17c29-d0ce-47a6-83f9-012a406381de" TYPE="ext4"

```
![image](https://github.com/Khai2708/OS_lab/assets/90145797/82101bfb-9eb9-4188-8652-b0edfd006c34)
![image](https://github.com/Khai2708/OS_lab/assets/90145797/0349e3aa-6752-4b15-a0f8-ca6e04f5f74b)
