# Module 6: Practicing piping
## `>` 
This is used to direct the output to the given file
## Challenge 1: Redirecting output
In this we have to write `PWN` to `COLLEGE` file, so we can use `echo` command to get the output `PWN` nd then `>` to redirect to `COLLEGE` file
```
hacker@piping~redirecting-output:~$ echo PWN > COLLEGE
Correct! You successfully redirected 'PWN' to the file 'COLLEGE'! Here is your
flag:
pwn.college{M6Pw9QnbbGp7qCkUVf8IGYy2ZeS.dRjN1QDL2EjN0czW}
```
## Challenge 2: Redirecting more output
This challenge teaches us that we can redirect any output of any command<br>
Here we have to use `/challenge/run` and redirect it to `myflag` file
```
hacker@piping~redirecting-more-output:~$ /challenge/run > myflag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will output a reward file if all the tests pass : /flag
[HYPE] ONWARDS TO GREATNESS!
[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.
[TEST] You should have redirected my stdout to a file called myflag. Checking...
[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
```
Now we can just `cat` the file to get the output which contains flag
```
hacker@piping~redirecting-more-output:~$ cat myflag
[FLAG] Here is your flag:
[FLAG] pwn.college{ckPFG2RHDzTmmmaey2NObDuWAVw.dVjN1QDL2EjN0czW}
```
## Challenge 3: Appending output
`>>` will append the output to the existing file

The `/challenge/run` will first write the first half of the flag to `/home/hacker/the-flag`,<br>
then we have to use append mode to write the second flag
```
hacker@piping~appending-output:~$ /challenge/run >> /home/hacker/the-flag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /home/hacker/the-flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] Good luck!

[TEST] You should have redirected my stdout to a file called /home/hacker/the-flag. Checking...

[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
I will write the flag in two parts to the file /home/hacker/the-flag! I'll do
the first write directly to the file, and the second write, I'll do to stdout
(if it's pointing at the file). If you redirect the output in append mode, the
second write will append to (rather than overwrite) the first write, and you'll
get the whole flag!
hacker@piping~appending-output:~$ cat /home/hacker/the-flag
 |
\|/ This is the first half:
 v
pwn.college{A5DAPG5mhGNdAVnQ47PQGbdDhDb.ddDM5QDL2EjN0czW}
                              ^
     that is the second half /|\
                              |

If you only see the second half above, you redirected in *truncate* mode (>)
rather than *append* mode (>>), and so the write of the second half to stdout
overwrote the initial write of the first half directly to the file. Try append
mode!
```
## File Descriptor (FD)
File Descriptor (FD) is a number the describes a communication channel in Linux.<br>
Three type of FD
FD 0: Standard Input
FD 1: Standard Output
FD 2: Standard Error










