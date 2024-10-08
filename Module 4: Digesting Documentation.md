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
Type `/` and then `flag`, this will display all the ouccruence of `flag` then use `n` to go to next matched entry.<br>
After searching we get `--zqywtrh` as the argument which when passsed will give the flag
```
hacker@man~searching-manuals:~$ /challenge/challenge --zqywtrh
Initializing...
Correct usage! Your flag: pwn.college{41-J5F9jzbWHh14AJw2VawLYjGB.dVTM4QDL2EjN0czW}
```
## Challenge 5: Searching for manual
## Challenge 6: Helpful programs
First we run `/challenge/challenge -h` to get the info that how the program work
```
hacker@man~helpful-programs:~$ /challenge/challenge -h
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to give you the flag
```
Here `-g` will give the flag when passed correct argument, and `-p` will print the correct argument<br>
```
hacker@man~helpful-programs:~$ /challenge/challenge -p
The secret value is: 51
hacker@man~helpful-programs:~$ /challenge/challenge -g 51
Correct usage! Your flag: pwn.college{MsWNF05fdiJSgZH17OSn63oNqhH.ddjM4QDL2EjN0czW}
```
## `help` command 
This will print the description of the builtin command specified as the argument

## Challenge 7: Help for builtins
First run `help challenge` to get get the options of `challenge` command
```
hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!

    Options:
      --fortune         display a fortune
      --version         display the version
      --secret VALUE    prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "AvImjeoo".
```
`--secret` is the argument which will give the flag when `AvImjeoo` is passed
```
hacker@man~help-for-builtins:~$ challenge --secret AvImjeoo
Correct! Here is your flag!
pwn.college{AvImjeooG3wACHEDDBRzL3wSH1F.dRTM5QDL2EjN0czW}
```
