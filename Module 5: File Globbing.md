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
The square brackes are, essentially, a limited form of ?, in that instead of matching any character, [] is a wildcard for some subset of potential characters, specified within the brackets<br>
In this challenge we have to pass the the argument such that it will match the properties of `flag_b`, `flag_a`, `flag_s`, `flag_h`<br>
We can write it as `file_[bash]` and then pass it to `/challenge/run`
```
hacker@globbing~matching-with-:~$ cd /challenge/files
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[bash]
You got it! Here is your flag!
pwn.college{8MmTFFYyPbcmgKrEfBxupit6CTs.dNjM4QDL2EjN0czW}
```
## Challenge 4: Matching paths with `[]`
Thinking and working sasme as previous challenge, we now just have to do it to paths<br>
```
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[bash]
You got it! Here is your flag!
pwn.college{k4kKQYEEwIw45WrYhniwJR3ImHp.dRjM4QDL2EjN0czW}
```
## Challenge 5: Mixing globs
First cd to the location
`hacker@globbing~mixing-globs:~$ cd /challenge/files`
then I listed all the files in the location to get some pattern of the names of the files
```
hacker@globbing~mixing-globs:/challenge/files$ ls
amazing      delightful   great       jovial    magical     pwning   splendid   victorious  youthful
beautiful    educational  happy       kind      nice        queenly  thrilling  wonderful   zesty
challenging  fantastic    incredible  laughing  optimistic  radiant  uplifting  xenial
```
Here all the file name starts from a unique alphabet, so for our desired files we can just use their first letter<br>
So the argument would be `[cep]*`
```
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [cep]*
You got it! Here is your flag!
pwn.college{MYpvoOBvbq_ALMlL-UFV8DLNxec.dVjM4QDL2EjN0czW}
```
## Challenge 6: Exclusionary globbing
The `!` is to to exclude the charachters defined inside the square brackets, this is only true when the `!` is used just after the `[` bracket<br>
In this challenge we have to exclude the files which starts from p,w and n<br>
so the argument would be, `[pwn]*`
```
hacker@globbing~exclusionary-globbing:~$ cd /challenge/files
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]*
You got it! Here is your flag!
pwn.college{YiMRS-FMJ5MYnsudwxUyFvFJgnc.dZjM4QDL2EjN0czW}
```

