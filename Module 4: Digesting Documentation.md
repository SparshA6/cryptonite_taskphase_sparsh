# Digesting Documentation
## Challenge 1: Learning from documentation
This challenge is to give an idea that how documentation helps in knowing how to use a command<br>
We just have to pass `--giveflag` argument to `/challenge/challenge`
```
hacker@man~learning-from-documentation:~$ /challenge/challenge --giveflag
Correct argument! Here is your flag:
pwn.college{0-H32E4SRik3aiN3hpcIeA0gtET.dRjM5QDL2EjN0czW}
```
## Challenge 2: Learning complex usage
There are functions which takes arguments to their arguments.<br>
In the challenge we have to pass the path of the flag file which is `/flag` to `--printflie` argument of `/challenge/challenge` file

```
hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile /flag
Correct argument! Here is the /flag file:
pwn.college{oy0uW5xug25ZFgGJD48mnqbN2Vm.dVjM5QDL2EjN0czW}
```
## `man` command
This command will display (if available) the manual of the command you pass as an argument
## Challenge 3: Reading Manual
first read the manual
```
CHALLENGE(1)                                      Challenge Commands                                     CHALLENGE(1)

NAME
       /challenge/challenge - print the flag!

SYNOPSIS
       challenge OPTION

DESCRIPTION
       Output the flag when called with the right arguments.

       --fortune
              read a fortune

       --version
              output version information and exit

       --lhetva NUM
              print the flag if NUM is 465

AUTHOR
       Written by Zardus.

REPORTING BUGS
       The repository for this dojo: <https://github.com/pwncollege/linux-luminarium/>

SEE ALSO
       man(1) bash-builtins(7)
```
here for getting the flag we have to give `465` to `--lhetva` argument
```
hacker@man~reading-manuals:~$  /challenge/challenge --lhetva 465
Correct usage! Your flag: pwn.college{YMlO4Y6VDPhCNet5JvP4GaPstdb.dRTM4QDL2EjN0czW}
```
## Challenge 4: Searching manual
We can use `/` to search in the manual
```
hacker@man~searching-manuals:~$ man challenge
```
After searching we get `--zqywtrh` as the argument which when passsed will give the flag
```
hacker@man~searching-manuals:~$ /challenge/challenge --zqywtrh
Initializing...
Correct usage! Your flag: pwn.college{41-J5F9jzbWHh14AJw2VawLYjGB.dVTM4QDL2EjN0czW}
```
## Challenge 5: Searching for manual
