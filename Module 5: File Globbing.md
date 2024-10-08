# File Globbing
## Challenge 1: Matching with `*`
When shell encounters a `*` character in any argument<br>
the shell will treat it as "wildcard" and try to replace that argument with any files that match the pattern
In this challenge we have to cd to `/challenge` with using atmost 4 character<br>
so we can write `/ch*` instead of `/challenge` because here `*` is be replaced by `allenge`, because `/ch*` follows same structure as `/challenge`
```
Connected!
This challenge resets your working directory to /home/hacker unless you change
directory properly...
hacker@globbing~matching-with-:~$ cd /ch*
hacker@globbing~matching-with-:/challenge$ ./run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{clrJ-2RTqHUgufndsEBeo99yzs7.dFjM4QDL2EjN0czW}
```
## Challenge 2: Matching with `?`
`?` Works same as `*` but replace only one character
```
This challenge resets your working directory to /home/hacker unless you change
directory properly...
hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ ./run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{gaEGBxh26jgE1IAGK9h4ec-9Q18.dJjM4QDL2EjN0czW}
```
## Challenge 3: Matching with `[]`
hacker@globbing~matching-with-:~$ cd /challenge/files
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[bash]
You got it! Here is your flag!
pwn.college{8MmTFFYyPbcmgKrEfBxupit6CTs.dNjM4QDL2EjN0czW}
