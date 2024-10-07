# Module 3: Comprehending Commands
## 
## `cat` command
cat is used for reading out files provided as arguments<br>
If you give no arguments at all, cat will read from the terminal input and output it
## Challenge 1: cat: not the pet, but the command!
This was a simple challenge, we just have to read `flag` file using `cat` command
```
hacker@commands~cat-not-the-pet-but-the-command:~$ cat flag
pwn.college{ghiEBltHv9oQ9G17CkHtl9dJT6r.dFzN1QDL2EjN0czW}
```
## Challenge 2: Catting absolute paths
In this challenge we just have to use `cat` command using absolute path
```
hacker@commands~catting-absolute-paths:~$ cat /flag
pwn.college{4Q06tVRLmrQFeNvdAtQtCsmD0ta.dlTM5QDL2EjN0czW}
```

## Challenge 3: more catting practice
same as previous challenge
```
Connected!
You cannot use the 'cd' command in this level, and must retrieve the flag by
absolute path. Plus, I hid the flag in a different directory! You can find it
in the file /lib/compat-ld/flag. Go cat it out **without** cding into that
directory!
hacker@commands~more-catting-practice:~$ cat /lib/compat-ld/flag
pwn.college{shGlwJkXSg49pz5yCzVUvFqekUC.dBjM5QDL2EjN0czW}
```
## `grep` command
This command is use to search for a specific content which was passed as argument
## Challenge 4: grepping for a needle in a haystack
just have to search for flag in the file, the flag starts from pwn.college
```
hacker@commands~grepping-for-a-needle-in-a-haystack:~$ grep pwn.college /challenge/data.txt
pwn.college{kbNUC7VW2wFTdVtplB6ECuIh58Y.ddTM4QDL2EjN0czW}
```

## `ls` command
ls will list files in all the directories provided to it as arguments, and in the current directory if no arguments are provided.
## Challenge 5: Listing files 
We have to list the files in the challenge directory to get the file name. After we get the file name we just have to open it
```
hacker@commands~listing-files:~$ cd /challenge
hacker@commands~listing-files:/challenge$ ls
19506-renamed-run-31783  DESCRIPTION.md
hacker@commands~listing-files:/challenge$ /challenge/19506-renamed-run-31783
Yahaha, you found me! Here is your flag:
pwn.college{EVGFbOYDyGThAKO72MQnBE7TGwH.dhjM4QDL2EjN0czW}
```
## `touch` command
We can create a new, blank file by touching it with the touch command
## Challenge 6: touching files
In this challenge we have to create two files to get the flag `/tmp/pwn` and `/tmp/college`<br>
The `tmp` folder is already there so we have to cd it and then create files in it
```
hacker@commands~touching-files:~$ cd /tmp
hacker@commands~touching-files:/tmp$ ls
bin  hsperfdata_root  tmp.G9qthVCks5
hacker@commands~touching-files:/tmp$ touch pwn
hacker@commands~touching-files:/tmp$ touch college
hacker@commands~touching-files:/tmp$ /challenge/run
Success! Here is your flag:
pwn.college{8J0bNSUaLNR3AnVWarJdM2u_SuA.dBzM4QDL2EjN0czW}
```

## `rm` command
This is used to remove file which is passed as argument
## Challenge 7: removing files
```
hacker@commands~removing-files:~$ ls
delete_me  m
hacker@commands~removing-files:~$ rm delete_me
hacker@commands~removing-files:~$ ls
m
hacker@commands~removing-files:~$ /challenge/check
Excellent removal. Here is your reward:
pwn.college{gWsBiRvJwdDmK5bWdVyjtriOLbb.dZTOwUDL2EjN0czW}
```
## Challenge 8: hidden files
We have to use `ls -a` to list the files starting with `.`
```
hacker@commands~hidden-files:~$ cd /
hacker@commands~hidden-files:/$ ls -a
.   .dockerenv           bin   challenge  etc   lib    lib64   media  nix  proc  run   srv  tmp  var
..  .flag-3049459025136  boot  dev        home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~hidden-files:/$ cat .flag-3049459025136
pwn.college{4KdbkQyrC3ro7wtDO0nLDZ4jcNc.dBTN4QDL2EjN0czW}
```
## Challenge 9: An epic file quest

## Challenge 8: Making directories
We have to make a `/tmp/pwn` directory and make a `college` file in it! Then run /challenge/run<br>
just following the steps
```
hacker@commands~making-directories:~$ cd /tmp
hacker@commands~making-directories:/tmp$ mkdir pwn
hacker@commands~making-directories:/tmp$ cd pwn
hacker@commands~making-directories:/tmp/pwn$ touch college
hacker@commands~making-directories:/tmp/pwn$ /challenge/run
Success! Here is your flag:
pwn.college{wS7LLC5s2JxR_LKpw3A5LsyiDfy.dFzM4QDL2EjN0czW}
```
## Challenge 9: Finding files
We have to find a file named `flag`, and try opening each file one by one to get the flag<br>
We have to ignore all the the permission denied message
```
hacker@commands~finding-files:~$ cd /
hacker@commands~finding-files:/$ find -name flag
find: ‘./root’: Permission denied
find: ‘./etc/ssl/private’: Permission denied
find: ‘./tmp/tmp.G9qthVCks5’: Permission denied
./usr/local/share/radare2/5.9.5/flag
./usr/local/lib/python3.8/dist-packages/pwnlib/flag
./usr/share/locale/frp/flag
find: ‘./var/cache/apt/archives/partial’: Permission denied
find: ‘./var/cache/ldconfig’: Permission denied
find: ‘./var/cache/private’: Permission denied
find: ‘./var/log/private’: Permission denied
find: ‘./var/log/apache2’: Permission denied
find: ‘./var/log/mysql’: Permission denied
find: ‘./var/lib/apt/lists/partial’: Permission denied
find: ‘./var/lib/mysql-keyring’: Permission denied
find: ‘./var/lib/php/sessions’: Permission denied
find: ‘./var/lib/private’: Permission denied
find: ‘./var/lib/mysql-files’: Permission denied
find: ‘./var/lib/mysql’: Permission denied
find: ‘./run/mysqld’: Permission denied
find: ‘./run/sudo’: Permission denied
find: ‘./proc/tty/driver’: Permission denied
find: ‘./proc/1/task/1/fd’: Permission denied
find: ‘./proc/1/task/1/fdinfo’: Permission denied
find: ‘./proc/1/task/1/ns’: Permission denied
find: ‘./proc/1/fd’: Permission denied
find: ‘./proc/1/map_files’: Permission denied
find: ‘./proc/1/fdinfo’: Permission denied
find: ‘./proc/1/ns’: Permission denied
find: ‘./proc/7/task/7/fd’: Permission denied
find: ‘./proc/7/task/7/fdinfo’: Permission denied
find: ‘./proc/7/task/7/ns’: Permission denied
find: ‘./proc/7/fd’: Permission denied
find: ‘./proc/7/map_files’: Permission denied
find: ‘./proc/7/fdinfo’: Permission denied
find: ‘./proc/7/ns’: Permission denied
./opt/pwndbg/.venv/lib/python3.8/site-packages/pwnlib/flag
./opt/radare2/libr/flag
./nix/store/pmvk2bk4p550w182rjfm529kfqddnvh3-python3.11-pwntools-4.12.0/lib/python3.11/site-packages/pwnlib/flag
./nix/store/1yagn5s8sf7kcs2hkccgf8d0wxlrv5sz-radare2-5.9.0/share/radare2/5.9.0/flag
hacker@commands~finding-files:/$ cat ./usr/local/share/radare2/5.9.5/flag
cat: ./usr/local/share/radare2/5.9.5/flag: Is a directory
hacker@commands~finding-files:/$ cat ./usr/local/lib/python3.8/dist-packages/pwnlib/flag
cat: ./usr/local/lib/python3.8/dist-packages/pwnlib/flag: Is a directory
hacker@commands~finding-files:/$ cat ./usr/share/locale/frp/flag
pwn.college{42FZMsttZgQnd1R8Q_STJBZyNqp.dJzM4QDL2EjN0czW}
```
## Challenge 10: linking files
Here the `/challenge/catflag` is reading `/home/hacker/not-the-flag file` file.
I first run the `/challenge/flag` to see what happens
```
hacker@commands~linking-files:~$ /challenge/catflag
About to read out the /home/hacker/not-the-flag file!
cat: /home/hacker/not-the-flag: No such file or directory
```
There is no `/home/hacker/not-the-flag` file, but `/challenge/flag` is reading it.<br>
So I created a symlink for `/flag` with `/home/hacker/not-the-flag`
```
hacker@commands~linking-files:~$ ln -s /flag ~/not-the-flag
hacker@commands~linking-files:~$ /challenge/catflag
About to read out the /home/hacker/not-the-flag file!
pwn.college{oVZfPATM5wzK3vyk7bxGcA8pJ6b.dlTM1UDL2EjN0czW}
```
