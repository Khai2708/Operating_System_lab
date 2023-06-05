
# OS_lab
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
