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
## Challenge 5: 
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
