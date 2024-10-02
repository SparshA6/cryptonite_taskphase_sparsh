# Module 2: Pondering Paths

## Challenge-1: The Root
In this challenge we have to invoke a program by giving its absolute path.<br>
Absolute path starts form `/`, the program name is `pwn` and it is in the root directory.<br>
so the command would be `/pwn` this is the absolute path of pwn program<br>
which means run the program `pwn` which is inside the root directory

```
hacker@paths~the-root:~$ /pwn
BOOM!!!
Here is your flag:
pwn.college{Y8RFssG2WH3l6HXi3wf98Dskanb.dhzN5QDL2EjN0czW}
```

## Challenge-2: Program and Absolute path
In this challenge we have to invoke `run` program which is inside `challenge` folder and the `challenge` folder is in root directory.<br> 
So, the absolute path will be `/challenge/run`
```
hacker@paths~program-and-absolute-paths:~$ /challenge/run
Correct!!!
/challenge/run is an absolute path! Here is your flag:
pwn.college{0CJQSL09ICL6SMCjpFmukOh4BU3.dVDN1QDL2EjN0czW}
```
##
### `cd` command
This means change directory, this command is to use to go to some other directory by providing path as the argument
`cd <path>`
## Challenge-3: Position thy self
The challenge says that we have to execute `/challenge/run` program from a specific path (which it will tell you), which means the command `/challenge/run` will give the path from where we have to execute the program.

So, 
```
hacker@paths~position-thy-self:~$ /challenge/run
Incorrect...
You are not currently in the /usr/aarch64-linux-gnu/include/gnu directory.
Please use the `cd` utility to change directory appropriately.
```
This gives the path where we have to jump and execute our program
```
hacker@paths~position-thy-self:~$ cd /usr/aarch64-linux-gnu/include/gnu
```
After jumping we now have to execute our program
```
hacker@paths~position-thy-self:/usr/aarch64-linux-gnu/include/gnu$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{MvghcL3tTdHfTkEfVG-SdwQu0Hc.dZDN1QDL2EjN0czW}
```
## Challenge 4: Position elsewhere
process and thinking same as previous
```
hacker@paths~position-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /usr/bin directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-elsewhere:~$ cd /usr/bin
hacker@paths~position-elsewhere:/usr/bin$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{0N3TJ-jTzONNvVTDnLJ2-JhopWC.ddDN1QDL2EjN0czW}
```
## Challenge 5: Position elsewhere
Process and thinking same as previous
```
hacker@paths~position-yet-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /proc/67 directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-yet-elsewhere:~$ cd /proc/67
hacker@paths~position-yet-elsewhere:/proc/67$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{09jY0QTiOG-x6eYytAfx0t1IND6.dhDN1QDL2EjN0czW}
```
## Challenge 6: Position elsewhere
















